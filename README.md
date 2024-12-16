# To Reproduce!


1.  Install the 3 dependencies found in the requirements.txt file
1.  Create a .env file in the root directory that contains NEO4J_PASSWORD=yourpassword
1.  Create a folder called 'data' in the root directory and store the 'Hollins data' file in that directory
1.  In the terminal at the root directory, run 'docker compose up'
1.  Finally, run all cells in midterm.ipynb sequentially

# 
# CONTENT

A graph statistics exploration using webpage linking data from Hollins University (hollins.edu). Utilizes the Neo4j graph database to store webpage nodes and link relationships, and the 
Neo4j Graph Data Science library to assess page ranks for each collected webpage. Explores various page rank iterations and creates mock search results by selecting random web pages and ordering by page rank values stored in a Redis database instance. Additional analysis includes the longest shortest paths between nodes, implementing the betweenness centrality algorithm to 
identify central nodes, and community detection implementations like label propagation.
