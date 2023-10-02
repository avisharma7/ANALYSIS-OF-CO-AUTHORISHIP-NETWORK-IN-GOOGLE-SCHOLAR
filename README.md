# Co-Authorship Network Analysis using Google Scholar Data

## Project Overview

The Co-Authorship Network Analysis project focuses on extracting data from Google Scholar to create and analyze co-authorship networks among researchers. By analyzing these networks, the project aims to provide insights into the influence of researchers in their respective fields. The key components and objectives of the project are as follows:

### Introduction

To construct a co-authorship network, the project requires the name of an author. From the author's Google Scholar profile, the list of co-authors is extracted, and this information is used to create a network with authors as nodes and their relationships as edges. The project employs web scraping techniques in Python to achieve this. After constructing the network, various centrality measures are applied, including degree centrality, closeness centrality, and betweenness centrality. Additionally, PageRank, an example of eigenvector centrality, is used for ranking authors. The results are then visualized.

### Modules of the Proposed System

The project is divided into four modules to ensure reusability and maintainability:

#### 1. Web Scraping

   - **Objective**: Obtain data from Google Scholar by scraping author profiles.
   - **Description**: The web scraping module uses Python's Beautiful Soup and requests modules to fetch data from Google Scholar. It parses the HTML response to extract author information.

#### 2. Creating Network and Subnetwork

   - **Objective**: Create co-authorship networks and generate subnetworks.
   - **Description**: After collecting data through web scraping, the project constructs a network by establishing connections between authors. It also prunes weak nodes to generate a subnetwork for further analysis.

#### 3. Network Analysis

   - **Objective**: Calculate centrality measures such as degree centrality, closeness centrality, betweenness centrality, and PageRank for authors in the network.
   - **Description**: The network analysis module applies various centrality measures to assess the importance of authors within the co-authorship network. PageRank, a widely-used algorithm for ranking web pages, is used to rank authors based on their influence.

#### 4. Result Visualization

   - **Objective**: Visualize the co-authorship network for pattern observation.
   - **Description**: This module creates visualizations of the co-authorship network to make it easier to identify patterns and key actors within the network.

### Proposed System Model

The proposed framework mainly consists of the web scraping module. It takes the Google Scholar URL of an author and the maximum number of nodes to be considered. It extracts co-authors' information from that URL and adds them to the network. Once the maximum number of nodes is reached, the loop breaks, and a final network of co-authors is obtained. Centrality measures are then calculated for each node, and a subgraph of the most prominent actors is generated by filtering them through the PageRank algorithm.

### Proposed System Analysis and Design

The system comprises three main components: the web scraper, network generator, and network analyzer.

#### Web Scraper

   - **Implementation**: Utilizes Beautiful Soup to parse HTML and fetch author information from Google Scholar profiles.
   - **Description**: This component sends requests to author profile URLs, extracts HTML data, and processes it to obtain the required information.

#### Network Generator

   - **Implementation**: Utilizes the networkx library.
   - **Description**: Generates the co-authorship network based on the data collected by the web scraper. It creates a dictionary of co-authors and uses it to build the network. A subnetwork with nodes having PageRank scores higher than the average value is also generated.

#### Network Analysis

   - **Implementation**: Utilizes networkx's centrality measures and algorithms.
   - **Description**: Calculates various centrality measures, including degree centrality, closeness centrality, betweenness centrality, and PageRank, for each node in the network.

### Centrality Measures

- **Degree Centrality**: Measures the number of edges incident on a node.
- **Closeness Centrality**: Calculates the average length of the shortest paths between a node and all other nodes in the graph.
- **Betweenness Centrality**: Identifies nodes that act as critical bridges in the shortest path between other nodes.
- **PageRank Algorithm**: Ranks nodes based on their influence in the network, originally designed by Google to rank web pages.

### Result Visualization

The co-authorship network is visualized to facilitate pattern observation. Node sizes in the graph are determined by node degree, aiding in the visualization of the network's structure.

## Getting Started

To get started with this project:

1. Clone the repository to your local machine.

2. Ensure you have the necessary Python libraries installed, including Beautiful Soup, requests, and networkx.

3. Configure the web scraper module to specify the Google Scholar author profiles you want to scrape.

4. Run the project to collect data, generate the network, analyze centrality measures, and visualize the results.

## Contribution Guidelines

If you'd like to contribute to this project, please follow these guidelines:

1. Fork the repository on GitHub.

2. Create a feature branch for your contributions.

3. Submit a pull request detailing the changes you've made and their purpose.

4. Ensure your code is well-documented and adheres to coding best practices.

## Support

For any questions, issues, or assistance with using this project, please feel free to reach out to the project maintainers.

Thank you for your interest in the Co-Authorship Network Analysis project!

--- 

*Note: This readme provides a general structure and description of the project. Ensure that you update the document with specific details, such as installation instructions and contact information, as needed for your project.*
