During second training at Smart Methods Company# Control panel for robot arm with database
With my second training at the Smart Methods Company on the Internet of Things track, We start with the second task in the first project, which is a robotic arm that controls a camera. But the difference from the first one is that it is linked to the database with more details and methods that I like to add attached to this description :)
This description contains many content for your benefit, and it's best to read it completely 📖

In this animation a sequence of site traffic and appearance on the response page and database for this project.

![alt text](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/blob/main/Control%20panel%20for%20robot%20arm%20with%20database/GIF%20of%20the%20process%20from%20clicking%20to%20store%20data%20and%20appearing%20in%20response.gif "GIF of using the task")

Photo of the site:

![much-a image](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/blob/main/Control%20panel%20for%20robot%20arm%20with%20database/Pictures%20of%20the%20main%20page.png) 

Photo of the Response site:

![much-a image](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/blob/main/Control%20panel%20for%20robot%20arm%20with%20database/Pictures%20of%20the%20response%20page.png) 

Photo of the structure in database:

![much-a image](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/blob/main/Control%20panel%20for%20robot%20arm%20with%20database/Image%20for%20structure%20in%20phpMyAdmin.png) 

Photo of the data in database:

![much-a image](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/blob/main/Control%20panel%20for%20robot%20arm%20with%20database/Image%20for%20data%20in%20phpMyAdmin.png) 

# Component Diagram of software 
The purpose of a component diagram is to show the relationship between different components in a system by lucidchart website.
I tried to do something simpler for what I implemented in the image and designed it through a template in a program draw.io

![much-a image](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/blob/main/Control%20panel%20for%20robot%20arm%20with%20database/Image%20of%20component%20Diagram%20of%20software.png) 


# DRY (Don't repeat yourself)
The definition from Wikipedia is: "a principle of software development aimed at reducing repetition of software patterns, replacing it with abstractions or using data normalization to avoid redundancy."

I noticed that I have to repeat the following code in each line of the site buttons, which is 10, therefore, 11 lines are repeated with changing one letter (which will be stored in the database), which will lead to an increase of 110 lines  like that : 

`if (isset($_POST['Right-submit'])) {
    $sql = "INSERT INTO direction_and_motor_values (date,Forwards, Left, Right, Backwards, motor_1, motor_2, motor_3, motor_4, motor_5, motor_6) VALUES ('','', '', 'Right', '', '', '', '', '', '', '');";
    
    if ($conn->query($sql) === TRUE) {
      echo "New record created successfully";
    } else {
      echo "Error: " . $sql . "<br>" . $conn->error;
    }   
    $conn->close();
    } `

The solution for that, after what I thought, is to do one function via PHP and every time we need it as it performs the operation by call function in one line

`WritingToDatabase($conn,'', '', 'Right', '', '', '', '', '', '', '');`

I have implemented it myself and I like it so whoever wants to use it informs me about that because it is the first effective function I implement in PHP :)

And this is a some lines of function  WritingToDatabase :

    $sql = "INSERT INTO `direction_and_motor_values` (`date`,`Forwards`, `Left`, `Right`, `Backwards`, `motor_1`, `motor_2`, `motor_3`, `motor_4`, `motor_5`, `motor_6`) VALUES ('$date','$Forwards_value', '$Left_value', '$Right_value', '$Backwards_value', '$motor_1_value', '$motor_2_value', '$motor_3_value', '$motor_4_value', '$motor_5_value', '$motor_6_value');";

    if ($conn->query($sql) === TRUE) {
    echo "New record created successfully";
    } else {
    echo "Error: " . $sql . "<br>" . $conn->error;
    }
`

The connection variable `$conn` has been passed to avoid many problems that appeared

# Response page
The benefit of it is to show what was last done on the site by reading from the database

In this line, access to the database to read after fetch the resulting rows as an array with specific rows
`echo $direction_commands[count($direction_commands)-1]['date'];`


# Future work
One of the additions to the site is to link the play button to communicate with the robot and to add a more beautiful form, use the JavaScript language to draw the movements of the six motors and the direction such as through canvas

Soon, God willing, the next task I will do this program, but for Windows devices via the C# language, to learn more about dealing with these matters in an actual project, if it is published it will be in this repository 🔜



# Steps to create a database:

1 - Create a database with 10 rows which is the number of buttons (date and time increased later) . This was created via a program XAMPP From the databases and control panel availability feature phpMyAdmin

![much-a image](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/blob/main/Control%20panel%20for%20robot%20arm%20with%20database/Steps/1%20Create%20a%20database.png) 

2- Then add names, type, and size to each element, like motors, by designing them in the web via HTML, the section space that will be stored from 1 to 100 was added to this size

![much-a image](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/blob/main/Control%20panel%20for%20robot%20arm%20with%20database/Steps/2%20Add%20items%20and%20attributes%20to%20the%20database.png) 


3  - The need to use the date arose, so it was added at the beginning with ease and it was also easy to modify one line in a function that was done to achieve the principle of DRY to modify the writing line of the database

![much-a image](https://github.com/MohammadYAmmar/Robot-arm-with-a-camera/blob/main/Control%20panel%20for%20robot%20arm%20with%20database/Steps/3%20easy%20modify%20with%20new%20function.png) 
