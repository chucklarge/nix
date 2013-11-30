csvkit is a suite of utilities for converting to and working with CSV.
https://csvkit.readthedocs.org/en/latest/

    csvstat -c 2 --sum sales.csv
    4771.31

    csvgrep -c 1 -r "^2013" ./sales.csv | csvstat -c 2 --sum
    743.07
