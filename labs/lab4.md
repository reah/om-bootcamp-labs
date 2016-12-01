# The Final Stretch

![Dog](http://i.giphy.com/fJdpdS5jaDje8.gif)

You are now all ready to make your first app! As outlined in yesterday's lecture, you will be making a dating app to match you to your celebrity soulmate based on the Watson Personality API.

Here is the *end-to-end workflow* for a user of this application:

1. Ginni wants to know who her celebrity soulmate is so she heads over to our website, www.celebritysoulmate.com (unfortunately, we won't actually be getting a domain name for this exercise).
2. She will see a home-page full of celebrity photos and she will be able to click on each of them to see their top personality traits. This interactive page grabs her attention and she decides to proceed onwards.
3. The next page she sees is a quiz. Each personality trait on the quiz is accompanied by a slider that goes from 0-10. The slider is used so that Ginni can determine how much of that personality trait applies to her. For example, Ginni would probably give herself a 10 for leadership.
4. After filling out the quiz, Ginni presses submit and the next page she sees is her top 10 celebrity matches.
5. Ginni then laughs, shares it on Facebook, decides to invest in the app, and makes you a billionaire by the age of 26.
6. You, with a sudden influx of money and little to no capacity to adjust to such levels of opulence, succumb to poor financial decisions.
7. After buying a Ferrari because "you have to go to Walgreens in style", a private island because "your neighbors get kinda loud", and several high-end clubs because "you're a billionaire and don't want to wait in line", you realize you are in desperate need of a stimulus package of sorts in order to maintain the standard of living you have elevated yourself into.
8. Plauged by the inability to produce even a semblance of a fiscal plan, you decide to liquidate the assets you possess. Unfortunately you painted all your exotic cars in hot pink and filled the back-seats with Jello because "you can lmao". The resale value plummets on top of the already accumulated loss by virtue of depreciation.
9. You realize that this dating app you created and this bootcamp is the reason for all your grievances. As you fall asleep, you vow to avenge yourself by marring the reputations of Reah, Anand, and Ginni.
10. Then you wake up and realize none of this happened haha idk why you're still reading this lmaoooo we have literally so much work to do hahaha yall OMs are crazy :joy:

![South Park](http://i.giphy.com/l0HlwgLWLYSbYA0OA.gif)

# Running the App

1. Download a ZIP from [here](https://drive.google.com/open?id=0B3ZWKY61mrenOWFxLWVrV0p2RXc). This file contains helpful files for the project.
2. Move the ZIP to Desktop/bootcamp.
3. Double click on the ZIP to extract its contents. You should see a folder called `watson-dating`.
4. Open Terminal and type `cd ~/Desktop/bootcamp/watson-dating`
5. Terminal implements tabs just like browsers. Press `command+t` twice to open two new tabs. One of these tabs will run the *front-end*, one will run the *back-end*, and the last one will be a spare in case you want to test something on Python.
6. In the first tab type
```
cd front-end
npm i
``` 
This is using a type of Javascript called Node.js. `npm` stands for "Node Package Manager". `npm i` is telling the Node Package Manager to install everything it needs to in order to run the front-end of our app. You only ever have to type this once, so if the app ever crashes, you don't need to run this command again. To start running the front-end server, type `npm start`.
```
npm start
```

In the second tab type the following:
```
cd api
pip install flask
pip install flask-cors
pip install python-twitter
```
These commands help install the packages Python needs in order to run our back-end API. To actually start running the back-end server, type
```
python app.py
```
*As a reminder, the front-end of the app contains all the things users actually see and interact with. The front-end is generally kept minimal with focus on presentability and speed. The back-end of the app does all the hard work and logic. The front-end and the back-end are in constant communication as information goes to and fro. In general, back-ends are accessed through APIs. Here, we have written our own little API for our front-end to talk to.*

Go to [http://localhost:8080/](http://localhost:8080/) to access the front-end. Things don't exactly work but that's because there are huge gaps right now in our code base that you get to fill in!!! Turn up!!!!

# Lab Work

![Work](http://i.giphy.com/ZKZiW6GSx8eSA.gif)

In Sublime, open Desktop/bootcamp/back-end/logic.py. `logic.py` is a template for you to write your code into. See all the `import` statements at the top? Like we did in the last lab, Python has a great feature wherein it can invoke functions from other packages.

In the same way, there are a couple of files that have `import logic` at the top of them and they are invoking the functions that you have to write in this file.

Open the file and follow the instructions in the comments. Good luck!