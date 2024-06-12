# Research-TrafficAdaptor
This project is trying to recreate https://dl.acm.org/doi/abs/10.1145/3557915.3560938 .
This project involves clustering and analyzing traffic trajectories using K-means clustering and transition matrix analysis. The primary goal is to understand the movement patterns by clustering geographic coordinates and then analyzing the transitions between these clusters.

## Introduction

This project processes traffic trajectory data from multiple files, extracts latitude and longitude coordinates, performs K-means clustering on these coordinates, and constructs a transition matrix to understand the transitions between clusters. The transition matrix is further analyzed to discretize the transitions using K-means clustering.

## Data Extraction

We use Geolife GPS trajectory dataset https://www.microsoft.com/en-us/research/publication/geolife-gps-trajectory-dataset-user-guide/ for this project. This is a GPS trajectory dataset collected by Microsoft Research Asia in GeoLife project by 182 users in a period of over three years (from April 2007 to August 2012).
The data is stored in multiple PLT files, each containing trajectory information. The latitude and longitude coordinates are extracted from these files, which are then used for clustering analysis.

## Clustering Trajectories

K-means clustering is used to cluster the latitude and longitude coordinates. The number of clusters can be adjusted as needed. The clustering helps in identifying distinct movement patterns within the trajectory data.

## Transition Matrix Construction

A transition matrix is constructed to capture the transitions between different clusters. Each element in the matrix represents the probability of moving from one cluster to another.

## Discretizing the Transition Matrix

To further analyze the transition matrix, it is discretized using K-means clustering on the transition probabilities. This helps in grouping similar states together and understanding the overall movement dynamics.

## Requirements

- Python 
- NumPy
- Scikit-learn
- Matplotlib

