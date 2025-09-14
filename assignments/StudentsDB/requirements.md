
# 🎓 **Unit 2, Assignment 1: Student Records Manager**

### **Problem Statement**

Write a **console-based Student Records Manager** that allows users to maintain information about students. The program should let users **add, display, and search for students**, while demonstrating **C++ string handling and formatting features**. You can use the employee database program as a reference from last week's exercise. 

---

### **Data Requirements**

Each student has the following fields:

* `id` (int)
* `name` (std::string)
* `age` (int)
* `major` (std::string)
* `email` (std::string)

---

### **Functional Requirements**

1. **Add Student**

   * Prompt the user for all student details and store them in a `std::vector<Student>`.
   * Validate numeric input (e.g., `id`, `age`).

2. **Display All Students**

   * Print a neatly formatted table of all students using `std::format`.
   * Example format:

     ```
     ID    Name                 Age   Major       Email
     ----------------------------------------------------------
     101   Alice Johnson        20    CS          alice@uni.edu
     102   Bob Smith            21    Math        bob@uni.edu
     ```

3. **Search by ID**

   * Prompt for an ID and display the matching student if found.
   * Show “Student not found” otherwise.

4. **Search by Name (string\_view)**

   * Prompt for a full name and search using `std::string_view` without copying data.

5. **Count Students by Major**

   * Display how many students are in each major.
   * Example:

     ```
     CS: 3
     Math: 2
     Physics: 1
     ```

6. **Exit**

   * Quit the program gracefully.

--- 
 
**NOTE** Please ensure that your program handles errors gracefully, displaying appropriate messages to users as needed.

