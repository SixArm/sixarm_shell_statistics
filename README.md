# Shell » NUMS: Numbers Utilities for Mathematics and Statistics

Numbers utilities including mathematics and statistics.

These shell scripts calculate based on lists of numbers.

Example:

    $ echo "1 2 4" | nums --sum
    7

See the `nums` script for details and options.

This repo also contains a bunch of simplified awk scripts to calculate on numbers:

  * `nums-col-count`, `nums-row-count`: Print the count, i.e. how many columns or rows.
  * `nums-col-min`, `nums-row-min`: Print the minimum number.
  * `nums-col-max`, `nums-row-max`: Print the maximum number.
  * `nums-col-range`, `nums-row-range`: Print the range of the numbers.
  * `nums-col-sum`, `nums-row-sum`: Print the sum of the numbers.
  * `nums-col-median`, `nums-row-median`: Print the median of the numbers.
  * `nums-col-mean`, `nums-row-mean`: Print the mean of the numbers, i.e. the average.
  * `nums-col-sum-of-squares`, `nums-row-sum-of-squares`: Print the sum of squares of the numbers.
  * `nums-col-variance`, `nums-row-variance`: Print the variance of the numbers.
  * `nums-col-standard-deviation`, `nums-row-standard-deviation`: Print the standard deviation of the numbers.
  * `nums-col-coefficient-of-variance`, `nums-row-coefficient-of-variance`: Print the coefficient of variance of the numbers.


## Examples

Example scripts:

    $ echo "1 2 4" | nums-col-count
    3

    $ echo "1 2 4" | nums-col-min
    1

    $ echo "1 2 4" | nums-col-max
    4

    $ echo "1 2 4" | nums-col-range
    3

    $ echo "1 2 4" | nums-col-sum
    7

    $ echo "1 2 4" | nums-col-median
    2

    $ echo "1 2 4" | nums-col-mean
    2.33333

    $ echo "1 2 4" | nums-col-ss
    4.66667

    $ echo "1 2 4" | nums-col-sd
    1.24722

    $ echo "1 2 4" | nums-col-cv
    0.534523

    $ echo "1 2 4" | nums-col-all
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
