import csv

def export_students():
    cursor.execute("SELECT * FROM students")
    data = cursor.fetchall()

    with open("students.csv", "w", newline='') as file:
        writer = csv.writer(file)
        writer.writerow(["ID", "Name", "Age", "Course"])
        writer.writerows(data)

    print("Data exported to students.csv")
