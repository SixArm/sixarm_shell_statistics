# Shell » Statistics scripts

Statistics scripts that calculate based on lists of numbers.

Example:

    $ echo "1 2 4" | n-col-stats
    count: 3 min: 1 max: 4 sum: 7 range: 3 median: 2 mean: 2.33333 sumsq: 4.66667 sd: 1.24722 cv: 0.534523

There are specific scripts to calculating by column list or by row list:

  * `n-col-count`, `n-row-count`: Print the count, i.e. how many columns or rows.
  * `n-col-min`, `n-row-min`: Print the minimum number.
  * `n-col-max`, `n-row-max`: Print the maximum number.
  * `n-col-range`, `n-row-range`: Print the range of the numbers, i.e. max - min.
  * `n-col-sum`, `n-row-sum`: Print the sum of the numbers.
  * `n-col-median`, `n-row-median`: Print the median of the numbers.
  * `n-col-mean`, `n-row-mean`: Print the mean of the numbers, i.e. the average.
  * `n-col-sumsq`, `n-row-sumsq`: Print the sum of squares of the numbers.
  * `n-col-sd`, `n-row-sd`: Print the standard deviation of the numbers.
  * `n-col-cv`, `n-row-cv`: Print the coefficient of variance of the numbers, i.e. sd / mean.
  * `n-col-all`, `n-row-all`: Print all of the above statistics of the numbers.


## Examples

Example scripts:

    $ echo "1 2 4" | n-col-count
    3

    $ echo "1 2 4" | n-col-min
    1

    $ echo "1 2 4" | n-col-max
    4

    $ echo "1 2 4" | n-col-range
    3

    $ echo "1 2 4" | n-col-sum
    7

    $ echo "1 2 4" | n-col-median
    2

    $ echo "1 2 4" | n-col-mean
    2.33333

    $ echo "1 2 4" | n-col-sumsq
    4.66667

    $ echo "1 2 4" | n-col-sd
    1.24722

    $ echo "1 2 4" | n-col-cv
    0.534523

    $ echo "1 2 4" | n-col-all
    count: 3 min: 1 max: 4 range: 3 sum: 7 median: 2 mean: 2.33333 sumsq: 4.66667 sd: 1.24722 cv: 0.534523


## Requirements

These statistics scripts are simple:

  * They are implemented using the shell command `awk`, and do not need any higher-level languages.

  * For more power, we recommend the R language: http://www.r-project.org/


## Help

Sample code to split a column-oriented list of numbers into a row-oriented list of numbers:

    echo "1 2 4" | tr ' ' '\n'

    echo "1 2 4" | sed 's/\s\+/\n/g'

    echo "1 2 4" | awk '{for(i=1;i<=NF;i++) print $i}'
