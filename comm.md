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

comm -12 a.txt b.txt
d
e
f

comm -23 a.txt b.txt
a
b
c

comm -13 a.txt b.txt
g
h
i
