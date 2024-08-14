[00:00:00] **Alex Volkov:** And let's go.

[00:00:14] **Alex Volkov:** The air horn goes off and we're off on Thursday. I, August 8th. Welcome everyone to your, weekly AI summary news. with a lot of energy, my name is Alex Volkov, an AI evangelist with weights and biases. I'm joined here on stage by LDJ, a good friend of mine, often a co host here, and Junyang, Justin Lin from the Qwent team, with announcements also as well.

[00:00:41] **Alex Volkov:** I see some, I see some strawberries in the audience. Already. So we're going to talk about those as well. it's been, it's been quite a week. I will say, and I said this kind of before we started recording, last week was insane, insane last week compared to everything that I did. And I've been doing this for more than a year and a half weekly.

[00:01:00] **Alex Volkov:** Last week was insane. insane enough that we had maybe five breaking news. We have state of the art on top of state of the art. the week before it was also insane because we had three open source models breaking state of the art. This week was okay. Feels LDJ, I don't know, tell me, this week felt okay?

[00:01:16] **Alex Volkov:** Manageable? We could actually focus on work, I think?

[00:01:19] **LDJ:** Yeah, I feel like this week was pretty manageable, but who knows, there might be, some breaking news from OpenAI

[00:01:25] **Alex Volkov:** Yeah, so far, so far. Manageable, so far, to this point. 


## [00:01:28] Breaking News: Qwen2-Math Release[00:01:28] Co-Hosts and Guest Introductions

[00:01:28] **Alex Volkov:** Alright, and we have breaking news. Technically, technically breaking news, Junyang? because you guys just released this. so we're gonna get to it once Actually, no, before I do a summary. I think, I think it deserves, I think it deserves the breaking news thing.

[00:01:46] **Alex Volkov:** I just love pressing this button.

[00:01:53] **Alex Volkov:** Only on X on Thursday. I and you guys know that there's no, there's no Thursday. I, bigger pleasure of mine than announcing breaking news, but letting the folks who actually broke the news to come here and talk about them as well. junior Yang, the floor is all yours. Please, please feel free to tell us what you guys just launched, which I think looks very, very cool.

[00:02:16] **Junyang Lin:** Yeah, thanks, Alex. 


## [00:02:17] Qwen2-Math Model Details and Performance

[00:02:17] **Junyang Lin:** Yeah, we just released, Qwent2Math, a specific math specific language model. Yeah, previously we have been doing, building a large language model, general large language model, but this is, actually our second time after CodeQwent we are building a math specific, large language model, and this is our first try of a math language model, and we find that it is Really, really effective.

[00:02:39] **Junyang Lin:** You can check the scores. Actually, we guys are actually a bit surprised. So just using 72b model, Qwent2Math72b, so in the math evaluation, the data set, that's it, math, it can achieve 84. Yep. So it is outcompeting, general language model, just like Gemini, GPT 4, and Cloud 3. 5. I understand that they are general language model, not specifically for math, but, we just find that, the way that we build our pre training dataset and post training dataset.

[00:03:16] **Junyang Lin:** And also our methods, you can check a little bit, about our methods in the blog so you can find some IIHF stuff. they are really effective. Yeah, and we find that they can actually solve some, yeah, competition test problems. Just some, IMO stuff. Yeah, we have tested, AIME, AMC, and we have checked some, IMO cases.

[00:03:41] **Junyang Lin:** And we find that for some simple cases it can actually solve the problem. I think it's math is much better than me. Yeah. Yeah. 

[00:03:49] **Alex Volkov:** Wow, 

[00:03:50] **Junyang Lin:** that's, yeah, 

[00:03:52] **Junyang Lin:** that's, it. Yeah. 

[00:03:53] **Alex Volkov:** that's that's, that's incredible. so first of all, just to recap, like super quick, this is a 72 billion parameter model. 


## [00:03:59] Discussion on Model Licensing and Applications

[00:03:59] **Alex Volkov:** Could you speak about the license? Do you think this is the standard clan 

[00:04:03] **Junyang Lin:** actually released three models of, we have 1.5, we have 7,000,000,072 and 4 72. We are still using the old, terminal license?

[00:04:13] **Junyang Lin:** but for 1.5 and 7 billion, we are using Apache 2.0. 

[00:04:17] **Junyang Lin:** Hell yes. That's incredible. That's awesome. And, the 72 billion parameter model, beats GPT 4 and, and CloudSonic as well on the math evaluation. yeah I think, it beats, both of them, yeah. for GPT 40 it's around, 76 and Keep close with, I find it's about, 71, 

[00:04:41] **Junyang Lin:** yeah, 

[00:04:42] **Alex Volkov:** So just to tell folks about the, the, there's the task mathematics, like solving math problems. There's also the, the evaluation framework math as well. The zero shot at math. this model gets 84 beating GPD 4, beating Klotzhon and beating Gemini 1. 5 Pro. Basically all of the huge companies with billions of dollars foundational models, there's now an open weights model,That beats them on this specific task of math.

[00:05:07] **Alex Volkov:** How do the 7 billion and the 1. 5 billion perform as well? I see, I see there's like a best performance to size ratio triangle that you guys posted. Could you speak about this a little

[00:05:20] **Junyang Lin:** yeah, yeah. Yeah, you can also check the performance, with our tables, in our blobs, including a base language model and instruct models. I think you'd focus more on, instruct models. 1. 5 and 7 billion, is performing quite well. And for, 7 billion parameter model, it's math can also achieve 80.

[00:05:40] **Junyang Lin:** So I think this is for the first time, that a 7 billion model that can, achieve 80. we find that even if we. Scale the model size. It is really hard to further increase the score. So for 72B, it is around 84. And I think it is really, really hard to achieve 90. But that's all we get for now. And a little bit?

[00:06:02] **Junyang Lin:** surprising is that the 1.

[00:06:04] **Junyang Lin:** 5B is out of our expectation. It is achieving 70. So we have to, we have done a lot, Decontamination to check, yeah, whether we have some contamination that we don't know, but, we have checked it, but, we didn't find a problem. you can check the scores, in our table, for the instruct models.

[00:06:24] **Junyang Lin:** I think you'll find it very surprising. Yeah. 

[00:06:26] **Alex Volkov:** That's very surprising. I'll just add that I'm looking at some scores. We've talked about Mistral releasing MathStrel not that while ago. What, a month ago? A month and a half? I don't know if you guys remember exactly when they released it. MathStrel is a 7 billion parameter model that gets 56, right? 56 on this task.

[00:06:46] **Nisten:** This is insane. this is Yeah, this, what, Sona 3. 5 gets what, 71? 72? This gets 70? And it's a 1. 5b? I could run that on someone's watch. real. 

[00:07:03] **Junyang Lin:** I'm not pretty sure about, yeah, it's real performance for with the 1. 5B. Maybe it is a little bit, small. I'm not sure it is actually overfitting, but we, we don't know.

[00:07:14] **Junyang Lin:** But for the 72B, we have checked cases. We found that, it's really robust. 7B is also okay. Yeah. 

[00:07:22] **Nisten:** Yeah. And I've, I've used the regular 0. 7B before, so I wanted to ask, is this the same, around the same architecture as the 0. 7B and the work that you guys did is more on the. On the data side that you were able to to achieve this? 

[00:07:36] **Junyang Lin:** Yeah, we only work on the data set. We use the same architecture. Actually, we initialize the model with QwenT 2. 7b and also like QwenT 2 1. 5b, 1. 5b and 1. 72b. Yeah. Just initialize with the launch language model and then train it with our newly constructed math specific data sets. Yeah, this is what what we did.

[00:08:00] **Junyang Lin:** I think the effort actually attributed to the construction of the pre training data sets and also the post training data set. Yep. 

[00:08:10] **Nisten:** Oh, holy cow. Good. Good job, guys. 

[00:08:12] **Alex Volkov:** Yeah, incredible job.

[00:08:14] **Nisten:** Yeah, and also really Apache license too, so any anyone can use the [00:08:20] The smaller ones. I love small models. Gonna, gonna be running this because, and this is without, it's scoring all of that without tool use.

[00:08:28] **Nisten:** Yeah, so once, because we saw before that, was Numina math. they were getting to write some Python and then it could solve, it could solve, Olympiad problems, but with, with using tools. This one is just doing it. It's just doing it raw. And once you pair it with tool use, it'll probably be. Even better, but yeah, this is pretty insane.

[00:08:49] **Nisten:** This is this is next level. 

[00:08:51] **Junyang Lin:** Yeah, we have We have constructed a lot of data with the form of like chain of thought and also program of thought But chain of thought mostly and we find that it's actually very effective And for the post training, we have done a lot with rejection sampling to create a lot of data sets.

[00:09:09] **Junyang Lin:** Yeah, create a lot of data, so you have a lot of data sample, so the model can learn how to, yeah, generate the correct answers. Yeah, chain of thought is 

[00:09:19] **N8:** very effective, yeah. 

[00:09:22] **Alex Volkov:** Junaid, what's the point of a specific model versus a general model? So now you have this data set. Isn't, conceptually, couldn't you like roll this into a bigger general model for I don't know, 2. 5, whatever? And that, that would perform as well?

[00:09:38] **Junyang Lin:** Yeah, that's a good question. actually, this is actually our side project for our general large length model for the mass specific large length model. we built this model for the purpose of, synthetic data, actually, because we think that, it is really hard to, yeah, crawl enough, like mathematics specific data and put it into general language model to really increase its capability.

[00:10:03] **Junyang Lin:** We think that, if we can really, build an expert model in mathematics, so we can use this model to generate more synthetic data because it's capable of solving hard problems. So you, you can achieve, get some data where it is very hard to get from the, yeah, from the 

[00:10:24] **N8:** internet. Yep. 

[00:10:26] **Alex Volkov:** Oh, that's awesome. Okay. So this is a specific model, synthetic, and because it's Apache 2 license, at least for the 7b, folks can also generate synthetic data as well. this is incredible. Nisten, go ahead. Yeah. Yeah. Go ahead.

[00:10:38] **N8:** Sorry, 

[00:10:39] **Nisten:** since This is based off of the, the, the 7b, could we, would it be possible to generate a Laura? I'm going to give it a, a try, or is it going to be too, too different to find the, the mask that, that, that applies on top? I don't know. I think because I already use 7b, like I've, I've used it just for, for random stuff.

[00:10:59] **Nisten:** If you could just generate a Laura and you can just switch to math. Out of that, that would be cool, or is it just like way too over trained and has changed a lot? I'm not sure, it's just, I'm just throwing out the idea out there, but. 

[00:11:13] **Junyang Lin:** Yeah, so your question is, it's about how we train the model or, whether you can use LoRa to fine tune the model.

[00:11:20] **Junyang Lin:** Yeah, I'm not sure about the question. 

[00:11:23] **Nisten:** Oh, I meant to generate a A difference between the, the regular Quin seven B and, and the math Quin, and to save only, let's say the, the, the mask, on top. And then it would be a lot faster to switch in between the two on a, on a low powered device. I was thinking.

[00:11:45] **Nisten:** Oh yeah, 

[00:11:45] **Junyang Lin:** I'm not, I'm not pretty sure about that, whether you can, I think you're, you're going to, combine it to, when you're doing, math tasks, you would like to switch to, yeah, things like, yeah, the math, math model. I'm not pretty sure how to, how to do it, but, for the finetuning, you can just, train it just just like you did with, Quantum 7B or, Mistral.

[00:12:07] **Junyang Lin:** Yeah, things are quite similar. 

[00:12:10] **Nisten:** All right, we're going to be trying on, we'll, we'll, we'll post anyway, but Yeah, this is pretty, this is pretty amazing. We just got more toys that we don't have time to play with. 

[00:12:18] **N8:** Yeah, 

[00:12:20] **Alex Volkov:** Junaid, thank you so much for coming up and obviously, a huge shout out and kudos to your team who worked on this as well. so hopefully they'll hear this. you guys are releasing incredible models and putting up an open source, which we always, always appreciate.

[00:12:32] **Alex Volkov:** folks in the chat or folks who are listening, please give us, like a clap emoji and we'll see you in a bit. As a reaction for the Qwen to maths that are now state of the art in math in open source and not only in open source, right? You're getting like probably the highest scores in this math, in this math tasks, it looks like.

[00:12:49] **Alex Volkov:** If I'm not mistaken, this is state of the art on at least this, this math task. what other, there's also Minerva math, there's other Olympiad bench, there's college math, and MMLU STEM as well. I'm seeing like other evals that you've collected. And one last thing I'll ask you before we're gonna do like a recap, and obviously feel free to stay here and we'll chat more about this, is that, you only released the English version of this, Chinese version coming up soon, correct?

[00:13:14] **Alex Volkov:** Correct.

[00:13:16] **Junyang Lin:** because this is actually a test, on how we build a math specific model. So we just use English data, at the, at the beginning, but this month we will try to build a bilingual one and later multilingual. 

[00:13:28] **Junyang Lin:** Yep. 

