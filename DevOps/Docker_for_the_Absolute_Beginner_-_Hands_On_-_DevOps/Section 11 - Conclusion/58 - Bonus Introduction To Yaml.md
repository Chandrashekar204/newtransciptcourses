# Bonus Introduction To Yaml

*Section: Conclusion*

1 In this lecture, we take a look at what YAML files are. 2 If you are familiar with YAML already, feel free to skip this section and head over to the next one. 3 If you have not worked with YAML in the past, I would highly recommend going through this 4 because the rest of the course depends on YAML. 5 Docker Compose files, for instance, are written in YAML. 6 Configuration files like Docker Compose files are text files written in a particular format called YAML.

7 Say, if you have worked with other data structure formats like XML or JSON, you should be able 8 to easily pick it up. 9 Don't worry, if you haven't worked with any of these, you should still be able to easily 10 pick it up by going through the examples that follow. 11 A YAML file is used to represent data, in this case, configuration data. 12 Here is a quick comparison of the same sample data in three different formats.

13 On the left, we have XML, where we display a list of servers and their information. 14 The same data is represented in JSON format in the middle, and finally in YAML format on the right. 15 Take a minute to compare the three formats and notice how YAML uses far less punctuation 16 than the others. 17 Let's take a closer look at YAML. 18 If you take data in its simplest form, a key-value pair, this is how you would define it in YAML.

19 Key, then a colon, then the value. 20 The keys here are fruit, vegetable, liquid, and meat. 21 And the values are apple, carrot, water, and chicken. 22 Remember, you must have a space following the colon that separates the key and the value. 23 Now let's take a look at how an array is represented. 24 Say we would like to list some fruits and vegetables. 25 We would write fruits followed by a colon, then on the next line, enter each item with 26 a dash in the front.

27 That dash indicates the line is an element of an array. 28 How about a dictionary? 29 A dictionary is a set of properties grouped together under an item. 30 Here we represent the nutrition information of two fruits. 31 The calories, fat, and carbs are different for each fruit. 32 Notice the blank space before each item. 33 You must have an equal number of blank spaces before the properties of a single item so 34 they are all aligned together.

35 Let's take a closer look at spaces in YAML because this is where things go wrong most often. 36 Let's say we have a dictionary representing the nutrition information of a banana, the 37 total calories, fat, and carbs. 38 Notice the number of spaces before each property. 39 That indentation tells YAML that those key value pairs fall within banana. 40 What if we accidentally added extra spaces in front of fat and carbs?

41 Then they would fall under calories and become properties of calories, which doesn't make any sense. 42 This will result in a syntax error that tells you mapping values are not allowed here because 43 calories already has a value set, 105. 44 You can either set a direct value or a dictionary under a key. 45 You cannot have both. 46 The number of spaces before each property is key in YAML and you must make sure they 47 are right to represent your data correctly.

48 And don't mix tabs and spaces. 49 Pick one, usually two spaces, and stick to it. 50 Let's take it to another level. 51 You can have lists containing dictionaries containing lists. 52 In this case, I have a list of fruits. 53 The elements of the list are banana and grape, but each of those elements is itself a dictionary 54 containing nutrition information. 55 A lot of students new to YAML have asked when to use a dictionary versus a list.

56 Let me explain that. 57 First, it is important to understand that XML, JSON, and YAML are all just ways to represent data. 58 The data could be about an organization and all of its employees and their personal details, 59 or it could be data about a school and all of its students and their grades, or it could 60 be data about an automobile manufacturing company and all of its cars. 61 It could be anything.

62 Let's take an example of a car. 63 A car is a single object and it has properties such as color, model, transmission, and price. 64 To store different properties of a single object, we use a dictionary. 65 In this simple dictionary, I have the properties of the car defined in a key value format. 66 This need not be as simple as that. 67 For example, if we need to split the model further into a model name and a make year, 68 we could represent this as a dictionary within another dictionary.

69 The single value of model is now replaced by a small dictionary with two properties, name and year. 70 Now, let's say we would like to store the names of six cars. 71 The names are formed by the color and the model. 72 To store these, we would use a list or an array since these are multiple items of the 73 same type of object. 74 Since we are only storing the names, we have a simple list of strings.

75 What if we wanted to store all the information about each car, color, model, transmission, and price? 76 We would then change the array from a list of strings to a list of dictionaries. 77 We expand each item in the array and replace the name with the dictionary we built earlier. 78 This way, we can represent all the information about multiple cars in a single YAML file 79 using a list of dictionaries.

80 That's the difference between a dictionary, a list, and a list of dictionaries. 81 Before we wrap up, let's take a look at some key notes. 82 A dictionary is an unordered collection, whereas a list is an ordered collection. 83 What does that mean? 84 The two dictionaries you see here have the same properties for a banana. 85 However, the order of the properties, fat and carbs, does not match. 86 In the first dictionary, fat is defined before carbs.

87 In the second, carbs comes before fat. 88 But that doesn't really matter. 89 The properties can be defined in any order, and the two dictionaries will still be the 90 same as long as the values of each property match. 91 This is not the same for lists. 92 Arrays are ordered collections, so the order of items matters. 93 The two lists shown below are not the same, because apple and banana are at different positions.

94 This is something to keep in mind while working with these data structures. 95 Also remember that any line beginning with a hash is automatically ignored and considered a comment. 96 That's the YAML primer. 97 We're now ready to head over to the exercises and have fun playing with YAML files.
