Here’s a **summary of the key points** from your code:

---

### 🔹 **1. Data Loading & Preparation**

* Reads all CSV files from a specified folder.
* Cleans and standardizes columns: strips whitespace, parses `Date` and `Expiry`, converts numeric fields (`Strike Price`, `Close`).
* Drops rows with missing critical data.
* Sorts data by `Date`, `Option type`, `Expiry`, and `Strike Price`.

---

### 🔹 **2. Option Selection Logic**

* **Weekly Option (Buy):** Chooses the **lowest premium > ₹10** for both Call (CE) and Put (PE).
* **Monthly Option (Sell):** Chooses the **highest premium < ₹500** for both Call (CE) and Put (PE).

---

### 🔹 **3. Entry & Exit Strategy**

* Entry happens **every Friday**.
* Exit is the **next Thursday**.
* Determines the **nearest weekly expiry** and the **next monthly expiry** from the entry date.

---

### 🔹 **4. Trade Execution Simulation**

* Buys weekly CE and PE options.
* Sells monthly CE and PE options.
* Calculates PnL for each leg using:

  ```
  PnL = (Exit - Entry) * Quantity
  ```
* Quantities:

  * Weekly legs: 20,000
  * Monthly legs: 10,000

---

### 🔹 **5. Risk Guard Clause**

* If **Sell Legs PnL < Buy Legs PnL**, assumes all legs exited at entry price (no loss or gain), simulating a **stop-loss** protection.

---

### 🔹 **6. Result Compilation**

* Stores:

  * Entry/Exit dates
  * Leg type
  * Strike Price
  * Entry/Exit price
  * Quantity
  * Individual Leg PnL
* Adds a **"TOTAL" row** per trade cycle.

---

### 🔹 **7. Output**

* Saves result to CSV:
  `Nifty50_Options_PnL_Per_Leg.csv`
* Prints:

  * CSV path
  * Total PnL across all trades if any were generated.

---

Let me know if you want a **visual representation** or a **strategy explanation**!
