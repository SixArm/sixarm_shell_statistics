# Shell » Statistics scripts

Statistics scripts for lists of numbers using shell pipes:

  * `row-count`: Print the count.
  * `row-min`: Print the minimum number.
  * `row-max`: Print the maxmium number.
  * `row-sum`: Print the sum of the numbers.
  * `row-median`: Print the median of the numbers.
  * `row-mean`: Print the mean of the numbers.
  * `row-range`: Print the range of the numbers.
  * `row-sd`: Print the standard deviation of the numbers.
  * `row-stats`: Print all of the above statistics of the numbers.


## Examples

Example: suppose you have a file `nums` like this:

    1
    2
    4

Example scripts:

    $ cat nums | row-count
    3

    $ cat nums | row-min
    1

    $ cat nums | row-max
    4

    $ cat nums | row-sum
    7

    $ cat nums | row-median
    2

    $ cat nums | row-mean
    2.33333

    $ cat nums | row-range
    3

    $ cat nums | row-sd
    1.24722

    $ cat nums | row-stats
    count: 3 min: 1 max: 4 sum: 7 range: 3 median: 2 mean: 2.33333 sd: 1.24722


## Requirements

These statistics scripts are simple:

  * They use shell commands such as `awk` and `sort`; they do not need any higher-level languages.

  * They are POSIX standard; they do not use any extensions from GNU tools or specific shells.

  * For more power, we recommend the R language: http://www.r-project.org/


## Help

These statistics scripts are line-oriented; the scripts expect one number per line.

To process a list that has multiple numbers per line, such as:

    1 2 3
    4 5 6

Split each line, such as:

    cat nums | tr ' ' '\n'

    cat nums | sed 's/\s\+/\n/g'

    cat nums | awk '{for(i=1;i<=NF;i++) print $i}'