[00:13:30] **Alex Volkov:** Oh, I see. Alrighty. folks, before I do a TLDR, I want to say hi to a friend of mine, and also a great guest. We're going to talk about, some stuff that we have together, cooking. hey Mark, you want to introduce yourself to the, to the folks? I think it's your first time talking here? I think it is.

[00:13:45] **Mark Saourifm:** Yeah, I think so. nice to see you again, Alex. hi everyone. my name is.

[00:13:48] **Mark Saourifm:** Mark Saroufim I'm an engineer on, I work on, I've been working on PyTorch for the last, like four years or so now at Meta I also spent a lot of time in online communities and one thing I've been personally very excited about has been, competitive coding agents.

[00:14:01] **Mark Saourifm:** Recently, 

[00:14:03] **Alex Volkov:** So that's awesome. And we'll talk about, we'll talk about some stuff, as regards to this in a bit. 


## [00:14:07] TLDR and Other AI Announcements

[00:14:07] **Alex Volkov:** So I think, I think it's time for us to do a TLDR, Here's the TLDR of everything that we've talked about on Thursday, on August 8th, on ThursdAI. We started the show with breaking news from our friend Junyang Ling from The Qwentin and Alibaba, they . I I love the Qwentin because they often time their releases on Thursday. So Ang actually dmd me before they drop this.

[00:14:34] **Alex Volkov:** Quinn two math 72 billion instruct is a new state of the art open weights model that beats GB GBT four and clots on it and Germany. One, Gemini 1. 5 Pro on math tasks. it gets a ridiculous 84 points on the math, evaluation benchmark, zero shot, which is quite incredible. They released three models there.

[00:14:56] **Alex Volkov:** They released the 72 billion parameter, Quantum Math, the 7 billion parameter, Instruct, and the 1. 5 billion parameter Instruct. We, like we heard from directly from Junyang what they did there. It's quite incredible. Compared to previous. Math specific models, like Mathstral from Mistral, for example, from like maybe a month ago, it looks like this 1.

[00:15:18] **Alex Volkov:** 5 billion parameter beats that model like significantly. And that one was 7 billion parameter. it's, it's not often, like lately it's, it's, it's very often that we talk about models that beat GPT 4, which is quite incredible. And I find it very exciting that like open source beats GPT 4 and this, and this, and this, this, this now looks like the best.

[00:15:36] **Alex Volkov:** Math, Math, MathFocusedModel. That you can use, and, the, the licensing for the 7 billion parameter and the 1. 5 billion parameter are Apache 2 and 7 billion parameter you can run on, Nisten I think mentioned, it can run on your smartwatch. quite incredible and the numbers it gets on these, on these tasks, are, are just mind blowing.

[00:15:56] **Alex Volkov:** Junyoung talked about decontamination efforts that they did, a lot to make sure that none of these math problems went into the training set as well. And we had a long conversation, definitely worth checking out. and I love when breaking news happen and the folks who broke the news come and talk about them here live on ThursdAI, it's incredible.

[00:16:15] **Alex Volkov:** also we've talked about, OpenBMB. Dropping a new vision model, a 8 billion parameter, mini CPM version 2. 6. it's a VLM that understands images, multi images and video. And because it's an 8 billion parameter, it can run basically on the phone. They actually have videos of it running on an iPad. It's incredible in OCR as well.

[00:16:36] **Alex Volkov:** And I, I, I, [00:16:40] I've read out a few examples of videos that I, I uploaded and it captioned. And it's quite incredible. It's incredible because again, we're getting a GPT 4 level vision model. 8 billion parameters. I'm still, it's really hard for me to get used to something to say something like this. It's an open source 8 billion parameter model that you can use and probably fine tune for your own task, but you don't have to because general it's really, really good.

[00:17:06] **Alex Volkov:** At OCR, it, there's an benchmark. They're called OCR bench. This model gets 852 points where G PT four oh gets 736. this model is better at OCR than Gemini. 1.5 than, than CLOs on it, at least on this benchmark. Quite impressive, quite impressive, the folks at OpenBnB, also, Junaid mentioned that they've used GWEN, in, in, in some of this, so definitely worth checking this out, I will add the link to try this out in the show notes,Extremely impressive, like small models beating this.

[00:17:34] **Alex Volkov:** And I've tried a few videos on my own and it was quite, quite stunning. And we also talked about Biggie Smalls from our friend here, Nisten, that blew up on Hug Face for the past week. I think it was one of the, like the eighth, maybe, trending. model on Hug Face, Nisten set out just to play around and then at some point he got to a point where he wanted to build the smallest, fastest LLM, that could possibly run on the smallest, possible hardware.

[00:17:57] **Alex Volkov:** And folks here on stage were, getting quite technical as to how this was possible, including a new, A new optimizer from Eric Hartford from Cognitive Computation. And this model runs up to 30, 330 tokens per second, which is ridiculous because it's not optimized hardware, but it's an optimized model and definitely worth listening to this conversation if you're, if you're, interested.

[00:18:20] **Alex Volkov:** And it was like a very illuminating conversation about Optimizer as well. After the open source conversation, we went into the big companies and APIs section, where we talk about everything big companies do for us. And, Basically anybody that serves an API, we've talked, we started with OpenAI introducing a Structured Outputs in its API.

[00:18:39] **Alex Volkov:** Structured Outputs is the ability for developers to provide a schema for OpenAI and the, the, the API will return like a JSON structure exactly per that schema, which is something that a friend of the pod, Matt Schumer, said that they do with just prompting and it works. OpenAI decided to train models better To actually comply to these structures with a hundred percent accuracy.

[00:19:04] **Alex Volkov:** And this is what they posted on their thread. In addition to this, they also mentioned multiple ways in which they did this to their models. And in addition to this, at the end of that blog post, they said that this model is now 50 percent cheaper on inputs and 30 percent cheaper on outputs, or 33 percent cheaper on outputs, which costs now 10.

[00:19:22] **Alex Volkov:** 1 million outputs compared to the previous GPT 4. 0 model, which is crazy. Again, quite insane, we're getting 50 percent cheaper, just without fanfare, we're going towards intelligence too cheap to meter, it's crazy. And also folks here on stage commented that this actual model, the new GPT 40 2024 0806 This is actually better in multiple benchmarks.

[00:19:46] **Alex Volkov:** Not only for just structured output in different other benchmarks as well, which is not often the case. Sometimes people are getting very excited about new models and then they claim they're dumber. On multiple benchmark, they're like lateral intelligence and different things that people mentioned. This model seems to fare better, including on Zebra Bench from LNAI, so definitely worth listening to that conversation as well.

[00:20:09] **Alex Volkov:** And shout out to OpenAI for lowering the, the price of this model by a significant amount. And also giving some developers what they want. We then had a little bit of a, of a fun time speculating about some strawberries. I will not go into this too much. Too deep into the TLDR, but there has been a post from Sam Altman, posting about strawberries and then multiple people from OpenAI also posted strawberry related themed images.

[00:20:34] **Alex Volkov:** And we tried to understand what, what this was about. And thanks to, Yam and LDJ and some other folks, we, we went deep into the lore of the strawberry discussion on X. And if you're interested in some,less factual reporting, more,conceptual, trying to understand the meme sphere. This, this conversation is for you as well.

[00:20:54] **Alex Volkov:** We then also talked about Mistral. Mistral released a fine tuning ability on their platform. So you can now upload your data into Mistral and then you can fine tune their best model again. G PT four, biding level model ral large V two, which they announced a couple weeks ago. Now you can actually fine tune it on their platform and, and serve it via a p on their platform.

[00:21:13] **Alex Volkov:** And they also announced agents. Agents in Misra are not agentic loop running kind of agents like the ones that we talk about usually like ER and crew. AI agents for Mistral are more similar to some of like GPTs for open AI or projects in Tropic where those are. agents, you as a user build, they have an agent builder.

[00:21:32] **Alex Volkov:** And I think over the API as well, you can share examples for a few shot prompting, and you can give a system prompt in advance and you save this agent and they deploy it via the API for you and also to their like chat platform called LeChat. And then you can interact with this, agent basically. It will just know And we'll have examples of the previous stuff that you said.

[00:21:52] **Alex Volkov:** So basically like projects in the topic. the cool thing about this is that they're planning to have a big potential with tool use going forward and different other things. But for now, their agents are more similar to the other examples. We also briefly covered,Character AI's, acquisition, executive acquisition to Google, which is not an actual acquisition, but, Noam Shazir, the author of the Transformers paper, or one of the authors of the Transformers paper, is going back to Google, and Character AI is going to use LLAMA models for their, For the characters, rather than building foundational models for themselves.

[00:22:27] **Alex Volkov:** And we had a conversation about that as well. In this week's buzz category, we had a friend of the pod for the first time here, Mark Sorfim from the PyTorch team, and talked about the NeurIPS Hacker Cup. that's been running for a long time, that, there's going to be sessions with Mark and Weiwei from Microsoft and a bunch of folks from Weights Biases and a bunch of other folks in the kind of, code generation or code understanding, LLM area.

[00:22:54] **Alex Volkov:** And, just trying to solve very hard, difficult engineering challenges without necessarily agentic approaches. and, definitely worth listening to this and joining. the Weights Biases platform where, just 1b. me slash Hockercup, where you can get caught up to speed and like up, up the, up your level if you want to join this, this year.

[00:23:13] **Alex Volkov:** Very interesting conversation. Definitely. We're, we're definitely going to talk about this a little bit more. And, at the end, we have a nice conversation that if you will not remember, that both of us geeked out basically on Cursor, which is a VS code,code editor. It's a clone of VS code that neither of us are getting paid by Cursor.

[00:23:32] **Alex Volkov:** We just love it so much that we decided to have a geek out conversation about this live, about their new feature called Composer. that's basically an agentic approach to multi file editing. so if you have used Cursor and you haven't used Composer, listen to this. If you haven't used Cursor, strongly, strongly recommend to give it a try and listen to us geeking out about this because this will boost your productivity.

[00:23:52] **Alex Volkov:** And also, of course, Biggie Smalls. Of course, BiggestModels, Nisten, maybe we'll start with this because this is in open source.

[00:23:59] **Alex Volkov:** So I think we'll just switch to open source. Let's go.

[00:24:20] **Alex Volkov:** Let's get it started. 


## [00:24:21] Biggie Smalls Model and Performance

[00:24:21] **Alex Volkov:** Um, oftentimes the folks who are here on stage are also trending in multiple places. this week was Nisten's trending. Nisten, you were trending on Hug Face, like trending spaces or trending models to download. Correct?

[00:24:34] **N8:** it was more like I was just 

[00:24:35] **Nisten:** hacking around edit because I needed some tiny model for my os. And, so at first I was using 1. 5d, but I needed even smaller, so then I just ended up finding, the smallest one. So yeah, a lot went in it and, ended up with, with Biggie Smalls. Sorry, I'm in a I'm in a public space right now, but someone just messaged me [00:25:00] today, and apparently they're trying it out at the, the large Harjan Collider, because it runs so fast, 

[00:25:06] **Alex Volkov:** Wait, are you 

[00:25:06] **Nisten:** they're looking at, yeah, using Biggie Smalls for, industrial equipment, like automation stuff.

[00:25:13] **Nisten:** yeah, someone that listens to the pod messaged me this. I don't know if they're joking. I know they are legit, but I don't know if this is, if they're just making it up. 

[00:25:22] **Alex Volkov:** Somebody who listens to ThursdAI, works at Large Hardware Collider, is going to use Biggie Smalls?

[00:25:27] **Nisten:** Yeah. Yeah. Yeah. They use, they've been working for like over a year and using, they've been using GPT 4 vision to do, industrial system safety, like the electricals and stuff. Like they have vision looking at them and seeing if, like switches went off or I don't know what goes on in there. Lost the physics in grade 10, but it, they're, they're using it.

[00:25:47] **Nisten:** And, yeah, it's, it's a very tiny model. I think you can train a Laura of it. In 45 seconds, if you want it, and you can do a full fine tune in, in, in about an hour, the, the code's all open source. And, yeah, it's, it's one of the fastest models that kind of sounds coherent or pretends to have a conversation with you.

[00:26:10] **Nisten:** And, the fastest that anyone ran it on a single CPU core on M3, someone, people are hitting like 280 tokens per second now. And we might be hitting 300 with, Justine's new optimizations, and once we prune it, we, we might hit, I, I don't know, I don't know what, what TPS, but, it's, it's pretty, this is, this is pretty crazy what happens when you try and match the model, when you try and mold it.

[00:26:40] **Nisten:** to the hardware that it's on. And the reason it works so well on a single CPU core is because, you remove a lot of the memory bottlenecks that happen when, stuff's moving between cores and you end up using all the cache for that one core. And That's what gives it like that insane, like completely insane,speed up.

[00:26:58] **Nisten:** But yeah, the code's all open source. I think it's also a great model for, for teaching. It uses mainly the Capybara dataset, which LDJ made, and the dataset is fairly clean, it's low toxic, there's not,there's not that much data in there for it to be toxic, so if you're, like, teaching kids or stuff, or you're an instructor, it's a very good model to, to teach people LLMs with, there's something there for everybody, there's a whole new optimizer, So you can go from PhD to the starter level with just like that one piece of code, just messing around with that.

