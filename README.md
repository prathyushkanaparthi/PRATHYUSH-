students = {}
courses = {}
def add_course(course_id, course_name):
    courses[course_id] = course_name
    print(f"Course {course_name} added successfully!")
def remove_course(course_id):
    if course_id in courses:
        print(f"Course {courses[course_id]} removed.")
        del courses[course_id]
    else:
        print("Course not found!")def view_courses():
    for cid, cname in courses.items():
        print(f"Course ID: {cid}, Name: {cname}")
# Example usage
add_course("C101", "Python Programming")
add_course("C102", "Database Systems")view_courses()
