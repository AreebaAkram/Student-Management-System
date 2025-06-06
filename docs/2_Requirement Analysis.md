# Step # 1 - Requirement Analysis

Requirement analysis performed using IBM Watsonx. The chat link is [Link](https://eu-de.dataplatform.cloud.ibm.com/wx/prompts/sessions/ace7dc7e-7712-4b1c-8bc8-7a74f3938aa9?project_id=1739216a-c865-46cd-9e32-4651efe49011&context=wx)

## Introduction to Student Management System
The student management system is a software application designed to manage and track student information, academic records, and other related data. To develop an effective system, it's essential to analyze the functional and non-functional requirements.

### Identifying Stakeholders
The stakeholders of the student management system include:

<li>Students: The primary users of the system, who will use it to access their academic records, course schedules, and other relevant information.</li>
<li>Teachers: The instructors who will use the system to manage their courses, track student progress, and communicate with students. </li>
<li>Administrators: The school or university staff responsible for managing the system, maintaining student records, and generating reports. </li>
<li>Parents: The guardians of students who may use the system to monitor their child's academic progress. </li>

### Gathering Requirements
To gather requirements, we can use various techniques such as:

<li> Interviews: Conducting one-on-one interviews with stakeholders to understand their needs and expectations. </li>
<li> Surveys: Distributing questionnaires to stakeholders to collect data on their requirements. </li>
<li> Workshops: Organizing workshops with stakeholders to discuss and prioritize requirements. <l/i>
<li> Observations: Observing the current processes and systems used by stakeholders to identify areas for improvement. </li>
<li> Understanding Limitations, Objectives, and Desires of Stakeholders </li>
  
### The limitations, objectives, and desires of stakeholders include:

**Students:**
<li> Limitations: Limited access to academic records, difficulty in tracking course schedules.</li>
<li> Objectives: Easy access to academic records, ability to track course schedules, communicate with teachers.</li>
<li> Desires: User-friendly interface, mobile accessibility, personalized notifications.</li>
  
**Teachers:**
<li> Limitations: Manual tracking of student progress, difficulty in communicating with students.</li>
<li> Objectives: Automated tracking of student progress, ability to communicate with students, manage courses.</li>
<li> Desires: Easy-to-use interface, ability to generate reports, integrate with other systems.</li>

**Administrators:**
<li> Limitations: Manual maintenance of student records, difficulty in generating reports. </li>
<li> Objectives: Automated maintenance of student records, ability to generate reports, manage system. </li>
<li> Desires: Secure and reliable system, ability to track system usage, integrate with other systems. </li>

**Parents:**
<li> Limitations: Limited access to child's academic records, difficulty in tracking child's progress. </li>
<li> Objectives: Access to child's academic records, ability to track child's progress, communicate with teachers. </li>
<li> Desires: User-friendly interface, mobile accessibility, personalized notifications. </li>

### Categorizing Requirements
The requirements can be categorized into:

**Functional Requirements:**
<li> User authentication and authorization</li>
<li> Student information management</li>
<li> Course management</li>
<li> Grade management</li>
<li> Reporting and analytics</li>

**Non-Functional Requirements:**
<li> Performance: The system should respond to user requests within 2 seconds.</li>
<li> Security: The system should ensure the confidentiality, integrity, and availability of student data.</li>
<li> Usability: The system should be easy to use and navigate.</li>
<li> Scalability: The system should be able to handle an increasing number of users and data.</li>

### Analyzing Requirements
The requirements can be analyzed using techniques such as:

<li> Use Case Diagrams: To visualize the interactions between stakeholders and the system.</li>
<li> Sequence Diagrams: To illustrate the sequence of events in the system.</li>
<li> Class Diagrams: To model the data structures and relationships in the system.</li>

### Prioritizing Requirements
The requirements can be prioritized using techniques such as:

<li> MoSCoW Method: To categorize requirements as Must-Haves, Should-Haves, Could-Haves, and Won't-Haves. </li>
<li> Kano Model: To categorize requirements as Basic, Performance, and Excitement factors.</li>


### Validating Requirements
The requirements can be validated using techniques such as:

<li> Reviews: Conducting regular reviews with stakeholders to ensure the requirements are met. </li>
<li> Prototyping: Creating a prototype of the system to test and validate the requirements.</li>
<li> Testing: Conducting unit testing, integration testing, and system testing to ensure the requirements are met.</li>

### Example UseCase: 
#### Use Case: Student Information Management
##### Primary Actor: Administrator
##### Goal: To manage student information
##### Precondition: The administrator is logged in to the system
##### Triggers: The administrator wants to add, update, or delete student information
##### Description:
1. The administrator logs in to the system.
2. The administrator navigates to the student information management page.
3. The administrator adds, updates, or deletes student information.
4. The system validates the input data.
5. The system updates the student information database.
##### Postcondition: The student information is updated in the database.


### Example Code:

##### Student Information Management System
class Student:
    def __init__(self, name, email, grade):
        self.name = name
        self.email = email
        self.grade = grade

class StudentInformationSystem:
    def __init__(self):
        self.students = []

    def add_student(self, student):
        self.students.append(student)

    def update_student(self, student_id, student):
        for i, s in enumerate(self.students):
            if s.email == student_id:
                self.students[i] = student
                break

    def delete_student(self, student_id):
        for i, s in enumerate(self.students):
            if s.email == student_id:
                del self.students[i]
                break

##### Create a student information system
sis = StudentInformationSystem()

##### Create a student
student = Student("John Doe", "johndoe@example.com", "A")

##### Add the student to the system
sis.add_student(student)
