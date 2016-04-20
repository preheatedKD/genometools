..
    Copyright (c) 2015, 2016 Florian Wagner
    
    This file is part of GenomeTools.
    
    GenomeTools is free software: you can redistribute it and/or modify
    it under the terms of the GNU General Public License, Version 3,
    as published by the Free Software Foundation.
    
    This program is distributed in the hope that it will be useful,
    but WITHOUT ANY WARRANTY; without even the implied warranty of
    MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
    GNU General Public License for more details.
    
    You should have received a copy of the GNU General Public License
    along with this program. If not, see <http://www.gnu.org/licenses/>.

Changelog
=========

Version 2.0 (2016-??-??)
---------------------------

- Made library compatible with both Python 2.7 and Pyhon 3.x
- New "enrichment" subpackage for testing gene set enrichment
- `expression.ExpMatrix` now subclasses the Pandas DataFrame,
  and `expression.ExpProfile` now subclasses the Pandas Series
- New plotting API based on plotly in `expression.plot`

Version 1.2.3 (2016-03-16)
--------------------------

- Fixed a bug in class basic.GeneSet (basic/geneset.py) that occured when
  calling repr() on GeneSet objects containing unicode strings.
- basic.GeneSetDB.read_tsv() now takes the file encoding as an argument.
- Made quantile normalization use a stable sorting algorithm (merge sort),
  which is important if there are many identical values (e.g., 0) in the data.

Version 1.2.2 (2016-02-26)
--------------------------
- Improved quantile normalization method (it now has a smaller memory
  footprint and handles missing data)

Version 1.2.0
-------------

- added classes for handling gene sets (see `genometools.basic`)
- added classes for handling expression data (see
  `genometools.expression`)
- reorganized package structure, created sub-packages based on data source
  (e.g., `genometools.ensembl`) or method (e.g., `genometools.rnaseq`)
- added script for finding all SRA run IDs for a given SRA experiment ID
  (``sra_find_experiment_runs.py``)
- added functions for obtaining URLs for GEO data series (see
  `genometools.geo`)
- added unicode support for all scripts

Version 1.1.0
-------------

- added documentation
- converted all tabs to four spaces
- added convenience function to configure a logger (misc.configure_logger)
  using Python's `logging` module
- added logging capabilities to the scripts extract_protein_coding_genes.py
  and extract_entrez2gene.py
- added chromosome patterns for five species to extract_protein_coding_genes.py