[00:27:33] **Alex Volkov:** That's crazy, man.

[00:27:34] **Nisten:** but yeah, maybe LDJ wants to talk a little bit about the dataset. Yeah, I just, also 

[00:27:39] **N8:** wanted to note that, Nisten and I were testing it on, the M3 Max and with, four CPU 

[00:27:43] **Alex Volkov:** Wait, before you note, before you jump in and note, could you please introduce yourself to the folks who never heard you here 

[00:27:49] **N8:** Oh, sorry. Yeah, yeah. Sorry about that. I'm in eight programs. I do, I'm a researcher in resident at Nous Research. I just did a bit of work with Nisten on this model and testing it on different platforms. And I work a lot with synthetic data and LLM fine tuning. 

[00:28:06] **Alex Volkov:** All right, and now to your note, please go ahead.

[00:28:09] **N8:** Yeah, I don't want to interrupt LDJ's Capybara stuff. Capybara is awesome. But, I just wanted to say that the The model can get up to 330 tokens per second on four CPU cores using, an M3 Max, which, out of the box, Llama. cpp, which I find insane.

[00:28:27] **N8:** that you can run like in a hundred, yeah, 330 tokens per second. That's like rock speeds. It's very, very fast.

[00:28:34] **Alex Volkov:** That's insane. That's absolutely insane. Nisten, sometimes he was like, I think you threw, did you throw biggest smalls at the end there, for last Thursday? just completely at the end. And then, 

[00:28:46] **N8:** Yeah, it was, it was random, 

[00:28:48] **Nisten:** so I was trying to, to fine tune it, like a lot of stuff went into this. one was the evolutionary model merging to make the Frankenstein, and then, it was LDJ's dataset, which, there's a lot of secret sauce that goes into making that, and Distributing the data the right way amongst different subjects.

[00:29:05] **Nisten:** And, then, I kept fine tuning with different stuff. I saw that Eric here from, Cognitive Computation had just pushed out, a day before a new optimizer. Eric wants to talk about the new optimizer. so I just used that and, so that ended up making it way more coherent because it wasn't.

[00:29:25] **Nisten:** So that's the thing. It's just like such a small dot with a model that any optimizations, any stuff you throw at it, you notice an improvement right away. And that's why it's good for teaching. But yeah, I, basically, I just, hacked together whatever, the best little things I could find in the community.

[00:29:44] **Nisten:** And, and two of those ingredients are here. LDJ made the dataset and,Cognitive Computations made the, optimizer. yeah, it's, I want to also let the, LDJ talk a bit about it and, also, Next Eric, because yeah, there's a lot going on. This is a stupid little model. 

[00:30:04] **Alex Volkov:** That's super cool. Cognitive, oh, go ahead, LDJ.

[00:30:09] **LDJ:** Yeah. I was actually wanting to ask real quick, Nisten, how much faster do you think it might be able to be if you did speculative decoding with something like a hundred million or 200 million parameter model? 

[00:30:21] **Nisten:** I have no idea. We're in uncharted territory. Might be able to push 500 with Justine's optimizations.

[00:30:29] **Nisten:** if you go to 4 bit and it starts smushing together, it Two 4 bit operations into 8 bit, registers, might be able to hit Oh, there's people, there's like hardware engineers trying to get it to work on FPGAs. now, there's a, there's a lot going on. Yeah, we, we might hit 500, but yeah, I, I want to say, I used, actually used Qwent 0.

[00:30:53] **Nisten:** 5b for this job first, and then it, it was still, it was fast, but I needed, I need it way faster. The main idea is that I just want one CPU core to do stuff in the background and no more than that.so the constraints breed creativity and that, yeah. So might go a little bit more, might need data.

[00:31:19] **Nisten:** I don't know. 

[00:31:20] **Alex Volkov:** don't, but the thing, the funny thing is that, I'm sorry to interrupt that. I think Eric was building this optimizer to train LAMA 4 0 5 B, so that it could run better. And, with in, yeah, with like smaller, smaller batches, they can run better on like limited hardware. And I applied it like on literally the world's smallest model.

[00:31:40] **Nisten:** So it's pretty hilarious that that worked and it worked well. So it's, yeah, pretty excited to see what's going to, what's going to happen next. New optimizers, new 

[00:31:54] **Nisten:** hardware.

[00:31:54] **Alex Volkov:** so Eric's also here on stage, but also the thing that I'm hearing that's incredible. This is like everybody who's here on stage contributed in some way. And this is like quite honestly, like insane to me. And also Nisten, I don't know if you already met Mark, but Mark, this is Nisten, our like resident. Like a crazy hacker that does crazy experiments.

[00:32:14] **Eric Haftford:** Nisten, this is Mark who works on PyTorch. And I'm sure that he has a trick or two that you probably haven't yet optimized. Yeah, I just wanted to make a quick comment about, about the, the optimizer. It's called, Grok Adam W, and it was basically inspired by the, the Grok FAST paper. And, the idea is to teach the model to generalize. So instead of just repeating by rote, It, it actually is able to, generalize on the task and the GrokFast is the accelerated version of that.

[00:32:46] **Eric Haftford:** And all I wanted to do was take that GrokFast paper and make it accessible so that it can be in the Transformer. And it can be used by things like Axolotl for training models with very little, overhead and resistance to get that going. Andand it's just a very fortunate occurrence that, that it was useful for biggie small right out of the gate.

[00:33:11] **Eric Haftford:** And so I'm, yes, that's true, I'm trying to, use this for the bigger models. By the way, I forgot to introduce myself. I'm Eric Hartford. I founded Cognitive [00:33:20] Computations and I work on the Dolphin and Samantha models. and yeah, so I'm, right now I'm integrating it with Transformer Library and, soon hopefully to all the, all your favorite trainers. 

[00:33:32] **Alex Volkov:** That's awesome. Thank you for coming up, Eric. And, it looks like we have quite a quorum here on stage as well, but I also want to say hi to Yam. Yam, what's up? Welcome. 

[00:33:41] **N8:** Hey, how are you doing? How are you 

[00:33:42] **Alex Volkov:** Good. You missed your friend. You missed your strawberry friend here. He was here before. 

[00:33:46] **Yam Peleg:** really, really, the story was 

[00:33:48] **Alex Volkov:** Yes. And then left not on stage though, so I don't know if that's a person or, or, or GPT

[00:33:54] **Yam Peleg:** No one knows Nolan Know Wanted. 

[00:33:56] **N8:** I do wanted to talk a little about the Strawberry Man. I've been 

[00:33:59] **Alex Volkov:** Yeah. Not, not yet. Not yet. We, we'll get there. We'll get there. This is gonna be the second, the second part of the of the talk.

[00:34:04] **Yam Peleg:** Yeah, I just, I just wanted to say about this topic,the, the thing about the Optimus, people, just to tell the audience that's a big thing, right? If it, if it works well, it improves every model that you throw at it.

[00:34:18] **Yam Peleg:** so it's a huge thing if it works well, and I think, all of us, like you said, we, we need to talk, behind the scenes and just get to the point where we can, infrastructure wise, implement optimizers that can be sharded well, because this is the thing that's stopping people from trying different optimizers on larger models that we, the parallelism and, and all of that, you can implement optimizers, but There is an implementation and an implementation you can actually run at scale.

[00:34:48] **Yam Peleg:** And these are two different things. And I think this is something that stops many of these initiatives that have a lot of potential, especially this one. Seriously, the numbers are incredible. Yeah. It's a huge thing. It's a huge thing. 


## [00:35:04] Challenges and Solutions in Optimizer Research[00:35:04] Exploring Tensor Subclasses in PyTorch[00:35:04] Introduction to Optimizers and Distributed Systems

[00:35:04] **Nisten:** I just want to say something. I don't want to go too technical on this, 

[00:35:08] **Alex Volkov:** Oh yeah, you think, you think we're not there yet, already?

[00:35:11] **Yam Peleg:** no, no, no, no. I'm just saying we can talk, we can talk about this a lot. I just want to say that to everyone listening, look, it's much, it's much more simple than you probably think. go and look at, there are minimal implementations of 0.

[00:35:25] **Yam Peleg:** 3. For example, there are minimal, minimal for education purposes, go and look them up. You will understand them, and it's very important, I think, just to spread this specific knowledge, because I think that optimizers research is just stuck because of this, just because people don't know how to approach it, the sharding part, the distributed part. So go and search it up. That's it. That's what I wanted to say, and let's not go too deep

[00:35:50] **Alex Volkov:** So I will say this, I will say this, because of the people here on stage and because this week was not like a crazy, crazy news week that we have to get to everything. I like these discussions. I like the people who meet the people here on stage and then like crazy, incredible things happen. And so like Nisten said, biggest, smallest happened due to a new optimizer thing and copy bar and initialized by Qwen, like all of these things.

[00:36:10] **Alex Volkov:** And now we have Mark here also can chime in with like different, Different suggestions. I love these discussions. we do have to move, move forward because we've talked about Qwen a little bit, and we want to talk about OpenBMB as well. but, I, I think that when we are able to have those discussions, I'm very, very welcoming of those, and I'm just like incredible, the community that goes around ThursdAI and talks about these things, I think there needs to be a place for this as well.


## [00:36:34] OpenBMB Vision Model: A Deep Dive

[00:36:34] **Alex Volkov:** So, I think we're moving forward folks for the, the OpenBMB, vision model, which is a 8 billion parameter vision model that it's really, it's really a challenge to talk about vision models here because you have to see their output and try them for yourself, and not just trust us.

[00:36:50] **Alex Volkov:** That's one. And two, people are getting, maybe used to very good vision models because now all of the foundational models they use, GPT 4, Gemini, Sonnet, like all of these are like very good vision models. They see very well. this one is an open source 8 billion parameter model that understands images, multi images and video, and it could technically run on your phone.

[00:37:12] **Alex Volkov:** And, and I think that's insane. maybe folks remember there's like a viral video of a toddler running around on like super speed and also use this for, I think I posted this. I use, I use this to, to showcase a segment, anything too. 


## [00:37:23] Showcasing Vision Model Capabilities

[00:37:23] **N8:** Wait, you made the amazing segment Anything 2 Demo? That's I showed that to all of like my Whoa! Epic crossover 

[00:37:29] **Alex Volkov:** The, the toddler one. I don't know if that's the one you're 

[00:37:32] **N8:** Yeah, the toddler one with the holographic background

[00:37:35] **Alex Volkov:** the toddler metrics. 

[00:37:36] **N8:** off anything. Yeah, . 

[00:37:38] **N8:** my mind. 

[00:37:39] **Alex Volkov:** thank you. this what blew my mind is it took, took one, one click, but or two clicks on their demo. So basically I showed the, the original video of this to ba basically for folks who are like listening to this, have no idea what innate and I are talking about.

[00:37:52] **Alex Volkov:** There's a video of somebody who posted about their like 1-year-old toddler and, and, it sped up like maybe five x. So the toddler looks like he's running around. and I just uploaded this video to open, BB. 8 billion parameters, yeah? This is the output. The video captures a young child's journey through an outdoor park setting.

[00:38:08] **Alex Volkov:** Initially, the child This is a video uploaded, not an image. Initially, the child is seen sitting on a curved stone pathway besides a fountain, dressed in a casual clothing with green t shirts and dark pants. As the video progresses, the child stands up and begins to walk around the paved path, moving away from the camera towards open, grassy areas dotted with trees and benches.

[00:38:27] **Alex Volkov:** Child continues to explore different sections of the park, blah, blah, blah. It's Quite ridiculous. 


## [00:38:32] Performance and Benchmarks of Vision Models

[00:38:32] **Alex Volkov:** The, the, just the detailing and the specific detailing of progression within the video is quite, quite, quite, quite impressive for an 8 billion parameter model, and, we've been saying this, that like smaller and smaller models will be better and better at this, I don't think I've seen such quality from such a small parameter model.

[00:38:51] **Alex Volkov:** They obviously posted benchmarks as well.they claim that they beat, GPT 4. Vision level for 8 billion parameter model, which to me is incredible. They also do OCR very well. So you can upload videos of like tutorials. You can upload images. another thing, if you guys remember a couple of weeks ago, I had the Apple intelligence, which Kind of like prompt.

[00:39:14] **Alex Volkov:** I had a video of me just like selecting Apple intelligence waitlist on my iPhone. I uploaded this and also got a response that was like very clear. Like this user is using the iPhone settings to do this, this, and this. And the model basically read all the text in this video and told me exactly what happens.

[00:39:30] **Alex Volkov:** And this is again, ADL imperative model. So quite crazy, quite crazy. And I think that now we've gotten to a almost state of the art. On, on multiple like vision benchmarks, actually, yeah, there's, there's a few benchmarks that I can like a shout out. There is the, OCR bench, which I haven't heard of before.

[00:39:50] **Alex Volkov:** This model gets the highest score on OCR bench based on what they posted. There's also the. 852 on OCRBench. Thank you. there's also the OpenCompass. It gets the highest score as well. And then MMMU, which is like a massive multi model, evaluation. This gets almost 50. So this is a bit, a bit less than like the main, the main, the main models.

