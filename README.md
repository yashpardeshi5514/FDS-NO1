# Input for students playing cricket
cricket = []
cri = int(input("Enter the number of students playing cricket: "))
for i in range(cri):
    name_cricket = input("Enter the name of the student playing cricket: ")
    cricket.append(name_cricket)
 
# Input for students playing badminton
badminton = []
bad = int(input("Enter the number of students playing badminton: "))
for i in range(bad):
    name_badminton = input("Enter the name of the student playing Badminton: ")
    badminton.append(name_badminton)
 
# Input for students playing football
football = []
foot = int(input("Enter the number of students playing Football: "))
for i in range(foot):
    name_football = input("Enter the name of the Student playing Football: ")
    football.append(name_football)
 
# Function to find students who play both cricket and badminton
def unicribad():
    uni_cri_bad = []
    for i in range(cri):
        for j in range(bad):
            if cricket[i] == badminton[j] and cricket[i] not in uni_cri_bad:
                uni_cri_bad.append(cricket[i])
    print("1.Number of students who play both Cricket and Badminton:\n", uni_cri_bad)
 
# Function to find students who play either cricket or badminton but not both
def orcribad():
    or_cri_bad = []
    for i in range(cri):
        if cricket[i] not in badminton and cricket[i] not in or_cri_bad:
            or_cri_bad.append(cricket[i])
    for j in range(bad):
        if badminton[j] not in cricket and badminton[j] not in or_cri_bad:
            or_cri_bad.append(badminton[j])
    print("2.Number of students who play either Cricket or Badminton but not both:\n", or_cri_bad)
 
# Function to find students who play neither cricket nor badminton
def neithercrinorbad():
    neither_cri_nor_bad = []
    for i in range(foot):
        if football[i] not in cricket and football[i] not in badminton:
            neither_cri_nor_bad.append(football[i])
    print("3.Number of students playing neither Cricket nor Badminton:\n", len(neither_cri_nor_bad))
 
# Function to find students who play cricket and football but not badminton
def criandfootnotbad():
    cri_foot_not_bad = []
    for i in range(cri):
        if cricket[i] in football and cricket[i] not in badminton:
            cri_foot_not_bad.append(cricket[i])
    print("The number of students who play cricket and football but not badminton:\n", len(cri_foot_not_bad))
 
# Main logic
n = (input("Press Enter to get answers "))
if n == "":
    print("ANSWERS ARE: ")
    unicribad()
    orcribad()
    neithercrinorbad()
    criandfootnotbad()
else:
    print("SORRY WRONG ANS")
