vk.com community members sex and age distribution (population pyramid)
Script for obtaining a graph and data on the distribution of VK community members by gender and age (Age-sex pyramid)

Example:



Launch
Install packages fromrequirements.txt
Replace templates secret.jsonwith your login and password
Enter a short link to the community or user in the TARGET variable
Launch
The data and graph will be saved in the same directory in a folder of the same name as TARGET
Note: Yes, entering your username and password is not the best method, but it is the easiest. You can analyze my code and the vk-api code yourself to make sure they are safe. If you want to implement the Implicit Flow authorization method, then I am ready to cooperate.

Functions
The class is divided into 4 main functions:

get_members_ids - gets the ids of all community members or friends of the user

get_users_data - gets data about the age and gender of these ids

Because VK has a limit on the number of API method calls per day. It will be possible to analyze communities with a huge number of users no more than a couple of times a day. Therefore, to save requests, data about participant ids and additional fields are saved as json in the same folder. After saving the data, I recommend turning off the get_members_ids and get_users_data calls

calculate - calculates various parameters about users, change at your discretion
make_plot - builds a histogram of distribution by gender and age
A short link to the community or user id is suitable as a TARGET. Don't forget to change type group_members / user_friends
