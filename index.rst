.. include:: cyverse_rst_defined_substitutions.txt

|CyVerse logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_

**BioInfoSummer18 - Advanced Kallisto RNA-Seq (Bulk and Single Cell)**
========================================================================

Goal
----
This draft tutorial will introduce some of the features of the |Kallisto| and
|Sleuth| tools for RNA-Sequencing of bulk and single-cell samples.

.. warning::
   This tutorial is still in its draft form. These datasets are not
   yet available on the CyVerse Data Store, but are available on an
   Amazon AMI and docker container. These will later be migrated to
   |VICE|. Additionally, these materials are part of a workshop collection
   and not yet designed for independent use. These should not be relied
   on for analysis of your own data - they are merely useful examples that
   can inform your own analysis.


----

.. toctree::
	:maxdepth: 2

	Tutorial home <self>

Prerequisites
-------------

Downloads, access, and services
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*In order to complete this tutorial you will need access to the following services/software*

..
	#### comment: delete any row not needed in this table ####

.. list-table::
    :header-rows: 1

    * - Prerequisite
      - Preparation/Notes
      - Link/Download
    * - CyVerse account
      - You will need a CyVerse account to complete this exercise
      - |CyVerse User Portal|
    * - Docker
      - You must have access to Docker to run this tutorial
      - |Dockerhub|
    * - Amazon AWS Account
      - You can run this tutorial from this AMI:
      - ami-042909f3c5b9bf6ed

Platform(s)
~~~~~~~~~~~

*We will use the following CyVerse platform(s):*

 ..
   #### comment: delete any row not needed in this table ####

.. list-table::
    :header-rows: 1

    * - Platform
      - Interface
      - Link
      - Platform Documentation
      - Quick Start
    * - Data Store
      - GUI/Command line
      - |Data Store|
      - |Data Store Manual|
      - |Data Store Guide|
    * - Discovery Environment
      - Web/Point-and-click
      - |Discovery Environment|
      - |DE Manual|
      - |Discovery Environment Guide|
    * - VICE
      - A flexible environment for using Jupyterlab, RStudio, and RShiny
      -
      - |Vice Documentation|
      -


Important links for this workshop
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Workshop logistics
````````````````````````

.. list-table::
    :header-rows: 1

    * - Resource/Description
      - Link
    * - Gitter channel - we will have live chat and share through this channel
      - |Gitter|
    * - Opening poll
      - |Google opening poll|

Software resources
````````````````````
.. list-table::
    :header-rows: 1

    * - Resource/Description
      - Link
    * - Bioconductor - resource for R-based bioinformatics tools
      - |Bioconductor|
    * - Bioconda - Reproducible software installation
      - |Bioconda|
    * - CyVerse Learning Center - CyVerse learning materials
      - |CyVerse Learning Center|

Papers
```````
.. list-table::
    :header-rows: 1

    * - Resource/Description
      - Link
    * - A survey of best practices for RNA-seq data analysis
      - |Conesa|
    * - Fast and accurate single-cell RNA-seq analysis by clustering of transcript-compatibility counts
      - |Ntranos|
    * - Differential analysis of RNA-seq incorporating quantification uncertainty
      - |Pimentel|
    * - Tackling the widespread and critical impact of batch effects in high-throughput data
      - |Leek|
    * - AmpUMI: design and analysis of unique molecular identifiers for deep amplicon sequencing
      - |Clement|
    * - Tutorial: guidelines for the experimental design of single-cell RNA sequencing studies
      - |lafzi|

Other learning resources
`````````````````````````

.. list-table::
    :header-rows: 1

    * - Resource/Description
      - Link
    * - BioInfoSummer Workshop slides
      - |slides|
    * - Hemberg single cell RNA-Seq wiki (very comprehensive)
      - |Hemberg wiki|
    * - How to Use t-SNE Effectively
      - |tsne|
    * - Dana Pe'er: "Having fun with single-cell RNA-seq: imputation and manifolds"
      - |peer|
    * - Lior Pachter: Differential analysis of count data in genomics
      - |Pachter|
    * - Principal Component Analysis (PCA) clearly explained (2015)
      - |statquest|
    * - Single-cell RNA-Seq tools
      - |SC Tools|
    * - Seurat pipeline for SC RNA-Seq
      - |Seurat|

----

**Fix or improve this documentation**

Search for an answer:
|CyVerse Learning Center| or
|CyVerse Wiki|

Post your question to the user forum:
|Ask CyVerse|

