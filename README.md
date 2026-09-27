[Akan_Name_Generator_README.md](https://github.com/user-attachments/files/32699780/Akan_Name_Generator_README.md)

Akan Name Generator: 
A lightweight Python script that calculates a person's traditional Ghanaian Akan day name (kra-din) based on their date of birth and gender.

Features

 Automatically determines the day of the week from a given date.
 Maps the day to the correct traditional male or female Akan name.
 Handles case-insensitive gender inputs (e.g., "MALE", "Female", "male").
 Includes error handling for invalid dates and gender formats.
 
Prerequisites

 Python 3.x
 No external libraries required (uses Python's built-in ⁠datetime⁠ module).
 
 Installation

 1.Download the Python file (e.g., ⁠akan_names.py⁠) to your local machine, or clone the repository if you are using Git:
 git clone https://github.com/yourusername/akan-name-generator.git

 2.Open your terminal or command prompt and navigate to the folder where the file is saved.

 3.You can now run the script directly or import it into your own projects.

 Usage

 Simply import the ⁠AkanNameGenerator⁠ class and call the ⁠get_name⁠ method with a date of birth (⁠YYYY-MM-DD⁠) and a gender (⁠Male⁠ or ⁠Female⁠).

 Example Code

 from datetime import datetime
# (Assuming the AkanNameGenerator class is defined in your current directory)

   # Example 1: Male
   
try:


    result_male = AkanNameGenerator.get_name("2007-09-20", "MALE")
    print(f"Result: {result_male['akan_name']} (Born on {result_male['day_of_week']})")

   # Example 2: Female
    result_female = AkanNameGenerator.get_name("2007-09-20", "FEMALE")
    print(f"Result: {result_female['akan_name']} (Born on {result_female['day_of_week']})")

    except ValueError as e:
    print(f"Invalid input: {e}")

  Expected Output
 
    Result: Yaw (Born on Thursday)
    Result: Yaa (Born on Thursday)

  Returns
  
The ⁠get_name⁠ method returns a dictionary containing:
 ⁠date_of_birth⁠: The original date string provided.
 ⁠day_of_week⁠: The calculated day of the week.
 ⁠gender⁠: The normalized gender string.
 ⁠akan_name⁠: The generated traditional name.
