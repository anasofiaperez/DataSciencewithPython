# Created by Ana Sofia Perez Rodriguez
# PS1. Problem 3. Part 1
# Hailstone Numbers
# Final Results Part 1:
# Number of good pairs: 33
# Total different patterns: 2015
# Total patterns: 2048

import itertools
maxSteps = 1000
goodpairs=[]
total=0
overall_seq_set=set()
for a, b in itertools.product(range(11), range(11)):
    cycleSet = set()
    isGoodPair = True
    init_x=1
    while init_x <= 1000 and isGoodPair:
        seq = []
        converges=False
        x = init_x
        init_x += 1
        for i in range(maxSteps):
            if x % 2 == 0:
                x = x//2
            else:
                x = a*x+b

            if x in seq:
                converges=True
                cycleStart = seq.index(x)
                cycleSet.add(frozenset(seq[cycleStart:]))
                break

            seq.append(x)

        if not converges:
            isGoodPair = False

    if isGoodPair:
        goodpairs.append([a,b])
        print("Converges: a="+str(a)+", b="+str(b))
        print(cycleSet)
        print("Number of different cycles: "+str(len(cycleSet))+"\n")
        total+=len(cycleSet)
        for cycle in cycleSet:
            overall_seq_set.add(cycle)
print("Number of good pairs: " + str(len(goodpairs)))
print("Total different patterns: "+str(len(overall_seq_set)))
print("Total patterns: "+str(total))


#Created by Ana Sofia Perez Rodriguez
#PS1. Problem 3. Part 2
#Hailstone Numbers
# Final Results Part2:
# Number of good combinations: 3217
# Total different patterns: 20061
# Total patterns: 234646

import itertools
maxSteps = 1000
goodnums=[]
total=0
overall_seq_set=set()
for a1, b1, a2, b2 in itertools.product(range(11), range(11), range(11), range(11)):
    cycleSet = set()
    areGoodNums=True
    init_x=1
    while init_x <= 1000 and areGoodNums:
        seq = []
        converges=False
        x = init_x
        init_x += 1
        for i in range(maxSteps):
            if x % 3 == 0:
                x = x//3
            elif x%3==1:
                x = a1*x+b1
            else:
                x=a2*x+b2

            if x in seq:
                converges=True
                cycleStart = seq.index(x)
                cycleSet.add(frozenset(seq[cycleStart:]))
                break

            seq.append(x)

        if not converges:
            areGoodNums = False

    if areGoodNums:
        goodnums.append([a1, b1, a2, b2])
        print("Converges: a1="+str(a1)+", b1="+str(b1)+", a2="+str(a2)+", b2="+str(b2))
        print(cycleSet)
        print("Number of different cycles: "+str(len(cycleSet))+"\n")
        total+=len(cycleSet)
        for cycle in cycleSet:
            overall_seq_set.add(cycle)
print("Number of good combinations: " + str(len(goodnums)))
print("Total different patterns: "+str(len(overall_seq_set)))
print("Total patterns: "+str(total))
