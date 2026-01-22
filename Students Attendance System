# Student Attendance Management System

students = {}
attendance_file = "attendance.txt"

def add_student():
    student_id = input("Enter student ID: ")
    name = input("Enter student name: ")
    students[student_id] = name
    print("Student added successfully!")

def mark_attendance():
    if not students:
        print("No students available.")
        return
    with open(attendance_file, "a") as file:
        for sid, name in students.items():
            status = input(f"Is {name} present? (P/A): ").upper()
            file.write(f"{sid},{name},{status}\n")
    print("Attendance marked successfully!")

def view_attendance():
    try:
        with open(attendance_file, "r") as file:
            print("\nAttendance Records:")
            print(file.read())
    except FileNotFoundError:
        print("No attendance records found.")

def menu():
    while True:
        print("""
1. Add Student
2. Mark Attendance
3. View Attendance
4. Exit
""")
        choice = input("Choose an option: ")
        if choice == "1":
            add_student()
        elif choice == "2":
            mark_attendance()
        elif choice == "3":
            view_attendance()
        elif choice == "4":
            print("Exiting system...")
            break
        else:
            print("Invalid option")

menu()
