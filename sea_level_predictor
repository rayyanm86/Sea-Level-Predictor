import pandas as pd
import matplotlib.pyplot as plt
from scipy.stats import linregress

def draw_plot():
    df = pd.read_csv("epa-sea-level.csv")
    plt.figure(figsize=(10, 6))
    plt.scatter(df['Year'],df['CSIRO Adjusted Sea Level'], label='Original Data', color='g')
    
    #first_line
    line_info = linregress(df['Year'],df['CSIRO Adjusted Sea Level'])
    years_ext = list(range(1880, 2051))
    sea_levels_all = [line_info.slope * year + line_info.intercept for year in years_ext]
    plt.plot(years_ext,sea_levels_all, 'r', label='Best Fit: All Data')

    #second_line
    second_line = df[df['Year'] >= 2000]
    line_info_sec = linregress(second_line['Year'],second_line['CSIRO Adjusted Sea Level'])
    years_sec = list(range(2000,2051))
    sea_levels_sec = [line_info_sec.slope * year + line_info_sec.intercept for year in years_sec]
    plt.plot(years_sec,sea_levels_sec, 'b', label='Best Fit: From 2000')

    plt.xlabel('Year',fontsize=15)
    plt.ylabel('Sea Level (inches)', fontsize=15)
    plt.title('Rise in Sea Level')
    plt.legend()
    
    plt.savefig('sea_level_plot.png')
    return plt.gca()
