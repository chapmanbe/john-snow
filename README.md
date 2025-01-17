# john-snow

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/chapmanbe/john-snow/HEAD?labpath=code%2Fpython%2FRelations.ipynb)

Spatial analysis playground using data related to the [1854 cholera outbreak in Soho](https://en.wikipedia.org/wiki/1854_Broad_Street_cholera_outbreak) and Dr John Snow's ['cholera map that changed the world'](https://www.theguardian.com/news/datablog/2013/mar/15/john-snow-cholera-map). 

## data
Data are from several sources:
- `data/csds` contains data prepared by [Center for Spatial Data Science](https://geodacenter.github.io/data-and-lab//snow/).
  - `snow7/pumps.shp` (vector) is points for each location of a pump
- `data/dani` contains data prepared by [Dani Arribas-Bel](https://bitbucket.org/darribas/reproducible_john_snow/src/master/):
  - `polys.shp` (vector) is building blocks (footprints) from the Ordnance Survey (OS data © Crown copyright and database right, 2015)
  - `Cholera_Deaths.shp` (vector) is points for each location of at least one death (attribute value gives death count by location)

The data sets above are based in some way on data prepared by [Robin Wilson](http://blog.rtwilson.com/john-snows-cholera-data-in-more-formats/) and other sources.

## code

### python

- [Relations.ipynb](https://github.com/jamesdamillington/john-snow/blob/main/code/python/Relations.ipynb) is a python notebook using the [shapely package](https://pypi.org/project/Shapely/) exploring some examples of spatial relations, specifically:
  - distances (between points);
  - within and contains (points and polygons);
  - overlaps (of polygons);
  - buffers (around points; technically an operation, but it makes sense to consider them here)
- [Operations.ipynb](https://github.com/jamesdamillington/john-snow/blob/main/code/python/Operations.ipynb) is a python notebook using the [shapely package](https://pypi.org/project/Shapely/) exploring some examples of spatial operations, specifically:
  - differences (between polygons);
  - intersections (of polygons);
  - unions (of polygons)
- [Voronoi.ipynb](https://github.com/jamesdamillington/john-snow/blob/main/code/python/Voronoi.ipynb) is a python notebook providing overview of Voronoi Diagrams (Thiessen Polygons) using the [pysal package](https://pysal.org/libpysal)
- [SpatialJoins.ipynb](https://github.com/jamesdamillington/john-snow/blob/main/code/python/SpatialJoins.ipynb) is a python notebook that uses spatial joins to analyse data with geometries created in the [Spatial Relations](https://github.com/jamesdamillington/john-snow/blob/main/code/python/Relations.ipynb), [Spatial Operations](https://github.com/jamesdamillington/john-snow/blob/main/code/python/Operations.ipynb) and [Voronoi](https://github.com/jamesdamillington/john-snow/blob/main/code/python/Voronoi.ipynb) notebooks
- [Arribas-Bel_etal_2017.ipynb](/code/python/Arribas-Bel_etal_2017.ipynb) re-implements python code from [Arribas-Bel _et al._ (2017)](http://doi.org/10.1007/978-3-319-50590-9_17) for more recent versions of packages

### R

RMarkdown files equivalent to python notebooks will be forthcoming

## pdf

- [OSullivanUnwin2003_Section7_4.pdf](https://github.com/jamesdamillington/john-snow/blob/main/pdf/OSullivanUnwin2003_Section7_4.pdf) is an excerpt (section 7.4) from O'Sullivan and Unwin (2003), relevant to the notebook on Join Counts

### References

- Johnson, S. (2006) [_The Ghost Map_](https://en.wikipedia.org/wiki/The_Ghost_Map) London: Penguin
- O'Sullivan, D. and Unwin, D.J. (2003) _Geographical Information Analysis_ London: Wiley
