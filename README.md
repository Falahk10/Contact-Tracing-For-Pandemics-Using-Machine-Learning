# Contact-Tracing-with-Machine-Learning
This is a contact tracing program that utilizes machine learning, enabling governments or local agencies to efficiently track individuals in situations like COVID-19 or for security purposes. By applying machine learning clustering techniques, this code helps identify how many people have come into contact with a specific individual.

# Getting Started
To use this code, you must have Python installed along with the following libraries:

numpy
pandas
seaborn
matplotlib
datetime
sklearn
Additionally, a JSON file named "livedata.json" containing people's location data is required as input.

Code Structure:
Importing Libraries: The code begins by importing the necessary libraries and setting up a visualization environment.

Data Loading: It reads the "livedata.json" file and stores the data in a pandas DataFrame named df.

Data Cleaning: Null values in the dataset are checked and handled.

Visualization: A scatter plot is created using latitude and longitude, with points colored based on each person’s unique "id".

Contact Detection: The DBSCAN clustering algorithm is used to identify individuals who have been within close proximity (6 feet) of each other based on their location data.

Contact Function: A function, get_infected_name(), is defined to take a person’s name as input and return a list of individuals who were in contact with them.

Output: The function is called with the input name "Bob," and it outputs that "Judy had come in contact with the patient."

### This output dashboard visualizes the machine learning algorithm's results, where individuals are tracked by forming clusters based on a specified radius.
<div align="center">
    <a href="./">
        <img src="https://user-images.githubusercontent.com/68246393/144760224-57cd18b6-701a-4ab4-98a6-5db1f5f542b0.png" width="59%"/>
    </a>
</div> <br>

The output consists of a scatter plot displaying individuals' latitude and longitude, with their IDs labeled on the graph. Additionally, the function outputs the names of people who came into contact with the patient.

Conclusion:
This code is beneficial for government or local agencies in scenarios like COVID-19 or for security purposes. It can be customized to incorporate different location data or to adjust DBSCAN parameters for specific needs. The program effectively identifies individuals who interacted with a specific person, aiding in efficient contact tracing.<br> 


<div align="center">
    <a href="./">
        <img src="https://user-images.githubusercontent.com/68246393/213873513-d87731aa-e75e-4cb3-9889-54ef4b968e25.png" width="59%"/>
    </a>
</div> <br>

### In the output, the scatter plot reveals a cluster containing only two individuals. When "Bob" is entered as the patient, the program identifies "Judy" as a person who came into contact with him.
