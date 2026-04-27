import matplotlib.pyplot as plt

def show_marks_graph():
    sid = int(input("Enter Student ID: "))

    cursor.execute("SELECT subject, marks FROM marks WHERE student_id=?", (sid,))
    data = cursor.fetchall()

    subjects = [row[0] for row in data]
    marks = [row[1] for row in data]

    plt.bar(subjects, marks)
    plt.xlabel("Subjects")
    plt.ylabel("Marks")
    plt.title("Student Marks Graph")
    plt.show()