[00:40:13] **Alex Volkov:** but again, 8 billion parameters. 

[00:40:15] **N8:** sorry, but I think MMU is also about like world knowledge and it's meant to be like the equivalent of MMU for vision. So I think obviously a smaller model is gonna do worse on that, but like with the OCR stuff, that's more of just raw vision ability, and I think that's where it really excels. 

[00:40:30] **Alex Volkov:** Yeah, absolutely. 


## [00:40:30] Discussion on Vision Language Models

[00:40:30] **Alex Volkov:** Uh, I want to hear, thanks Nade, I want to hear Nisten's reactions because you've built like vision models before. Juniaing also, we'd love to hear from you, as you're seeing like this, like size of models and, and you guys, you've built CoinVision before. We'd love to hear your thoughts on like how this model performs this well on some of these benchmarks.

[00:40:48] **N8:** Yeah, 

[00:40:49] **Junyang Lin:** we actually have some collaborations with OpenVMB. so you can find that this 2. 6 is, actually based on, yeah, Qwent27B. Yeah. they have done a lot of great job in building good vision, datasets. It's very impressive that they are using, yeah, multi images and video. and very impressive results.

[00:41:10] **Junyang Lin:** You can check the demo. Yeah, you can find the performance. Yeah, we care a lot about MMMU, but I think it, it is actually relying much on large language models. if they are using larger models to build their vision model, the experimental results will be much better, but this one 

[00:41:32] **N8:** is pretty good.

[00:41:33] **N8:** Yeah.

[00:41:34] **Alex Volkov:** Yeah, so this is, we've been saying this before, and Nisten, feel free to chime in here, that like sometimes vision models [00:41:40] need, bigger kind of logic model behind them to actually, perform better. And this is just an eight billion parameter model that performs very well, but maybe on the logic stuff,it may need a bigger brain behind this, but it still performs very well.

[00:41:52] **Alex Volkov:** I don't know if he has a chance to play around with this. but I got to wonder what this model would look like on a 72, brain.

[00:42:01] **N8:** Yeah, and we've said this 

[00:42:03] **Nisten:** before a couple of months ago that, and I remember you, Junaid, when you guys said you moved to 14b, and I tried moving Baklava to 11b, and it was performing better because it could get like more time to chew at the tokens. But I think what's happening now is the small models are just getting smart too, They can process the, the, the unit better and, and for the audience, the, the way that these VLMs, visual language models are done is you have the, the vision brain, like the VIT, the, or like the clip encoder, if, if you've heard that, and you have the, the language brain, which is, Either Qwen, Lama, Diggy, whatever, whatever you use.

[00:42:44] **Nisten:** And then what you do is you like, you train a little slice of brain in between them, like silicon brain. It's called a projection layer. And then eventually the, the vision brain learns to talk to, to the language brain. And you end up with a, with a VLM. And it's the same thing that they do for the newer voice stuff.

[00:43:05] **Nisten:** It's the exact same thing. It's just, you have like your, your whisper or whatever your, your, your speech encoder is. And so this is, this is how these work. And that's why when people say, oh, the, the base it was, it was quite is because it was a language based that's, taking that, that vision data, which is just token.

[00:43:24] **Nisten:** Same as, you have language tokens, like you have a vocabulary of tokens, and then it, it chews on that, and it, it digests it, and it comes up, comes up with the right, the right answers. yeah, so what's happening now is that the smaller models are getting, are getting really good too, and, I guess you don't need as big of a, of a language model base to, to, to get better results, but those results would still happen if you went bigger. 

[00:43:51] **Alex Volkov:** Go ahead, Jan.

[00:43:54] **N8:** Yeah, I just, I just want to ask, both, 

[00:43:56] **Yam Peleg:** both for myself and people in the audience, for everybody, interested, I don't have a lot of experience with vision language models, but I would assume that most of the, that more, the jump in performance would be smaller when you increase the weight, the number of parameters, because I would assume that a lot of the power of the model comes from the how, how fine the vision part is trained, and the resolution of it to distinguish between small, smaller and smaller parts of the image.

[00:44:28] **Yam Peleg:** So I would, I would think, I'm asking the people here, is this the case? is this mostly about how the parameters are trained? Others in the vision language model, or do you actually see a large performance jump in using a larger base, for example, because I would just guess that. It's the vision part, just, but you got, 

[00:44:51] **Alex Volkov:** Junaid, go ahead.

[00:44:51] **Nisten:** you can tile it that, that's why you can tile it. But yeah. Ian, go go, go ahead.

[00:44:57] **Junyang Lin:** Yeah. I think, you can use a small vision language,vision adapter,a small VIT This is, our experience. you can use a very small VIT and use, use a very large, language model. It is good. we have tried apple's, DN it is a really, really great model.

[00:45:11] **Nisten:** Yes, sorry, just really quick. To Jan, you can put four images together, you can, you can put nine of them together. So in that case, I would guess just from common sense, a larger language base would help to understand, tiling. and there's no real, limit to how much you can go with that.

[00:45:30] **Nisten:** You can put more tiles of smaller language models. There's a lot of, a lot of work still to be done 

[00:45:35] **N8:** in the field. 

[00:45:38] **Alex Volkov:** Yep. And I think that, with this, I think we've concluded the open source section of ThursdAI. We also had, we also had internal LM to talk about, but I think that besides the Apache 2 and some synthetic data that they did, I haven't found anything like crazy interesting, nor state of the art stuff.

[00:45:54] **Alex Volkov:** and we're approaching the one hour mark of our conversation, eh, and we also have some breaking news after this. So for now, for now, I think that, at least I saw in comments that many people came in here for the strawberry or the strawberry discussion, but definitely for the strawberry count, as well.

[00:46:09] **Alex Volkov:** And we're, we're going to try to recap some of this, craziness on X though. This is not our usual style. As you guys know, I like to report on what actually happened and not like speculation, but I think this is too juicy to, to stop because, folks who are unfamiliar, we have a group chat behind the scenes for the speakers of ThursdAI, and there are so many strawberries in the group chat that like, this is obviously impossible to ignore.

[00:46:33] **Alex Volkov:** So let's do a quick recap. for folks who stepped in, in the middle, there's like almost 200 of you here. let's do a quick, just a reset of the space. And then we're going to talk about big companies and APIs and, and, and, and everything in between. and I think we'll start with this week's buzz before.

[00:46:48] **Alex Volkov:** So let's do a quick, a quick reset.

[00:46:56] **Alex Volkov:** so you're on ThursdAI for August 8th, my name is Alex Volkov, I'm here on stage with a bunch of experts in different fields, some, correlating fields, friends of ThursdAI pod co hosts, and it's been incredible so far, we've talked about open source, we've talked about Qwen2, which, Jun Yang, the representative of the Qwen team, the, I want to say, Techly Chief Evangelist Officer, Chief Evangelist Officer of the Gwent team announced live on stage and they just launched it today.

[00:47:24] **Alex Volkov:** We also talked about OpenBMB, 8 billion parameter, incredible vision model that's probably state of the art, beats GPT 4 vision. It's quite incredible to me that we keep saying open source beats GPT 4, open source beats GPT 4, and it's not even a, like a crazy thing to us. it's oh, yeah, sure.

[00:47:40] **Alex Volkov:** this thing beat GB four. and we also talked about Biggie Smalls, from, from Niton here, which is a, the fastest,lm, the smallest, fastest LM that you can possibly run. And then there's a whole conversation here about how, efforts of the folks here on stage and in the audience led to this model running at almost 300 and something, tokens per second on, on single devices.

[00:48:02] **Alex Volkov:** and now. 

[00:48:02] **N8:** 330 tokens per 

[00:48:03] **Alex Volkov:** 330. I'm sorry. I'm sorry. and now I think, before we move on to talk about the big company, APIs, which is like our next big segment, I will slide into this week's buzz. This week's buzz is a, is a place or a category in ThursdAI where I talk about, things that are related to Weights Biases, the place where I work.

[00:48:20] **Alex Volkov:** I'm an AI evangelist with Weights Biases. Weights Biases, for those of you who are unfamiliar, for folks in the audience, is, the leading,world, ML experimentation tooling, and also up and coming and soon to be leading in LLM observability tooling as well with our new, toolkit called Weave, which you should try.

[00:48:38] **Alex Volkov:** And there's a course that I just launched on, on Weights Biases course. You'll have this in the show notes as well, but this is not what I want to talk about in, in, in this corner. This, in this week's buzz today, I want to chat with Mark about our mutual work with Mark Sarofim from Meta and the PyTorch team, and also Wei Wei from Microsoft, if I'm not mistaken, and some folks from my team as well.

[00:49:03] **Alex Volkov:** Mark, so basically the microphone is yours. Could you introduce the challenge and like what we're doing together and how folks can go in there?

[00:49:10] **Mark Saourifm:** Sure, yeah, thank you Alex. I will say you're probably the first person I know who's pronounced my name correctly in the US, so thank you for that. okay, so here's the premise of the competition. 


## [00:49:19] Hacker Cup and Competitive Coding

[00:49:19] **Mark Saourifm:** Like, basically, Hacker Cup is a very old competitive programming competition that's been going on for about 10 years.

[00:49:27] **Mark Saourifm:** it sort of like has a cult following, you can see a lot of sort of communities like Codeforces where people solve like these really, really hard problems and they do it for decades, like basically, the best humans. Need about four or five years of dedicated training before they can like reliably solve the hardest problems.

[00:49:43] **Mark Saourifm:** The reason why this challenge is interesting is because what we've observed is there was like a lot of buzz on Twitter around like coding agents that solve Leap Code style problems. And I want to argue that those problems are not very interesting because they're also solvable by [00:50:00] Googling. Like basically the data is already there?

[00:50:02] **Mark Saourifm:** It's leaked. And these problems are like, they're, they're standard. I would also posit that This is why the main reason why a lot of SWEs really hate lead code, because at this point it's not really a test of cognitive ability, it's more a test of like memorization.the right way to change sort of the dynamic is one, to make the problem significantly harder.

[00:50:22] **Mark Saourifm:** this is why competitive coding is interesting. And two, not release the test set until the day of a competition. Basically, the way this is going to work is that the competition will, in HackerCup, will now have a human track and two AI tracks. One for open models and one for closed models. When the competition opens up, humans will see a problem.

[00:50:41] **Mark Saourifm:** They'll copy paste, the problem into their model, they'll run it, and then they'll spit the output back out. basically, none of those models have access to this data. our suspicion, at least if you use chat dpt or clod with, chain of prompting, with linting, and, with a human in the loop to solve problems, we've managed to solve one practice problem out of, about, 40 problems, and the interesting thing about a lot of these problems is that it's not like even they require a lot of code, often there's a mathematical trick or an insight.

[00:51:13] **Mark Saourifm:** one problem, we call it the dim sum problem, has a two line coding solution where no LLM opener closed has managed to solve it.so we really, our goal here is to really push the state of the art of AGI, of competitive coding, and whoever wins this competition, in our opinion, will have a very commercially interesting model that can solve like very novel agents.

[00:51:35] **Mark Saourifm:** And at this point, if a model does make a significant dent of this competition, I think people would need to acknowledge that, LLMs can do a form of planning.

[00:51:45] **Mark Saourifm:** This is incredible. And, you guys also organized a series of Of, kind of like getting folks up to speed. And I will invite folks to also participate in those because I think you're speaking there as well, Mark?

[00:51:57] **Mark Saourifm:** That's right, actually, yeah, So so, so thanks to a lot of our friends at Weights Biases. we, we approach this problem in two ways. one is, it's obviously a community effort, and for context, last year at the NeurIPS LLM Efficiency Competitions, the winners were not, famous people in the ML community, they were people that came out of nowhere, they did, a very interesting effort with, regards to data curation, and then they won.

[00:52:19] **Mark Saourifm:** similarly, I think, what we're doing now with, the Weights Biases team is, we're setting up, about, six lecture series. where we're inviting some of the best people in the sort of, in, in the code generation community. So you'll, you'll have people like Omar from DSPI, Ofer from,from the SWE agent team.

[00:52:35] **Mark Saourifm:** like we have folks from the TorchTune team, from Weights Biases. So we really want to lift the floor and that way people can if they have an interesting take on this problem, we, we want, we want them to participate as well.

[00:52:46] **Alex Volkov:** So everybody's welcome. I pasted the link, in the show notes as well. And, obviously if this is of interest to you and you want to participate in this Hacker Cup and, and if you're going to NeurPS, even if you don't, I think this is, this works via the Discord, right? Like you don't have to be there.

[00:53:01] **Alex Volkov:** Correct me if I'm wrong, 

[00:53:01] **Mark Saourifm:** Yeah. Yeah. Yeah.

[00:53:03] **Mark Saourifm:** that's right. basically, the, the, all of the competition is essentially going to be happening online, both HackerCupand the, and, and participating in the Discord community. NeurIPS is more of a cherry on top. I think if I, if I recall, Alex, you were there at the workshop year, if I, if I remember correctly.

