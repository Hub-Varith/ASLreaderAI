# ASLreaderAI
An American Sign language (ASL) learning platform by using AssemblyAI to perform a speech-to-text translation on microphone input and we use that text to display translated ASL hand signs of those words, alongside results of an emotion detecting ML model, created by Flask.
Here's the link to the ML model Repo: https://github.com/Hub-Varith/als-emotion-ai-api

You can try out the live demo at: https://joe9go.github.io/ASLreaderAI/

## Inspiration
We wanted to provide an easy-to-use tool for purposes such as learning ASL or translating from audio to a form an ASL speaker can better understand.

## What it does
The tool allows one to record their voice or other audio sources, and once one stops recording, it will use AssemblyAI's API to generate a transcript of that recording. It then displays ASL hand signs along with that transcript, with the option to cycle between 3 different dictionaries of interpreters. It also performs an ML-based sentiment analysis to predict what emotions were felt by the speaker.

## How we built it
The audio input and connection to the AssemblyAI API were done through javascript. The text received from the AssemblyAI API will be sent to the sentiment analysis API, built by flask, hosted by Heroku.

## Challenges we ran into
Connecting the various resources we had together was the main challenge. It would have been simpler with each part separated: a "record and save your voice" button, an "upload your voice to AssemblyAI" button, some links that say "click here to go to someone's ASL dictionary site" and "click here to try out a sentiment analysis AI". It was quite a tedious set up communication between these different systems, exacerbated by the short deadline and made worse still by the time zone disparities within our team. I don't think there was so much as an hour when all 4 of us were talking together. For sentiment analysis, we've run into overfitting problems and an imbalanced dataset which lots of times had been wasted. However, we managed to clean up the dataset and boost up the accuracy to >83%.

## Accomplishments that we're proud of
The pride of an accomplishment goes hand-in-hand with its difficulty. We managed to bring all the features that challenged us together into a single page. It significantly reduces the hassle for a user compared to what there would be without putting in the effort to streamline those features.

## What we learned
Theo: I came into this without having used javascript before, so that was a learning experience for me. While working on it, using the AssemblyAI API seemed difficult, but in retrospect, I was able to get it working within a few hours of work, and in a programming language I hadn't used before at that.

Alex: I discovered that web development is actually really cool and rewarding to do. I thought it would be a bore, but seeing it work in the end: using our product felt great!

Hub: I've never hosted a rest API on the cloud before and had little experience with NLP. However, I managed to train the NLP model in time and host it.

Zeaan: I worked on the frontend of the website and helped on hosting the flask sentiment analysis api, and built on my past experience with those to explore new options.

What's next for ASL Speech to Text
Create our own dataset of hearing-impaired people signing and implement grammar in the algorithm.

Improve sentiment analysis model to multi-class classification which includes anger, happy, sad, etc.
