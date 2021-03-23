# Health-Management-System
Log and retrieve daily exercise and food details

def getdate():
    import datetime
    return datetime.datetime.now()
while(True):
    update_retrive = int(input("What do you want: 0 Quite, 1 update details, 2 Retrieve Details\n"))
    if update_retrive==1:
        client_name = int(input("Chose Name: 0 Quite, 1 Harry, 2 Rohan, 3 Hammad\n"))
        if client_name==1:
            option = int(input("Select for update value: 0 Quite, 1 Exc, 2 Food details\n"))
            if option==1:
                with open("Harry_Exc.txt","a") as f:
                    f.write(str(getdate())+"   "+input("Enter Exc:\n")+",  ")
                    print("Successfully written")
            elif option==2:
                with open("Harry_Food_details.txt","a") as f:
                    f.write(str(getdate())+"   "+input("Enter food:\n")+",  ")
                    print("Successfully written")
            elif option==0:
                break
            else:
                print("wrong Number")
        elif client_name==2:
            option = int(input("Select for update value: 0 Quite, 1 Exc, 2 Food details\n"))
            if option == 1:
                with open("Rohan_Exc.txt", "a") as f:
                    f.write("  "+str(getdate())+"   "+input("Enter Exc:\n")+",  ")
                    print("Successfully written")
            elif option==2:
                with open("Rohan_Food_details.txt","a") as f:
                    f.write("  "+str(getdate())+"   "+input("Enter food\n")+",  ")
                    print("Successfully written")
            elif option==0:
                break
            else:
                print("wrong Number")
        elif client_name==3:
            option = int(input("Select for update value: 0 Quite, 1 Exc, 2 Food details\n"))
            if option == 1:
                with open("Hammad_Exc.txt", "a") as f:
                    f.write("  "+str(getdate())+"   "+input("Enter Exc:\n")+",  ")
                    print("Successfully written")
            elif option == 2:
                with open("Hammad_Food_details.txt", "a") as f:
                    f.write("  "+str(getdate())+"   "+input("Enter food\n")+",  ")
                    print("Successfully written")
            elif option==0:
                break
            else:
                print("wrong Number")
        else:
            print("Wrong Number")
        if client_name==0:
            break
    elif update_retrive==2:
        client_name_R = int(input("Chose Name: 0 Quite, 1 Harry, 2 Rohan, 3 Hammad\n"))
        if  client_name_R==1:
            option_R=int(input("Select for Details: 0 Quite, 1 Exc, 2 Food details\n"))
            if option_R==1:
                with open("Harry_Exc.txt") as f:
                    print(f.readlines())
            elif option_R==2:
                with open("Harry_Food_details.txt") as f:
                    print(f.readlines())
            elif option_R==0:
                break
            else:
                print("wrong number")
        elif client_name_R==2:
            option_R=int(input("Select for Details: 0 Quite, 1 Exc, 2 Food details\n"))
            if option_R==1:
                with open("Rohan_Exc.txt") as f:
                    print(f.readlines())
            elif option_R==2:
                with open("Rohan_Food_details.txt") as f:
                    print(f.readlines())
            elif option == 0:
                break
            else:
                print("wrong Number")
        elif client_name_R==3:
            option_R = int(input("Select for Details: 0 Quite, 1 Exc, 2 Food details\n"))
            if option_R == 1:
                with open("Hammad_Exc.txt") as f:
                    print(f.readlines())
            elif option_R == 2:
                with open("Hammad_Food_details.txt",) as f:
                    print(f.readlines())
            elif option == 0:
                break
            else:
                print("wrong Number")
        elif option == 0:
            break
        else:
            print("wrong Number")
    elif update_retrive==0:
        break
    else:
        print("Wrong Number")
