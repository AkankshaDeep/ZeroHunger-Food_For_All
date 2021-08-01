Food_For_All
============

Solution for Zero hunger

### About

In the words of John F. Kennedy, the war against hunger is truly mankind's war against liberation. Today, the total food produced in the world is enough to feed 10 billion people. The current world population is around 8 billion even then approximately 800 million i.e 10% of the people on this planet are still hungry. This proves that the cause of hunger is not food scarcity but the inefficient distribution and wastage of food. According to UN approximately 1.3 billion tons i.e 30-40% of the total food produced is wasted every year. It is clear that social inequalities, which give rise to excesses and insufficiencies in supply, distribution, and availability of food and essential nutrients.

Our solution is to create a technology-based ecosystem to quickly map people in need and food sources to help efficiently distribute food and prevent food from wastage. 'Food For All' is an application where food receiver/donor will be able to log a request regarding their food need or extra food available for donation via a phone call. Once the request is placed, the system will process data to connect the receiver with a donor based on various parameters like location, quantity available/required, etc. 

Our application has two major entities: Donor & Receiver
Donor: Any individual, household, restaurant, event manager, store, industries, retailers and consumers, etc who has an extra meal and wants to give it to someone in need. 
Receiver: Any person in need of food, requesting for themself or on behalf of someone else(who doesn't have access to a phone) in need.

### Flow

![image](https://user-images.githubusercontent.com/88237381/127761965-4b5f7343-a919-48c4-92b1-2216c6a93944.png)


1. The User(donor/receiver) makes a call to the Tollfree number to register their request.
2.  We use the Text to speech +Watson Services to create an audio chatbot and Speech to Text +Natural Language Processing services to log the request.
3. Once the request is received, the Request Processing Service of the application makes a call to the Maps API to get the required location data. This  
   service then extracts the attributes like request type: donor/receiver, address, pin code, Quantity, etc to create a query.
4. The query then inserts all acquired data into the database.
5. Once the data has been successfully saved in the database, the Request Processing Service sends back a confirmation message.
6. For the user, who was of type 'receiver', the message includes the address of the nearest food donor where food is currently available. For users who were        of type 'donor,' the message includes a confirmation and appreciation note.

The mapping of the donor with a receiver is done by deploying AI-based data processing based on various factors like the quantity of food required by the receiver, quantity of food available with the donors, location of donor and receiver, etc.
In the above flow, as soon the system receives a request for food from a 'receiver' the system selects an appropriate and available food donor and maps it to the 'receiver' and sends the response back immediately with donor information.

However, if there were no available donors in the system at the time the request was logged by 'receiver', the system sends just a request acceptance message. When a donor becomes available the application sends another message to the receiver whose request was previously unfulfilled with information about the location of the food donor. 

The application also has the feature which notifies the previously registered donors requesting to donate food if possible when the number of requesters is quite high and very few or no donor is currently available. 
    

### Scope of Uses

The current application hopes to reduce hunger by making food that would otherwise be thrown, expired or wasted, available to people in immediate need of food. However, in future, the current application may be expanded to help NGOs, Food banks, or other individuals & organizations working towards 'Zero Hunger' to easily find out the location of people in need as well as entities who can provide food. The AI-based data processing model of the application can also help analyze the data collected to get important insights like when food need is maximum when food supply is maximum, reasons for the fluctuations, how to properly manage the supply and demand, etc. It can also provide useful suggestions and point towards factors that need to be minimized to achieve our goal of 'Zero Hunger'.



### Watch The Video

https://youtu.be/PrPXB8swbPU

### Pre-requisites
IBM Cloud account: Create an IBM Cloud account.





