from tkinter import*
from tkinter import messagebox

def login():
    username=Entry1.get()
    password=Entry2.get()

    if (username==" "and password==" "):
        messagebox.showinfo("","blank not allowed")

    elif(username=="gagandeep" and password=="deepu"):
        messagebox.showinfo("","login sucess")

    else:
        messagebox.showinfo("","incorrect username and password")

root=Tk()
root.title("login page")
root.geometry("300x200")

global Entry1
global Entry2
Label(root,text="username").place(x=20,y=20)
Label(root,text="password").place(x=20,y=70)

Entry1=Entry(root,bd=5)
Entry1.place(x=140,y=20)

Entry2=Entry(root,bd=5)
Entry2.place(x=140,y=70)

Button(root,text="login",command=login,height=3,width=13,bd=6).place(x=100,y=120)

root.mainloop
