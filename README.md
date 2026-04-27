# week6_admin_controls.py

admin_password = "admin123"

def admin_login(password):
    return password == admin_password

# Example usage
if admin_login("admin123"):
    add_course("C103", "Data Science")
else:
    print("Access denied!")
