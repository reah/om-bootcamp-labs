# Day Three

![Computer](http://i.giphy.com/acj7QJGgBBeUg.gif)

## APIs
APIs are the reason why people don't need to reinvent the wheel everytime they decide to make an app. APIs *expose* functions for us to be able to use the services of another company.

### Examples of APIs
[Twitter API](https://dev.twitter.com/rest/tools/console)

[Google Maps API](https://developers.google.com/maps/documentation/javascript/examples/map-simple)

[IBM Watson Personality Insights](https://personality-insights-livedemo.mybluemix.net/)

Make sure you check out that last one because it's what we're going to be using for the next few days.

## Getting Started with the IBM Watson API
### Credentials
In order to use any API service, you first have to acquire credentials that identify who you are and what your purpose is.

1) Go to Bluemix at https://bluemix.net

![Homepage](../resources/1.png)

2) Log-in with your IBM credentials

![Credentials](../resources/2.png)

3) Scroll down to the bottom of the page where you see services and select "Create Service"

![Create Service](../resources/4.png)

4) Search for "personality insights" and select the Watson service that appears below

![Personality Insights](../resources/6.png)

5) Name your service and credentials and press "Create"

![Naming](../resources/8.png)

6) In the Personality Insights page, select the "Service Credentials" tab

![Service Credentials](../resources/10.png)

You've just created a set of credentials for yourself in order to use IBM Watson's API! These credentials are meant to be private. You should never share these credentials with anyone.

## SDKs
SDKs give you all the tools you need in order to easily run APIs. If APIs are pieces of wood, SDKs are hammers, nails, rulers, and saws.

### Installing Watson SDK for Python
Go into terminal and type `sudo pip install watson-developer-cloud`. This will prompt you for a password, type in the password to your Mac computer.

If this shows an error, it means that `pip` hasn't been installed yet. Run `sudo easy_install pip` and then after that completes, run the command above again and it should work.

# Let's Get Down to Business

![Mulan](http://i.giphy.com/k3wPtPBEt6kq4.gif)

1) Find a large body of work you'd like to run personality insights on. There are some cool examples on [this website](http://www.americanrhetoric.com/top100speechesall.html). The longer the speech, the better!

2) Open a new Sublime file, copy and paste the speech inside it, and save it as `speech.txt` within Desktop/bootcamp.

3) Open a new Sublime file, go to the bottom right where it says "Plain Text" and select "Python". This is us telling Sublime that we will now be working on a Python file.

4) Copy the following into your Python file:
```
speech = open('speech.txt').read()
print speech
```
As you might be able to tell, this opens our speech text file and reads it into a variable named `speech` and then prints it.

5) Save this file as `lab3.py` in Desktop/bootcamp and run it in Terminal just to ensure that it works as expected (you should see a huge speech print out).

*As a reminder, you must first type `cd ~/Desktop/bootcamp` to get terminal in the right place to run the Python code and then `python lab3.py`*