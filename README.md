## Reading and writing SVMlight format

`read.svmlight()` and `write.svmlight()` read/write sparse matrices in SVMlight format.
You will find other functions for this on the internet, but the ones I found were either slow or handled only dense (=normal) matrices.

Benchmark to convert a dgCMatrix with 2,500,000 rows and 8,500 columns (1.1GB in memory) => 5 minutes

You would take hours if not days with regular packages for such sizes!

## Installation

```r
devtools:::install_github("IDEXX/sparsity")
```

Original source (felixr/sparsity) does not compile properly and Laurae2/sparsity uses zero based
column numbering which is broken in H2O (see https://0xdata.atlassian.net/browse/PUBDEV-3734)!
Hence the reason of this repository for those who needs only the SVMLight format >_>
