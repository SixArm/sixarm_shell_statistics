# Shell » Statistics scripts

Statistics scripts for lists of numbers using shell pipes:

  * `n-count`: Print the count.
  * `n-min`: Print the minimum number.
  * `n-max`: Print the maxmium number.
  * `n-sum`: Print the sum of the numbers.
  * `n-median`: Print the median of the numbers.
  * `n-mean`: Print the mean of the numbers.
  * `n-range`: Print the range of the numbers.
  * `n-sd`: Print the standard deviation of the numbers.
  * `n-stats`: Print all of the above statistics of the numbers.

Example: suppose you have a file `nums` like this:

    1
    2
    4

Example scripts:

    $ cat nums | n-count
    3

    $ cat nums | n-min
    1

    $ cat nums | n-max
    4

    $ cat nums | n-sum
    7

    $ cat nums | n-median
    2

    $ cat nums | n-mean
    2.33333

    $ cat nums | n-range
    3

    $ cat nums | n-sd
    1.24722

    $ cat nums | n-stats
    count: 3 min: 1 max: 4 sum: 7 range: 3 median: 2 mean: 2.33333 sd: 1.24722

These statistics scripts are simple:

  * They use shell commands such as `awk` and `sort`; they do not need any higher-level languages.

  * They are POSIX standard; they do not use any extensions from GNU tools or specific shells.

For more sophisticated statistics needs, we recommend the R language: http://www.r-project.org/
