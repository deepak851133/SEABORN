Seaborn Visualization Guide

📌 Introduction

Seaborn is a powerful Python library for statistical data visualization built on top of Matplotlib. It provides an easy way to generate visually appealing and informative graphs with minimal code.

📥 Installation

To install Seaborn, use:

pip install seaborn

Ensure you also have Matplotlib and Pandas installed:

pip install matplotlib pandas

📊 Key Seaborn Concepts

1️⃣ Basic Plots

🔹 Line Plot

import seaborn as sns
import matplotlib.pyplot as plt

sns.lineplot(x=[1, 2, 3, 4], y=[10, 20, 25, 30])
plt.show()

🔹 Scatter Plot

sns.scatterplot(x="total_bill", y="tip", data=sns.load_dataset("tips"))
plt.show()

🔹 Histogram

sns.histplot(data=sns.load_dataset("penguins"), x="flipper_length_mm", bins=20)
plt.show()

2️⃣ Categorical Plots (sns.catplot)

Seaborn provides various categorical plots:

Kind

Description

bar

Shows mean values with error bars

count

Counts occurrences of a category

box

Shows distributions with quartiles & outliers

violin

Combines KDE and box plots

swarm

Shows all data points without overlapping

strip

Similar to swarm but allows jitter

point

Connects means with confidence intervals

🔹 Example: Box Plot

sns.catplot(x="day", y="total_bill", data=sns.load_dataset("tips"), kind="box")
plt.show()

3️⃣ Advanced Visualizations

🔹 Pair Plot

Shows relationships between multiple numerical variables.

sns.pairplot(sns.load_dataset("iris"), hue="species")
plt.show()

🔹 Heatmap (Correlation Matrix)

import numpy as np
import pandas as pd

data = sns.load_dataset("flights").pivot("month", "year", "passengers")
sns.heatmap(data, annot=True, fmt="d", cmap="coolwarm")
plt.show()

🎯 Customization & Styling

Seaborn provides themes to improve visualization aesthetics:

sns.set_theme(style="darkgrid")

Other styles: whitegrid, dark, white, ticks

To customize colors:

sns.color_palette("pastel")

📌 Conclusion

Seaborn makes data visualization easier and more visually appealing than raw Matplotlib. It is highly useful for exploratory data analysis (EDA) and statistical insights.

For more details, check out the official documentation: Seaborn Docs
