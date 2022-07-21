# Automated-attendance-system-using-Face-recognition-and-MYSQL-database
 	 

AUTOMATED ATTENDANCE SYSTEM USING REAL TIME FACE RECOGNITION AND MYSQL DATABASE
A MINI PROJECT REPORT


ABSTRACT

Nowadays Educational institutions are concerned about regularity of student attendance. Even in pandemic situation attendance is still a major issue in schools and colleges. Mainly there are two conventional methods of marking attendance which are calling out the roll call or by taking student sign on paper. They both were more time consuming and difficult. Hence, there is a requirement of computer-based student attendance management system which will assist the faculty for maintaining attendance record automatically. In this project we have implemented the automated attendance system using 'PYTHON' and 'MYSQL'. We have projected our ideas to implement an “Automated Attendance System Based on Face Recognition”. The application includes face identification, which saves time as well as being purely software based it can be flagged as eco-friendly as it reduces the use of paper. This system also eliminates the chances of fake attendance because of the face being used as a biometric for authentication. Hence, this system can be implemented in a field where attendance plays an important role. The proposed system is designed using PYTHON as well as SQL database. The algorithm used in the system is based on image comparison on the basis of the encoded values of the face from the image from database with the image recorded by the system in run time. The system has output in the form of MYSQL DATABASE.
 
CHAPTER – 1 INTRODUCTION
 
1.1	OVERVIEW OF THE PROJECT:

The Attendance System using Face – Recognition is a replacement way method for the traditional way of marking attendance. The proposed system is PYTHON based system supported with MySQL database. This system can be implemented on a single faculty system of a particular institute. This system is proposed to be based on biometrics, i.e. Face Authentication. Since there is presence of biometrics, this system completely eliminates the chances of fake attendance which is a problem with the traditional methods of attendance.

The Attendance management is the significant process that were carry out in every institute to monitor the performance of the student. Every institute does this is its own way. Some of these institute use the old paper or file-based system and some have adopted strategies of automated attendance system using some biometric technique. A facial recognition system is a computerized software which is suited for determining or validating a person by performing comparisons on patterns based on their facial appearances. In this system OpenCV & Face Recognition libraries were used which are one of the popular libraries for face detection by using these libraries system first capturing the student photos and storing them into the database which were further used for the training purpose after that at the time of attendance when system camera get on system will detect the faces that were present in the frame the faces were detected by using HOG i.e. (Histogram of Oriented Gradients) which were carried out in the system. After that if image that were present in the \frame is tilted then Face Landmark Estimation algorithm will be carried out and face will be transformed to be as close as possible to perfectly centered. After that system will encode all the images that were present in the database as well as the face which were detected in the frame. For performing encoding Deep Conversional Neural Network algorithm will get carried out & for each face 128 measurements were generated then the measurements of the face that were detected in frame it gets compared with the measurements of the faces that
 
were present in the image which is earlier stored in the database. So, at last by using simple liner SVM algorithm system will find the person in database of know peoples (i.e. capture at the starting of the project) who has closest measurements to the image that were detected by camera. After finding perfect match system will generate the name and date & time & present mark and store the entry in a MYSQL database by connecting MYSQL and PYTHON using the MYSQL API.

1.2	OBJECTIVE OF THE PROJECT:

The objective of face recognition is, from the incoming image, to find a series of data of the same face in a set of training images in a database. The great difficulty is ensuring that this process is carried out in real-time, instead of using the conventional methods, this proposed system aims to develop an automated system that records the student’s attendance by using facial recognition technology. The main objective of this work is to make the attendance marking and management system efficient, time saving, simple and easy.

Our primary goal is to help the lecturers, improve and organize the process of track and manage student attendance and absenteeism. Additionally, we seek to:

1.	Provides a valuable attendance service for both teachers and students.
2.	Reduce manual process errors by provide automated and a reliable attendance system uses face recognition technology.
3.	Increase privacy and security which student cannot presenting himself or his friend while they are not.
4.	Produce monthly reports for lecturers.
5.	Flexibility, Lectures capability of editing attendance records.
 
