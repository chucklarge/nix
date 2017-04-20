jq is a lightweight and flexible command-line JSON processor.
http://stedolan.github.com/jq/


```curl https://reports.com?report=124966440840 | jq -r '.results[] | .tags' | sort | uniq
