# cis7
cis7 project
Anthony Mendoza
In this project i'll be solving what trips the specialist can take, the shortest path and cost, and creating a c++ program that represents the trip, low-cost, and shortest path. Some solution ill be implementing in the project is trying to find the shortest path and low cost trips and using the Floyd-Warshall algorithm. To start us off we first need to know what type of paths/routes the specialist can take. When we calcuate and start off we can see that the specialist can take different routes just to get to these 3 different places, But we also have to figure out which route will be best to take.
Riverside → Moreno Valley → Perris → Hemet
Riverside → Hemet → Moreno Valley → Perris
Riverside → Hemet → Perris → Moreno Valley
Riverside → Moreno Valley → Hemet → Perris
Riverside → Perris → Moreno Valley → Hemet
Riverside → Perris → Hemet → Moreno Valley
![Screenshot 2024-12-08 124654](https://github.com/user-attachments/assets/46ea477a-d5ee-4b12-82e6-c4faaaa1e716)

Based off the the graph we can tell the distants from each location. In order to make things easily we can organize this information.
Riverside to Moreno Valley: 16
Riverside to Perris: 24
Riverside to Hemet: 33
Moreno Valley to Perris: 18
Moreno Valley to Hemet: 26
Perris to Hemet: 30
Now we can figure out the shortest route to take by adding each provided distance to figure out the shortest route. 
Riverside → Moreno Valley → Perris → Hemet
Distance: 16 + 18 + 30 = 64
Riverside → Moreno Valley → Hemet → Perris
Distance: 16 + 26 + 30 = 72
Riverside → Perris → Moreno Valley → Hemet
Distance: 24 + 18 + 26 = 68
Riverside → Perris → Hemet → Moreno Valley
Distance: 24 + 30 + 26 = 80
Riverside → Hemet → Moreno Valley → Perris
Distance: 33 + 26 + 18 = 77
Riverside → Hemet → Perris → Moreno Valley
Distance: 33 + 30 + 18 = 81
After we calucated the distance we can tell that the shortest distance from Riverside and the other location, it is best to go from Riverside to Moreno Valley to Perris and lastly Hemet since the total of distance is 64.
To create a C++ program to represnet the trips, low-cost and shortest path we would have to use an adjacency Matrix, Floyd-Warshall Algorithm, and a output. The Matrix represents the grpah that includes the cities and distances. The Floyd-Warshall would find the shortest paths between all pairs of cities. Lastly output would use both the other apporaches and print the matrix and the distance.

This code allows us to see the shortest distants from the different routes.

To write the Pseudocode we have to define INF and initilalize the adjaceny matrix adjMatrix with the distance from the cities. After we then have to print the adjacency matrix using printMatrix function. For Floyd-Warshall algorithm we set n to the size of the adjancency matrix, use dist to initiailize the distance matrix with the values from the adjacney matrix. Latestly we use the printMatrix function again to print the shortest path matrix. 

