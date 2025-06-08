

---

**I. Building the "Airline Travel.csv" Branch (Top Flow)**

This branch starts with the `Airport Codes.hyper` file, processes it, and then joins it into another flow.

1.  **Drag and Drop `Airport Codes.hyper` Input:**
    * From the "Connections" pane on the left, **drag and drop** `US Airports.hyper` (or `Airport Codes.hyper` if that's the exact name in your list) onto the flow pane.
    * This will create an `Input` step named `Airport Codes`.

2.  **Add a "Split Route" Clean Step:**
    * Click the `+` icon next to the `Airport Codes` input step.
    * Select **"Clean Step"**. A new clean step will appear.
    * **Rename** this step: Click on its default name (e.g., `Clean 1`) and type `Split Route`.
    * **Configure Split Route:** Double-click the `Split Route` step to open its configuration pane.
        * Identify the field that contains route information (e.g., `Route`, `Origin-Destination`).
        * Click the **three dots (...)** next to that field's name in the Profile Pane (bottom section).
        * Select **"Split Values"** and choose **"Automatic Split"** (or "Custom Split" if you know the delimiter).
        * **Rename** the newly created split fields (e.g., `Route - Split 1` to `Origin` and `Route - Split 2` to `Destination`).

3.  **Add a "Pivot" Step:**
    * Click the `+` icon next to the `Split Route` step.
    * Select **"Pivot"**. A new pivot step will appear.
    * **Rename** this step: Click on its default name (e.g., `Pivot 1`) and type `Pivot`.
    * **Configure Pivot:** Double-click the `Pivot` step.
        * From the `Fields` list on the left of the pivot pane, **drag and drop** the `Origin` field and the `Destination` field into the "Pivot 1 (Rows to Columns)" area. This will transform the `Origin` and `Destination` columns into rows, often creating a new field like `Pivot1 Field Names` (for the original field names) and `Pivot1 Field Values` (for the values).
        * **Rename** the `Pivot1 Field Names` field to `Airport Type` and `Pivot1 Field Values` to `Airport Code` (or similar appropriate names).

4.  **Add a "Join" Step (Preparation for later):**
    * Click the `+` icon next to the `Pivot` step.
    * Select **"Join"**. A new join step will appear.
    * **Rename** this step: Click on its default name (e.g., `Join 1`) and type `Join`.
    * **Keep this step empty for now** as we will connect the other flow to it later.

---

**II. Building the "Frequency Segment.csv" Branch (Bottom Flow)**

This branch processes `Employee Flights.xlsx` and `Southwest 2019.csv`, unions them, cleans them, aggregates, and outputs to a CSV.

1.  **Drag and Drop `Employee Flights.xlsx` Input:**
    * From the "Connections" pane, **drag and drop** `Employee Flights.xlsx` onto the flow pane, *below* the `Airport Codes` branch.
    * This creates an `Input` step named `Employee Flights`.

2.  **Add "Clean 1" Step:**
    * Click the `+` icon next to the `Employee Flights` input step.
    * Select **"Clean Step"**.
    * **Rename** this step: `Clean 1`.
    * **Configure Clean 1:** Double-click `Clean 1`. Perform any necessary initial cleaning (e.g., removing whitespace, changing data types, renaming fields).

3.  **Drag and Drop `Southwest 2019.csv` Input:**
    * From the "Connections" pane, **drag and drop** `Southwest 2019.csv` onto the flow pane, *next to* the `Employee Flights` input.
    * This creates an `Input` step named `Southwest 2019`.

4.  **Add "Clean 2" Step:**
    * Click the `+` icon next to the `Southwest 2019` input step.
    * Select **"Clean Step"**.
    * **Rename** this step: `Clean 2`.
    * **Configure Clean 2:** Double-click `Clean 2`. Perform any necessary initial cleaning for this dataset, ensuring fields match `Employee Flights` for unioning (e.g., same column names, compatible data types).

5.  **Add a "Union" Step:**
    * **Drag the `Clean 2` step and drop it directly onto the `Clean 1` step.**
    * Tableau Prep will offer options; select **"Union"**. This creates a new `Union` step.
    * **Rename** this step: `Union`.
    * **Configure Union:** Double-click `Union`. Review the "Field Mappings" to ensure columns from both inputs are correctly aligned. Drag unmapped fields to correct matches if necessary.

6.  **Add a "Cleanup" Clean Step:**
    * Click the `+` icon next to the `Union` step.
    * Select **"Clean Step"**.
    * **Rename** this step: `Cleanup`.
    * **Configure Cleanup:** Double-click `Cleanup`. This step is described as "Merge & remove fields, recap values, calc Frequency Segment."
        * **Merge Fields:** If you have duplicate fields (e.g., `ID_x`, `ID_y` from a previous join that should have been a union), you can select both, right-click, and choose "Merge Fields."
        * **Remove Fields:** Select any unnecessary fields and click the **three dots (...)** then **"Remove Field"**.
        * **Recap Values (Group and Replace):** For categorical fields, identify inconsistent spellings or values (e.g., "CA", "California"). Select them in the Profile Pane, right-click, and choose **"Group Values"** $\rightarrow$ **"By selection"** (or use phonetic/spelling grouping).
        * **Calculate Frequency Segment:**
            * Click the **"+"** next to any field name in the Profile Pane and select **"Create Calculated Field"**.
            * Write the calculation logic for `Frequency Segment` here based on your business rules (e.g., `IF [FlightCount] >= 50 THEN 'High' ELSE 'Low' END`).

7.  **Add a "Frequency Seg." Aggregate Step:**
    * Click the `+` icon next to the `Cleanup` step.
    * Select **"Aggregate"**. A new aggregate step will appear.
    * **Rename** this step: `Frequency Seg.`.
    * **Configure Aggregate:** Double-click `Frequency Seg.`. This step is described as "Rollup to frequency segment level."
        * **Drag and Drop:**
            * **Grouping Fields:** Drag the `Frequency Segment` field (created in the previous step) from the `Fields` list to the "Grouped Fields" section.
            * **Aggregated Fields:** Drag other numerical fields (e.g., `FlightCount`, `PassengerCount`) to the "Aggregated Fields" section and choose the desired aggregation (e.g., `SUM`, `AVG`, `COUNT`).

8.  **Add an "Output" Step for `Frequency Segment.csv`:**
    * Click the `+` icon next to the `Frequency Seg.` step.
    * Select **"Output"**. A new output step will appear.
    * **Rename** this step: `Frequency Segment.csv`.
    * **Configure Output:** Double-click `Frequency Segment.csv`.
        * For "Output Type," select **"File"**.
        * Click **"Browse"** to choose where to save the file.
        * For "Output Name," type `Frequency Segment`.
        * For "Save as type," select **"Comma Separated Value (.csv)"**.
        * Click "Accept" or "Save."

---

**III. Completing the "Airline Travel.csv" Branch with the Join**

Now, we connect the two branches.

1.  **Drag and Drop the `Cleanup` step onto the `Join` step:**
    * **Drag and drop** the `Cleanup` step (from the bottom branch) onto the `Join` step (from the top branch).
    * Tableau Prep will offer to "Add to Join." Select this option.

2.  **Configure the `Join` Step:**
    * Double-click the `Join` step.
    * **Define Join Clause:**
        * You'll see two tables in the join pane. **Drag and drop** the `Airport Code` field from the "Airport Codes" branch onto the corresponding airport code field from the "Employee Flights/Southwest" branch (e.g., `Origin Airport Code` or `Destination Airport Code`). This defines your join condition.
        * Adjust the **Join Type** (e.g., `Inner`, `Left`) as needed.
    * **Remove Duplicates/Unwanted Fields:** In the "Profile Pane" (bottom section of the join step), hide or remove any duplicate fields resulting from the join (e.g., if both tables had an "Airport Code" field, keep one and remove the other).

3.  **Add an "Output" Step for `Airline Travel.csv`:**
    * Click the `+` icon next to the `Join` step.
    * Select **"Output"**. A new output step will appear.
    * **Rename** this step: `Airline Travel.csv`.
    * **Configure Output:** Double-click `Airline Travel.csv`.
        * For "Output Type," select **"File"**.
        * Click **"Browse"** to choose where to save the file.
        * For "Output Name," type `Airline Travel`.
        * For "Save as type," select **"Comma Separated Value (.csv)"**.
        * Click "Accept" or "Save."

---

**Final Step: Run the Flow**

* Once all steps are configured, click the **"Run Flow"** button (or "Publish" if you're publishing to Tableau Server/Cloud) in the top right corner of Tableau Prep Builder to execute the entire workflow and generate your output files.

