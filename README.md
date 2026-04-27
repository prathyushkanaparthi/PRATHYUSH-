def search_student():
    keyword = input("Enter name or course to search: ")
    cursor.execute("SELECT * FROM students WHERE name LIKE ? OR course LIKE ?", 
                   ('%' + keyword + '%', '%' + keyword + '%'))
    data = cursor.fetchall()

    print("\n--- Search Results ---")
    for row in data:
        print(row)
