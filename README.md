# StudentController.java

```java
package dataManagement.dm;

import org.apache.commons.io.FileUtils;
import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.core.io.ClassPathResource;
import org.springframework.http.HttpHeaders;
import org.springframework.http.HttpStatus;
import org.springframework.http.MediaType;
import org.springframework.http.ResponseEntity;
import org.springframework.util.StreamUtils;
import org.springframework.web.bind.annotation.*;
import org.springframework.web.multipart.MultipartFile;

import java.io.*;
import java.nio.charset.StandardCharsets;
import java.util.List;
import java.util.Optional;

@RestController
@RequestMapping("/api/students")
public class StudentController {
    @Autowired
    private StudentService studentService;

    // Rest of the Java code goes here...
}
----------------------------------------------------------------------------------------------------------------------------------------------------------------------

## StudentController.java

Controller class for handling student-related operations. This class defines various endpoints for managing student data and file uploads.

### Endpoints:
- **GET** `/api/students/`: Retrieves all students.
- **GET** `/api/students/{id}`: Retrieves a student by ID.
- **POST** `/api/students/`: Creates a new student.
- **PUT** `/api/students/{id}`: Updates an existing student.
- **DELETE** `/api/students/{id}`: Deletes a student by ID.
- **GET** `/api/students/html`: Retrieves HTML content from a static file.
- **POST** `/api/students/{id}/upload`: Handles file upload for a specific student.
- **GET** `/api/students/{id}/view`: Retrieves a file associated with a student for viewing.
------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# StudentService.java

```java
package dataManagement.dm;

import org.springframework.beans.factory.annotation.Autowired;
import org.springframework.stereotype.Service;

import java.util.List;
import java.util.Optional;

@Service
public class StudentService {
    @Autowired
    private StudentRepository studentRepository;

    // Rest of the Java code goes here...
}
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## StudentService.java

Service class for managing student-related operations. This class provides methods to interact with the StudentRepository.

### Methods:
- **getAllStudents()**: Retrieves all students.
- **getStudentById(Long id)**: Retrieves a student by ID.
- **createOrUpdateStudent(Student student)**: Creates or updates a student.
- **deleteStudentById(Long id)**: Deletes a student by ID.
