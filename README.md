def enroll_course(student_id, course_id):
    if student_id not in students:
        print("Student not found!")
        return
    if course_id not in courses:
        print("Course not found!")
        return
    students[student_id]["courses"].append(course_id)
    print(f"{students[student_id]['name']} enrolled in {courses[course_id]}")

# Example usage
register_student("S001", “sai")
add_course("C118", "Python Programming")
enroll_course("S001", "C118")
