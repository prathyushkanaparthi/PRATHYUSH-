# week1_student_registration.py
students = {}
def register_student(student_id, name):   
       if student_id in students:
        print("Student already registered!")
    else:
        students[student_id] = {"name": name, "courses": []}
        print(f"Student {name} registered successfully!")
def view_students():
    for sid, info in students.items():
        print(f"ID: {sid}, Name: {info['name']}")
# Example usage
register_student("S001", “sai")
register_student("S002", “thor")
view_students()