[00:53:19] **Mark Saourifm:** so hopefully there are the ideas that we would also invite interesting speakers in the code generation community. So if you are going to be in NeurIPS in Vancouver, you can come hang out. And if you are going to be one of the winners, we'll invite you to basically co author,like the workshop paper with us, where we synthesize the lessons from, from the, from, from the best submissions.

[00:53:37] **Mark Saourifm:** So super, super cool. And, I'm, I'm very, very excited to take a look at all of these, incredible guest speakers. and I've added the, the, the link to the show notes as well. So if you're into, like code generation, if you're into solving problems, all of this, definitely worth checking out. Mark, thank you so much for coming up.

[00:53:54] **Mark Saourifm:** Feel free to stick around with us. Cause we're going to talk about a bunch of other stuff, going forward. this concludes the, the, this week's buzz though, because we have a bunch of other to talk about. Yeah, go ahead. Yeah. Okay. So moving forward, I see, you're trying, you're trying to bait, bait, bait strawberry back in.

[00:54:09] **Mark Saourifm:** So before we, before we get to the strawberry, 

[00:54:11] **Mark Saourifm:** the expert in the field, the 

[00:54:13] **Mark Saourifm:** the expert, 

[00:54:14] **Mark Saourifm:** to get the expert 


## [00:54:15] OpenAI's Structured Outputs and API Updates

[00:54:15] **Mark Saourifm:** strawberries in the field, before we get to the strawberry kind of debate, I want to super quick, talk about OpenAI's, structured outputs in API. So OpenAI,announced, a new approach, probably new models. definitely new, a new training for their model.

[00:54:30] **Mark Saourifm:** They talked about how, how they actually achieved this. OpenAI introduces structured outputs in their APIs and also. Drop prices as well. And so under the hood, they did they improved reliability for their models to match Jason's schema. So developers can provide schema. I think, I see Matt Schumer with us as well.

[00:54:48] **Mark Saourifm:** Matt, a friend of the pod often comes up and gives like incredible deep dives. Have you had a chance to play with, structured outputs yet? Does this affect significantly the stuff that you guys do? and do you want to give us a brief overview of how, how cool this is?

[00:55:02] **Matt Shumer:** so you're actually going to be disappointed. Also, thanks for having me. I have not played with it. I've actually barely played with any of the structured output, solutions. Pretty much anywhere. I've essentially found that with good enough prompting, you can essentially get what you want without needing to deal with some of this.

[00:55:17] **Matt Shumer:** And I was seeing reports that, for example, OpenAI structured output is quite a bit slower than their normal API. So I personally haven't had a real need for it. Anything I can do with prompting, which is rare, because prompting really is, quite good for most of this stuff. You can use things like function calling.

[00:55:31] **Matt Shumer:** And for Hyper8, most of what we do in prod is based on fine tuned models because the scale that we're at requires it. so we essentially just, if we need JSON, we just fine tune the models to always use that format. then there are things like JSONformer, that was from, I think, a couple years ago that's interesting to look into, but personally, I haven't really had a need.

[00:55:48] **Matt Shumer:** It's interesting. I feel like a lot of what OpenAI has shipped recently has been, very interesting technical solutions to problems that sort of exist. not solving the bigger problems. 

[00:56:00] **Matt Shumer:** at least my take. Can 

[00:56:01] **Alex Volkov:** All right. Take taken. but, but I want to read out, the, the kind of, so you, you, you basically say the same thing that they, touch on. They say a lot of people just do prompting and they actually have a comparison chart between prompting alone and the percentage of how, how, how much their model prompting alone adheres to a schema, not just outputting JSON, specific JSON, but like a specific schema, schema defines like what type of fields, etc.

[00:56:25] **Alex Volkov:** And, they said that, even though their newest model, was trained to understand the complicated schemas and how best to produce outputs for them, just prompting that didn't give them like the, the response they wanted, they only got 93 percent on their benchmark. and so they went, they wanted to do a deterministic engineering based approach, which we know in this field of LLMs, determinism is not something that's like a super easy to do.

[00:56:48] **Alex Volkov:** And so they did a constrained decoding approach, which achieved a hundred percent reliability on structure. So if you, if you pass strict equals true, while Matt, you're probably right. It's probably going to be a little bit slower, for folks for whom this is like extremely important to get the same exact schema back all the time.

[00:57:04] **Alex Volkov:** And for many developers that develop with. Something identical in Python or, or, with, with Node as well, with TypeNode as well. So they support in their SDK now, this constraint, like decoding with schema providing. so that's super cool. Many people do actually want this. There's a few libraries that, that this is what they do.

[00:57:23] **Alex Volkov:** Instructor and,Type, TypeChat, I believe, and also Marvin. There's a few libraries now that, folks don't necessarily need to use. And the digital thing they announced during this blog post is that, Oh, by the way, this model is now 50 percent cheaper. And it's like with no fanfare at the end, quietly, Oh, this model is now 50 percent cheaper.

[00:57:42] **Alex Volkov:** What often happens though, with these models from OpenAI that they release is that people get excited about them. And they're like, Oh, this model is exactly the same, but cheaper. And then folks find out that it's not quite exactly the same. And sometimes this model actually is like a little bit less, less good as well.

[00:57:56] **Alex Volkov:** 

[00:57:56] **LDJ:** Yeah, I think it's also worth noting that, there's a recent benchmark called ZebraLogic that a lot of people are looking towards since it seems to be a pretty good proxy for reasoning in models. And Cloud 3. 5 SONET was number one for a while, but with this new GPT 4.

[00:58:10] **LDJ:** 0 model, at least in the easy version of this benchmark, before it was about,10 or 12 percent gap between GPT 5 SONNET, [00:58:20] and now 3. 5 SONNET is still ahead, but GPT 4. 0 version is now only like 2 percent behind. So it seems like they might have made some type of a significant, reasoning increase to this new GPT 4.

[00:58:33] **LDJ:** 0 version as well. 

[00:58:34] **Alex Volkov:** that's from Allen Institute for AI, if I'm not mistaken, the ZeroLogic. And so you're basically, this model now climbs, climbs higher. oh, it's now at the top, right? The leaderboard and code. And, yeah, 

[00:58:50] **Alex Volkov:** In ZeroEval, it's number one, but in ZebraLogic itself, which is a subset of ZeroEval, in ZebraLogic, it's still, I think, behind 3. 5 Sonic. 

[00:59:00] **Alex Volkov:** know, and then go ahead and then yum.

[00:59:04] **N8:** yeah, I just wanted to back that up. I have my own, personal benchmark that I have of, lateral thinking puzzles, and I, ran the new GPT4L on that, and it scored roughly, Five to ten percent higher than all previous models and outscored the previous version a ton. So and these are like really hard lateral thinking puzzles that require like innovative reasoning ability.

[00:59:24] **N8:** So I'm just really excited about that because it's I think they did make a breakthrough with reasoning. 

[00:59:29] **Alex Volkov:** Wow. All right. All right. interesting. They're not talking about like any specific kind of advances in the model itself. They are talking about they, they trained it to be better on structured output, but you're saying just generally on your tasks, on logic, it also performs better compared to other GPT 4s, 4 O 

[00:59:45] **Alex Volkov:** Yeah, the previous version got 0. 7, and this new version is getting between 0. 75 and 0. 77, which is pretty big considering that. 

[00:59:56] **Alex Volkov:** oh, that's awesome. 

[00:59:57] **Alex Volkov:** It's getting one to two more questions right. 

[01:00:00] **Alex Volkov:** yeah. that was great. Yeah, go ahead.

[01:00:02] **Alex Volkov:** Yeah, I just want to, I just want to add a little bit of background to about the whole thing everyone is talking about. the thing is that, we are at a point where there are many benchmarks and many tests. And there are models that are really good on this benchmark, but somehow people call it a big bottle smell.

[01:00:22] **Alex Volkov:** They, they are good on the benchmark and they look nice, but there is something that Different models just feel a little bit better. Even the benchmark that uses humans to choose which model is better on the same prompt, even there we can't distinguish what the thing is. So what everyone is talking about right now is different type of tests that try to capture this very Hard thing to capture, whether it's, Zebra logic or, or different logic or, or different benchmarks that people have on their own that they developed and are not releasing because as soon as you release something and talk about it, the models learn somehow, the models somehow get better on it, And it doesn't capture the same thing. the feeling is still, the big model smell still there. This is why you see all those new benchmarks that are, Wild and new and, and try to test very hard things. And, and so when a model gets really good on those types of benchmarks that no one saw except for you, it means something because we all just want to get the ranking that aligns to the best way possible with the feeling that you have towards the model.

[01:01:36] **Alex Volkov:** so that's, that's what everyone's talking about. A big thing when you have a model that. Pretty much everyone agrees on benchmarks that are wild, and there is no way it was trained on, or even not trained on, even was tested during training by the developers on. It's a big thing when a model gets better on this.

[01:01:54] **Alex Volkov:** So this is what everyone is excited about at moment, 

[01:01:57] **Alex Volkov:** and I think it's great. Yeah.

[01:01:58] **Alex Volkov:** And I think it's absolutely worth mentioning that, like you said, there are a bunch of different evaluations that people don't expose to the internet. So these models can't like, learn on, and that's why we're trying to get as many folks from those evals and benchmarks to come in here and tell us directly.

[01:02:14] **Alex Volkov:** but also we're trying to collect as, our, our vibes, feelings we're trying to add by adding up all of those different ones. And some of the ones that I'm looking at as the AIDR. chat. Ader is a, a mark. I think, I don't know if Ader. Ader is the, a non agentic kind of, code writing agent and they have a, LLM leaderboard as well for code editing specific.

[01:02:36] **Alex Volkov:** Not code writing, but code editing. and Ader has their own like a benchmark LLM that I've been looking at for, for quite a while. Sonnet is still the top one here. and this new model gets, that's very close to the top, I think 90. 8 percent correct edit format, which is great. And then also BigCodeBench, we talked with Terry Yu here on, on, on the podcast and then,LifeBench from, from BinduReady and supported with Yann LeCun, so we're looking at a bunch of different leaderboards also to get like a sense, to not just, to not just look at LMSys Arena, for example, any other comments on this before we talk about the other OpenAI stuff.

[01:03:13] **Alex Volkov:** plus 

[01:03:13] **Alex Volkov:** one for ZebraLogic. I've also found it when I was testing DeepSeaCoder that that benchmark reflected most accurately how smart the model was at solving issues. Just from a practical perspective, I've never looked at the dataset, I've never ran the benchmark, but whenever I saw the rankings there, it fit with, my 

[01:03:35] **Alex Volkov:** anecdotal views as well. 

[01:03:37] **Alex Volkov:** We should, we should get Bill, Bill in here to talk about ZebraLogic next. I'll reach out. Yeah, I have some friends in LNA. We should get Bill to talk about ZebraLogic here on stage. and then go ahead and then we'll move on and talk about, 

[01:03:48] **Alex Volkov:** yeah, I'll be really quick. I just wanted to shout out AgentBench. It's a really unique benchmark that some of you might have seen, and it's designed to capture the big model smell. It, rates the original GPT 4, Yam knows about this, from, March, the original release, way over GPT 4. 0, and it basically tests the model's ability to give it a query, say, a query.

[01:04:08] **Alex Volkov:** Tell me an interesting story, give me an interesting fact about World War II, or summarize the Dark Ages. Test the model's ability to generate novel answers that aren't like its previous ones and still make sense. And this ended up correlating to, the ability of a model to have a lot of unique responses, and to have an intriguing latent space, and to not be hyper optimized to deliver one really, really, clean answer.

[01:04:33] **Alex Volkov:** And it's very refreshing, and it uses an LLM to verify if a model's answers are nonsensical, and an embedding model to ensure that they're distinct. And I think it's pretty cool. I'll attach the link below. 

[01:04:43] **Alex Volkov:** Alrighty, thank you, thank you. 


## [01:04:44] Strawberry Conspiracy: Theories and Speculations

[01:04:44] **Alex Volkov:** Um Okay, folks, I think it's time to talk about some, some fruits and some . I think LDJI think I, I called you like yesterday because I haven't caught up, like to all the drama, even though not, not even drama. but I, I, I, maybe I'll do like the preface. Yesterday Sam Altman posted a, an image.

[01:05:02] **Alex Volkov:** Of, it said it's a nice summer day in the garden. And this is, this was an image of strawberries. And then the internet freaked out. LDJ, could you tell us why the internet freaked out? what was going on? what's so special about this image?

[01:05:16] **Alex Volkov:** so I guess for some of the lore, I think I actually put something in our group chat that I'll just scroll up for and reference that real quick. 

[01:05:23] **Alex Volkov:** Yep.

[01:05:24] **Alex Volkov:** but essentially there's been leaks going on for a while, or alleged leaks of course, like you never really know if they're true or not until the company ends up confirming them.

[01:05:32] **Alex Volkov:** But, there were some rumors over the past few months I think by articles published by Bloomberg, Reuters, the information that are all generally considered pretty reputable, saying that QSTAR is now part of something called STRAWBERRY, or now has been renamed to STRAWBERRY, something of that sort, and is on the cusp of having a new type of reasoning breakthrough, or a new level of reasoning that wasn't previously capable of current models.

