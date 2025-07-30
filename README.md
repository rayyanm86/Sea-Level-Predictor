# Sea-Level-Predictor
This project analyzes historical sea level data and predicts future sea levels using linear regression. Two lines of best fit are plotted: one based on all available data and another based only on data from the year 2000 onward.


## 📁 Files

- `epa-sea-level.csv` — Dataset from the EPA containing yearly sea level measurements.
- `sea_level_predictor.py` — Main Python script to generate the plot.
- `sea_level_plot.png` — Output image showing the scatter plot and regression lines.
- `README.md` — You're reading it!


## 📊 Features

- Reads sea level data from a CSV file.
- Uses `matplotlib` to visualize data.
- Fits two linear regression lines using `scipy.stats.linregress`:
  - One using **all data**.
  - One using data from **2000 onwards**.
- Saves the final plot as `sea_level_plot.png`.
- ![image alt]("https://github.com/rayyanm86/Sea-Level-Predictor/blob/3444c472e232d83e101ca9ea606f8332186e3ccc/sea_level_plot.png")


## 🧪 How to Run

1. Ensure you have Python 3 installed.
2. Install the required libraries:

   ```bash
   pip install pandas matplotlib scipy
