def calculate_grade():
    sid = int(input("Enter Student ID: "))

    cursor.execute("SELECT marks FROM marks WHERE student_id=?", (sid,))
    data = cursor.fetchall()

    if not data:
        print("No marks found")
        return

    avg = sum([m[0] for m in data]) / len(data)

    if avg >= 90:
        grade = "A"
    elif avg >= 75:
        grade = "B"
    elif avg >= 60:
        grade = "C"
    else:
        grade = "Fail"

    print("Average:", avg)
    print("Grade:", grade)
    