[01:05:58] **Alex Volkov:** And, this is just in the past few months, and prior to that, of course, there's a lot of rumors and talk about something called QSTAR, which also still vague, but also around that same line of reasoning. Being better at reasoning, being better at math, and things like that. So as soon as Sam Altman, just yesterday, I believe it was, he posted a picture of a bunch of strawberries.

[01:06:19] **Alex Volkov:** And everybody's going wild, and he almost never posts on Twitter. So that's a big thing. And then a few hours later, you have Roon, who's also rumored to be an OpenAI employee. He's posting

[01:06:30] **Alex Volkov:** I think confirmed. think confirmed at this 

[01:06:34] **Alex Volkov:** I think so. I like still a kind of pseudonymous or something, but he posted a picture [01:06:40] at a, I guess a party, it seemed or gathering with people.

[01:06:43] **Alex Volkov:** And there's just a table with a pile of strawberries on top of it. And another OpenAI employee said that he's at an OpenAI dinner and posted a picture of a plate with just a single strawberry in the middle. so it seems like they're at a strawberry themed party or something, and they're alluding to a lot of things. 

[01:07:01] **Alex Volkov:** And so what could they be alluding to? Yam, what do you think?

[01:07:07] **Alex Volkov:** Okay, there is a little bit more to the story, 

[01:07:11] **Alex Volkov:** Yeah. Please give us. 

[01:07:12] **Alex Volkov:** conspiracy theory, conspiracy theories start a year ago. First, I don't want to spread conspiracy theories. I had a little bit of time a couple of hours ago, so I wrote a thread, I don't know, about what happened last night. It was part of, look, it was funny, look, and just, just look at everything that happened, and I don't want people to think that anything of this is more, than just a theory.

[01:07:32] **Alex Volkov:** I guess let's have fun in conspiracy theory. That's first. Okay. I don't know anything. Yeah,

[01:07:38] **Alex Volkov:** the thing goes like this. Last year at the end of, 2023, there was, an incident that, we don't really know a lot about, about the Altman leaving open ai. Then coming back and, and I, Ilia is, disappearing for a couple of months later and everyone started conspiracy.

[01:07:57] **Alex Volkov:** The theories started. What did Ilia see? And, and, it started there. and so there were rumors and leaks about a new algorithm that, algorithm or training method or whatnot, that heavily improves models, models, reasoning and capabilities and so on called QSTAR. We know nothing about it, except that, it might exist.

[01:08:19] **Alex Volkov:** Okay. That's, that's the thing. Now, a couple of months later, and there were many conspiracy theories about what is going on. We don't really know, okay? It's not a big secret that OpenAI are working on better models, future models. This is what they do. It's not a secret, okay? The thing is that we had some major publications calling it a code named Strawberry now, and yesterday, not only we got some, I don't know, strawberry themed stuff, we also got from pretty, I don't know, confirmed sources I'd open AI, but I think, I think that, a new model is going live, strawberry is going live, and we had a new account popping out of nowhere, talking about strawberries a lot, a lot, like a lot for a human, a lot.

[01:09:15] **Alex Volkov:** And things started to explode for, a couple of hours everywhere. That's 

[01:09:22] **Alex Volkov:** in general

[01:09:23] **Alex Volkov:** for, for us in our bubble. And this account, joined our space in the beginning a little bit, which, I was just like, I won't try to summarize everything, but before I get to LDJ and then Nate, I will say, yum, your, your position was that this account potentially could be run by like an agent that's using this like new model and this is super advanced, right?

[01:09:42] **Alex Volkov:** This is the game we're playing. This is the kind of the assumption.

[01:09:46] **Alex Volkov:** I don't know. I'll start by, I don't know. I have no idea, all I'm saying, and what got me to this thinking is that it was a little bit too much for a human, it was way too much in terms of volume, and also aligned with people in OpenAI saying the project is going live, we're starting, and the accounts saying it all the time, again and again and again.


## [01:10:11] Speculations on Strawberry AI

[01:10:11] **Alex Volkov:** So I just thought, and maybe many other people also got to the same conclusion, wait, it might be a model, because it's everywhere. thousands and thousands of tweets, come on, what human can even do this? And, I don't know, I just started to interact with it, and, and I don't know, I just posted everything in a thread if you want, I don't want to spread conspiracy theories.

[01:10:33] **Alex Volkov:** Probably, Strawberry, the real one, is And you would model anyway, so that's 

[01:10:37] **Alex Volkov:** my take. Sure.


## [01:10:38] Technical Feasibility of Strawberry AI

[01:10:38] **Alex Volkov:** my super quick, very logic based, reaction to this, given that, whatever account joined the space and then reacted to something I said, with my voice. I don't know if they have the technical ability to, to pipe this sound to a model while also learning how to join a space on X.

[01:10:54] **Alex Volkov:** I don't think that that's like super straightforward via the UX. so it feels like a person just like saying, Hey, I'm just like LARPing, but we'll see. LDJ, you want to, you want to comment and then, Let's comment on the strawberry a little bit.

[01:11:05] **Alex Volkov:** Yeah. 


## [01:11:06] Confirmation of Strawberry AI Subdomains

[01:11:06] **Alex Volkov:** So I remember now that there is actually technically some type of confirmation we have of something called Strawberry OpenAI because there's a lot of people that kind of stock the subdomains that are registered under like the main OpenAI. org or OpenAI. com main domains. And within those subdomains, there is some registered that say things like Strawberry and the name of it.

[01:11:30] **Alex Volkov:** And say things like, Straw, CUA, and CUA is usually an acronym used for Computer Using Agent, which basically, in other words, means something autonomously using a computer. 

[01:11:42] **Alex Volkov:** something like some, something that could use Twitter, for example, the UI to do stuff 

[01:11:48] **Alex Volkov:** oh, actually, that's, yeah, I didn't even connect that, but theoretically, yeah. And, 


## [01:11:53] Bloomberg and Reuters Reports on Strawberry AI

[01:11:53] **Alex Volkov:** Oh, these subdomains that include the word straw or strawberry within them, there's two or three of them that popped up over the past two weeks, and Bloomberg and or Reuters reported over the past two weeks that on specifically July 9th, OpenAI held an all hands meeting where they actually demoed or demonstrated some type of strawberry capabilities to all the employees, and I guess maybe announced their progress on the project.

[01:12:18] **Alex Volkov:** And on that same day, there's a sub domain registered on that same July 9th day that says large lang demo external. So there's like a lot of things coinciding there and confirming at least a lot of the things coming out of Bloomberg Reuters.

[01:12:36] **Alex Volkov:** So we have a leak from Bloomberg. We have some OpenAI employees. we have some LARPers, but definitely yesterday. Either the folks are playing into this meme. , but we definitely have, like Sam Altman, we have a bunch of folks from OpenAI jumping in on this and like doubt that this is the meme. 


## [01:12:53] Community Reactions and Speculations

[01:12:53] **Alex Volkov:** Like, it seems that, it's all but confirmed that like at least something is happening.

[01:12:58] **Alex Volkov:** Though we do remember Sam Altman sometimes does, he went into Reddit and said, a GI was achieved internally. And then basically 

[01:13:04] **Alex Volkov:** yeah. 

[01:13:05] **Alex Volkov:** We remember that the person has the ability to troll. Like we remember this from previously. However, a lot of times it's best since then. And this is also like more, more folks confirming with strawberry pictures.

[01:13:17] **Alex Volkov:** So at least something's happening now. Now what? we'll see. N8, go ahead. What's your, what's your take on this? And then Nisten, I would like to hear you like, just like,your take.

[01:13:28] **Alex Volkov:** the strawberry guy for a while. Weeks ago. And August 1st, he was active, he was going crazy, yapping about strawberries, pinging chatGBT, begging Sam Altman to release something, nothing happened. And he goes right back to the grift. He has been tweeting out strawberries since then.

[01:13:44] **Alex Volkov:** For weeks, I don't know when he first showed up on my feed, but I've been around him for a long time, and this account, what it does is it constantly hypes up a hype cycle with KingSamOutman. ChasCPT responds randomly occasionally, but then nothing actually happens. So I, at least my conjecture is this account's probably a LARPer or someone who's pretty desperate for attention, and then Sam A might be engaging with this account to generate actual hype for Strawberry, which is probably a real thing.

[01:14:13] **Alex Volkov:** So I think the, Then again, that's just a hypothesis, but I doubt the account is truly like a legitimate source of leaks or like a secret AI model because it did the whole strawberry schtick before a week ago begging for something to be released. It was wrong, and then it moved along. 

[01:14:29] **Alex Volkov:** Yeah. Okay. I, I'm. Yeah, I don't know. LDJ, go ahead. Read out the history super quick, and I think we can move on. I think speculated enough, 

[01:14:37] **LDJ:** Yeah, so here's the brief summary of the timeline of of a report from Reuters and the information in Bloomberg. 


## [01:14:43] Summary of OpenAI's Project Timeline

[01:14:43] **LDJ:** So around 2021 it's allegedly said that project GPT 0 started internally at OpenAI and that involved a couple of employees and it's named after AlphaZero which is called Focused on being able to scale up inference time compute [01:15:00] for better problem solving, and as well as hopefully allowing self play and reinforcement learning, things like that.

[01:15:06] **LDJ:** Then a few years later, apparently that GPT 0 became QSTAR, with more advancements being made, and then Sam Altman said that some type of breakthrough was made around November of last year, he said this publicly. And then, apparently in these past few months, it's become something now known as Project Strawberry, and now There's other people involved, and some, one of the original people said to have been involved, Jacob Paciocchi for QSTAR. He's now Chief Scientist of OpenAI after Ilya Setskover left as well, which is interesting. And yeah, that's pretty much all the details of the timeline.

[01:15:40] **LDJ:** He's one of the early people or co founders as well, right? Jakub Jakub? Jan, go ahead. Thanks, LDJ. 


## [01:15:47] Integrating RL Agents with LLMs[01:15:47] DeepSeq's Content Caching Innovation

[01:15:47] **Alex Volkov:** Uh, all right, folks, I think we're moving on forward to actual reporting and not, speculation, because we have a few more stuff to talk about specifically around, around one thing I want to mention, because I think that this is going to be the future.

[01:16:00] **Alex Volkov:** And I want to hear like thoughts super quick is that DeepSeq. The folks from DeepSec in their API introduced something called content caching on disk, which significantly, if, if, if you don't know what content caching means, and we've talked about content caching after Google I. O. for a little bit, the problem with large language models, especially with like agentic and content caching, Content, constantly repeating queries.

[01:16:20] **Alex Volkov:** There's a lot of like repetitive inputs, especially when like with the chat, every time you send the chat query, the model basically gets all the previous chats, as an agent loop runs the, the, the model gets all the previous chats in every, in every new request, basically the context window grows.

[01:16:35] **Alex Volkov:** and this leads to unnecessary commutation, just, And then DeepSeq basically implemented caching. Caching is a known problem in, in software engineer world, but here in the LLM world, like the first time I heard about something like caching was, like productionized caching was from, from Google.

[01:16:51] **Alex Volkov:** They said that they're going to introduce this in lower costs, but you have to opt into this. DeepSeq implemented this kind of automatically. And, when you hit the caching on their end, you basically get a 90 percent reduction in price. Cachemist costs you 14 cents, which is still ridiculously cheap.

[01:17:07] **Alex Volkov:** I think like 14 cents is one of the cheaper APIs out there, if I'm not mistaken, for this level of intelligence. 14 cents per input tokens, per, M tokens per million tokens. If you, if you hit the cash, it's going to be 0. 14. So there's going to be like one, 1. 4 cents. If you hit cash per million tokens, 1.

[01:17:26] **Alex Volkov:** 4 cents per million tokens, if you hit the cash and, and they claimed that 90 percent of the back and forth, conversations are just like you bypassed recomputation, because they just they, they analyze what you sent, which is quite incredible. I haven't played with this yet. I haven't played with DeepSeq API too much.

[01:17:46] **Alex Volkov:** I just played with it a little bit. I want to hear maybe from Nisten and Matt as well from you. I want to hear if, just, just thoughts about why isn't everyone doing this? And will this become like an industry standard?

[01:18:00] **Alex Volkov:** in 

[01:18:00] **Alex Volkov:** a way, they are, but it's not, it's not complete. there's a little bit more going on here with how DeepSeq do it. Because DeepSeq always does some, some, some next stuff that people don't even realize what happened. cloud projects, if you use Sonnet 3. 5 and you use projects, is also part of context caching.

[01:18:21] **Alex Volkov:** And, when you hear this in combination with speculative decoding That's also a form of, of, of KV caching. So DeepSync is just, is putting together speculative decoding. And the KVCache. Now, why does this matter? Why is this any good? You can also do this on your own. You can do this on your own with Llama CPP.

[01:18:43] **Alex Volkov:** And, the simplest way you can implement this on your own is you have a very long conversation, let's say you had your lecture. you're in school, you had your lecture. What you do is you preload that. In a cache file, and you can do this on CPU, by the way, I'll always show CPUs, and,so now you have your like 30, 000 tokens of your professor talking or whoever was talking.

