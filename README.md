# To Reproduce!


1.  Install the 3 dependencies found in the requirements.txt file
1.  Create a .env file in the root directory that contains NEO4J_PASSWORD=yourpassword
1.  Create a folder called 'data' in the root directory and store the 'Hollins data' file in that directory
1.  In the terminal at the root directory, run 'docker compose up'
1.  Finally, run all cells in midterm.ipynb sequentially

# 
# CONTENT


[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/koCfb7gj)
# 4300 Take Home Midterm

**Draft - more detail to be added**

**Due Date:**  Nov 6, 2024 @ 11:59pm - Committed to GitHub

As part of a consulting team, You've been tasked by your manager to precompute
graph statistics for a collection of interconnected webpages.  You're starting 
with assessing the page rank for each collected webpage.  To make retrieval as
efficient as possible, you will store the page rank values in to Redis to support
fast ordering of results from future searches.  

## Important Details


1.  You may do this exam in teams of up to 2 students.  You may also choose to do it independently. 
1.  You can compose your solution by using either a Jupyter Notebook OR a stand-alone Python script.  
    1.  The effort needed to reproduce your output should be minimal and MUST BE CONTAINED IN YOUR REPO's README. 
   

### Your tasks:

1.  One member: fork this repository.  Add the other member as a team/collaborator. 
1.  Clone to your local machines. 
1.  Create a functional docker-compose.yaml file with the following characteristics:
    1.  a neo4j container with appropriately mapped folders for data persistence
    1.  a Redis container with appropriately mapped folders for data persistence
    1.  
1.  Download and write code to import the sample graph data set into Neo4j. The data set you will use can be found [here](https://www.dropbox.com/scl/fi/osrq5b1kdxei0ps1ywk15/Hollins-data.gz?rlkey=p6l9m9pw26y4diqnpz45oc7vv&dl=0).   (Note that it was originally found [here](https://www.limfinity.com/ir/).)
    1.  The data set contains the URLs for a little over 6000 webpages all from the same domain.
    1.  There are the over 20,000 edges connecting the various web pages
    1.  Explore the dataset in a text editor to get a feel for its structure.
1.  Explore the graph, characterize it.  
    1.  How many Nodes?
    1.  How many edges?
    1.  What's the longest shortest path? 
    1.  Any other characteristics of the graph that you think might be valuable or important. 
1.  Using the PageRank algorithm contain in the Neo4j add-on library, calculate the PageRank value of each web page.
    1.  How does the number of iterations algorithm parameter affect the runtime and output?  Can you characterize how many pages change rank based on number of iterations *x* and *x+10*? *x+20*? 
    1.  There are other page rank parameters that are available for you to modify.  I'll let you know ASAP if I think you need to change the defaults. 
1.  Store the calculated page rank value in Redis.  
1.  From all possible web pages included in the dataset, randomly generate 10 subsets of size 10 and 10 subsets of size 50.  For each subset, reorder the elements of the set into a list and print to the screen or in a Jupyter cell them in decreasing order based on their page rank value. Include the page rank value with each link. 
    1.   How does the orderings change as you adjust the number of iterations as in 6.1 above, if at all?  