API
===========================================================================================

Import pandas and cellDancer modules as::
   
   import pandas as pd
   import celldancer as cd
   import celldancer.cdplt as cdplt
   import celldancer.utilities as cdutil
   import celldancer.simulation as cdsim

After the `preprocessing <data_preprocessing.html>`_ (optional, ``cdutil.adata_to_df_with_embed``) and the loading of the data (``pd.read_csv``), the RNA velocity could be estimated by ``cd.velocity``. The projection of RNA velocity to vector fields in the embedding space could be calculated by ``cd.compute_cell_velocity`` and visualized by ``cdplt.scatter_cell``. The pseudotime could be calculated by ``cd.pseudo_time`` and visualized by ``cdplt.scatter_cell`` or ``cdplt.scatter_gene``, the UMAP based on reaction rates could be calculated by ``cd.embedding_kinetic_para`` and visualized by ``cdplt.plot_kinetic_para``. Genes with different kinetics could be simulated by ``cdsim.simulate``. cellDancer results could be integrated with dynamo for downstream analysis by ``cdutil.to_dynamo`` and ``cdutil.export_velocity_to_dynamo``.


Toolkit functions
-------------------
Preprocessing and APIs to dynamo (cdutil)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. currentmodule:: celldancer
.. rubric:: Functions
.. autosummary::
   :toctree: .

   adata_to_df_with_embed
   to_dynamo
   export_velocity_to_dynamo

Velocity estimation and analysis (cd)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. currentmodule:: celldancer
.. rubric:: Functions

.. autosummary::
   :toctree: .

   velocity
   compute_cell_velocity
   pseudo_time
   embedding_kinetic_para

Plotting (cdplt)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. currentmodule:: celldancer.cdplt
.. rubric:: Functions

.. autosummary::
   :toctree: .

   scatter_gene
   scatter_cell
   plot_kinetic_para
   PTO_Graph


Simulation (cdsim)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
.. currentmodule:: celldancer.simulation
.. rubric:: Functions
.. autosummary::
   :toctree: .

   simulate