[01:19:06] **Alex Volkov:** And then, you save it on disk, so there's going to be a couple of gigabytes of that context. And then you start off every conversation from that, and you don't have to recompute it, so you don't have to wait again, because it takes a while for 30, 000 tokens to actually process, whereas loading it from disk is just, it's free.

[01:19:25] **Alex Volkov:** DeepSeek went a step ahead in this, and also did caching for, for other queries. So they, they've done this in a more advanced and dynamic way, but it is essentially quite similar to how cloud projects works, you add in a bunch of papers or a bunch of code. And, Yeah.

[01:19:45] **Alex Volkov:** it's, it, everyone should be using it this way. Everyone should be using LLMs this way. 

[01:19:53] **Alex Volkov:** Interestingly, 

[01:19:54] **Alex Volkov:** It's, it's pretty big deal. Yeah. 

[01:19:55] **Alex Volkov:** the Gemini kind of approach is that you opt into this and you decide where, what I like about DeepSix approach is like, it's automatic. Once they detect the same input tokens, they just automatically like turn on the caching and they, they read from disk, which is super cool. Matt, if you want to chime in on this as well, feel free because there's price significant here and you guys are running a lot of millions of tokens, super back and forth.

[01:20:21] **Alex Volkov:** Yeah, I haven't had a chance to use it personally, but this is one of the innovations that I'm actually really, really excited about for a few reasons. but the main one that I really think about is for many things, not all, for many things, I think we're moving away from this sort of era of fine tuning to scale, and fine tuning to get really, really great results, for specific tasks and towards many shot prompting.

[01:20:42] **Alex Volkov:** as an example, some agent tasks that we've tested. You can fine tune a model on a million examples, and a million good examples, use a ton of compute to do that, go through the complexity of that, the complexity of then serving that fine tuned model as opposed to, a prompted model.

[01:20:57] **Alex Volkov:** or you can show, let's say, Gemini 1. 5 Pro with its really massive context window, a hundred examples or even less. And often what I find is that the prompted model actually does quite a bit better than the fine tuned model. I think there are many possible reasons for this. but whatever the reasons are, that's powerful. And if you can cache all those examples, suddenly you have the ability to do like fine tuning on the fly, but it doesn't cost you all that extra, all that much extra to actually serve. so I think it's actually quite powerful. I've been hoping that this trend continues and more providers start to add this because it would make developing really robust and really reliable, and really good LLM applications that aren't just, you know,one shot or few shot prompts, really possible for the first time.

[01:21:42] **Alex Volkov:** So that's what I'm really excited about here. I think there are definitely other. Really interesting things like, put your entire code base in there, that sort of stuff. But for me and how we use LLMs in our products, I am very, very excited about the idea of like,instead of generating, or instead of gathering a million examples and doing that fine tuning process and going through the hell that that is, because it's not fun, instead just saying, okay, let's curate a hundred gold examples that we know are fantastic and show the model the few things we really wanted to do really well, and suddenly you have something that's better than if you fine tuned it, and it's cheaper, and it's faster, and you don't have to worry about managing infra.

[01:22:17] **Alex Volkov:** I think that's quite powerful, so I'm super excited about that. 

[01:22:20] **Alex Volkov:** I'm with you completely on this because we've talked about long context versus like rag or anything like this. And one of the things that always came up, always, was cost and speed. Cost and speed were like the two things that people talked about reg, obviously citations and everything. this is the first thing that starts to show that long context can still win potentially down the future.

[01:22:42] **Alex Volkov:** And the, the two things that were going for reg, like speed, et cetera, this now directly attacks those kind of arguments against long context. Against using those a hundred, thousand examples, for example, because again, if you like, if you cache all those back and forth, And they are immediate and they cost one cent per million, one cent per million tokens.

[01:23:01] **Alex Volkov:** I can't believe I'm saying this. Like literally, I can't believe that these words are coming out of my mouth. It costs one cent per million input tokens to do in this caching. if they're cached, then, then, then it's it's basically nothing. Like it's basically, you don't even count this.

[01:23:17] **Alex Volkov:** Yeah, I will say for RAG [01:23:20] specifically, when we're talking about the traditional form of RAG, not like whatever people are doing today with it or whatever they're calling it, even if it's not actually RAG. But when I say RAG, I mean like pulling in lots of data to answer questions based on the data.

[01:23:30] **Alex Volkov:** I still think the models have a little bit of a way to go to be able to use their context effectively enough to make inferences based on multiple different positions in the data. But when we're talking about things like, let's just say an agent type task, like some of the stuff we do, you're not needing to remember every single little thing in the data.

[01:23:46] **Alex Volkov:** You're needing it to understand how to do something. And that's what the context window is good enough for today. So very, yeah, very much thought on with everything you're saying. I think it's going to be huge.

[01:23:55] **Alex Volkov:** And I'm hoping that more folks will implement this and Nisten, you're probably right. Like it's implemented behind the scenes for many folks. Like I'm hoping that more folks in the API provider layer will expose this to developers. And a quick comment on this and we're going to move on from, from gaffing to another topic.

[01:24:09] **Alex Volkov:** Super quick.

[01:24:11] **Alex Volkov:** Very quick.

[01:24:11] **Alex Volkov:** Yes. DeepSeek is especially well suited for this because their model uses, I think, multi head latent attention. Tior Taxis knows more about this than I do, but what it is, is basically they can store the, Cast tokens using lower rank vectors than most other models, and that can result in much less cache space for many more examples, and that's why they can serve their caches so cheaply. 

[01:24:38] **Alex Volkov:** Oh, interesting. Oh, that's, that's awesome to know. Thanks. This is 

[01:24:41] **Alex Volkov:** One additional thought actually, total side note here, but I could see actually within the next couple years some major model providers start to enable fine tuning, but it's actually this under the hood. And they may not explain this to the user, maybe they will, but I wouldn't be shocked if we started seeing like actual model providers saying look, find your model, and you upload the dataset, and you press go, and it's not actually doing any weight updates, it's just essentially 

[01:25:04] **Alex Volkov:** caching all the examples. 

[01:25:06] **Alex Volkov:** Haha, that's interesting. I think you did a great segue to the next thing that I wanted to like super quickly, mention. And speaking of, like names that people call things and those are not the actual things. 


## [01:25:15] Mistral's Fine-Tuning and Agent Updates

[01:25:15] **Alex Volkov:** Mistral came out with a quick update of their finetuning system. So now you can, the, the model that came out.

[01:25:22] **Alex Volkov:** Was that a week ago? Was that two weeks ago? I don't even remember. I think two weeks ago. Mistral Large V2, which is also GPT 4 bidding model on some, some metrics. That model is now fine tunable on their platform, the platform, and then they announce also agents in their platform. So the fine tuning version of, of Mistral's API, you can upload, like Matt, you just said, and I think that they are updating weights.

[01:25:46] **Alex Volkov:** You can upload a bunch of data of yours, and then they will host the fine tuned Mistral large v2, fine tuned for your task on their API. I think the pricing they didn't mention, but I think the pricing stays the same, which is quite incredible. And, oh, by the way, they have a native integration with Weights Biases.

[01:26:02] **Alex Volkov:** So if you want to see how that finetuning process goes, you just need to plug in your Weights Biases key. And, that's, that's super easy. And everybody should do this. Everybody should have this integration. But then also they announced agents. And very interestingly, and I don't know if this is like a French thing or anything, but their agents are not agentic.

[01:26:20] **Alex Volkov:** There's no loop in there. What their agents are is like very similar to GPTs or projects in on topic, where you upload or share examples for few shot prompting, and they pre save this. And, they basically, then you can deploy those agents either via their API. So you can like then talk to, It's kind of like, it's like the, the fine tuning without the fine tuning, the math you just mentioned.

[01:26:39] **Alex Volkov:** Also, you can upload like a bunch of few shots and then they will expose an API input for you, and then you can talk to this model, but fine tuned for your, like few shot examples with a specific system prompt, but again, it's not agentic, at least to this point, they said that may in the future, they're working on adding tool use, but right now there's no tool use.

[01:26:58] **Alex Volkov:** And you also can deploy this on their chat platform. And if, if it's deployed on the chat platform, it's free. To use for your team members. like GPTs in OpenAI, like projects in Entropiq, like similar to this. Mistral now also has, but not, not super agentic, which is, which is very interesting.

[01:27:14] **Alex Volkov:** It's still in early alpha. it has potential. And, OpenAI just shared a thread. Let's do it, folks. Let's do it. I think, I think this is it, maybe. Is it? No, it's not. I got excited. 


## [01:27:31] OpenAI's GPT-4.0 System Card

[01:27:31] **Alex Volkov:** OpenEdger shared, we're sharing the GPT 4. 0 system card. End to end safety assessment outlines what we've done to track, address safety challenges.

[01:27:39] **Alex Volkov:** This is not the strawberry thing, right? No, they just talk about system challenges, a hundred red teamers across 45 languages. And I'm reacting in real time. Like I'm seeing this tweet as it comes out. Yeah, 

[01:27:53] **Alex Volkov:** Okay. 

[01:27:54] **Alex Volkov:** minute heart attack, not strawberry. Relax, everyone. Breathe. system card focus on evaluating the novel risk presented GPT 40 audio capabilities as well as the guardrails we implemented to prevent the generation of harmful biased copyright content.

[01:28:06] **Alex Volkov:** we care deeply about the impact of technology. So this is just, for, for folks who are interested in safety, this is for them. System card is usually pretty cool. We can probably, dive in there and see, you know.what they're looking for. So for example, key areas of risk evaluation, they're looking at speaker identification to know who's, who's speaking, sensitive trait attribution, stuff like this.

[01:28:28] **Alex Volkov:** it's pretty cool. We're not going to like super react like real time, unless this is the strawberry stuff. but yeah, they gave us like a super quick heart thing, super quick, but this is not what we were like super expecting, to, to get, Exactly right now. They do share a bunch of audio stuff, and just to remind you, before, after they announced the audio a interface the advanced audio interface that we had Cristiano present to us live on show last week then the whole Scarlett Johansson thing came about and you know there were concerns about OpenAI's approach there and so they they're probably releasing some stuff they said that they're worried about releasing this widely and they need to to test this a little bit more so this looks like The, the reason, or I guess this looks like the outcome of that thinking a little bit more before releasing this to, to everybody else.

[01:29:19] **Alex Volkov:** They have voice generation examples here. They're like a good one or a bad one. and I'm assuming that they're thinking about different like prompt injection techniques that are now, useful with voice. Go ahead LDJ, if you want to react to this real time as well, feel free.

[01:29:34] **Alex Volkov:** Yeah, so this is actually pretty interesting. Right now, I'm on their page, and it seems like they have this type of preparedness framework similar to Anthropic, which I don't think OpenAI has talked about this before, but they give a score of 1 out of 4 for 4 different categories, cyber security, biological threats, persuasion, and autonomy.

[01:29:54] **Alex Volkov:** They rank it, they rank GPT 4 0 level 1 on all of these, except for persuasion, apparently they consider it level 2. And I guess they go into more detail about what is the difference between each level of jump in each category. 

[01:30:08] **Alex Volkov:** Yep. So it looks 

[01:30:10] **Alex Volkov:** That is going to be It's going to be jailbroken as soon as it comes out, they need to do a lot more than 140 languages.

[01:30:19] **Alex Volkov:** They need to just post it to a bunch of schizos on Twitter to actually make it say things. 

[01:30:25] **Alex Volkov:** This is, this is the, this is the open source ethos, right? the more open source this is, the the harder, this is what Mark Zuckerberg does, right? The more open source this is, the harder it is to, to break. Because there's a bunch of skeezers on Twitter trying to break this. And then posting it back.

[01:30:40] **Alex Volkov:** so yeah, we're moving on from this breaking news. Unless we have some reacting comments. But I don't know if that's like super, super crazy important right now. Nisten, anything else? No? Or are we good? We're good. Okay. I think the last thing that I wanted to mention after Mistral, NVIDIA leak, I don't think we have time to talk about.


## [01:30:58] Character AI's Acquisition and Future Plans

[01:30:58] **Alex Volkov:** Um, Character AI, I'll just mention this. Also, there's not like a lot of stuff. This is not this space. You probably heard this in multiple spaces before. Character AI executive buyout. Character AI is the company, that does very well. I think they're the, they crossed the 300 million mark. web visits, and they're, like, doing incredibly well.

[01:31:15] **Alex Volkov:** Noam Shazir, the guy behind, Attention Is All You Need, in addition to seven other authors, but he was, like, the main, Looks like he was the main, the main guy there, even though he didn't take the main attribution because he's like a nice person, he then went after 17 years at Google, he went and founded a character AI, which if I'm not mistaken, the average use time of this website for many people is like [01:31:40] above 35 minutes or something.

[01:31:41] **Alex Volkov:** it does very well. They decided to, to, to get, I could hire, or like they, they got bought out by Google or I could hire by Google. the company still works, but many people left back into Google DeepMind, including Noam, and there's a specific agreement. And for some reason, they also announced that, Character AI will pivot to meta.

