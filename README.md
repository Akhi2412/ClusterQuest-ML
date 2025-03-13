# ClusterQuest-ML

**# Problem Statement**
In the realm of social media, understanding the intricate dynamics of user interactions and community structures is important for businesses aiming to effectively engage with their target audience and capitalize on digital marketing opportunities.

In this project, we aim to build a system capable of automatically analyzing social media networks and identifying and clustering communities that can significantly benefit businesses operating in this space. Here's how such a system can be beneficial to businesses:
Audience Segmentation: By identifying clusters of users with similar interests, behaviors, or demographics, businesses can tailor their content and marketing strategies to resonate with specific audience segments. For example, a fashion brand could identify clusters of users interested in sustainable fashion and craft targeted campaigns to appeal to this eco-conscious audience.
Influencer Identification: Social media networks are teaming with influencers who wield significant influence over their followers. By analyzing network structures and identifying influential users within specific communities, businesses can strategically partner with influencers whose values align with their brand, maximizing the impact of influencer marketing campaigns.
Community Engagement: Engaging with social media communities in a meaningful way is essential for building brand trust and fostering customer relationships. By understanding the structure of social networks and the dynamics of user interactions, businesses can identify opportunities to engage with communities authentically, participate in relevant conversations, and provide value to users.
In summary, a solution that automates the analysis of social media networks and identifies cohesive communities can empower businesses to better understand their audience, optimize their marketing efforts, and foster genuine connections in the digital realm. By leveraging insights derived from social network analysis, businesses can navigate the complex landscape of social media with confidence and achieve their marketing objectives effectively.


**Machine Learning Problem**
In this problem, we aim to build Machine Learning models in order to cluster several social media users together. This is an unsupervised learning problem. However, we are not working with a structured tabular dataset like before. We are going to work with a special kind of data called Graph Data.

**About the dataset**
Download the dataset from https://snap.stanford.edu/data/facebook_combined.txt.gz
At its core, graph data represents relationships between entities. Imagine social networks like Facebook or Twitter, where users are connected to each other through friendships or follows. Each user is a node in the graph, and the connections between them are edges. This structure allows us to model complex relationships and interactions in a way that traditional tabular data cannot capture.
**Fundamentals of Graph Representation**
**Nodes (Vertices)**: These are the entities in our graph. In a social network, nodes could represent users, while in a transportation network, they could represent cities or airports.
**Edges (Links)**: These represent the relationships between nodes. In a social network, edges could indicate friendships or follows, while in a transportation network, they could represent roads or flight routes.
**Attributes**: Nodes and edges can have associated attributes that provide additional information. For example, a user node in a social network could have attributes such as age, location, or interests.

**Types of Graphs**
**Directed Graphs**: In these graphs, edges have a direction, indicating a one-way relationship between nodes. For example, in a Twitter network, the "follows" relationship is directed.
**Undirected Graphs**: Here, edges represent bidirectional relationships between nodes. For instance, in a Facebook network, friendships are typically undirected.

**Local vs Global Features**
**Local Features**
**Node-Level Features**: These are properties or characteristics specific to individual nodes in the graph. For example, in a social network graph, node-level features might include attributes such as age, gender, number of connections, etc.
**Edge-Level Features**: Similarly, these features are specific to the edges connecting nodes in the graph. They might represent properties such as edge weight, distance, similarity between connected nodes, etc.
Local features capture information about individual elements (nodes or edges) in the graph without considering the entire graph structure. They are typically used for tasks like node classification, link prediction, or recommendation systems.

**Global Features**
These features describe overall properties of the entire graph. They are derived by aggregating or summarizing information from all nodes and edges in the graph. Examples of graph-level features include graph density, average degree, centrality measures (e.g., betweenness centrality, closeness centrality), graph motifs, etc.

**Understanding the Facebook Graph Dataset**
The dataset consists of a file called facebook_combined.txt. 
Each line in the dataset denotes a connection between two users represented by corresponding user ids. For example, the following row denotes a connection between a user with user-id 1104 to a user with user-id 1404.

1104 1404

You can create a graph out of the connections represented by this data.
If you observe closely in the data file, you will notice that there is no entry in the file for a connection from user 1404 to user 1104 (opposite of the row above). This is because in Facebook, a friendship is a two way connection, which means that two friends on Facebook always follow each other. This is unlike X (formerly, Twitter) which exhibits follows type (one-way) relationship. On X, if you follow someone, they cannot see your updates unless they follow you as well. For e.g. on if you follow Elon Musk, you will be able to see his updates, however, he won’t be able to see your updates unless he follows you as well. While on Facebook, if you and your father are friends, both you and he will be able to see each other’s updates. Therefore, this dataset is an example of an undirected graph.


**Approaching the Problem**
You need to prepare a Jupyter Notebook consisting of the following:

**Data Collection**: Download the dataset from here. You need to work with facebook_combined.txt file.

**Graph Representation**: Load the txt file as Graph. Instructions given in the next section.

**Feature Engineering:** Derive informative features from the loaded graph. Instructions on engineering new features given in the next section.

**Data Preparation**: Prepare the feature-engineered data for clustering. This may involve normalization or scaling of the features, handling missing values, or any other necessary preprocessing steps to ensure the data is suitable for clustering algorithms.

**Exploratory Data Analysis**: Using charts and visualizations, explore patterns and summarize the characteristics of the dataset.

**Clustering**: Apply clustering algorithms to group nodes based on their shared structural properties. Consider techniques such as k-means, hierarchical clustering, DBSCAN etc. Experiment with different parameter settings and evaluation metrics to find the most appropriate clustering approach for the given problem.

**Evaluation**: Assess the quality of the generated clusters by employing appropriate evaluation metrics. Evaluate the clustering performance using metrics such as the silhouette score, Calinski-Harabasz index, and Davies-Bouldin index.

