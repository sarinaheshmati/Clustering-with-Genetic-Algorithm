# Clustering with Genetic Algorithm

This repository contains a project that explores clustering the Iris dataset using a Genetic Algorithm (GA) and compares its performance against the traditional K-means clustering algorithm. The project demonstrates the strengths of GA in overcoming some common challenges associated with K-means, such as sensitivity to initial conditions and the risk of getting trapped in local optima.

## Project Overview

- **Dataset**: The [Iris dataset](https://archive.ics.uci.edu/ml/datasets/iris), a classic dataset used in machine learning, contains 150 samples of iris flowers, with three species represented and four features per sample.

- **Objective**: To apply a Genetic Algorithm for clustering the Iris dataset and compare the results with those obtained from K-means clustering. The goal is to highlight the effectiveness of GA in finding better clustering solutions.

## Key Components

### Genetic Algorithm Implementation

- **Population Initialization**: A diverse initial population of potential cluster centers is generated randomly. Each solution is represented as a matrix corresponding to the cluster centers.

- **Selection Process**: The GA selects a mix of the best-performing solutions and some average ones to promote diversity and avoid premature convergence to local optima.

- **Crossover and Mutation**: New generations of solutions are created through crossover (combining parents) and mutation (introducing random changes), which helps the algorithm explore the solution space more thoroughly.

- **Clustering Process**: The GA iterates over 100 generations, refining the cluster centers to achieve optimal clustering. The fitness of each solution is measured by how well it groups the data points according to their features.

### Challenges and Considerations

- **Diversity Maintenance**: One of the challenges addressed by this project is maintaining diversity in the population to prevent the algorithm from getting stuck in suboptimal solutions.

### Overcoming Challenges in Genetic Algorithm

In the crossover and mutation phases, specific strategies were implemented to enhance the performance of the Genetic Algorithm:

- **Adaptive Crossover**: To prevent premature convergence, 80% of the parents were selected from the top-performing individuals, while 20% were chosen from a secondary tier. This approach maintained diversity and avoided local optima by ensuring a wider exploration of potential solutions.

- **Strategic Mutation**: To balance exploration and exploitation, the mutation rate was dynamically adjusted. Larger mutations were applied in early generations to explore widely, while more refined mutations were used in later stages to fine-tune the best solutions.

These innovative strategies significantly improved the clustering results compared to traditional methods.


### Results and Analysis

- **Visualization**: Clustering results are visualized in 2D using Principal Component Analysis (PCA) to reduce dimensionality. The GA consistently produces well-separated clusters, particularly excelling in cases where K-means struggles.

- **Accuracy**: The Genetic Algorithm achieves an accuracy range of 87% to 94%, typically around 90%, compared to 83% accuracy with K-means. This demonstrates the robustness of GA in clustering tasks.

- **Heatmap Analysis**: A detailed heatmap analysis shows the correctness of cluster assignments, confirming the GA's superior performance, particularly in distinguishing between clusters that are not linearly separable.

### Visualization and Analysis

#### Genetic Algorithm (GA)

- **2D Cluster Visualization**: The following image demonstrates the 2D visualization of clusters generated using the Genetic Algorithm (GA).

  <img width="929" alt="Screenshot 1403-06-06 at 8 08 20 AM" src="https://github.com/user-attachments/assets/5e25b36d-e12b-4f4e-b146-c4cca77bda85">

- **Correctness Heatmap**: The heatmap below shows the accuracy of the clustering labels for GA, indicating how well the clusters were formed.

  <img width="687" alt="Screenshot 1403-06-06 at 8 09 09 AM" src="https://github.com/user-attachments/assets/a38d18f8-b8cc-4dfa-9579-0739c8b901b8">

#### K-means Clustering

- **2D Cluster Visualization**: This image displays the 2D visualization of clusters generated using the K-means algorithm.

  <img width="929" alt="Screenshot 1403-06-06 at 8 08 37 AM" src="https://github.com/user-attachments/assets/2655deff-1fb5-4be3-bd21-9eefcfb5fe29">

- **Correctness Heatmap**: The heatmap for K-means illustrates the accuracy of the clustering labels, which is notably lower compared to GA.

  <img width="672" alt="Screenshot 1403-06-06 at 8 09 45 AM" src="https://github.com/user-attachments/assets/06ba915a-a8ba-4a8a-9e55-5e2e1b394734">

## Conclusion

This project highlights the potential of Genetic Algorithms in clustering tasks, especially in scenarios where traditional methods like K-means may fail to find optimal solutions. By simulating natural selection, GA can navigate complex solution spaces more effectively, leading to better clustering results.