[01:32:01] **Alex Volkov:** And Llama, and we'll use Llama for their characters, and for some reason they didn't say Gemini. And I don't know, maybe a quick reaction from folks from, from like this announcement and Gnome. Anybody wanna talk about this, of, this acquisition and why would they choose like Llama? Like I know why, like Llama is cool, but still, why not Gemini if they're getting bought out by Google?

[01:32:22] **Alex Volkov:** Hmm.

[01:32:25] **Alex Volkov:** Also, there were some statistics on the amount of users of AI companions, like AI girlfriends, AI boyfriends. The largest percentage of paying users, I don't remember who I heard it from. It was a particular person. I'm not gonna mention who, but it was like the vast majority of paying users are our older women of of these apps and and they're using them a lot.

[01:32:48] **Alex Volkov:** So if you're gonna use Gemini for that you're gonna need to, it's probably a lot more safety RLHF than than Meta for this type of work. So Yeah.

[01:32:59] **Alex Volkov:** whereas with LLAMA it's pretty easy tojailbreak and make it like a adopt personality. So 

[01:33:07] **Alex Volkov:** Yeah. 

[01:33:07] **Alex Volkov:** I don't know. That's been my experience in the past.

[01:33:09] **Alex Volkov:** I haven't tried the new, the new Gemma, but it's probably just better off at this squirrel playing stuff. It might just be that. Like they, they need a good product.


## [01:33:17] Cursor: The Ultimate Coding Assistant

[01:33:17] **Alex Volkov:** Uh, I think we've covered pretty much everything that I want to talk about besides this one thing that I invited Matt to talk about here. oh, we also didn't follow up from last week, so Matt, we'll talk and then we'll see if we have time, to, to, to last thing.

[01:33:29] **Alex Volkov:** we sometimes talk about tools. We don't often talk about tools, but I really wanted to, geek out with Mac about, this one tool that many people use. But if you are in the audience and you don't use it yet, I really, really want to be the person who tells you about Cursor. if you haven't yet, heard about Cursor.

[01:33:44] **Alex Volkov:** sh, it's a VS It's a code clone. It's a complete clone. So if you download Cursor. sh, I think it's free even, unless you want to, to, to, to pay for it and then get a little bit more, it's a complete VS Code clone to the extent of there's the one button import, for all your settings and plugins and everything.

[01:34:01] **Alex Volkov:** And then,if you are using Copilot and you're like very happy, yay, I'm programming with AI, Cursor is going to blow your mind because it's like a way more, just like advancements of, of how an AI integrated, into your workflow editing could be. And I think that after a while, everybody who uses Cursor understands that there's no way back to, to Copilot.

[01:34:23] **Alex Volkov:** Copilot.is introduced chat way later than Cursor. So Cursor, you, you could have chatted about the different things. a few things that I use in Cursor before I can adjust with that is that you're able to select like a bunch of code that you have and hit command K and ask things to, to happen to this code.

[01:34:39] **Alex Volkov:** And like Cursor will go to Sonnet and Cursor always like the focus of Cursor always update the latest best model. you can also go to like open router and use DeepSeq if you want. And Gemini, I think, You can just select a bunch of code and ask stuff to happen to it. Or you can like, do things on the whole file.

[01:34:56] **Alex Volkov:** Those are just like some of the things. Now, recently Corsair introduced like a new feature, which I haven't played with. And Matt is getting like very excited about. so it's called Composer. Matt, could you, could you maybe tell me about Composer? Because I don't know what this is.

[01:35:10] **Alex Volkov:** Yeah, at a high level, think of it as taking all the parts of, essentially, Cursor that you like, and stringing them together as an agent. That's at least my read on it, so stringing them together as an agent to actually execute, not just, advise. when you're asking Cursor for an edit, aside from doing the command K, If you're doing command L and you're asking to chat with it, it's just giving you advice on what you can do to files, and you can apply it, but you still have to do everything manually, and you're like the conductor, but a low level conductor where, you have to do a lot of the grunt work.

[01:35:40] **Alex Volkov:** What Composer does is it takes away a lot of that grunt work, so it doesn't fundamentally change the way that it interacts with your codebase from a sort of Understanding level, but it changes how it interacts with the code base from an actual, interaction, perspective. So basically I can say, go and add this feature.

[01:35:54] **Alex Volkov:** It'll go and search through all the files in my code base, figure out exactly which files it needs to edit to make that feature happen. And then it'll say, okay, read through these files and make some edits. It'll go and make those edits in the files and it'll put it all together. And I just have to click accept at the end and I can go and test the feature.

[01:36:11] **Alex Volkov:** it's, it's more similar in spirit to something like, a Devin, than anything else. But it's a little bit nicer in terms of, you have your hands on the wheel. With Devin, it's sort of like, come back an hour later and we'll see what happens. From my understanding, it could be wrong there. with Composer, it's sort of like, a happy medium between the original cursor design and, and Devin.

[01:36:29] **Alex Volkov:** Where, your hands are off the wheel, to some extent. you're letting it run and make changes to your files, but you approve everything at the end. You give it feedback in steps. It's not just going, you can't feedback whenever. It's like here, like I'm gonna stop there. You tell me if this is good or not, right?

[01:36:48] **Alex Volkov:** And it's pretty awesome. as a sort of test, I was on a plane, on Sunday, and I literally just was like, can I build a SaaS 20 minutes? And It did, with Stripe, authentication, everything. It was, it was mind 

[01:36:59] **Alex Volkov:** Wow,

[01:37:00] **Alex Volkov:** I will say though, the UX is definitely very early, and understandably, right?

[01:37:04] **Alex Volkov:** It's something very new, and there's no sort of good design pattern for this yet. They're figuring it out. there are a lot of bugs, right? Sometimes it just times out, and you're just left hanging, and you have to resend the message, but you can't hit a retry. It's, it's, it's a little messy right now, but, I think with the current balance of control that it has, And the sort of general capabilities of the models today, it's, it's really promising.

[01:37:26] **Alex Volkov:** if models get just a little bit better, I could see it really making a dent in the, in the AI engineering space. 

[01:37:32] **Alex Volkov:** that's incredible. I, I need to try this,cause I opened this up and I didn't really understand that this, it's multi file editing as well. does multiple things, correct?

[01:37:42] **Alex Volkov:** Yeah. the UI, it honestly took me a few minutes to get used to, and I think with everything else Cursor has done, it's just you get it, seamless. This is the first thing I think they've done where it's okay, I don't really get this. But, once you start picking it up, and you figure it out a little bit, I don't even know that I'm, using it perfectly, right at this point, but still, I think I know enough about it to get a lot done.

[01:38:02] **Alex Volkov:** but the UI is definitely a little clunky and weird today, and hopefully they've fixed that. Got some ideas to iron that out. 

[01:38:08] **Alex Volkov:** But it's really cool that someone's even innovating in this space, because the traditional UI is just like a human in the loop running the code, and then I think agents are like, maybe have linters in between to just make sure the code compiles, I think it's cool that they're doing things like multi file editing, and I'm yeah, pretty curious to see more projects along those lines.

[01:38:23] **Alex Volkov:** Yeah. I'm, I'm very excited, like curious to, to try it out and see if it actually, can, can do things for me. Because even the basic cursor stuff, just in the side pane, for example, is just quite honestly incredible. What other features of Cursor do you use, Matt, that there are nowhere else?

[01:38:41] **Alex Volkov:** Yeah, so before that, one of the things I want

[01:38:42] **Alex Volkov:** I will say that, this is not a sponsored anything, I just love Cursor so much that, I just want you guys to know about this, so you'll be super productive. this is literally what's happening oh, one tip I would just give to anybody using pretty much any of the egistic stuff in Cursor, and this is just a good prompting pattern generally. what I'll do is I'll have it, let's say I'm having it generate a landing let's just say. You can apply this technique to pretty much anything, but this is super useful.

[01:39:04] **Alex Volkov:** let's say we're having it generate a landing page. The first thing I'll do is I'll ask Cursor to generate that landing page, right? Then I will actually open up the Composer and I'll say, Okay, you are a, act as a, I don't know, a design critic, you're Dylan Field of Figma, and you're a world class designer, and you know everything about design, and this was done by a junior designer.

[01:39:24] **Alex Volkov:** Please critique the hell out of it, be incredibly harsh, and tell me what's wrong with it. It'll go and do that, and then I'll say, okay, what would you do to change that? It'll give me a whole set of changes, and then you actually take those changes back to Cursor and say, go and add these changes, and it'll come out so much better.

[01:39:37] **Alex Volkov:** So it's, for anybody who's going to use it for the first time, that is one of the most useful things you can do with it. For pretty much any of their features aside from their like sort of tab, tab, tab co pilot. just asking it to critique itself and then asking it to implement those changes makes a world of difference.

[01:39:50] **Alex Volkov:** It's like using a next generation model versus a last generation model. but to your question, the features I use. So the main thing really is if I'm working in an established code base, the main thing I [01:40:00] use is, the sort of type ahead. So it's, I believe they call it, CursorTab.

[01:40:04] **Alex Volkov:** Let me pull it up and see.it's called, Yeah,

[01:40:07] **Alex Volkov:** CursorTab. And it's very similar to GitHub Copilot, it's quite a bit better, it's faster, it's got better context, but the cool thing about it is it does like inline editing, where it can actually fix mistakes in my code backwards, not just forwards, with Copilot, it essentially only predicts the next few, words or whatever.

[01:40:25] **Alex Volkov:** With Cursor's version, can actually show a diff for something, and it's hard to explain without showing it visually, so I'm trying my here. But it can show you like sort of like a diff of a line of code two lines back and you just press tab and it fixes it if there's something wrong. Or, I've even noticed if you copy something, let's just say I'm prototyping something and I'm using a hard coded API key, don't kill me, right?

[01:40:50] **Alex Volkov:** and I have it copied to my clipboard and I'm going to paste it in, it somehow already knows I have that as soon as I enter the file and it just puts it there and I just press tab.

[01:40:58] **Alex Volkov:** I noticed this as 

[01:40:59] **Alex Volkov:** done some magic 

[01:41:00] **Alex Volkov:** It knows the contents of a clipboard and it uses it smartly, which is crazy, and I've definitely noticed as well. I want to add, before we end Matt, I think that one thing that I often use is that I add the docs feature. You can add documentation to anything by just like giving it the URL.

[01:41:15] **Alex Volkov:** It will go, index, scan this, and then you can At tag in the chat. And you can say anywhere you talk to Coursera, you can like at tag, whatever docs. So this new library Fast. HTML from Jeremy Howard, for example, wasn't in there. And neither LLM, like no LLMs know about this cause it's new. You can still get Coursera to give you like decent output by just like tagging those docs and all of these models now have long context and it works really, really well, even for like proprietary stuff.

[01:41:41] **Alex Volkov:** If you're okay with sending those tokens to, to, to Entropic. And also somebody. Told me over Twitter that you can just like paste links. So if you don't wanna do like the whole docs, you can literally just paste a link to the specific doc or a question and answer in Stack Overflow or whatever you want.

[01:41:56] **Alex Volkov:** And this will go and index this in the context of the question. So they'll, they'll go, they'll index and they'll put it in the context and they will answer as well. and then use, write you the code. The right code, for this, so you can send like a PR URL or different things like this. So definitely, if you haven't, after all this, have been convinced to use Cursor, you're beyond our help.

[01:42:15] **Alex Volkov:** But if you, if you haven't tried this, I strongly recommend, that you do give it a chance and let us know in the comments. let me know in the comments if this was, this was something up your alley. Absolutely. Go ahead, Matt.

[01:42:28] **Alex Volkov:** yeah.

[01:42:29] **Alex Volkov:** last note on Cursor for me is it's so damn effective that we actually require everybody on the team to use it. If you don't use it, you're not good.basically it's, it's, if you're using it right, if you're using it wrong, you're getting a probably 2x output. If you're using it right, you're closer to 10x or even more.

[01:42:43] **Alex Volkov:** It's, it basically enables you to do things that you couldn't do previously and the things that you could do previously, you're going to do, significantly faster. So 

[01:42:50] **Alex Volkov:** should be using it if you're coding. 


## [01:42:51] Conclusion and Thank You

[01:42:51] **Alex Volkov:** And I think that this is everything that we've talked about on ThursdAI for August 8th. it's been a Compared to previous weeks, it's been a chill week, but still, we've talked for 2 hours and 10 minutes, and there's more that I have to talk about here, basically covering that last week as well. We also didn't get the strawberry news that potentially, we were waiting for, so maybe this will come, next on this Thursday, but with that, I want to thank everybody who joined on stage, from, YAM and Nisten and LDJ, We had Jun Yang here as well, Matt Schumer and Mark Serafim, all the folks who help week to week and do an incredible job and like diving deep into the topics.

[01:43:27] **Alex Volkov:** And also everybody who listens to this from week to week, all of you in the audience, new ones who came from Starbreeze and decided to stick around and listen to us discuss like very technical things. this ThursdAI is getting released as a podcast and a newsletter. If you're not subscribed, please do And, with that, we'll see you next week. Happy Thursday, everyone. Cheers.

