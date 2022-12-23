cellDancer - Estimating Cell-dependent RNA Velocity
===========================================================================================

**cellDancer** is a modularized, parallelized, and scalable tool based on a deep learning framework for the RNA velocity analysis of scRNA-seq. The gene phase portraits of `Sulf2` in the pancreatic endocrinogenesis data and `Gnao1` in the mouse hippocampus development data below show the training process of the DNN (deep neural network).

.. image:: _static/training_progress.png
  :width: 100%
  :alt: cell_type_u_s_sample_df

cellDancer's key applications
========================================================
* Estimate cell-specific RNA velocity for each gene.
* Derive cell fates in embedding space.
* Estimate pseudotime for each cell in embedding space.


Latest news
^^^^^^^^^^^^^^^^^^^^
- To be updated.

.. toctree::
    :caption: cellDancer
    :titlesonly:

    API
    release_notes

.. toctree::
   :maxdepth: 2
   :caption: Tutorials

   notebooks/installation
   data_preprocessing
   notebooks/case_study_gastrulation
   notebooks/case_study_neuro
   notebooks/case_study_pancreas
   notebooks/case_study_hgforebrian

.. toctree::
   :maxdepth: 2
   :caption: Application of dynamo

   notebooks/case_study_pancreas_dynamo


