### C++ Program to Batch Update User Profiles

#### **Objective:**
Create a C++ program that processes user profile data stored as JSON files in a directory structure. It should apply a series of transformations to the user data and write the updated profiles into a new output directory. 

#### **Requirements:**

1. **Directory Structure**: 
    - You will be working with the directory called `user_profiles` (included in this repo), that contains sub-directories such as `admins`, `editors`, `viewers`, etc.
    - Each sub-directory contains JSON files that represent individual user profiles (e.g., `admin1.json`, `editor1.json`).

2. **Task Overview**:
    - Write a C++ program that reads each JSON file, performs specific updates to the contents, and writes the modified profiles into a new output folder. The output folder should include a timestamp in its name, and the folder structure should mirror the `user_profiles` folder.
  
3. **Required Functionality**:

    a. **Command-line Argument**:
       - The program must accept the path to the `user_profiles` directory as a command-line argument.

    b. **Email Replacement**:
       - All email addresses ending in `@company.com` must be replaced with `@newcompany.com`.

    c. **Value Replacement**:
       - The script should replace specific values in the JSON files based on a predefined map of replacements. 
       - For example:
         - The value `"enabled"` should be replaced by a JSON object: `{"status": "enabled", "since": "2024-10-01"}`.
         - The value `"manage_users"` should be replaced by a JSON object containing permission details: `{"permission": "manage_users", "granted_at": "2024-10-05", "level": "full"}`.

    d. **Output Directory**:
       - The modified JSON files should be written into a new folder with the current timestamp in the format: `user_profiles_updated_YYYYMMDD_HHMMSS`.

4. **Exceptions**:
    - Handle edge cases, such as missing keys in the JSON files, and ensure your program is robust to errors. Files that are not processable for any reason should be copied as-is to the destination folder.

#### **Example Folder Structure:**
```plaintext
user_profiles/
├── admins/
│   ├── admin1.json
│   ├── admin2.json
├── editors/
│   ├── editor1.json
│   ├── editor2.json
├── viewers/
│   ├── viewer1.json
│   ├── viewer2.json
```

#### **Replacement Map Example:**

- **Emails**: Replace all emails ending in `@company.com` with `@newcompany.com`.
- **Other Replacements**:
    - `"enabled"` → `{"status": "enabled", "since": "2024-10-01"}`
    - `"disabled"` → `{"status": "disabled", "since": "2024-10-01"}`
    - `"manage_users"` → `{"permission": "manage_users", "granted_at": "2024-10-05", "level": "full"}`
    - `"view_content"` → `{"permission": "view_content", "granted_at": "2024-09-25", "level": "read-only"}`

#### **Output Example:**
If your program is run at `2:35 PM` on `2025-11-16`, the output folder could be named `user_profiles_updated_20251116_143500`, with the modified JSON files inside.

#### **Submission:**
1. Create a Unit_08_01_UserProfileUpdater folder in your homework repository
1. Add your C++ source files (*.cpp, *.h, any other files needed).
2. A sample output folder containing the updated JSON files.

#### Hints and Suggestions 

1. Use the [nlohmann/json](https://github.com/nlohmann/json) library to read and modify JSON files. 
1. Use `std::filesystem` for directory traversal and file I/O.
1. Use `std::chrono` for generating the timestamp.

