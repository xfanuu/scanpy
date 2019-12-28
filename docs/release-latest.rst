.. role:: small
.. role:: smaller

.. rubric:: New functionality

- :func:`~scanpy.tl.ingest` maps labels and embeddings of reference data to new data, see the `ingest PBMC tutorial`_ and the `ingest Pancreas tutorial`_ :pr:`651` :smaller:`S Rybakov, A Wolf`
- :mod:`~scanpy.queries` recieved many updates including enrichment through gprofiler_ and more advanced biomart queries :pr:`467` :smaller:`I Virshup`
- :func:`~scanpy.set_figure_params` allows setting `figsize`

.. _gprofiler: https://biit.cs.ut.ee/gprofiler/
.. _ingest PBMC tutorial: https://scanpy-tutorials.readthedocs.io/en/latest/integrating-pbmcs-using-ingest.html
.. _ingest Pancreas tutorial: https://scanpy-tutorials.readthedocs.io/en/latest/integrating-pancreas-using-ingest.html

.. rubric:: Code design

- :mod:`~scanpy.pp.downsample_counts` now always preserves the dtype of it's input, instead of converting floats to ints :pr:`865` :smaller:`I Virshup`
- allow specifying a base for :func:`~scanpy.pp.log1p` :pr:`931` :smaller:`G Eraslan`
- run neighbors on a GPU using rapids :pr:`850` :smaller:`T White`
- landing page overhaul, ecosystem page, release notes overhaul :pr:`960` :smaller:`A Wolf`
- parameter docs from typed params :smaller:`P Angerer`

.. warning::

   * Changed default solver of :func:`~scanpy.tl.pca` from `auto` to `arpack`.
   * Changed default behavior of `use_raw` of :func:`~scanpy.tl.score_genes` from `False` to `None`.