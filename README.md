# swigg_shiny
Shiny app for visualizing genome graphs from SWIGG

# In development, current priorities:

  1. Interactive plot
    - Goal: view attributes of a node or edge when you hover over it in the plot
    - Plan: since plotly currently doesn't work with ggraph, try converting code from ggraph to igraph
  
  2. Add UI-responsive table
    - Goal: Get table of attributes for selected nodes and edges
    - Plan: 
      1. Add tab with table
      2. Add filtering for table
      3. Make table automatically filter based on selections (nodes, edges) in plot
      4. Make plot automatically label based on selections (rows) in table
      5. Add download button for table 

  3. Deploy on shinyapps.io (rather than rstudio.cloud or locally via GitHub code)
    - Goal: user can upload data (swigg-generated xml and swigg-annotation-generated (or custom made) annotation/attributes table)
    - Plan:
      1. Add upload SWIGG xml button
      2. Add upload SWIGG annotation/attributes tsv button
      3. Change inputs to "selectizeOption" to generalize to work with user/custom tsv files
      4. Add step to check format of tsv and compatibility with SWIGG xml --> generate ERROR if not compatible
      5. Add additional inputs based on user/custom tsv files
