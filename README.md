# 🧠 EEG Topoplot Hardcoding with `imagesc`

This repository demonstrates how to **manually implement a topographical scalp plot (topoplot)** using MATLAB's `imagesc` function — a pixel-based alternative to EEGLAB's `topoplot` function. It visualizes EEG data by interpolating electrode potentials over a 2D scalp map.

---

## 📜 Project Description

This coursework explores the inner workings of EEG topoplot generation. Instead of relying solely on EEGLAB’s built-in `topoplot`, we **manually interpolate and visualize EEG channel activity** using MATLAB’s plotting and interpolation functions. This allows a deeper understanding of:

- Electrode coordinate transformations
- Grid-based interpolation (`scatteredInterpolant`)
- Data visualization with `imagesc`
- Comparison with EEGLAB’s `topoplot` function

---

## ⚙️ How It Works

### Step-by-step Breakdown:

1. **Load EEG Data**  
   Load the `.mat` file containing EEG data, channel positions, and metadata.

2. **Convert Spherical to Cartesian Coordinates**  
   Use `pol2cart()` to convert polar electrode locations to 2D Cartesian space for plotting.

3. **Plot Electrode Locations**  
   Display the electrodes using `scatter()` on a 2D plane.

4. **Generate a 2D Grid for Interpolation**  
   Create an evenly spaced meshgrid covering the electrode area for interpolation.

5. **Select and Average EEG Data**  
   Choose a timepoint (e.g., 200ms) and average across epochs.

6. **Interpolate Data Across Grid**  
   Use `scatteredInterpolant()` to spread electrode data over the grid.

7. **Visualize with `imagesc()`**  
   Plot the interpolated grid data using pixel-based rendering.

8. **Compare with `topoplot()`**  
   Finally, visualize the same data using EEGLAB’s `topoplot()` for comparison.


