CoSpar - dynamic inference by integrating state and lineage information
=======================================================================

|PyPI| |PyPIDownloads| |Anaconda| |Bioconda| |Docs|

.. image:: https://user-images.githubusercontent.com/4595786/104988296-b987ce00-59e5-11eb-8dbe-a463b355a9fd.png
   :width: 300px
   :align: left

**CoSpar** is a toolkit for dynamic inference from lineage-traced single cells. |br|
The methods are based on
`Wang et al. Nat. Biotech. (2022) <https://www.nature.com/articles/s41587-022-01209-1>`_.

Dynamic inference based on single-cell state measurement alone requires serious simplifications. On the other hand, direct dynamic measurement via lineage tracing only captures partial information and its interpretation is challenging. CoSpar integrates both state and lineage information to infer a finite-time transition map of a development/differentiation system. It gains superior robustness and accuracy by exploiting both the local coherence and sparsity of differentiation transitions, i.e., neighboring initial states share similar yet sparse fate outcomes.  Building around the :class:`~anndata.AnnData` object, CoSpar provides an integrated analysis framework for datasets with both state and lineage information. When only state information is available, CoSpar also improves upon existing dynamic inference methods by imposing sparsity and coherence. It offers essential toolkits for analyzing lineage data, state information, or their integration.

CoSpar's key applications
^^^^^^^^^^^^^^^^^^^^^^^^^
- infer transition maps from lineage data, state measurements, or their integration.
- predict the fate bias of progenitor cells.
- order cells along a differentiation trajectory leading to a given cell fate.
- predict gene expression dynamics along a trajectory.
- predict genes whose expression correlates with future fate outcome.
- generate a putative fate hierarchy, ordering fates by their lineage distances.

Community usage
^^^^^^^^^^^^^^^
- Our analysis of in vivo cell fate choice of HSCs from DARLIN mice, having only a single time point (with both lineage and transcriptome information in single cells). Ref: `L. Li,...,S.-W. Wang, F. Camargo, Cell (2023) <https://doi.org/10.1016/j.cell.2023.09.019>`_. Notebooks available `here <https://github.com/ShouWenWang-Lab/DARLIN_tutorial>`_. It is also available in the `EXAMPLES` session of this website.

- Analysis of in vitro lineage tracing data of HSPCs in `Jindal et.al., Nat. Biotech. (2023) <https://www.nature.com/articles/s41587-023-01931-4>`_.

Recorded Talks
^^^^^^^^^^^^^^
- `Jun 1: Single-Cell Data Science 2022 <https://singlecell2022.hku.hk/>`_. This is a 20-min short talk focusing more on the utility of CoSpar: `talk video <https://www.youtube.com/watch?v=HrDQpW3kJFo>`_

- `Oct 19, 2022: Invited MIA talk at Broad Institute <https://www.broadinstitute.org/talks/learning-cell-differentiation-dynamics-lineage-tracing-datasets>`_. This is an one-hour talk focusing on the Machine Learning part of CoSpar: `talk video <https://www.youtube.com/watch?v=rYzQUYPPNlU>`_.


.. Upcoming talks
.. ^^^^^^^^^^^^^^
.. - `Sep 15: Temporal Single-Cell Analysis (SCOG) <https://twitter.com/fabian_theis/status/1305621028056465412>`_
.. - `Nov 12: Single Cell Biology (SCB) <https://coursesandconferences.wellcomegenomecampus.org/our-events/single-cell-biology-2020/>`_



Reference
^^^^^^^^^
`S.-W. Wang*, M. Herriges, K. Hurley, D. Kotton, A. M. Klein*, CoSpar identifies early cell fate biases from single cell transcriptomic and lineage information, Nat. Biotech. (2022) <https://www.nature.com/articles/s41587-022-01209-1>`_. [* corresponding authors]



Support
^^^^^^^
Feel free to submit an `issue <https://github.com/ShouWenWang-Lab/cospar/issues/new/choose>`_
or send us an `email <mailto:wangshouwen@westlake.edu.cn>`_.
Your help to improve CoSpar is highly appreciated.

Acknowledgment
^^^^^^^^^^^^^^
Shou-Wen  wants to thank Allon Klein for his mentorship, and Tal D. Scully, Qiu Wu  and other lab members for testing the package. He wants to acknowledge the generous support of the Damon Runyon Foundation through the Quantitative Biology Fellowship.


.. toctree::
   :caption: Main
   :maxdepth: 1
   :hidden:

   about
   api
   release_note


.. toctree::
   :caption: Tutorial
   :maxdepth: 1
   :hidden:

   installation
   getting_started
   20210602_loading_data
   20211010_preprocessing
   20211010_clonal_analysis
   20211010_map_inference
   20211010_map_analysis

.. toctree::
   :caption: Examples
   :maxdepth: 1
   :hidden:

   20210121_all_hematopoietic_data_v3
   20210121_reprogramming_static_barcoding_v2
   20210121_lung_data_v2
   20210120_bifurcation_model_static_barcoding
   20220402_simulate_differentiation
   20231122_DARLIN_in_vivo_hematopoiesis


.. |PyPI| image:: https://img.shields.io/pypi/v/cospar.svg
   :target: https://pypi.org/project/cospar

.. |PyPIDownloads| image:: https://pepy.tech/badge/cospar
   :target: https://pepy.tech/project/cospar

.. |Anaconda| image:: https://anaconda.org/bioconda/cospar/badges/version.svg
   :target: https://anaconda.org/bioconda/cospar

.. |Bioconda| image:: https://img.shields.io/badge/install%20with-bioconda-brightgreen.svg?style=flat-square
   :target: https://anaconda.org/bioconda/cospar

.. |Docs| image:: https://readthedocs.org/projects/cospar/badge/?version=latest
   :target: https://cospar.readthedocs.io


..
  .. |travis| image:: https://travis-ci.org/theislab/cospar.svg?branch=master
     :target: https://travis-ci.org/theislab/cospar


.. |br| raw:: html

  <br/>

..
 .. |meet| raw:: html



.. |dim| raw:: html

   <span class="__dimensions_badge_embed__" data-doi="xxx" data-style="small_rectangle"></span>
   <script async src="https://badge.dimensions.ai/badge.js" charset="utf-8"></script>
