This is a site outlining some of the work my group did for our CSE291 project. We took the popular dimension reduction technique [UMAP](https://arxiv.org/abs/1802.03426) and decided to see if we could incorporate categorical as well as numeric data. This is a fairly common problem in data analysis and machine learning, as it is non-trivial to come up with a useful distance metric between observations on mixed feature types.

Here, we use a modified version of Gower distance (Gower, J.C. 1971) implemented in the [`daisy`](https://www.rdocumentation.org/packages/cluster/versions/2.1.0/topics/daisy) package in R.

The dataset we chose to use is the Pokemon dataset found [here](https://www.kaggle.com/alopez247/pokemon). For our Gower analysis, we dropped `Name, Number, Generation`.

We used the Python implemenation of [UMAP](https://umap-learn.readthedocs.io/en/latest/index.html) on this data, using `metric="precomputed"` for the Gower distance matrix.

Packages used:

- pandas
- numpy
- seaborn
- matplotlib
- bokeh
- PIL
- umap

Results can be found [here](docs/pokemon.md).
