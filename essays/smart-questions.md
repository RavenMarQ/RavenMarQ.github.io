---
layout: essay
type: essay
title: "Stupid Questions Beget Stupid Consequences"
# All dates must be YYYY-MM-DD format!
date: 2023-12-22
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

## Brief Overview

As per usual, if you want a TL;DR: here it is!

This essay is on the longer side, not because of what I say but, because I've included questions and answers from StackOverflow here (for your viewing pleasure). Besides that: in the online world, if you've had any amount of experience in how people act online, you know that people are selective in what they find interest in and how terse and standoffish many seem. That's why one has to ask smart questions whenever asking online and ensuring that your question comes from a place of exhausted options instead of first choice.

In the following essay, I will use the acronyms "RTFM" and "STFW" which mean "read the f*cking manual" and "search the f*cking web" respectively. 

## An Intro to Question-Asking Etiquette and Smart Questions

When seeking the advice from tech gurus, wizards, and [hackers](http://www.catb.org/~esr/faqs/hacker-howto.html) (essentially the Jedi council of the coding world) online, there are some steps and guidelines in which helps you come off less like an idiot and more like a fledgling who shows promise and can learn.

Terse, flaming, even cold: when asking a question anywhere, it's best that your question invokes a challenge that doesn't come off as a job. Note that most, if not all, of what I have and will say is derived from [here by Eric Raymond](http://www.catb.org/esr/faqs/smart-questions.html) (with a sprinkling of my own experiences).

### Before you decide to ask the council...

Here are *some* of the guidelines **BEFORE** posting a question:

1) Do your own research! (Manuals, searching the web, or even searching the forums for questions that might relate to your own)
2) Take some time to solve it yourself. Approach it from different angles if need be. Don't be stuck trying to do X with Y. Instead, think of how to do X with methods *OTHER* than Y.
3) Ensure that your question is relevant to the forum you are posting it to: if there are no ReadMes or some sort of "purpose"-esque page/section, then you can infer from the questions posted to said forum.

The first point ensures you don't get hit with the dreaded STFW and RTFM responses, which tend to be sarcastic, condescending, and especially degrading. I personally have taken note to do this myself, considering that I hated talking to my professors/teachers growing up, so I have experience finding it myself before asking for help.

The second point is to help you build substance and some sort of "repertoire" for your question to show that you've tried to overcome and how many ways you've approached your question. During this point one usually gains insights and understanding that also might circumvent the necessity of asking the question.

The third point is just courtesy and ensures that you don't get banned, your post taken down, or something similar due to irrelevance (or the fact that you're asking a question about GPUs in a Python coding thread).

The first and second points especially are important for making a good smart question, as these steps are actually things that problem solvers and competents. This sense of competency and work attempted makes hackers and such more likely to answer your question more thoroughly, nicely, or even at all. Many times, many people appreciate someone who deigns to reduce the time they waste asking someone to solve or give a hint/explanation about their problem.

### Asking the question

When asking your question, try to be specific. Don't plop on everything in your project and related items into your post: instead, chop down everything that doesn't affect your specific question until you get as small as you can. This is made easier if you followed the first two points I provided, as trying to solve a problem first comes from actually finding the specific problem.

Another important point is to be professional: grammar, spelling, and politeness. If you come off as professional, you come off as easy to teach. 

