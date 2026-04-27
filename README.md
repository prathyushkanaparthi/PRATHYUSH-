from tkinter import *

def gui_app():
    root = Tk()
    root.title("Student ERP System")

    Label(root, text="Student ERP", font=("Arial", 16)).pack()

    Button(root, text="Add Student", command=add_student).pack()
    Button(root, text="View Students", command=view_students).pack()

    root.mainloop()
