# SixArm.com » Shell » Statistics scripts

Statistics scripts for lists of numbers using shell pipes:

  * `n-min`: Print the minimum number.
  * `n-max`: Print the maxmium number.
  * `n-sum`: Print the sum of the numbers.
  * `n-median`: Print the median of the numbers.
  * `n-mean`: Print the mean of the numbers.
  * `n-range`: Print the range of the numbers.
  * `n-sd`: Print the standard deviation of the numbers.
  * `n-stats`: Print all of the above statistics of the numbers.

Example: suppose you have a file `demo.txt` like this:

    1
    2
    4

Example scripts:

    $ cat demo.txt | n-min
    1

    $ cat demo.txt | n-max
    4

    $ cat demo.txt | n-sum
    7

    $ cat demo.txt | n-median
    2

    $ cat demo.txt | n-mean
    2.33333

    $ cat demo.txt | n-range
    3

    $ cat demo.txt | n-sd
    1.24722

    $ cat demo.txt | n-stats
    n: 3 min: 1 max: 4 sum: 7 range: 3 median: 2 mean: 2.33333 sd: 1.24722

These statistics scripts run using simple shell commands, such as `awk` and `sort`.

These scripts can run on any typical shell, independent of higher-level languages.

For more sophisticated statistics needs, we recommend the R language: http://www.r-project.org/
