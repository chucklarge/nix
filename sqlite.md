    sqlite3 :memory: -cmd '.mode csv' -cmd '.import taxi.csv taxi' \
      'SELECT passenger_count, COUNT(*), AVG(total_amount) FROM taxi GROUP BY passenger_count'
  
  thanks simon!
  https://til.simonwillison.net/sqlite/one-line-csv-operations