1.3	BACKGROUND

Most lecturers have a significant number of students and it is hard to keep taking or tracking all their absence. Facial recognition is commonly used in many institutions to take attendance of a significant number of students. There are many errors that could occur during this process, including misidentification and self-recognition. Lecturer can control the errors and correct it.

1.3.1	Face Recognition Usage

“Face recognition rises from the moment that machine started to become more and more intelligent and had the advance of fill in, correct or help the lack of human abilities and senses”. Common uses of Facial recognition clarify in following points

*	Security can be crime-fighting it will recognize people based on their eyes, nose and face.
*	Searching for lost people.
*	Taking student or employee attendance


1.3.2	Face Recognition Techniques and Methods

“Many factors influence the process of face recognition such as shape, size, pose, occlusion, and illumination. Facial recognition, have two different applications: basic and advanced”. Major face recognition recognizes faces or no faces such as balls and animals. If it is a face, then the system searches for eyes, a nose, and a mouth. Advanced facial recognition manages the question on a specific face. This contains unique landmarks: “the width of nose, wideness of the eyes, the depth and angle of the jaw, the height of cheekbones, and the separation between the eyes, and makes a unique
 
numerical code.”


Utilizing these numerical codes, the system then matches that image with another image and distinguishes how comparable the pictures are to each other. The image provenance for face recognition include pre-existing pictures from various databases and video camera signals.
 
 

CHAPTER – 2 LITERATURE SURVEY
 
2.1	An Automatic Attendance System Using Image processing


Author: Dr. Suvarna Nandyal, Aziza Ahmedi

Year: 2015

The face is the identity of a person. The methods to exploit this physical feature have seen a great change since the advent of image processing techniques. The attendance is taken in every schools, colleges and library. Traditional approach for attendance is professor calls student name & record attendance. The system described in this paper aims to deviate from such traditional systems and introduce a new approach for taking an attendance using image Processing. This paper describes the working of An Automatic Attendance System in a classroom environment. Initially video clip of classroom is taken and is stored in the database, and these video is converted to frames/images, then they apply Face detection techniques such as Ada-boost algorithm to detect the faces in frames/images and then features are extracted of detected face by Histogram of Oriented Gradients (HOG) and Local Binary Pattern (LBP) algorithm. The system first stores the faces of the students in the database. The detected faces are compared with the faces stored in the database during face recognition by using Support Vector Machine (SVM) classifier. If the system recognizes Faces, the attendance gets marked immediately of recognized faces.
 
2.2	Study of Implementing Automated Attendance System Using Face Recognition Technique



Author: Nirmalya Kar, Mrinal Kanti Debbarma, Ashim Saha, and Dwijen Rudra Pal

Year: 2012


Authentication	is	a significant	issue in	system	control in	computer based communication. Human face recognition is an important branch of biometric verification and has been widely used in many applications, such as video monitor system, human-computer interaction, and door control system and network security. This paper describes a method for Student’s Attendance System which will integrate with the face recognition technology using Personal Component Analysis (PCA) algorithm. The system will record the attendance of the students in class room environment automatically and it will provide the facilities to the faculty to access the information of the students easily by maintaining a log for clock-in and clock-out time.
 
2.3	Support Vector Regression and Classification Based Multi- view Face Detection and Recognition


Author: Yongmin Li, Shaogang Gong and Heather Liddell

Year: 2000

A Support Vector Machine based multi-view face detection and recognition framework is described in this paper. Face detection is carried out by constructing several detectors, each of them in charge of one specific view. The symmetrical property of face images is employed to simplify the complexity of the modelling. The estimation of head pose, which is achieved by using the Support Vector Regression technique, provides crucial information for choosing the appropriate face detector. This helps to improve the accuracy and reduce the computation in multi-view face detection compared to other methods. For video sequences, further computational reduction can be achieved by using Pose Change Smoothing strategy. When face detectors find a face in frontal view, a Support Vector Machine based multi-class classifier is activated for face recognition. All the above issues are integrated under a Support Vector Machine framework. Test results on four video sequences are presented, among them, detection rate is above 95%, recognition accuracy is above 90%, average pose estimation error is around10Æ, and the full detection and recognition speed is up to 4frames/second on a PentiumII300 PC.
 
