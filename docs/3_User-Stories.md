# User Stories for Student Management System
User stories are generated using IBM Watsonx. The chat link is : [Link](https://eu-de.dataplatform.cloud.ibm.com/wx/prompts/sessions/ace7dc7e-7712-4b1c-8bc8-7a74f3938aa9?project_id=1739216a-c865-46cd-9e32-4651efe49011&context=wx)

The following user stories are based on the requirements gathered from stakeholders:

## Student User Stories
### As a student, I want to be able to log in to the system so that I can access my academic records.
**Acceptance Criteria:**
- The system allows students to log in with their username and password.
- The system authenticates student credentials and grants access to authorized users.
### As a student, I want to be able to view my course schedule so that I can plan my day.
**Acceptance Criteria:**
- The system displays the student's course schedule.
- The system updates the course schedule in real-time.
### As a student, I want to be able to view my grades so that I can track my progress.
**Acceptance Criteria:**
- The system displays the student's grades for each course.
- The system updates the grades in real-time.

## Teacher User Stories
### As a teacher, I want to be able to log in to the system so that I can manage my courses.
**Acceptance Criteria:** 
- The system allows teachers to log in with their username and password.
- The system authenticates teacher credentials and grants access to authorized users.
### As a teacher, I want to be able to create and manage courses so that I can organize my teaching materials.
**Acceptance Criteria:**
- The system allows teachers to create new courses.
- The system allows teachers to update and delete existing courses.
### As a teacher, I want to be able to grade assignments and exams so that I can track student progress.
**Acceptance Criteria:**
- The system allows teachers to create and manage assignments and exams.
- The system allows teachers to grade assignments and exams.

## Administrator User Stories
### As an administrator, I want to be able to log in to the system so that I can manage student and teacher accounts.
**Acceptance Criteria:**
- The system allows administrators to log in with their username and password.
- The system authenticates administrator credentials and grants access to authorized users.
### As an administrator, I want to be able to create and manage student and teacher accounts so that I can manage system access.
**Acceptance Criteria:**
- The system allows administrators to create new student and teacher accounts.
- The system allows administrators to update and delete existing student and teacher accounts.
### As an administrator, I want to be able to generate reports so that I can track system usage and student progress.
**Acceptance Criteria:**
- The system allows administrators to generate reports on system usage and student progress.
- The system updates the reports in real-time.

## Parent User Stories
### As a parent, I want to be able to log in to the system so that I can view my child's academic records.
**Acceptance Criteria:**
- The system allows parents to log in with their username and password.
- The system authenticates parent credentials and grants access to authorized users.
### As a parent, I want to be able to view my child's course schedule and grades so that I can track their progress.
**Acceptance Criteria:**
- The system displays the child's course schedule and grades.
- The system updates the course schedule and grades in real-time.

## Example User-Story

**Feature:** Student Login  
As a student, I want to be able to log in to the system so that I can access my academic records.

### Scenario: Successful Login

- **Given** I am on the login page  
- **When** I enter my valid username and password  
- **Then** I should be logged in to the system  
- **And** I should see my academic records

### Scenario: Invalid Login

- **Given** I am on the login page  
- **When** I enter my invalid username or password  
- **Then** I should see an error message  
- **And** I should not be logged in to the system

    
## Example code for user story:
# Student Login System
class Student:
    def __init__(self, username, password):
        self.username = username
        self.password = password

class StudentLoginSystem:
    def __init__(self):
        self.students = []

    def add_student(self, student):
        self.students.append(student)

    def login(self, username, password):
        for student in self.students:
            if student.username == username and student.password == password:
                return True
        return False

##### Create a student login system
sls = StudentLoginSystem()

##### Create a student
student = Student("johndoe", "password123")

##### Add the student to the system
sls.add_student(student)

##### Test the login function
print(sls.login("johndoe", "password123"))  # Should print: True

print(sls.login("johndoe", "wrongpassword"))  # Should print: False
