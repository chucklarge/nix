sum a column

    awk 'BEGIN {sum=0} {sum= sum+$0; print sum}' | tail -1
    
print as money USD

    awk '{printf "$%.2f\n",$1}'