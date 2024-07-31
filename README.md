import matplotlib.pyplot as plt

# Data for pie chart with further breakdown
labels = [
    'NN related cases (Total)', 
    'Software issues (NN related)', 
    'Hardware issues (NN related)', 
    'NN connection (Software cases)', 
    'NN connection (Hardware cases)'
]
sizes = [25, 11.25, 13.75, 5.4, 6.6]
colors = ['cyan', 'orange', 'green', 'red', 'purple']  # Changed from blue to cyan
explode = (0.1, 0, 0, 0, 0)  # explode the first slice (NN related cases)

# Create pie chart
plt.figure(figsize=(10, 10))
plt.pie(sizes, explode=explode, labels=labels, colors=colors, autopct='%1.1f%%', shadow=True, startangle=140)
plt.title('Detailed Breakdown of NN Related Cases')
plt.axis('equal')  # Equal aspect ratio ensures that pie is drawn as a circle.

# Display the pie chart
plt.show()