(If you don't speak the main language of the forum well, note that you do not speak the language in the post)

Finally: ***DON'T ASK FOR THE ANSWER***

Seriously: you open your question to better explanations and answers if you don't ask specifics like: "I'm trying to do X with Y" or "Does X happen if Y?"

Most of the time, this will also elicit STFW and RTFM responses, as it seems like you didn't do any research or tried to solve it yourself (even if you did).

(A related point is to make your question worded well-enough that people with similar issues can stumble upon your post)

With these in mind, make sure that you also explain what you've done beforehand and your logical reasoning so that you don't get answers that you've attempted before.

### Quickly before the next section

The link I provided at the beginning of this section actually is sufficient for explaining the dos-and-don'ts, but I will show threads here just to delve into tangible examples of smart and not-so smart questions. The reason why I've provided explanations here is so that I don't have to repeat myself over and over again when I am trying to make a point: 

***All of my points have been outlined!***

For the following example StackOverflow forum posts, I sorted by score and chose the top-most and the (close to) bottom-most posts. I will also add comments using brackets "[Insert Snarky Comment]" just to clue you in on things, let you know something, or to note what I'm skipping (for essay's length's-sake). I will also provide a link somewhere within the section to view the post.

## Here's what you should do!

StackOverflow is a good site for developers to ask questions and find answers, and that is where we will be finding our example of forum questions!

In the following example, I present the top-scored post with many good answers and an excellent example of how to ask your question: even when your question seems as menial as:

```
Q: Why is processing a sorted array faster than processing an unsorted array?

In this C++ code, sorting the data (before the timed region) makes the primary loop ~6x faster:

[Provides .cpp code here, relevant code:]
    int main()
    {
        // Generate data
        const unsigned arraySize = 32768;
        int data[arraySize];
    
        for (unsigned c = 0; c < arraySize; ++c)
            data[c] = std::rand() % 256;
    
        // !!! With this, the next loop runs faster.
        std::sort(data, data + arraySize);
    
        // Test
        clock_t start = clock();
        long long sum = 0;
        for (unsigned i = 0; i < 100000; ++i)
        {
            for (unsigned c = 0; c < arraySize; ++c)
            {   // Primary loop.
                if (data[c] >= 128)
                    sum += data[c];
            }
        }
        
        [Rest of code that converts the clock_t to console output]
    }

    * Without std::sort(data, data + arraySize);, the code runs in 11.54 seconds.
    * With the sorted data, the code runs in 1.93 seconds.
    
(Sorting itself takes more time than this one pass over the array, so it's not actually worth doing if we needed to calculate this for an unknown array.)

Initially, I thought this might be just a language or compiler anomaly, so I tried Java:

With a similar but less extreme result.

My first thought was that sorting brings the data into the cache, but that's silly because the array was just generated.

    * What is going on?
    * Why is processing a sorted array faster than processing an unsorted array?
    
The code is summing up some independent terms, so the order should not matter.
```
The heading of this question is exactly something someone might put into their Google search bar! But, why doesn't that elicit a STFW response?

Well, they have provided that they have some understanding of processing times and have shown that he has replicated his code by trying show that his X using a different Y showcases the same problem: slower processing times.

They are also specific and showcases that they've isolated their problem, and they are able to present their question as a small code block instead of asking "Why is my code running slow?" and linking to his whole project.

These points are some of the good things, including the very professional and ordered question, that made this question the top-scoring question of all-time on StackOverflow.

Below I will provide a shortened version of the answer, as it really is an in-depth [answer](https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array).

```
A: You are a victim of branch prediction fail.

What is Branch Prediction?
[Image here]
Consider a railroad junction:

Now for the sake of argument, suppose this is back in the 1800s - before long-distance or radio communication.

You are a blind operator of a junction and you hear a train coming. You have no idea which way it is supposed to go. You stop the train to ask the driver which direction they want. And then you set the switch appropriately.

Trains are heavy and have a lot of inertia, so they take forever to start up and slow down.

Is there a better way? You guess which direction the train will go!

    * If you guessed right, it continues on.
    * If you guessed wrong, the driver will stop, back up, and yell at you to flip the switch. Then it can restart down the other path.

If you guess right every time, the train will never have to stop.
If you guess wrong too often, the train will spend a lot of time stopping, backing up, and restarting.

Consider an if-statement: At the processor level, it is a branch instruction:
[Image here]
You are a processor and you see a branch. You have no idea which way it will go. What do you do? You halt execution and wait until the previous instructions are complete. Then you continue down the correct path.

Modern processors are complicated and have long pipelines. This means they take forever to "warm up" and "slow down".

Is there a better way? You guess which direction the branch will go!

    * If you guessed right, you continue executing.
    * If you guessed wrong, you need to flush the pipeline and roll back to the branch. Then you can restart down the other path.

If you guess right every time, the execution will never have to stop.
If you guess wrong too often, you spend a lot of time stalling, rolling back, and restarting.

[Insert in-depth explanation of analogy]

As hinted from above, the culprit is this if-statement:
    if (data[c] >= 128)
        sum += data[c];
        
[Applies failure of branch prediction to the provided code block with visualization]

What can be done?

If the compiler isn't able to optimize the branch into a conditional move, you can try some hacks if you are willing to sacrifice readability for performance.

Replace:
    if (data[c] >= 128)
        sum += data[c];
with:
    int t = (data[c] - 128) >> 31;
    sum += ~t & data[c];
    
This eliminates the branch and replaces it with some bitwise operations.
```
This is the top-voted answer, and for good reason: this is exactly what he was looking for. Out of the many answers, this one provides an explanation and reciprocates the same care and professionalism the question was asked with. If you want answers that are as in-depth, like they're essays, like this, then you should aim to ask questions like the first question...

But definitely not like:

## The second-most down-voted question



[Link To Forum Post](https://stackoverflow.com/questions/42384565/return-json-object-with-duplicate-keys-using-c-sharp)

```
Q: Return Json object with Duplicate Keys using C#

I'm using a WEB API to receive a request from a Client application to save Contact Information, and I need to send an Error Message only if the data has an error; otherwise nothing TODO

Earlier I Used a Dictionary<string, string>

For Example:
    Dictionary<string, string> error = new Dictionary<string, string>
    {
        {"SaveContactMethod_1", "FirstName Invalid"},
        {"SaveContactMethod_2", "LastName Invalid"},
        {"SaveContactMethod_3", "MiddleName Invalid"},
    }

the respective JSON Object is
    {
        "error" : {
            "SaveContactMethod_1":"FirstName Invalid",
            "SaveContactMethod_2":"LastName Invalid",
            "SaveContactMethod_3":"MiddleName Invalid"
        }
    }

But I need an UNIQUE Key (i.e., Duplicate Key), So I changed the Dictionary<string, string> to List<KeyValuePair<string, string>>
    List<KeyValuePair<string, string>> error = new List<KeyValuePair<string, string>>
    {
        new KeyValuePair<string, string>("SaveContactMethod", "FirstName Invalid"),
        new KeyValuePair<string, string>("SaveContactMethod", "LastName Invalid"),
        new KeyValuePair<string, string>("SaveContactMethod", "MiddleName Invalid"),
    }

the respective JSON Object is
    {
        "error" : [
            { "key":"SaveContactMethod", "value":"FirstName Invalid" },
            { "key":"SaveContactMethod", "value":"LastName Invalid" },
            { "key":"SaveContactMethod", "value":"MiddleName Invalid" }
        ]
    }
    
My Requirement: I need to add a Duplicate Key and I need the Json Output like a Dictionary.

Expected Output: JSON
    {
        "error" : {
            "SaveContactMethod":"FirstName Invalid",
            "SaveContactMethod":"LastName Invalid",
            "SaveContactMethod":"MiddleName Invalid"
        }
    }
```
Firstly, much like the first, the header could be problem. However, this can elicit a RTFM or STFW response, as the content does not showcase an attempt on the first two points I made about guidelines before posting a question.

We see a repeated head-against-wall hitting with the attempting X with Y. This is also made worse of how the content of the post is simply asking for the answer instead of opening it up to explanation. A requirement is ***LITERALLY*** denoted, and a large helping of .json files make it seem like they've just tossed their problem for the forums should solve...

And it is reflected in the **TWO** answers:

```
You have a classic "XY" problem. You have asked "How do I do X", but you really need to do Y and you think that X is the only way to get to Y -- but X is either impossible or very hard. By changing your requirements a little, you can get to Y a different way, but you haven't seen that yet since you're stuck on X.

Here's your X: the JSON format that you want to get:
    {
        "error" : {
            "SaveContactMethod":"FirstName Invalid",
            "SaveContactMethod":"LastName Invalid",
            "SaveContactMethod":"MiddleName Invalid"
        }
    }
    
This will, as others have said, throw away all the error messages except for one when you load it into your C# code.

However, there's a very simple way to get all the error messages. You simply need to change the JSON you're expecting to look something like this instead:
    {
        "error" : {
            "SaveContactMethod": [
                "FirstName Invalid",
                "LastName Invalid",
                "MiddleName Invalid"
            ]
        }
    }

If you only had a single error message, you should still use a list:
    {
        "error" : {
            "SaveContactMethod": [
                "FirstName Invalid"
            ]
        }
    }

That way when you load the JSON into your C# code, it will always have the same type, Dictionary<string,List<string>>, whether there was one error or many.

That's the Y in your XY problem. Instead of beating your head against the wall of "I want to have duplicate keys in JSON", find a way around the wall: have a single key with a list of values. And now you can do what you really needed, which is to get all the error messages from your form with just a single key name for every single error message.
```
A RTFM/STFW response. The answer reciprocates the terse and unprofessional care put into the question posed, but this answer is miles kinder than this next  answer:
```
No, this is not possible.

This would be invalid* JSON:

{
    "error" : {
        "SaveContactMethod":"FirstName Invalid",
        "SaveContactMethod":"LastName Invalid",
        "SaveContactMethod":"MiddleName Invalid"
    }
}
You can check this here [literally a link to a page to check json formatting]:

Warning:Duplicate key, names should be unique.[Code 23, Structure 9]
Warning:Duplicate key, names should be unique.[Code 23, Structure 13]

*Depending on what you call valid [link to a pre-existing StackOverflow forum about duplicate keys]

[Even worse, this is the edit:]

Since you don't seem to understand, what Depending on what you call valid means.

ECMA-262: [link to ECMAScript manual]
    In the case where there are duplicate name Strings within an object, lexically preceding values for the same key shall be overwritten.

That means: If you get three SaveContactMethod's, you only want "MiddleName Invalid" in ECMA Script (JS). With c# serialization, this would not even be possible. You need to write your own JsonSerializer for it.
```
A literal RTFM answer. **TWICE**. Even shorter, even more condescending.

Both of these answers answer with a simple answer akin to a yes/no. No deep explanation, referrals to the manuals, literal talking-down-to, and (if your account is tied to a professional/personal email) expect to be seen as lazy or incompetent. 

If you want all of this to happen to you, post a question like the second.

## Conclusion

In short?

Do as much as you can yourself before asking for help. And when you do ask for help, make sure that you can convey your question in essence and in an open-ended fashion.