----

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`__


.. Comment: Place Images Below This Line
   use :width: to give a desired width for your image
   use :height: to give a desired height for your image
   replace the image name/location and URL if hyperlinked


 .. |Clickable hyperlinked image| image:: ./img/IMAGENAME.png
    :width: 500
    :height: 100
 .. _CyVerse logo: http://learning.cyverse.org/

 .. |Static image| image:: ./img/IMAGENAME.png
    :width: 25
    :height: 25



.. Comment: Place URLS Below This Line

   # Use this example to ensure that links open in new tabs, avoiding
   # forcing users to leave the document, and making it easy to update links
   # In a single place in this document

   .. |Substitution| raw:: html # Place this anywhere in the text you want a hyperlink

      <a href="REPLACE_THIS_WITH_URL" target="blank">Replace_with_text</a>


.. |Github Repo Link|  raw:: html

   <a href="https://github.com/CyVerse-learning-materials/bioinforsummer-advanced-kallisto-and-single-cell" target="blank">Github Repo Link</a>

.. |Download Cyberduck| raw:: html

   <a href="https://cyberduck.io/" target="blank">Download Cyberduck</a>

.. |DE Application URL|  raw:: html

   <a href="https://de.cyverse.org/de/?type=apps&app-id=9b41c9e4-5031-4a49-b1cb-c471335df16e&system-id=de" target="blank">DE Application URL</a>

.. |Original App Documentation|  raw:: html

   <a href="http://www.drive5.com/muscle/manual/" target="blank">Original App Documentation</a>

.. |Atmosphere Image|  raw:: html

   <a href="https://atmo.cyverse.org/application/images/1384" target="blank">Atmosphere Image</a>

.. |Vice Documentation| raw:: html

   <a href="https://cyverse-visual-interactive-computing-environment.readthedocs-hosted.com/en/latest/index.html" target="blank">Vice Documentation</a>

.. |Kallisto| raw:: html

   <a href="https://pachterlab.github.io/kallisto/" target="blank">Kallisto</a>

.. |Sleuth| raw:: html

   <a href="https://pachterlab.github.io/sleuth/" target="blank">Sleuth</a>

.. |Gitter| raw:: html

   <a href="https://gitter.im/BioInfoSummer-kallisto/Lobby?utm_source=share-link&utm_medium=link&utm_campaign=share-link" target="blank">Gitter channel for chat</a>

.. |Google opening poll| raw:: html

   <a href="https://goo.gl/forms/GfwkIU3IFRWBwcxm1" target="blank">Google opening poll</a>

.. |Bioconductor| raw:: html

   <a href="http://bioconductor.org/" target="blank">Bioconductor</a>

.. |Bioconda| raw:: html

   <a href="https://bioconda.github.io/" target="blank">Bioconda</a>

.. |CyVerse Learning Center| raw:: html

   <a href="http://learning.cyverse.org/en/latest/" target="blank">CyVerse Learning Center</a>

.. |Conesa| raw:: html

   <a href="https://genomebiology.biomedcentral.com/articles/10.1186/s13059-016-0881-8" target="blank">Conesa</a>

.. |Ntranos| raw:: html

   <a href="https://genomebiology.biomedcentral.com/articles/10.1186/s13059-016-0970-8" target="blank">Ntranos</a>

.. |Pimentel| raw:: html

   <a href="https://www.nature.com/articles/nmeth.4324" target="blank">Pimentel</a>

.. |Leek| raw:: html

   <a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3880143/" target="blank">Leek</a>

.. |Clement| raw:: html

   <a href="https://academic.oup.com/bioinformatics/article/34/13/i202/5045706" target="blank">Clement</a>

.. |lafzi| raw:: html

   <a href="https://www.nature.com/articles/s41596-018-0073-y" target="blank">lafzi</a>

.. |Hemberg wiki| raw:: html

   <a href="https://hemberg-lab.github.io/scRNA.seq.course/index.html" target="blank">Hemberg wiki</a>

.. |tsne| raw:: html

   <a href="https://distill.pub/2016/misread-tsne/" target="blank">tsne</a>

.. |peer| raw:: html

   <a href="https://www.youtube.com/watch?v=8KpIDpPEGV4" target="blank">Pe'er (YouTube)</a>

.. |Pachter| raw:: html

   <a href="https://www.youtube.com/watch?v=ucPBBTjH5EE" target="blank">Pachter (YouTube)</a>

.. |statquest| raw:: html

   <a href="https://www.youtube.com/watch?v=_UVHneBUBW0" target="blank">Statquest (YouTube)</a>

.. |SC Tools| raw:: html

   <a href="https://www.scrna-tools.org/" target="blank">SC Tools</a>

.. |Seurat| raw:: html

   <a href="https://satijalab.org/seurat/" target="blank">Seurat</a>

.. |VICE| raw:: html

   <a href="https://cyverse-visual-interactive-computing-environment.readthedocs-hosted.com/en/latest/index.html" target="blank">VICE</a>

.. |Dockerhub| raw:: html

   <a href="https://hub.docker.com/r/jasonjwilliamsny/single-cell-training" target="blank">Dockerhub</a>

.. |slides| raw:: html

   <a href="https://de.cyverse.org/dl/d/3C1C5CB9-DBB4-425F-90AD-3865928243B7/BioInfoSummer18_RNA-seq.pptx" target="blank">Slides</a>
