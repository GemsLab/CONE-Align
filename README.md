# CONE-Align
This is a reference implementation for CONE-Align, an unsupervised network alignment method that uses node embeddings to model intra-graph node proximity and then aligns the embedding subspaces to make the node embeddings comparable across graphs.

**Acknowledgement**: parts of this code base were adapted from <a href="https://github.com/xptree/NetMF/blob/master/netmf.py">node embeddings</a> and <a href="https://github.com/facebookresearch/fastText/tree/master/alignment">subspace alignment</a>.

**Usage**: python3 conealign.py --true_align data/synthetic-combined/arenas/arenas950-1/arenas_edges-mapping-permutation.txt --combined_graph data/synthetic-combined/arenas/arenas950-1/arenas_combined_edges.txt --output_stats output/stats/arenas/arenas950_1.log --store_align --output_alignment output/alignment_matrix/arenas/arenas950-1 --embmethod netMF --store_emb --embeddingA emb/netMF/arenas/arenas950-1.graph1.npy --embeddingB emb/netMF/large/arenas950-1.graph2.npy

* Pass the path to the true alignment file as a command line argument to conealign.py with the --true_align flag
* Pass the path to the edgelist file of the combined input graph as a command line argument to conealign.py with the --input flag
* Specify a file to save the alignment accuracy and run time (in seconds) to with an --output_stats flag
* Specify the node embedding method with the --embmethod flag
* OPTIONAL: save the alignment results as a binary .npy matrix (in each row, the entry representing the node and its matched counterpart being 1 and others being 0) by using the --store_align flag and specifying the file to save alignment matrix to with the --output_alignment flag
* OPTIONAL: save the node embeddings for each graph as an .npy matrix by using the --store_emb flag and specifying the files to save embedding matrices to with the --embeddingA and --embeddingB flags

**Dependencies**: NumPy, SciPy, scikit-learn, NetworkX, PythonOT, Theano (this was tested with NumPy 1.17.3, SciPy 1.4.1, scikit-learn 0.19.1, NetworkX 2.1, PythonOT 0.7.0, Theano 1.0.4)

Please refer to our paper for more information and cite it if you find this code useful.  

**Paper**: Xiyuan Chen, Mark Heimann, Fatemeh Vahedian, and Danai Koutra. <a href="https://arxiv.org/pdf/2005.04725.pdf">Consistent Network Alignment with Node Embedding</a>. 2020.

**Citation (bibtex)**:

```
@misc{conealign,
    title={Consistent Network Alignment with Node Embedding},
    author={Xiyuan Chen and Mark Heimann and Fatemeh Vahedian and Danai Koutra},
    year={2020},
    eprint={2005.04725},
    archivePrefix={arXiv},
    primaryClass={cs.SI}
}
```
