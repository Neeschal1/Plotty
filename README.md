## Matplotlib
This is the AI/ML learning journey and learning matplotlib is at #3.

Table of Content:

        - Project Overview
        - Installation
        - Uses
        - Features
        - Examples



## Project Overview:

Matplotlib: Matplotlib is a Python library for visualizing data. It allows us to create line plots, bar charts, pie charts, histograms, scatter plots, and more to represent data graphically. For eg:
Let us make two python list:

x_axis = [10, 20, 30, 40, 50]
y_axis = [4, 5, 2, 3, 1]

plt.plot(
        x_axis,                      # Anything that needs to be in our x-axis
        y_axis,                      # Anything that needs to be in our y-axis
        marker = "o"                 # Makes the point of connection between x-axis and y-axis circular 
        markerfacecolor = "blue"     # Makes the marker's center color blue
        markeredgecolor = "red"      # Makes the marker border/edge color red
        linestyle = "-"              # Makes the --- line throughout the graph
        color = "green"              # Makes the line color green
        linewidth = 2                # Increase the width of line by 2
)










## Installation

Matplotlib library can be installed using the following command:

pip install matplotlib
conda install matplotlib









## Uses

Matplotlib is a powerful Python library used for data visualization, allowing users to represent data graphically to easily understand patterns, trends, and relationships. It supports various types of plots such as line graphs, bar charts, scatter plots, histograms, and pie charts, and enables extensive customization of colors, markers, labels, and titles. Matplotlib integrates seamlessly with libraries like NumPy and Pandas, making it ideal for data analysis and AI/ML projects, and also allows saving plots in formats like PNG or PDF for reports and presentations. Overall, it helps both beginners and professionals analyze, interpret, and present data effectively.

Types of matplotlib visualization:
1. Linear Graph Plots
2. Pie Chart
3. Bar graph (Vertical)
4. Bar graph (Horizontal)
5. Histograms


   1. Linear Graph Plots
   
      This type of matplotlib visualization creates the relationship in between two entities inside a graph, connecting each of their relationships in x-axis and y-axis. together, connecting all those meeting points makes a single graph that explains the data through the same graph plots.
      
      Notes: If the data is in nested python list, it creates the dots only.

      How to implement it?
      after installing the necesary packages, follow the following commands:

      - plt.figure(figsize=(10, 15)) # Determine your own desired chart size
      - plt.title("Give title to the main graph", fontsize=20, fontweight='bold', color='red') # These all are similar to css property
      - plt.plot(x_axis, y_axis, linestyle="-", color='blue', markercolor='orange', markeredgecolor='purple', linewidth=0.2) # mention the x_axis and y_axis variable in the beginning. blue color is for the line color, markercolor means the color of the center of the marked area where the x-axis and y-axis meet, markeredgecolor means the border color of the marker, linewidth means the thickness of the line drawn in the graph
      - plt.xlabel("Mention the name of x-axis of your graph") # You can mention the css property here also, just like in plt.title
      - ply.ylabel("Mention the name of y-axis of your graph") # You can mention the css property here also, just like in plt.title
      - plt.xticks(rotation=15) # You can mention the css property here also, just like in plt.title
      - plt.yticks(rotation=-15) # You can mention the css property here also, just like in plt.title
      - plt.grid(True, linestyle="-", linewidth=0.5) # plt.grid(True) shows the grid in overal frame of the graph.
      - plt.savefig("name_of_fig.png") # Save the figure in your currently working directory
      - plt.show() # View the entire data through the bargraph



   2. Pie Chart

      This type of matplotlib visualization shows the whole data inside a pie chart, a circular chart where all the entities are managed properly, each indicating with different color.

      How to implement it?
      after installing the necesary packages, follow the following commands:

      - plt.figure(figsize=(10, 15)) # Determine your own desired chart size
      - plt.title("Give title to the main pie chart", fontsize=20, fontweight='bold', color='red') # These all are similar to css property

        #Assume the data:
        
                data = {
                    "Food":30,
                    "Clothes":15,
                    "Shelter":20,
                    "Family":10,
                    "Education":15,
                    "Care": 10
        }

        plot_data = list(data.values()) # to gain access to the lefter values of the dictionaries
        indexes = list(data.keys()) # to gain access to the righter values of the dictionaries
  
        
      - plt.pie(plot_data, labels=indexes, startangle=120, autopct="%1.1f%%") # plot_data is the main data to visualize inside the pie chart, labels shows the description of the data shown inside the pie chart, startangle starts the piechart from a certain angle, autopct="%1.1f%%" shows the percent value inside the piechart
      - plt.show()
