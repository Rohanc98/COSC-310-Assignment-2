Please note:

I had a phone talk with Dr. Narayan on April 5th, and I explained him that I did not know how to implent an API in my code or how to use sockets (I was never really taught what an API, in the same fashion, I did not know what to write for the documentation part about APIs). He said he would have a look at my assignment, and asked me to describe what role I played in Assignment 2, the group part:

In A2, I played the following role: though my group-mate changed a lot of the code afterwarrd, I wrote a functional algorithm of sentences recognition and matching with a response. (the one with the 3 for loops in the Bot class). For this individual assignment (#3), I actually changed this code back to what I had (I think it works a bit better). Therefore, I was very actively involved in coming up with the algorithm and data structure that the program uses with this other group mate. Him and I were the 2 people in the team who came up with the main algorithm, though the other two team members did some crucial tasks and participated greatly as well (on different parts of the assignment). I also wrote almost all of the keywords and answers to the bot in the 2D array. In addition, I was a key element in leading the team, delegating different roles to my different team mates and communicating with them on Messenger and organizing the team and ensuring its efficient cooperation. 

Dear Dr. Narayan, dear TA, I appreciate your help and understanding. 

Sincerely.




Class Structure

Main Class:
-Main(): This method intializes the Bot and sets all needed variables for it.
    It also asks the user for input and then passes it to the Bot to pattern match.

Bot Class:
-Bot(name): initializing method, sets name of bot
-createResponseList(list): Initializes and sets the keys and responses list
-getSpecial(match,input): this method returns any special cases of responses
    that require additional conditions and variables
-getWeather(city): this method builds a string for the weather information
    of a given city
-getName(): this method returns the name of the bot
-getResponse(input): this method does the pattern matching and input checking.
    If there are any special input matches it calls getSpecial().

Weather Class: Gather weather information of a city
-weather(location): Initialize Weather Class and perform a GET request to open weather API
-getTemp(): return the temperature of the city
-getWeatherMain(): return the main description of the weather
-getWeatherDesc(): this method returns a more thorough description of the city's weather
-setWeatherInfo(): this method processes parse the given JSON and sets the weather information fields
-setTemp(): parse given JSON and gets the weather temperature

SpellCheck class : Perform a spelling check on a sentence
-SpellCheck(): Constructor for class and call setNewSentence method
-setNewSentence(sentence): set new sentence for the class and call process method
-process(): process the given sentence and set fixed sentence member field with the corrected sentence (if any)
-getCorrectedSentence(): returns the corrected sentence
-getRawSentence(): returns the unprocessed sentence, if needed
