Data Preparation
===========================================================================================

In our tutorials of `Delineating the transcriptional boost on single-cell resolution in gastrulation erythroid maturation data <notebooks/case_study_gastrulation.html>`_, `Inferring RNA velocities on each branch for branching genes in the mouse hippocampus development <notebooks/case_study_neuro.html>`_, and `Deciphering cell identity using the cell-specific reaction rates in pancreatic endocrinogenesis <notebooks/case_study_pancreas.html>`_, the data has already been prepared. To load your own data, the data format and the method to prepare the data is introduced below.

The input data for the prediction of velocity is in ``csv`` format. And could be loaded using ``pd.read_csv()``. Taking the `cell_type_u_s_sample_df.csv <https://drive.google.com/file/d/1XYWaJ3AyMspW7Wfy43LAcgsYm9GGDDh1/view?usp=sharing>`_ below as an example of 5 cells corresponding to 2 genes as shown below::

   import pandas as pd
   cell_type_u_s=pd.read_csv('your_path/cell_type_u_s_sample_df.csv')
   cell_type_u_s

.. image:: _static/cell_type_u_s_sample_df.png
  :width: 100%
  :alt: cell_type_u_s_sample_df

The gene information is represented by columns of ``gene_name``, ``unsplice``, and ``splice``. The cell information is represented by columns ``cellID``, ``clusters``, ``embedding1``, and ``embedding2``. ``unsplice`` and ``splice`` columns represent the spliced and unspliced counts, separately. ``cellID`` is the unique id of each cell. ``clusters`` represent the cell type of each cell. ``embedding1`` and ``embedding2`` are the 2-dimensional representation of all cells such as UMAP, PCA, or t-SNE. The sample could be viewed by 


Transfer adata format to dataframe
--------------------------------------
The two count matrices of unspliced and spliced abundances could be obtained from standard sequencing protocols. They could be counted by `velocyto <http://velocyto.org/velocyto.py/tutorial/cli.html#running-velocyto>`_ or `loompy/kallisto <https://linnarssonlab.org/loompy/kallisto/index.html>`_ pipeline. 

We also provide a function (``cd.adata_to_df_with_embed()``) to transfer from `Anndata <https://anndata-tutorials.readthedocs.io/en/latest/getting-started.html>`_ (a format of storing annotated data, usually are loom file) to ``csv`` format. For example, after the `preprocessing in Anndata format <https://scvelo.readthedocs.io/VelocityBasics/>`_. To transfer to pandas.DataFrame/csv format, ``cd.adata_to_df_with_embed()`` could be used. For example, in the command of::
    
   import pandas as pd
   import celldancer.utilities as cdutil
   cdutil.adata_to_df_with_embed(adata,
                                 us_para=['Mu','Ms'], 
                                 cell_type_para='celltype', 
                                 embed_para='X_umap', 
                                 save_path='cell_type_u_s.csv', 
                                 gene_list=['Hba-x','Smim1'])


``splice`` and ``unsplice`` columns are obtained from the ``['Ms', 'Mu']`` attributes of ``adata.layers``. Also, ``cellID`` column is obtained from ``adata.obs.index``. ``clusters`` column is obtained from ``['celltype']`` of ``adata.obs``. The ``embedding1`` and ``embedding2`` columns are obtained from ``['X_umap']`` attribute of ``adata.obsm``.

