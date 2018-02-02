  -h, --no-filename             Suppress the prefixing filename on output
  
    
    ack -h "php_event_name=([^&]+)&" --output "\$1" beacon.log
    
    ack -h "php_event_name=cart_payment&" beacon.log | ack "&total=([^&]+)&" --output "\$1"
    
    ack -h "\rAccount number \(see instructions\)([^\r]+)\r" --output "\$1" beluga.txt | sort > bbb.txt
