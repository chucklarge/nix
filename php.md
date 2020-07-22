   php one-liner
   
      csvcut -c2 file.csv | php -R '$out=[];parse_str(parse_url($argn, PHP_URL_QUERY), $out);echo $out["q"]."\n";' | sort | uniq -c | sort -nr
