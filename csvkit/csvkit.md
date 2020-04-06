csvkit is a suite of utilities for converting to and working with CSV.
https://csvkit.readthedocs.org/en/latest/

    csvstat -c 2 --sum sales.csv
    4771.31

    csvgrep -c 1 -r "^2013" ./sales.csv | csvstat -c 2 --sum
    743.07

    csvsql --query  "select ldap, sum(case when action='view' then count else 0 end) as 'views', sum(case when action='action' then count else 0 end) as 'actions' from Logger group by 1 order by 2 desc" Logger.csv | csvlook

https://onlinecsvtools.com/
