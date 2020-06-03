# CONE-Align
This is a reference implementation for CONE-Align, an unsupervised network alignment method that uses node embeddings to model intra-graph node proximity and then aligns the embedding subspaces to make the node embeddings comparable across graphs.  

**Usage**: (give a sample command to run and evaluate CONE-Align example dataset)

**Dependencies**: NumPy, SciPy, scikit-learn, NetworkX, PythonOT (update if needed--ideally say, "this was tested with versions X.XX of each dependency") 

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