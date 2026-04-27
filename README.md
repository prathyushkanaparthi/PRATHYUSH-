# week5_file_handling.py
import json
def save_data():
    with open("students.json", "w") as f:
        json.dump(students, f)
    with open("courses.json", "w") as f:
        json.dump(courses, f)
    print("Data saved successfully!")
def load_data():
    global students, courses
    try:
        with open("students.json", "r") as f:
            students = json.load(f)
        with open("courses.json", "r") as f:
            courses = json.load(f)
        print("Data loaded successfully!")
    except FileNotFoundError:
        print("No previous data found.")
