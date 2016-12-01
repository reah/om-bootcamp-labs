# The Final Stretch (Forreal This Time)

![Running](http://i.giphy.com/uOd62IKsc4Ffq.gif)

## Corrections
There are two misakes that have to be corrected in `insight.py`.

Change line 11 to be 
```
return trait.lower().replace(' ','_').replace('-', '_')
```

Change line 16 to be
```
for key, value in insights_dict.iteritems():
```

Sorry about that!

## JSONs SUCK
...so I will be providing you with the code to parse the personality insights.
```
def personality_insights_dict(insights):
    result = {}

    overall_traits = insights['tree']['children']
    big_five = overall_traits[0]['children'][0]['children']
    needs = overall_traits[1]['children'][0]['children']
    values = overall_traits[2]['children'][0]['children']

    for i in big_five:
        result[i['name']] = float(i['percentage'])
        for j in i['children']:
            result[j['name']] = float(j['percentage'])

    for i in needs:
        result[i['name']] = float(i['percentage'])

    for i in values:
        result[i['name']] = float(i['percentage'])

    return result
```

Now, with this, finish the lab from yesterday.

# After You Are Done
Congratulations! You're done!

You've successfully acquired 2 API credentials, used both of them, and now have some insights! Here's a round of applause
:clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap::clap:

Now you have 5 users. We have ammassed for you a sizeable database of tweets and their insights. It took a couple of hours to run this code so, in the interest of time, we have done it for you. We put everything together into a JSON file that has this model:
```
{
    {
        "insights": {
            "love": VALUE,
            "modesty": VALUE,
            "assertiveness": VALUE,
            "conscientiousness": VALUE,
            "adventurousness": VALUE,
            "gregariousness": VALUE,
            "stability": VALUE,
            "imagination": VALUE,
            "artistic_interests": VALUE,
            "anger": VALUE,
            "openness": VALUE,
            "trust": VALUE,
            "cautiousness": VALUE,
            "intellect": VALUE,
            "depression": VALUE,
            "achievement_striving": VALUE,
            "extraversion": VALUE,
            "liberty": VALUE,
            "cheerfulness": VALUE,
            "ideal": VALUE,
            "conservation": VALUE,
            "agreeableness": VALUE,
            "dutifulness": VALUE,
            "cooperation": VALUE,
            "orderliness": VALUE,
            "harmony": VALUE,
            "immoderation": VALUE,
            "openness_to_change": VALUE,
            "liberalism": VALUE,
            "self_discipline": VALUE,
            "closeness": VALUE,
            "emotional_range": VALUE,
            "anxiety": VALUE,
            "curiosity": VALUE,
            "hedonism": VALUE,
            "altruism": VALUE,
            "structure": VALUE,
            "morality": VALUE,
            "practicality": VALUE,
            "self_expression": VALUE,
            "sympathy": VALUE,
            "emotionality": VALUE,
            "friendliness": VALUE,
            "challenge": VALUE,
            "vulnerability": VALUE,
            "self_enhancement": VALUE,
            "excitement": VALUE,
            "excitement_seeking": VALUE,
            "activity_level": VALUE,
            "self_consciousness": VALUE,
            "self_efficacy": VALUE,
            "self_transcendence": VALUE
        },
        "screen_name": "SCREEN_NAME",
        "profile_url": "TWITTER_PROFILE_PIC_LINK",
        "name": "TWITTER_NAME"
    }
}
```

Download the ZIP folder from [here](https://drive.google.com/open?id=0B3ZWKY61mrenMGdXVE9sN0dCUjQ) into Desktop/bootcamp/watson-dating/back-end. Extract the ZIP folder by double clicking it. You should now have a folder called "userinfo" within Desktop/bootcamp/back-end

Now for the last step. Look at all the personality traits above and choose 10-20 traits that *you* think are most important when discussing compatibility (reccommended number, you can do as little as 1 trait or as many as all 56). 

Open Desktop/bootcamp/watson-dating/front-end/src/components/Quiz/Quiz.js with Sublime. Input those traits you selected into line 9. There are already some traits in an array but these are just the default traits we put there. Feel free to overwrite them or add to them. Note that you must type the traits exactly as they appear above otherwise the app won't work.

# Let's Find Your Match!

![Match](http://i.giphy.com/ikXcqqlSNH2Mw.gif)

Open two tabs like we did in the last lab in Terminal.

In the first tab type
```
cd ~/Desktop/bootcamp/watson-dating/front-end
npm start
```

In the second tab type
```
cd ~/Desktop/bootcamp/watson-dating/api
python app.py
```

Give each about 5 seconds to start up and navigate to http://localhost:8080/ and your app should be fully up and running! If on the home screen you don't see any pictures, then you might have to restart the back-end app. Don't fret, for some reason the code breaks sometimes. In that tab, type `control + z` to end Python and then type `python app.py` again to restart the back-end server.

Go through the app and see who you end up matching with!

# Congratulations!

![Congrats](http://i.giphy.com/RzFvuuV4zBhF6.gif)

In this course you have learned Python syntax, data structures, conditionals, loops, file operations, debugging, script usage, API usage, web architecture, and so much more! I hope we have been able to foster a little *crush* on programming for you that will maybe someday evolve into *true love*.

Thank you guys and good luck!

\- Anand & Reah