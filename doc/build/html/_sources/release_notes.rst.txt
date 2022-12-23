.. toolkit documentation master file, created by
   sphinx-quickstart on Wed Feb  9 17:10:01 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.
.. role:: small
.. role:: smaller

Release Notes
===========================================================================================

Version 1.1.3 :small:`Oct 16, 2022`
----------------------------------------------------------------------
- Added ``celldancer.utilities.to_dynamo`` and ``celldancer.utilities.export_velocity_to_dynamo`` to import cellDancer results to dynamo.
- Added deep learning parameters n_neighbors, dt, and learning_rate in function ``celldancer.velocity``.
- Added new loss function: mix, rmse in function ``celldancer.velocity``.

Version 1.1.2 :small:`Jun 27, 2022`
----------------------------------------------------------------------
- Updated three notebooks of case studies. 

Version 1.1.1 :small:`Jun 21, 2022`
----------------------------------------------------------------------
- Renamed ``celldancer.cdplt.graph`` to ``celldancer.cdplt.PTO_Graph`` in API section.

Version 1.1.0 :small:`Jun 15, 2022`
----------------------------------------------------------------------
- Added three notebooks of case studies. 
- Added Installation page and Data Preparation page.
- Added ``celldancer.adata_to_raw_with_embed`` in API section.

Version 1.0.2 :small:`May 3, 2022`
----------------------------------------------------------------------
- Optimized parallelized computing in ``celldancer.velocity``.

Version 1.0.1 :small:`Apr 5, 2022`
----------------------------------------------------------------------
- Updated APIs (``celldancer.velocity``, ``celldancer.compute``, ``celldancer.pseudotime``, ``celldancer.embedding``, ``celldancer.cdplt.scatter_gene``, ``celldancer.cdplt.scatter_cell``, ``celldancer.cdplt.plot_kinetic_para``, ``celldancer.cdplt.graph``).

Version 1.0.0 :small:`Dec 2, 2021`
----------------------------------------------------------------------
- Added index page.
- Added APIs (``celldancer.velocity``, ``celldancer.compute``, ``celldancer.pseudotime``, ``celldancer.embedding``, ``celldancer.cdplt.scatter_gene``, ``celldancer.cdplt.scatter_cell``, ``celldancer.cdplt.plot_kinetic_para``, ``celldancer.cdplt.graph``).