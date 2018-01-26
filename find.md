Find all directories named 'events'    

    find . -name "events"

-print0 : don't print newline after each result

    find . -maxdepth 2 -name "File*txt" -print0

delete stuff

    find . -name ".terraform" -type d -exec rm -rf {} +
