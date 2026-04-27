def view_registered_courses(student_id):
    if student_id not in students:
        print("Student not found!")
        return
    
    print(f"Courses for {students[student_id]['name']}:")
    for cid in students[student_id]["courses"]:
        print(f"- {courses[cid]}")

# Example usage
view_registered_courses("S001")
