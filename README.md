# helthmanagementsystem
this is python code that manage multi user with read write capability   

operation_perform = int(input("choose 1 for Read & 2 for Write :"))
choose_person = int(input("choose 1 for harry , 2 for rohan ,3 for johan :"))
choose_file=int(input("enter 1 for dite & 2 for exercise :"))
import datetime

def getdate():

    return datetime.datetime.now()

if operation_perform == 1:
    def readlog(cp,cf):
        if cp == 1 and cf == 1:
            f=open("harrydite.txt")
            flt=f.read()
            print(flt)

        elif cp == 1 and cf == 2:
            f=open("harryexercise.txt")
            flt=f.read()
            print(flt)

        elif cp == 2 and cf == 1:
            f=open("rohandite.txt")
            flt=f.read()
            print(flt)

        elif cp == 2 and cf == 2:
            f=open("rohanexercise.txt")
            flt=f.read()
            print(flt)

        elif cp == 3 and cf == 1:
            f=open("johandite.txt")
            flt=f.read()
            print(flt)

        elif cp == 3 and cf == 2:
            f=open("johanexercise.txt")
            flt=f.read()
            print(flt)
    readlog(choose_person,choose_file)

elif operation_perform == 2:
    def writelog(cp,cf):
        if cp == 1 and cf ==1:
            f = open("harrydite.txt","a")
            flt = f.write("\n"+str([str(getdate())])+" : "+input("Type new dite :"))
            print("Data Entry completed successfully !")

        elif cp == 1 and cf == 2:
            f = open("harryexercise.txt", "a")
            flt = f.write("\n" + str([str(getdate())]) + " : " + input("Type new exercise :"))
            print("Data Entry completed successfully !")

        elif cp == 2 and cf == 1:
            f = open("rohandite.txt", "a")
            flt = f.write("\n"+str([str(getdate())])+" : "+input("Type new dite :"))
            print("Data Entry completed successfully !")

        elif cp == 2 and cf == 2:
            f = open("rohanexercise.txt", "a")
            flt = f.write("\n" + str([str(getdate())]) + " : " + input("Type new exercise :"))
            print("Data Entry completed successfully !")

        elif cp == 3 and cf==1:
            f = open("johandite.txt", "a")
            flt = f.write("\n" + str([str(getdate())]) + " : " + input("Type new dite :"))
            print("Data Entry completed successfully !")

        elif cp == 3 and cf == 2:
            f = open("johanexercise.txt", "a")
            flt = f.write("\n" + str([str(getdate())]) + " : " + input("Type new exercise :"))
            print("Data Entry completed successfully !")
    writelog(choose_person,choose_file)
