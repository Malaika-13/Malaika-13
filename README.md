class Student {
  String name;
  String id;
  List<String> courses;

  Student(this.name, this.id, this.courses);

  void addCourse(String course) {
    courses.add(course);
  }

  void dropCourse(String course) {
    courses.remove(course);
  }

  void displayCourses() {
    print('Courses for $name (ID: $id):');
    for (var course in courses) {
      print(course);
    }
    print('');
  }
}

void main() {
  // Creating two instances of Student
  var student1 = Student('Alice', '001', ['Math', 'Science']);
  var student2 = Student('Bob', '002', ['English', 'History']);

  // Performing operations on student1
  student1.displayCourses();
  student1.addCourse('Physics');
  student1.displayCourses();
  student1.dropCourse('Science');
  student1.displayCourses();

  // Performing operations on student2
  student2.displayCourses();
  student2.addCourse('Geography');
  student2.displayCourses();
  student2.dropCourse('English');
  student2.displayCourses();
}
