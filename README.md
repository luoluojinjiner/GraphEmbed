[![''](https://github.com/fabriziocosta/GraphEmbed/blob/master/img.png)]

# GraphEmbed
Compute a 2D embedding of a data matrix given supervised class information.

Instances are materialized as nodes in a graph where edges connect the
nearest neighbors. Additional invisible nodes are placed to represent the
supervised classes and instances are linked to their respective classes.
The final embedding is obtained using the spring layout algorithm presented in:
Tomihisa Kamada, and Satoru Kawai. "An algorithm for drawing general
undirected graphs." Information processing letters 31, no. 1 (1989): 7-15.


## Usage

Standalone script usage:

```./graph_embed -i data.csv -t target.csv --fast```


## Help

```
Version: 1.0
Author: Fabrizio Costa [costa@informatik.uni-freiburg.de]

Usage:
  graph_embed -i FILE -t FILE  [-o NAME] [--cmap_name=NAME]
              [(-m N | --min_threshold=N)] [--multi_class_threshold=N]
              [--multi_class_bias=N] [--true_class_threshold=N]
              [--true_class_bias=N] [--nearest_neighbors_threshold=N]
              [--correlation_transformation]
              [--display] [--verbose]
  graph_embed (-h | --help)
  graph_embed --version

Options:
  -i FILE                           Specify input data file.
  -t FILE                           Specify target data file.
  -o NAME                           Prefix for output files [default: image].
  --display                         Display graphs.
  -m N, --min_threshold=N           Min num of elements per class [default: 5].
  --cmap_name=NAME                  Color scheme [default: gist_ncar].
  --correlation_transformation      Convert data matrix to corr coeff matrix.
  --nearest_neighbors_threshold=N   Number of neighbors [default: 5].
  --true_class_bias=N               Bias for clustering [default: 0.9].
  --true_class_threshold=N          Threshold for clusters [default: 3].
  --multi_class_bias=N              Multiclass bias [default: 0].
  --multi_class_threshold=N         Multiclass threshold [default: 3].
  -h --help                         Show this screen.
  --version                         Show version.
  --verbose                         Print more text.

  ```
