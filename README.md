# EXP-19

Aim

To study and implement real-world and interactive data visualizations using Python.

1. Treemap (plotly.express.treemap)
Theory

A treemap represents hierarchical data using nested rectangles. The size of each rectangle corresponds to a numerical value (such as budget). It is a space-efficient alternative to pie charts, especially useful when dealing with many categories.

Algorithm
Input: Provide hierarchical/categorical data with numerical values.
Space Division: Split the total display area into rectangles.
Rendering: Assign colors, draw rectangles, and label them accordingly.
Key Commands
px.treemap(...): Creates the treemap.
path=['Department']: Defines hierarchy levels (can include sub-levels).
values='Budget': Determines rectangle size based on numeric data.
2. Dendrogram (scipy.cluster.hierarchy)
Theory

A dendrogram is a tree diagram used in hierarchical clustering to show relationships between data points. The vertical axis represents distance (dissimilarity), and higher connections indicate greater differences.

Algorithm
Distance Calculation: Measure distance between all data points.
Agglomeration: Merge the closest points into clusters.
Linkage: Compute distances between clusters using methods like Ward’s method.
Repeat: Continue merging until one cluster remains.
Key Commands
linkage(data, method='ward'): Performs clustering computations.
dendrogram(linked): Visualizes the clustering structure.
3. Venn Diagram
Theory

Venn diagrams illustrate relationships between sets. Overlapping regions represent common elements, while separate areas show unique elements.

Algorithm
Input: Define sets A and B.
Set Operations: Calculate intersection (A∩B), A−B, and B−A.
Sizing: Adjust circle sizes based on element counts.
Rendering: Draw circles and label each region.
Key Commands
venn2([A, B], set_labels=...): Generates a two-set Venn diagram.
4. Sankey Diagram (plotly.graph_objects.Sankey)
Theory

Sankey diagrams show flow between stages, where the width of each connection represents the magnitude of flow. They are useful for tracking processes like energy transfer, finances, or student progression.

Algorithm
Node Definition: Identify all stages.
Link Definition: Define connections with source, target, and value.
Layout Optimization: Arrange nodes to minimize overlap.
Rendering: Draw flows with widths proportional to values.
Key Commands
go.Sankey(...): Creates the diagram.
node=dict(label=...): Defines nodes.
link=dict(source=..., target=..., value=...): Defines flow between nodes.
5. 3D Scatter Plot (plotly.express.scatter_3d)
Theory

A 3D scatter plot extends a 2D plot by adding a third axis, allowing visualization of relationships among three variables.

Algorithm
Input: Select three continuous variables.
Mapping: Assign values to X, Y, and Z axes.
Projection: Display 3D data on a 2D screen.
Interactivity: Enable rotation for better visualization.
Key Commands
px.scatter_3d(df, x=..., y=..., z=...): Creates an interactive 3D plot.
6. Radar Chart (plotly.graph_objects.Scatterpolar)
Theory

A radar chart (or spider chart) displays multivariate data on a circular grid. It is commonly used for comparing performance metrics or skill sets.

Algorithm
Axis Creation: Divide the circle into equal sections.
Scaling: Normalize data values.
Plotting: Mark values on each axis.
Connecting: Join points to form a polygon and optionally fill it.
Key Commands
go.Scatterpolar(...): Uses polar coordinates.
r=values: Sets radial distances (data values).
theta=skills: Defines categories.
fill='toself': Fills the polygon area.
Conclusion

Advanced visualization techniques go beyond simple data presentation to enable deeper analysis. While basic charts summarize data, tools like Sankey diagrams reveal flow patterns, dendrograms help in clustering analysis, and radar charts compare multiple variables effectively. Mastering libraries such as Plotly and SciPy enhances the ability to create insightful, interactive, and professional data visualizations.
