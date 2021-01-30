This repository contains implementation of algorithms proposed in the paper “Efficient Binary Embedding of Categorical Data” due to  Bhisham Dev Verma, Rameshwar Pratap, and Debajyoti Bera. The paper proposed two algorithms namely Cabin and Cham. Cabin take high dimensional categorical dataset as input and compress them into low dimensional binary vectors. Cham takes the binary sketch outputted by Cabin and outputs an estimation of original pairwise Hamming distance. 

We also provide implementation of  some of beaslines used in the paper for comparison such as Feature Hashing, SimHash, BCS, and Hamming LSH. 

Feature Hashing and SimHash takes high dimensional real valued vectors as input, and outputs low-dimensional real valued which closely estimate the original pairwise Inner product and Cosine similarity, respectively. We adhocly apply them for categorical vectors, and as their sketches are discrete vectors, we report the hamming distance from the sketch as the estimate of original pairwise Hamming distance between data points. We use the following reference of Feature hashing and SimHash respectively. 


@inproceedings{Feature_Hashing,
	author    = {Kilian Q. Weinberger and nirban Dasgupta and John Langford and Alexander J. Smola and Josh Attenberg},          
    title     = {Feature hashing for large scale multitask learning},  
    booktitle = {Proceedings of the 26th Annual International Conference on Machine    
               Learning, {ICML} 2009, Montreal, Quebec, Canada, June 14-18, 2009},     
    pages     = {1113--1120},          
    year      = {2009},          
    crossref  = {DBLP:conf/icml/2009},   
    url       = {https://doi.org/10.1145/1553374.1553516},  
    doi       = {10.1145/1553374.1553516},       
    timestamp = {Tue, 06 Nov 2018 16:58:29 +0100},     
    biburl    = {https://dblp.org/rec/conf/icml/WeinbergerDLSA09.bib},   
    bibsource = {dblp computer science bibliography, https://dblp.org}       
}


@inproceedings{SimHash,   
 author    = {Moses Charikar},   
  title     = {Similarity estimation techniques from rounding algorithms},  
  booktitle = {Proceedings on 34th Annual {ACM} Symposium on Theory of Computing,  
               May 19-21, 2002, Montr{\'{e}}al, Qu{\'{e}}bec, Canada},  
  pages     = {380--388},  
  year      = {2002},  
  crossref  = {DBLP:conf/stoc/2002},  
  url       = {https://doi.org/10.1145/509907.509965},  
  doi       = {10.1145/509907.509965},  
  timestamp = {Sun, 02 Jun 2019 21:10:33 +0200},  
  biburl    = {https://dblp.org/rec/conf/stoc/Charikar02.bib},  
  bibsource = {dblp computer science bibliography, https://dblp.org}  
}


We apply BCS and Hamming-LSH on the binary embedding outputted by the method BinEm (see line number 6-13 of Algorithm 1 stated in the paper “Efficient Binary Embedding of Categorical Data”). We use the following reference for BCS and Hamming LSH, respectively. 

@inproceedings{BCS,  
  author    = {Rameshwar Pratap and Raghav Kulkarni and Ishan Sohony},  
  title     = {Efficient Dimensionality Reduction for Sparse Binary Data},  
  booktitle = {{IEEE} International Conference on Big Data, Big Data 2018, Seattle,  
               WA, USA, December 10-13, 2018},  
  pages     = {152--157},  
  year      = {2018},  
  crossref  = {DBLP:conf/bigdataconf/2018},  
  url       = {https://doi.org/10.1109/BigData.2018.8622338},  
  doi       = {10.1109/BigData.2018.8622338},  
  timestamp = {Thu, 19 Mar 2020 16:53:40 +0100},  
  biburl    = {https://dblp.org/rec/conf/bigdataconf/PratapKS18.bib},  
  bibsource = {dblp computer science bibliography, https://dblp.org}  
}

@inproceedings{Hamming_LSH,  
  author    = {Aristides Gionis and Piotr Indyk and Rajeev Motwani},  
  title     = {Similarity Search in High Dimensions via Hashing},  
  booktitle = {VLDB'99, Proceedings of 25th International Conference on Very Large  
               Data Bases, September 7-10, 1999, Edinburgh, Scotland, {UK}},  
  pages     = {518--529},  
  year      = {1999},  
  crossref  = {DBLP:conf/vldb/99},  
  url       = {http://www.vldb.org/conf/1999/P49.pdf},  
  timestamp = {Thu, 12 Mar 2020 11:33:50 +0100},  
  biburl    = {https://dblp.org/rec/conf/vldb/GionisIM99.bib},  
  bibsource = {dblp computer science bibliography, https://dblp.org}  
}
