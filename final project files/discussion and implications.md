## Can LLMs Help Me Learn For Loops Without Having to Watch Youtube Videos?

### Introduction and Methods 

[Research](https://www.thinkwithgoogle.com/consumer-insights/consumer-trends/youtube-tutorial-video-statistics/) has shown that users are three times more likely to consult YouTube videos to learn about a product than they are to read instructions. While more people, especially Gen Z, gravitate towards the [short-form](https://www.uschamber.com/co/grow/marketing/are-short-form-or-long-form-videos-better-for-engagement) content (typically less than 10 minutes) on TikTok, there is still value in the long-form content that YouTubers create - otherwise, many of the popular YouTube channels would cease to have millions of subscribers as they do now. However, many YouTube videos on technical topics can be full of jargon and hard to understand if you are not familiar with the content, making you spend hours watching videos on different channels. The YouTube summarizer aims to solve this problem with the help of a Large Language Model (LLM). 

I decided to focus on a YouTube search ran by many people learning to code in Python: "how to run for loops Python." A [for loop](https://www.w3schools.com/python/python_for_loops.asp) is a function that iterates over a sequence, which can contain a list of numbers, for example. They can be tricky to learn and run as a novice programmer, making them an excellent but succinct point of comparison for the LLM-powered YouTube summarizer.


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

### Saves time, but mainly on longer videos 

The LLM summaries captured the main points of each video, hypothetically saving me time in picking which video would explain for loops the best. I also had the transcript from the process, so I could always refer back to that if I needed more detail. However, the summarizer would be most beneficial if I wanted to avoid watching much longer technical videos, say, an hour-long video. The videos I summarized for this project were around 10 minutes or less - not a huge time saver over going through the LLM summary process (i.e. getting URL, waiting for code to run, etc.).

### Likely to not cater to visual learners

On the flipside, the Khan Academy LLM summary did not contain a reference to the visual component of the video where he broke down a range function, which I find helpful as a visual learner. Based on the LLM summaries alone, I would end up picking the Bro Code video (even if the video I really would have preferred to watch is Khan Academy's video). Ultimately, the summarizer does not cater to different types of learners. 

### May harm YouTube creators' revenue

YouTubers mainly make money from ads that run on their videos (think the skippable ads at the beginning of the videos). If less people watch videos because they are summarizing the video content, it would decrease the revenue that creators generate from advertising, not to mention that it would hurt creators' general viewership. 

### Threatens to spread misinformation/disinformation

It would be easy to trust a summary of a harmful video with wrong or misleading information, especially if it sounds like what the title of the video suggests. But if were to actually watch the video, we might see some red flags - maybe based on the creator's tone or even if we read the comments section. Trusting an LLM to filter out misinformation and/or disinformation takes power away from us as users to decide what it right to consume on the internet. 

### May obliterate long-form content, or worse our attention span

If this summarizer can tell me the takeaways of learning Python, I may not feel obliged to watch or read anything long ever again. It may perpetuate the decrease we have seen in our attention spans [in recent times](https://www.apa.org/news/podcasts/speaking-of-psychology/attention-spans), as well as the rise in the consumption of short-form content on platforms like TikTok. For young people, this may mean poorer academic outcomes, as [research](https://www.sciencedirect.com/science/article/abs/pii/S0747563212001665?via%3Dihub) has found that college students with shorter attention spans are likely to spend more time on social media, and not be as immersed in their learning environments.



