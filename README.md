# covid19
n = int(input("tedad list bimar : "))

myliste = []

for i in range(1,n+1):
    name = input("name bimar ra vared konid:  ")
    famili = input("family bimar : ")
    age = int(input("sen bimar: "))
    pcr = input("natije test pcr (+,-): ")
    symptoms = input("natije test symptoms (+,-): ")
    illness = input("illness (+,-): ")
    myliste.append([name,famili,age,pcr,symptoms,illness])

m = []
for m in myliste:
    name = m[0]
    famili = m[1]
    age = m[2]
    pcr = m[3]
    symptoms = m[4]
    illness = m[5]

    if pcr == ("-") :
        if symptoms == ("-"):
            print(m[0],m[1],m[2], "natije test pcr shoma : (-) = bimar niyazi be moraghebat  nadard tarkhis level0 ")
    else:
        if age<60 :
            if symptoms == ("-") and illness == ("-"):
                print(m[0],m[1],m[2],"bimar be darman_level1 niyaz darad ")
            elif symptoms == ("+") and illness == ("-"):
                print(m[0],m[1],m[2],"bimar be darman_level2 niyaz darad")
            else:
                print(m[0],m[1],m[2],"bimar be darman_level3 niyaz darad")
        elif age >= 60:
            if pcr == ("+") or symptoms == ("+") or  illness == ("+"):
                print(m[0],m[1],m[2],"bimar ba darman level 4 niyaz darad ")
