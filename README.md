# Webex poll creators
___________________

Webex has a rudimentary polling system built into it. It's ok, but not great, and requires you to be *in a meeting to create a poll* which is madness.

This is a repo with some tools for creating poll files (`.atp` but really just XML) before meetings (or in my case, classes).

These are all just plain web pages where everything runs client side. You put in some options, hit save, and the embedded JS gives you a poll file you can open with Webex next time you have a meeting. The aim was to be self-contained and be able to run anywhere without installing anything.

## Generic poll creator (`index.html`)
This lets you just create generic polls with most of the options available.

## Exit poll creator (`topic_check.html`)
This creator is specifically for presenting the same multi choice options for a series of questions. My use case is for exit polls for classes ("How well did you understand topic X" style questions - to get a vibe check for how a class went).

# Things to note
- There's a `CORRECT` attribute in the answer field, but Webex doesn't seem to do anything with this. I kept it in because maybe it will do something one day.
- Webex activity reports will save poll results, so don't feel like you need to save the poll results web page that Webex gives you a link to (although it is nicer to look at than the CSV file of poll results)
- I *think* the 'no answer' attribute for the poll just lets people finish the poll without responding to a question?
- Showing results of multi-choice and multi-select during meetings is fine, but short answers just aren't displayed nicely. Nothing to do with this tool, just an FYI if you want to give respondents an idea of what is entered in the poll during the meeting.

Overall I couldn't find any documentation of the format or options anywhere, and anyone serious about polling in Webex will probably just use one of the apps from the polling and surveying ecosystem (if your institution lets you do that).