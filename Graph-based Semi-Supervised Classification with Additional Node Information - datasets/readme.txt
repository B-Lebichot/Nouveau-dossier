All the datasets are composed of an adjacency matrix "A", a class vector "Y" (to predict) and a feature matrix "X". Using a Chi-square test, we keep only the 100 most significant variable for each dataset. This is the 100F version of the datasets (features have been shuffled). For the other version (xF with x = [50,25,10,5]), the x first features are kept.

For all of the dataset, if more than one graph component was present, we only use the biggest connected component, deleting all the others nodes, features and target classes. Also, we choose to work with undirected graph for all the dataset. If an adjacency matrix "A" was not symmetric, we used A = (A + transpose(A))/2 to symmetrize it.


Four "WebKB cocite" [Senaimag08]: These four data sets consist of web pages gathered from computer science departments from four universities (there is four data sets, one for each university), with each page manually labeled into one of four categories: course, faculty, student and project [Macskassy-07]. The pages are linked by citation. Each web page in the dataset is described by a boolean word vector indicating the absence/presence of the corresponding word from the dictionary. The dictionary consists of 1703 unique words or features (words appearing less than 10 times were ignored).
Orginally, a fifth category Staff was present but since it contained only a very few instances, it was merged with the Project class.
The original dataset is available here http://linqs.cs.umd.edu/projects//projects/lbc/index.html. 
 
- Texas WebKB cocite: 183 nodes with 4 classes
- Cornell WebKB cocite: 195 nodes with 4 classes
- Washington WebKB cocite: 230 nodes with 4 classes
- Wisconsin WebKB cocite: 251 nodes with 4 classes

  	
Three "Ego Facebook" dataset [McAuley2012] consists of 'circles' (or 'friends communities') from Facebook. Facebook data were collected from survey participants using a Facebook application. The original dataset includes node features (profiles), circles, and ego networks for 10 networks. Those data are anonymized. Since some circles or even networks are very small, we keep the three biggest networks and we define the classification task as follow: We picked the majority circle (the target circle) and agregated all the others (non-target circles). The ego node (central node connected to all others), by construction, belongs to all the circles, so we chose to label it as belonging to the target circle for simplicity. Each dataset have two classes.
The original dataset is available here http://linqs.cs.umd.edu/projects//projects/lbc/index.html. 

- Ego Facebook 1912: 756 nodes, 480 features
- Ego Facebook 1684: 793 nodes, 319 features        
- Ego Facebook 107: 1045 nodes, 576 features
  	

The "CiteSeer" dataset [senaimag08] consists of 3312 scientific publications classified into six classes. The pages are linked by citation. Each publication in the dataset is described by a boolean word vector indicating the absence/presence of the corresponding word from the dictionary. The dictionary consists and 3703 unique words or features (words appearing less than 10 times were ignored). 
The original dataset is available here http://linqs.cs.umd.edu/projects//projects/lbc/index.html. 

- Citeseer: 3312 nodes, 3703 features, 6 classes  


  The "Cora" dataset [senaimag08] consists of 2708 scientific publications classified into one of seven classes (Case Based, Genetic Algorithms, Neural Networks, Probabilistic Methods, Reinforcement Learning, Rule Learning or Theory). The pages are linked by citation. Each publication in the dataset is described by a boolean word vector indicating the absence/presence of the corresponding word from the dictionary. The dictionary consists of 1433 unique words or features (words appearing less than 10 times were ignored). The composition of the data sets is shown on Table \ref{tabothers}.
The original dataset is available here http://linqs.cs.umd.edu/projects//projects/lbc/index.html. 

- Cora: 2708 nodes 1434 nodes 7 classes	
		

The "Wikipedia" [senaimag08] dataset consists of Wikipedia articles that appeared in the featured list in the period Oct. 7-21, 2009. Each document belongs to one of 19 distinct categories (such as Science, Sport, Art,...), which were obtained by using the category under which each article was listed. After stemming and stop-word removal, it represents the text of each document as a tf/idf-weighted feature vector, for a total of 4973 features. The pages are linked by citation. The composition of the data sets is shown on Table \ref{tabothers}.
The original dataset is available here http://linqs.cs.umd.edu/projects//projects/lbc/index.html. 

- Wikipedia: 3271 nodes 4973 features 14 classes

References:

[Senaimag08]: 
S. Prithviraj, G. Galileo, M. Bilgic, L. Getoor, B. Gallagher, and T. Eliassi-Rad. Collective classication in network data. AI Magazine, 29(3):93-106, 2008.

[McAuley2012]:
J. McAuley and J. Leskovec. Learning to discover social circles in ego networks. Advances in Neural Information Processing Systems (NIPS), 2012.