def attendance_percentage():
    sid = int(input("Enter Student ID: "))

    cursor.execute("SELECT COUNT(*) FROM attendance WHERE student_id=?", (sid,))
    total = cursor.fetchone()[0]

    cursor.execute("SELECT COUNT(*) FROM attendance WHERE student_id=? AND status='Present'", (sid,))
    present = cursor.fetchone()[0]

    if total > 0:
        percent = (present / total) * 100
        print(f"Attendance: {percent:.2f}%")
    else:
        print("No attendance data")
