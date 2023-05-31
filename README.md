# cancer
n = int(input("tedad list bimar : "))

myliste = []

for i in range(1,n+1):
    name = input("name bimar ra vared konid:  ")
    famili = input("family bimar : ")
    age = int(input("age bimar: "))
    cancertype = input("please inter 1 for benign and 2 for malignant: ")
    stage = input("inter 1 , 2 , 3 , 4 for stage : ")
    myliste.append([name,famili,age,cancertype,stage])

m = []
for m in myliste:
    name = m[0]
    famili = m[1]
    age = m[2]
    cancertype = m[3]
    stage = m[4]
    if cancertype == "1":
        if age<50:
            if stage == "1" or stage=="2":
                print(m[0],m[1],m[2],"darman :1_1 : pishnahad mishavad :")
            elif stage == "3":
                print(m[0], m[1], m[2], "darman :2_1 : pishnahad mishavad :")
            else:
                print(m[0], m[1], m[2], "darman :3_1 : pishnahad mishavad :")
        else:
            if stage == "1" or stage == "2":
                print(m[0], m[1], m[2], "darman :1_2 : pishnahad mishavad :")
            else:
                print(m[0], m[1], m[2], "darman :2_2 : pishnahad mishavad :")
    else:
        if stage == "1" or stage == "2":
            print(m[0], m[1], m[2], "darman :3_1 : pishnahad mishavad :")
        else:
            print(m[0], m[1], m[2], "darman :2_3 : pishnahad mishavad :")



