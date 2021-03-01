jq is a lightweight and flexible command-line JSON processor.
http://stedolan.github.com/jq/


    curl https://reports.com?report=124966440840 | jq -r '.results[] | .tags' | sort | uniq

    curl -s https://reports.com?report=8285601801 | jq -r '.results[] | .id + " " + .first + " " + .last + " " + .title'

    jq '[.[] | select(.task_id == "786927230688")][0] | .body_plain' file.json
