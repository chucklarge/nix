    wget https://raw.githubusercontent.com/chucklarge/examples/master/Common%20Data%20Formats/apache_logs/apache_logs

    cat apache_logs | rg -e 'GET ([^ |^?]+)' --only-matching | sort | uniq -c | sort -nr | head
