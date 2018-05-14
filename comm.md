    cat a.txt
    a
    b
    c
    d
    e
    f

    cat b.txt
    d
    e
    f
    g
    h
    i

in a and b

    comm -12 a.txt b.txt
    d
    e
    f

in a but not in b

    comm -23 a.txt b.txt
    a
    b
    c

in b but not in a

    comm -13 a.txt b.txt
    g
    h
    i


unsorted 

    comm -13 <(sort a.txt) <(sort b.txt)
