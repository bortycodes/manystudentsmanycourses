# manystudentsmanycourses
A Python program to build a set of tables using the Many-to-Many approach to store enrollment and role data.

This application will read roster data in JSON format, parse the file, and then produce an SQLite database that contains a User, Course, and Member table and populate the tables from the data file.


Run the following SQL command to check:

SELECT hex(User.name || Course.title || Member.role ) AS X FROM 
    User JOIN Member JOIN Course 
    ON User.id = Member.user_id AND Member.course_id = Course.id
    ORDER BY X
