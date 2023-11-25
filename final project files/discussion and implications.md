## Can LLMs Help Me Learn For Loops Without Having to Watch Youtube Videos?

### Introduction and Methods 

Before deciding to focus on for loops, I was interested in how well Large Language Models (LLMs) could summarize a YouTube video on a technical topic, such as coding - saving me time as a novice programmer. As a result, I created a LLM-powered YouTube summarizer with the goal of comparing content across different videos related to same topic - hence, for loops. Due to our usage of Python in this course, I decided that using for loops as a point of comparison across videos would not only be relevant, but generate a YouTube search with similar content, making it easier for me to see where the LLM could have gone wrong, or even right.  

To create the YouTube summarizer, I took the following steps: 

a) Convert YouTube video to a MP4 file using an online video-to-audio downloader

b) Generate transcription of MP4 file using Whisper, an automatic speech recognition system developed by OpenAI

c) Summarize transcription using LangChain, a library built on OpenAI's LLMs that is great for text summarization

When I finished running the code, I ended up with a concise summary of the video I had started with. To make sure the LLM accurately captured the gist of the three videos on for loops that I selected, I watched them myself. 


### Results

Surprisingly, the LLM (I specifically used Text-davinci-003) generated generally accurate summaries. Below I walk through each video. 

**[Programming with Mosh Video](https://www.youtube.com/watch?v=94UHCEmprCY&t=565s)**

`LLM-generated summary:
This lecture explains how to use for loops, range functions, and break statements in Python to create repetition and user-friendly messages. Examples are used to demonstrate how to use these functions and statements to generate numbers, send messages, and jump out of a loop when a task is successful. Attention is drawn to the importance of indentation.`

The summary described a high-level overview of what Mosh (the YouTuber) covered in his video. Aside from calling it 
"a lecture" - most likely because it generated the summary from the transcription - it was pretty spot on. However, I noticed that it did not mention specific for loops that Mosh did cover in his video, such as nested loops. Mosh had a more complex explanation for this part of the video, which I do not see as one of the examples that Langchain/LLM used. Other than that, the summary would help me determine whether I wanted to spend time watching this video. 

**[Khan Academy Video](https://www.youtube.com/watch?v=9LgyKiq_hU0)**

`LLM-generated summary:
This video introduces the concept of loops and the built-in Python function range, which can be used to generate lists of integers. It also explains how to use a for loop to iterate over a list of numbers, and how to set a range, start, stop, and step, and increment by a different number. Finally, it creates a loop that assigns i to a different element in a list of 0, 1, 2, 3, and 4, printing out each element in the list up to, but not including 5.`

The above summary captures the main points that Sal, from Khan Academy, was trying to convey in his video, which he essentially did in the first half of the video. He spent the second half explaining how to embed a variable in a for loop by drawing out the conceptual thinking behind it, which the LLM summary did not touch on. Do complex explanations or visual elements "weigh" less than more straightforward technical language? 

**[Bro Code](https://www.youtube.com/watch?v=KWgYha0clzw)**

`LLM-generated summary:
This article explains how to use four loops to execute a block of code a fixed number of times, such as counting from 1 to 10. It also explains how to use the range function and for loop to iterate over a string, and how to use the 'continue' and 'break' keywords within for and while loops. Examples are given to demonstrate how these techniques can be used.`

Bro Code said "use for loops to execute a block of code a fixed number of times" verbatim, which the LLM picked up in the summary. The rest of the summary was representative of the video content. 


### Discussion

These are summaries, after all, so it's probably okay that they leave out some of the additional details from the video. If I wanted more detail, I could simply read the transcriptions. That being said, the Khan Academy LLM summary did not contain a reference to the visual component of the video where he broke down a range function, which I find helpful as a visual learner.  Based on the LLM summaries alone, I would end up picking the Bro Code video (even if the video I really would have preferred to watch is Khan Academy's video). I could watch the videos like I did for this project, but I end up spending more time on getting the information I need, instead of saving time like I wanted to from the start. 

Now, does a comprehensive, accurate summary guarantee that the video I end up watching is the one to trust? What if it teaches me to run a for loop all wrong? Ultimately, this would fall on me, rather than the LLM. I could simply decide to watch one video and trust that it is showing me the correct code, or I could look at the other videos the LLM summarized, and compare for myself. When it comes to browsing the YouTube content, the LLM-powered YouTube summarizer provides a starting point for me as the user, and could give me more control over which content I want to prioritize. 

However, it could harm YouTubers' viewership if more people were to take screen the content through the summarizer before watching any videos. Among those who benefit would be students, like myself, and professionals who may consult YouTube for a specific task. 


