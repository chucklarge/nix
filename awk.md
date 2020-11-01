sum a column

    seq 10 | awk 'BEGIN {sum=0} {sum+=$0} END {print sum}'
    seq 10 | awk '{sum+=$0} END {print sum}'
    
    
average a column

    seq 10 | awk '{sum+=$0} END {print sum/NR}'
    
    
    
print number of lines

    seq -w 0 .005 .1 | awk 'END{print NR}'
    
    
    
print as money USD

    awk '{printf "$%.2f\n",$1}'
    
sample data
    
    awk 'BEGIN { srand(systime()); } {if (rand() < 0.3) { print $0; } }' data.csv
    
    
conditionals

    awk -F, '(($2 != "active" || $3 == "frozen") && $4 == "no_ato") {print $1}' ato.csv

ignore first two lines

    awk 'NR > 2' file.csv