2.4	Automated Attendance Management System Based On Face Recognition Algorithms


Author: Shireesha Chintalapati, M.V. Raghunadh


Year : 2013


In this paper they propose an automated attendance management system. This system, which is based on face detection and recognition algorithms, automatically detects the student when he enters the class room and marks the attendance by recognizing him. The system architecture and algorithms used in each stage are described in this paper. Different real time scenarios are considered to evaluate the performance of various face recognition systems. This paper also proposes the techniques to be used in order to handle the threats like spoofing. When compared to traditional attendance marking this system saves the time and also helps to monitor the students.
 
2.5	Automated Attendance System Using Face Recognition



Author: Akshara Jadhav, Akshay Jadhav Tushar Ladhe, Krishna Yeolekar.

Year: 2017


In modern times, face recognition has become one of the key aspects of computer vision. There are at least two reasons for this trend; the first is the commercial and law enforcement applications, and the second is the availability of feasible technologies after years of research. Due to the very nature of the problem, computer scientists, neuroscientists and psychologists all share a keen interest in this field. In plain words, it is a computer application for automatically identifying a person from a still image or video frame. In this paper they proposed an automated attendance management system. This system based on face detection and recognition algorithms, which automatically detects the student when he enters in the class room and marks the attendance by recognizing him. They used Viola-Jones Algorithm face detection which detect human face using cascade classifier and PCA algorithm for feature selection and SVM for classification. When compared to traditional attendance marking this system saves the time and also helps to monitor the students.
 

CHAPTER – 3 SYSTEM ANALYSIS AND DESIGN
 
3.1	EXISTING SYSTEM:

	In the existing system all the information is to be maintained in a hard file or Website. While searching any information it is difficult to access and time consuming. Some computer-based software’s are also used nowadays but they are not user-friendly and don’t provide portability. Faculty takes time to maintain these records. Some organizations use various software for maintaining student’s records but they are not very efficient. The main drawback of existing system is that it does not provide portability and is time consuming.

	Here the attendance will be carried out in the hand written registers. It will be a tedious job to maintain the record for the user. The human effort is more here. The retrieval of the information is not as easy as the records are maintained in the hand written registers.

DRAWBACKS:

	Human errors are high
	Manual time entry is very time consuming.
	Keyboard and printing errors are high
	Incorrect Entry of Times
	Too much paperwork
 
3.2	PROPOSED SYSTEM:

	To Overcome the problems in the existing system, Automated attendance management system using face recognition and MySQL RDBMS is the proposed system, the main aim of it is to overcome the disadvantages of the existing system and provide a error free automated attendance management.

	This project aims to design an automated attendance system using face-recognition and MySQL database. In this experiment, four investigation experiments were carried out: the accuracy rate of the face recognition system in actual check-in; the stability of the face recognition time and attendance system with real-time video processing; analysis of the skip rate of face recognition attendance system using real-time video processing; interface settings of face recognition attendance system using real-time video processing. The experimental results show that the automated attendance system achieves time and attendance results through face recognition technology and a database, which fully reflects the design of the overall algorithm.

ADVANTAGES:

	Cost and time efficient
	Automated Time Tracking System
	Highly customizable
	The entire environment is automated
	Eco-friendly


CHAPTER – 4

REQUIREMENT SPECIFICATION
 
HARDWARE AND SOFTWARE REQUIREMENTS:

4.1 HARDWARE REQUIREMENTS:

1.Laptop 
2.Mouse 
3.Webcam

4.2 SOFTWARE REQUIREMENTS:

1.Windows 11 2.PyCharm IDE
3.	PACKAGES AND MODULES USED
3.1	cmake
3.2	dlib
3.3	face-recognition
3.4	opencv
3.5	datetime
3.6	MySQL-connector-python
3.7	os
3.8	pip
4.	MYSQL community server
5.	Command prompt
 


 


 

 

