# Shell » NUMS: Numbers Utilities for Mathematics and Statistics

Numbers utilities including mathematics and statistics.

These shell scripts calculate based on lists of numbers.

Example:

    $ echo "1 2 4" | num --sum
    7

See the `num` script for details and options.

This repo also contains a bunch of simplified awk scripts to calculate on numbers:

  * `num-col-count`, `num-row-count`: Print the count, i.e. how many columns or rows.
  * `num-col-min`, `num-row-min`: Print the minimum number.
  * `num-col-max`, `num-row-max`: Print the maximum number.
  * `num-col-range`, `num-row-range`: Print the range of the numbers.
  * `num-col-sum`, `num-row-sum`: Print the sum of the numbers.
  * `num-col-median`, `num-row-median`: Print the median of the numbers.
  * `num-col-mean`, `num-row-mean`: Print the mean of the numbers, i.e. the average.
  * `num-col-sum-of-squares`, `num-row-sum-of-squares`: Print the sum of squares of the numbers.
  * `num-col-variance`, `num-row-variance`: Print the variance of the numbers.
  * `num-col-standard-deviation`, `num-row-standard-deviation`: Print the standard deviation of the numbers.
  * `num-col-coefficient-of-variance`, `num-row-coefficient-of-variance`: Print the coefficient of variance of the numbers.


## Examples

Example scripts:

    $ echo "1 2 4" | num-col-count
    3

    $ echo "1 2 4" | num-col-min
    1

    $ echo "1 2 4" | num-col-max
    4

    $ echo "1 2 4" | num-col-range
    3

    $ echo "1 2 4" | num-col-sum
    7

    $ echo "1 2 4" | num-col-median
    2

    $ echo "1 2 4" | num-col-mean
    2.33333

    $ echo "1 2 4" | num-col-ss
    4.66667

    $ echo "1 2 4" | num-col-sd
    1.24722

    $ echo "1 2 4" | num-col-cv
    0.534523

    $ echo "1 2 4" | num-col-all
    count: 3 min: 1 max: 4 range: 3 sum: 7 median: 2 mean: 2.33333 ss: 4.66667 sd: 1.24722 cv: 0.534523


## Requirements

These statistics scripts are simple:

  * They are implemented using the shell command `awk`, and do not need any higher-level languages.

  * For more power, we recommend the R language: http://www.r-project.org/


## Help

Sample code to split a column-oriented list of numbers into a row-oriented list of numbers:

    echo "1 2 4" | tr ' ' '\n'

    echo "1 2 4" | sed 's/\s\+/\n/g'

    echo "1 2 4" | awk '{for(i=1;i<=NF;i++) print $i}'
