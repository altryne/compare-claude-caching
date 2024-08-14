[00:00:00] **Alex Volkov:** As we're getting started with ThursdAI.

[00:00:11] **Alex Volkov:** Woo. I haven't done this in two weeks, three weeks. This is, yeah, cause, nevermind. Welcome to ThursdAI, everyone.welcome. Today's July 25th. My name is Alex Volkov. I'm an AI evangelist with weights and biases, and I've missed this. I've been on, on a break, on a holiday break for the past, Two weeks, there hasn't been a live show for the past two weeks, and, yeah, it was my birthday, so happy birthday, Alex.

[00:00:41] **Alex Volkov:** I celebrated with my family, I had a lot of fun, and, and Sam Altman just dropped a thread, so we're gonna see what's that about.yeah. I wrote an op ed in the Washington Post about why US needs to maintain its lead, blah, blah, blah. Not interesting. It's just another blog post. 


## [00:00:56] Recent AI Developments and Break Recap

[00:00:56] **Alex Volkov:** Alright, back to ThursdAI.

[00:00:58] **Alex Volkov:** I'm so excited just because I'm waiting for some breaking news from OpenAI as well, because they can't just let the lead go. for the past two weeks, we haven't had a show. And last week It was an insane week in AI as well. OpenAI released GPT 4. 0 Mini. We haven't talked about this. There was like a bunch of updates.

[00:01:15] **Alex Volkov:** And I got a bunch of feedback from all of you saying, Hey, how dare you take a break? How dare you, Alex, take a break? what's going on? while I was like having fun with my kids. and I'm very happy that the break that I took was last week and not this week becauseis this week insane or what, folks?

[00:01:32] **Alex Volkov:** Oh my god. This week. We've got the open weights state of the art model that beats GPT 4. 0. And I honestly did not believe that this day will come. And I'd be able to talk about this live on stage with my friends. And I'm very excited for today because we're going to cover all of the releases that we had.

[00:01:54] **Alex Volkov:** And not only did Meta release Meta Llama 3. 1. This week, also Mistral followed this up with another release of theirs, of large, Mistral Large 2, and then also DeepSeq, quietly updated and without Fanfare updated DeepSeq coder, which is probably the best coding, open weights, model. I actually don't know if they updated just the API or already updated the model as well.

[00:02:18] **Alex Volkov:** And not only that, we're still waiting for some other stuff to drop in probably around 30 minutes if the leaks are true and the embargoes are true. So we're going to sit here and we're obviously going to monitor everything and bring it to you live as we always do. on the show. And my, breaking news button is ready.

[00:02:38] **Alex Volkov:** Let me test this real quick. Let me test. I don't know. I haven't been here for a while. Let me test if this works. Okay, it works. 


## [00:02:45] Technical Tests and Guest Introductions

[00:02:45] **Alex Volkov:** so I'm going to just add a few friends of mine as speakers just to test because I don't want any technical issues on the show, so let me just double check. LDJ, if you can hear me do a little unmute and let's see if you can hear me and I can hear you.

[00:02:58] **Wolfram Ravenwolf:** Yep, I can hear you.

[00:02:58] **Alex Volkov:** Awesome. Coming through loud and clear. Welcome LDJ. Welcome. And Wolfram, let's see if we can come through as well.

[00:03:06] **Wolfram Ravenwolf:** I can hear you loud and clear, hope you can hear me

[00:03:08] **Alex Volkov:** Yes.

[00:03:08] **Wolfram Ravenwolf:** And I missed you! Welcome back! Hey 

[00:03:10] **Alex Volkov:** you too, brother. I miss you too. 


## [00:03:12] Mark Zuckerberg announcing Meta Llama 3.1

[00:03:12] **Alex Volkov:** This has been, it's been crazy two weeks, but I'm very happy that this is the week that I didn't miss because, Mark Zuckerberg, the GOAT, decided to go live And this time he did one, exclusive interview with our friend from the Rundown AI, Rowan Cheng.

[00:03:30] **Alex Volkov:** So shout out, a big shout out to Rowan. Did you guys see this? Did you guys see Rowan Cheng from the Rundown AI just like land an exclusive interview with Mark Zuckerberg with the chain and everything? So shout out Rowan. a huge shout out for this like crazy exclusive interview. Mark went up and said, Hey, Here is everything.

[00:03:48] **Alex Volkov:** And he talked about like the model, the distillation. We're obviously going to do whatever we do in ThursdAI, which is we're going to do it like a TLDR of everything we're going to talk about. I just really wanted to just collect the vibes super quick. And just as I'm looking through, I'm scrolling through like the list of like friends in the audience.

[00:04:05] **Alex Volkov:** I see Robert Scoble, I see Ryan Carson, who's sick. I hope you get better brother. I see Technium, Yang here. Jun Yang, feel free to,to come up. All of you, by the way, welcome to come up. All the regular friends of the show who've been here at least a few times. 


## [00:04:18] Meta's Open Source AI and Community Reactions

[00:04:18] **Alex Volkov:** Mark came up and talked about this model.

[00:04:20] **Alex Volkov:** And first of all, I want to say, before we dive into the model itself, the fact that this dude, like my age, I think he's younger than me. I don't know. he's,the owner of this insane, huge, like company runs like billions of dollars, whatever. And he knows what they released to this level is just incredible to me.

[00:04:36] **Alex Volkov:** He talks about distillation. He talks about like the technical details to this level was just like, I was floored. I was like, this is the dude. And also the amount of belief and, Just strong opinions he has about open source AI was just incredible to see. Not only did they release models, which we've been waiting for, and we're going to talk about in excruciating detail, they, he also released an op ed.

[00:05:02] **Alex Volkov:** I don't know if you guys had a chance to read the op ed. feel free to chime in, if you want to like chime in a little bit, he released like a manifesto basically of why open AI, open, real open AI, not the company open AI, it was like open source matters. And that manifesto is like also incredible.

[00:05:18] **Alex Volkov:** And so this was like definitely the week for open source AI. I feel like for maybe since the release, I think this week overshadows the release of Llama 3. This overshadows the release of LLAMA 3. LLAMA 3 came out and was incredible, we were like, Yay, LLAMA 3! And then, it was great.

[00:05:36] **Alex Volkov:** This time, this is the first time, as far as I am doing ThursdAI, and even before, that we get a model, since I think stable diffusion, that this model beats LLAMA 3. The foundational models. And I think it's incredible. I think it's worth this applause and we'll get to Wolfram to hear what you got, what do you have to say about the Meta Llama 3 and then we'll do a TLDR.

[00:06:00] **Alex Volkov:** So shout out to Meta. Yeah, go ahead then.

[00:06:04] **Wolfram Ravenwolf:** I wanted to say, yes, the original release was actually a pre release as Mark said, because, he wanted to put out the 3 before it was really ready, so that was the thing, and I was pretty disappointed with 3 because of the small context, only 8k, I mean it is what, was double what we had before.

[00:06:21] **Wolfram Ravenwolf:** But we already had much bigger models. So this is a real Lama 3, I would say, and it's great to have it now. And now I'm really happy. Now bring multimodal next, but I don't complain. So it's multilingual as well, and it's available in Europe everywhere. It's great. I love it.

[00:06:36] **Alex Volkov:** Yeah. And we're going to discuss multilinguality. We're going to discuss multimodality as well. LDJ, go ahead. Give us like initial thoughts when you see this drop, what, two days ago? I don't even know how much time passed. I think two days.

[00:06:50] **Wolfram Ravenwolf:** Yeah, 

[00:06:50] **LDJ:** it's been about two days. 


## [00:06:51] Sam Altman's Op-Ed and Open Source Debate

[00:06:51] **LDJ:** It's on the 23rd, so it's the 25th today, and I did want to mention real quick that you mentioned Zuck put out an op ed about being in support of open source, and Sam Altman just dropped something literally five minutes ago, and it's an op ed written by Sam on Washington Post titled, Who Will Control the Future of AI?

[00:07:14] **LDJ:** And it actually has, I searched quickly for, Anything talking about open source and he does say one sentence about open source basically saying that he thinks it should happen and thinks open source is a good thing.

[00:07:27] **Alex Volkov:** Wait, Sam thinks open source is a good thing?

[00:07:31] **LDJ:** Yeah, I could just read the single

[00:07:32] **Alex Volkov:** Yeah, give us a quick shout out.

[00:07:34] **LDJ:** Yeah, he literally just says a quote, making sure open source models are readily available to developers in those nations referencing like different countries will further bolster our advantage.

[00:07:46] **Alex Volkov:** Oh.

[00:07:46] **LDJ:** guess you have to read more of the context of why he thinks open source will bolster the America's Advantage, but yeah.

[00:07:52] **Alex Volkov:** maybe he should listen to his own advice then. So Sam, if you're listening to this, please release some stuff on open source. we would love it. We would love some stuff from OpenAI more in the open source. Maybe like 3. 5. You guys, basically 3. 5 is dead, right? Like I don't think it's possible to use it anymore.

[00:08:08] **Alex Volkov:** So maybe 3. 5. All right, we have breaking news from Lilken. all right, folks, we've been waiting for this. Let's go, let's get into it. And then we're going to talk about Metal Llama and everything. [00:08:20] Allwe've been waiting for this and I literally just saw this like a few minutes before I stepped into the space. 


## [00:08:37] Breaking News: Google DeepMind's New AI Achievement

[00:08:37] **Alex Volkov:** I don't have this in my notes, but Google DeepMind just dropped. we're presenting the first AI to solve international mathematical Olympiad problems at a silver medalist level.

[00:08:46] **Alex Volkov:** It combines AlphaProof, a new breakthrough model for formal reasoning, and AlphaGeometry2, an improved version of our previous system. International Math Olympiad, International Mathematical Olympiad problems are ridiculously hard. And soI'm just going to keep reading and then we're going to discuss this.

[00:09:02] **Alex Volkov:** Our system had to solve this year's six IMO, problems involving algebra, combinatorics, geometry, number theory. We then invited mathematicians and Dr. Joseph to oversee scoring. It solved four problems to get 28 points. for non geometry uses alpha proof, which can create proofs in lean. I don't know what lean is, I'm assuming some that stuff.

[00:09:22] **Alex Volkov:** This is basically, if you guys remember this whole thing, recent, recent thing where everybody like, goes crazy, where we asked CGPT what's a bigger number, 9. 9 or 9. 11? this is basically the answer to this, I'm assuming. yeah, this is quite big. I've seen that some people claim that OpenAI also has something like this, maybe with like QSTAR or something.

[00:09:45] **Alex Volkov:** And, there's some leaks that we're about to get Matthew Atling from,from Jimmy Apples. But yeah, Google DeepMind just dropped a new update basically that says, and is this in nature like they always do? Or is it just a blog post? Let's see. Just a blog post. that they've solved, that AI now solves International Mathematical Olympiad in, in silver level metal.

[00:10:08] **Alex Volkov:** This is crazy. This is crazy because we know that just like predicting the next token is not that great at math. anyone, quick reactions as you guys are reading through this? Maybe folks in the comments, feel free to also comment.

[00:10:19] **LDJ:** Yeah, I was wanting to clarify real quick, Lean is just, it's a programming language that mathematicians use commonly for things like theorems and like formalizing things in a programmatic way that can easily be verified.

[00:10:32] **Alex Volkov:** Amazing, thank you, LDJ. let's see what else we can, glean from this release that's interesting. Yeah, they have this, they have an example of Lean. Let me post this also to the top of the space. when presented with a problem, AlphaProves attempts to prove or disprove it by searching over possible steps in Lean.

[00:10:50] **Alex Volkov:** so this is what maybe people talked about, maybe QSTAR, I don't know. Maybe I'm talking, I don't even know

[00:10:56] **Junyang Lin:** That makes it, that actually makes it not 

[00:11:01] **Nisten:** all that impressive, I

[00:11:03] **Alex Volkov:** because they are. Yeah, Lean is used for a theorem, prover, so it can do,very hard math, not necessarily even competition, for more, stuff that physicists need to do or, theoretical physics and other things like that.

[00:11:18] **Nisten:** Yeah, then they need to use lean, but it sounds like they just trained the model on this language and then ahead it solved. But we'll see if we can solve nine 11.9 0.9. 

[00:11:28] **Junyang Lin:** We'll know it's good.

[00:11:29] **Alex Volkov:** Yeah, last thing I'll say, and we'll move on because we, if this is an attempt by Google DeepMind to steal Thunder from Meta, we're not gonna get it because Meta is still, Llama 3 is still the, 3. 1 is still the biggest news of this week. last thing I'll say is that, Powered with a novel search algorithm, also Geometry 2, can now solve 83 percent of all historical problems from the past 25 years, compared to 53 percent rate of its predecessor.

[00:11:54] **Alex Volkov:** So this is quite a huge jump from 53 percent to 83%. and it solved this year's IMO problem for within 19 seconds. so this is quite crazy because it also does geometry. LDJ, last comments about this or Juniang or Wolfram and then if not, we'll move forward.

[00:12:13] **LDJ:** Yeah. There's art, there's an article about 24 hours ago from the Verge actually on this, but I think they may accidentally published it earlier, something when they weren't supposed to, because they like immediately took it down. But according to that, the Verge article that got taken down. It was able to solve four out of six International Math Olympiad problems that they presented it with.yeah, that's interesting.

[00:12:35] **Alex Volkov:** Yep. Yep. Yep. And so shout out to folks at DeepMind for moving this forward. And as, as we know that just Next Token Prediction is not that good in math, even though everybody keeps doing the same thing, we keep throwing like math y problems on Next Token Prediction and showing like, see, it doesn't work.

[00:12:53] **Alex Volkov:** And then everybody's oh, this goes viral like crazy. 


## [00:12:55] TLDR and Overview of Today's Topics

[00:12:55] **Alex Volkov:** All right, folks, I think it's time for the TLDR of everything we're going to cover. And then I think it's time to dive in. Or I guess dive in. Delve in to Metal Llama 3. 1 updates and it's going to take us a while to cover because there's just so much to talk about.

[00:13:10] **Alex Volkov:** So we're not going to have any guests this week, but there's so many people I want to talk to that I reached out to. So look forward to the next episodes for actual like deep dives and guests because I have a huge queue of like awesome people coming. But for now, let's do a quick TLDR of everything we're going to talk about on ThursdAI.

[00:13:32] **Alex Volkov:** For July 25th.

[00:13:42] **Alex Volkov:** Let's go. This is. Hopefully everything, hopefully, because we're still waiting, I think, for some additional news, maybe from OpenAI. here's everything that, at least to,right now I have in my notes for July 25th, ThursdAI 2024. And obviously the biggest fish, the biggest thing, the biggest, entree on our menu today to discuss is Meta Llama 3.

[00:14:05] **Alex Volkov:** 1. Meta released, and gave us three new models in open weights, including an incredibly detailed paper, just an incredibly detailed paper full of, full of nuggets, full of information. I honestly, We'll not be able to relay most of it still, because I'm still like,we did multiple paper cup.

[00:14:23] **Alex Volkov:** Nevermind. So what did we get from, Metal Llama 3? We got three new models, 405 billion parameters is finally here. The biggest, Metal Llama 3. 1, 405 billion parameters. It's a dense model. 4 level intelligence. In fact, it beats GPT 4. 0 on multiple benchmarks. We also got updates to, LLAMA70B and 8 billion parameters as well.

[00:14:46] **Alex Volkov:** They are updated across the board. They have new capabilities as well, including tool use and multilinguality updated as well. We also got a license update. And so we're going to talk about that and what this means. And, we also seen that these models are now supported out of the gate with multiple providers.

[00:15:05] **Alex Volkov:** So you can now. Actually use these models instead of waiting for quantization. Meta just released also a bunch of evals as these models drop, but we're also going to do like an evals roundup. There's a lot of evaluation, providers. There's a lot of like new benchmarks in evals that we know and already like respect that we're going to cover and run through super quick, including our own reactions and folks here on stage who've tried these models already at this point.

[00:15:30] **Alex Volkov:** There's just so much to cover here. Besides the new bigger model, there's also the capabilities of the smaller models, the new capabilities across the board. I think the main thing to also cover is that the context window is huge. It's 128 context, 128, 000 tokens in the context window. Finally, including a new rope scaling method, that was outlined in the paper.

[00:15:51] **Alex Volkov:** And you can download these models, which is incredible. So we have a state of the art, beating GPT 4 O models that you can click on the download button, which is not only refreshing, it's quite incredible. And we've been waiting for this and it's incredible to just, just cover this as somebody who does this for a while.

[00:16:11] **Alex Volkov:** and there's probably more stuff that I haven't gotten in my notes. So we're going to also discuss those. And then, like a day after this Which was yesterday. Mistral, the French company that we all know and love, that gave us incredible models like Mistral 7B, that we all remember and love, announced Large V2, which is a 123 billion parameter model, which is currently, I think, in their API, and I believe it's Probably you can download as well.

[00:16:38] **Alex Volkov:** it's a non commercially [00:16:40] licensed model that you can use the API, but you cannot like download and post it on production. It's a strong multilinguality and they claim state of the art on function calling, which is interesting. also very high on benchmarks as well. Trenton, a lot of code. if you guys remember recently, they released CodeStral and MathStral.

[00:16:59] **Alex Volkov:** So based on their experience with this, they shoved like a bunch of that into this new model as well. and it already beats, it's quite incredible. They listed the day after Lama 3. 1, and it already beats Lama 3. 1 on at least a few of the coding, of the coding metrics, which is quite crazy because it was released a day after.

[00:17:19] **Alex Volkov:** so they probably waited and said, Hey, Let's wait and then run some evals and see if we can give a good story. So shout out, a huge shout out to Mistral for this. And now, we also have an update from DeepSeq Coder. DeepSeq Coder, for a long time, was the best open source model for code. And then, for a day or so, LLAMA 3.

[00:17:41] **Alex Volkov:** 1405 billion parameter was probably the best coder. And I think DeepSeq just released an update as well that beats it. And it looks like DeepSeq Coder v2. 2407. So that was yesterday as well. it looks like it's getting to 3. 5 sun at level. So we're going to also cover this and why it's only VAPI.

[00:18:02] **Alex Volkov:** You can download this as well. we also just had breaking news from DeepMind. They announced Alpha Geometry 2 that beats the International Math Olympiad at silver medalist level, which we just had breaking news. We're probably going to cover this as well. in this week's buzz category, I, all I could do to this week is try to do some comparisons.

[00:18:22] **Alex Volkov:** And so I'll just walk you through some related stuff as it happens to relate to all the releases. I ran some evaluations between the different LLAMA providers, using weights and biases weave to just see how different quantization In different providers affect some outputs. So we're going to walk through that because some providers which launched the same day as Lamba released, some of them actually serve quantized models, which, not to blame them, but some of those, reply in a different style, which is very interesting.

[00:18:55] **Alex Volkov:** So we're going to walk through that and maybe see an example with, using Words Bios as Weave, which is our evaluation framework of Words Bios. In the vision video category, I don't have a lot. This week, besides some updates from Kling, every week in vision and video category, I can't wait to tell you, hey, OpenAI finally released Sora.

[00:19:13] **Alex Volkov:** They didn't,maybe this week they want to overshadow Meta and release Sora for us. Maybe, I don't know, but it haven't happened yet. But in the vision video category, I will say that Lama 3. 5 V. is a thing. And in the paper, they actually talk about that they've trained, but not released a vision model and multimodal model of Lama 3.

[00:19:32] **Alex Volkov:** 1. And they actually gave us a path towards it. There's like a diagram of how they trained these models. And they also talk about the fact that these models will not be released, at least in Europe, because of some European AI laws. So we're gonna cover this just at least a little bit, which is sad. And it's a bummer.

[00:19:53] **Alex Volkov:** in the voice and audio category, I saw that a company daily announced a new open starter for real time voice and audio AI. It's called RTVI. We're going to cover this a little bit. The demos are great. And I hope that I'll be able to do like a live demo. we already did a few demos of live kind of conversational AIs and they weren't that great previously.

[00:20:13] **Alex Volkov:** So we'll see if this demo could work. it reacts like super quick. And. It's an open standard. So we definitely should talk about this as well. And in the AI art and diffusion category, we have stability, not silently, but trying to also get their day in the sun, but probably not the best week for stability to announce this.

[00:20:32] **Alex Volkov:** They announced something called stable video 4D, which is you provide a video and they, receive, you receive a novel view video from eight new angles, which is. It's quite crazy. It's quite crazy to see. and yeah, it's pretty cool. So I think this is most of what we currently have to talk about on ThursdAI for July 25th.

[00:20:52] **Alex Volkov:** I think that's plenty because we're going to start with Llama 3 and I think we can talk about at least that for an hour. let's actually get started with open source.

[00:21:16] **Alex Volkov:** All right, let's get it started. 


## [00:21:17] Deep Dive into Meta Llama 3.1

[00:21:17] **Alex Volkov:** We're obviously going to talk about Meta, LLAMA 3. 1, and I was thinking about how to approach this. So I've been talking about this since the leaks. Monday, I think, we started seeing leaks. The model was leaked, first of all, by Mikyu, if you guys remember Mikyu. Mikyu 2 was leaked, and apparently this was this model.

[00:21:37] **Alex Volkov:** And then, some metrics were leaked because of something on GitHub. And then the model card was leaked. Blah, blah, blah. So we already started thinking about this model, starting from Monday, and what this means. and then the actual kind of like model code was released and the model was released.

[00:21:51] **Alex Volkov:** And I was like trying to think about how to approach this beast of a release. and I think that we'll just start with the biggest model with the 4 or 5 billion parameters. It's a huge model. I think it weighs like 900 gigabytes. Nisten, what does it weigh? You download this multiple times, I think at this point.

[00:22:07] **Alex Volkov:** I think it's like incredibly

[00:22:09] **Nisten:** It's like 2, 000 people have grabbed it off of my fucking face now. The file is 800, the biggest one is like 820 gigs. If you get it in full BF16, it's 400 and about 410 gigs in 8 bit. And then, There's a bunch of other quantization, even made like a mixed one bit one that like still responds coherently.

[00:22:34] **Alex Volkov:** Better than the 70d, but it's a hundred gigs. And yeah, that's about, yeah, the full one is like 820. and a lot of it is synthetic data. They actually go deep into the synthetic data recipes in the paper, which we can probably cover a little bit later.

[00:22:50] **Alex Volkov:** it has 128 thousand tokens in the context window, which is incredible. And we've been when we got Meta Llama 3 back in a couple of months ago, we were like, why is it only 8k? And now we're getting finally a proper frontier model. And I think the best thing about this, obviously, are the evals, are the metrics.

[00:23:12] **Alex Volkov:** The 405 billion parameter model is not easy to run on your own. Like it's not a model that you'd be run, be running on your Mac, because it requires, I want to say 16 H100, 16 A100s. maybe Nisten can help me out here. It requires non consumer hardware basically, to be able to run this even in, I think half precision.

[00:23:36] **Alex Volkov:** Nisten help me out here. Unless you have some magic that you already run this on, the CPU or something. Yeah.

[00:23:47] **Nisten:** days ago10 days ago, LlamaCVP released, scalable vector extensions for CPUs that makes use of, newer ARM, server chips. And that one, bumped up the speed by three times. it's now on CPU runs up to a whopping 1. 67 tokens per second. And, otherwise in 8 bit was half a token per second on a 64 core, CPU.

[00:24:13] **Nisten:** Server CPU, which you can even buy these days for 1, 500 or 2, 000, but yeah, at best you can have a 2, 000 machine running like a token and a half a second, or you can use a slightly more quantized version, which with some custom schemas, it doesn't seem to have that much, but yeah. That much loss and, I can comment a bit on what I think the FBA guys did wrong, but that's probably for another space,when they hosted it.

[00:24:41] **Nisten:** But, yeah, I think you, you can run it on, haven't tested yet on an M two Ultra, but you need the biggest one. You need a 180 2, you need like a $6,000 Mac studio,to run in that, that one should be able to get, a usable speed.

[00:24:55] **Alex Volkov:** I've seen also folks from, Exo or Exa or [00:25:00] Exo. maybe Ray can post this in the comment, run this on a few Mac studios together, run something like this. Anyway, this model is huge. You cannot necessarily run this on a consumer hardware. However, the release Immediately, they partner, met a partner with multiple providers, which was great.

[00:25:15] **Alex Volkov:** Mark Zuckerberg actually shouted out Grok, our friends from Grok with a Q, not Grok with a K. and multiple others like Fireworks and DeepInfra and a bunch of others. And all of these providers, you can now access. Some of these 405B, already there. Perplexity already supports this. This is like the power of open source and the power of the infrastructure and ecosystem that Zuckerberg is talking about because, it's basically a drop in replacement.

[00:25:38] **Alex Volkov:** And for many of these folks, they can just upload the weights and then support this model in multiple of these places because it pretty much is the same, I think, chat, templates and everything. And let's talk about a little bit about the metrics. So we talked about the context window 128,the 405 billion parameter model has MMLU score of 88.

[00:25:55] **Alex Volkov:** 6. it beats GVT 4 on several benchmarks, if eval, so instruction following, I think eval, GSM 8K we know is not the best. It leaks sometimes into the. into the training data set, but it beats GPT 4 at 96. 8%. ARK Challenge at 96. 9%. and comes very close in other metrics. very close. and we said, it's 15 trillion tokens and trained on I think a lot of synthetic data, maybe something like even 90 percent of something like synthetic data, at least the SFT, which is,the secondary stage, a lot of synthetic data, in, in, in realm of new capabilities.

[00:26:33] **Alex Volkov:** Now, even at the evaluation stage, we got Supporting tool use, which is basically the ability to call function calling and tool use, which is very well received by everybody because for the longest time, we know that these models, it's one thing to give us a token prediction, but it's completely different thing if we want to actually use this for something more than just hey, write me a story or summarize this thing where we want these models to actually do something.

[00:27:00] **Alex Volkov:** And in order for these models to do something, for example, search the web, these models need. tool use. They need to be able to call different services and tools and functions. And so it's very good that Meta knows this. And they've built in these,probably data sets. And not only that, they actually showed in the metrics they released that the tool use scores, they, they posted together with these metrics are very high and comparable to, Even beating, GPT 4.

[00:27:27] **Alex Volkov:** So the tool used that they've used, the metric is BFCL. So Berkeley Function Calling Leaderboard and Nexus ZeroShot. this model beats GPT 4 Omni on the BFCL by significant amount. GPT 4 Omni gets 80 score and, Lama 3. 1405 billion parameter gets 88 on BFCL. So like it, it calls functions better.

[00:27:49] **Alex Volkov:** I'll remind everyone that a year ago, OpenAI came up with the function calling concept. Almost, literally a year ago, in June or something, June 16th, I think, OpenAI came up with this concept, we asked for JSON mode, if you guys remember, OpenAI was like, no, we'll give you function calling. And they invented this whole thing, and now they get beaten by OpenWay's model.

[00:28:07] **Alex Volkov:** I don't think they're going to take this lightly. I think we're going to see something from OpenAI. Plod 3. 5 Sonnet. is still the leading model, which is quite incredible. We also got it, what, two weeks ago or three, three weeks ago. quite incredible. The additional, additional thing we saw from new capabilities in new capabilities for these models is multilingual, multilinguality.

[00:28:27] **Alex Volkov:** the data mix that they've posted on the paper supports, I think. 10 percent of multilingual, something like this, LDJ maybe you have the score in front of you, but they also posted on the paper, the data mix of the different, data sets that they have. And multilinguality now is also introduced in evaluations.

[00:28:45] **Alex Volkov:** And, there's a multilingual eval called multilingual MGSM. And on that, Lama 3. 1 also beats GPT 4 Omni at 91. 6%. percent which GPT 4 Omni is 90%. Folks, this is crazy. I cannot honestly believe that I'm describing an open words model that we can download if you have almost a terabyte of space and we can technically run if you have access to all these CPUs or if you're able to run this on CPU and,and it beats GPT 4, which is the model that's the best right now for OpenAI.

[00:29:18] **Alex Volkov:** I cannot believe this. yeah, I would love to pause here and just Here your, you guys reactions to these metrics, to the fact that we have this now. Feel free to just unmute and go, maybe Wolfram you can go and then LDJ.

[00:29:31] **Wolfram Ravenwolf:** Okay, yeah, it's finally here, so I'm really happy because, like I said before, the original release of LLAMA 3 was a bit disappointing. And I was still using Mixtral 8x7, I think, and now we have this, and while the big model is great, not few, not many people can use it. But the 70B is there, and the 8B is there, so that is great.

[00:29:53] **Wolfram Ravenwolf:** they brought out the whole package, and I've used even the 8B a lot. I used to say, So small models aren't good enough, so I wouldn't even consider them. But now it really is good. I compared it with, Misra Namo and with the 70, 27 BA Google Gamma two. And it's, was better in many ways.

[00:30:14] **Wolfram Ravenwolf:** And I think this is a new little guy that can really compete with the big guy. So that was a big thing and I think a lot of people will use it. And, the Lama, CPP, I don't think it has the final. patches already, so everybody who has used it as a GGOF probably hasn't even seen the full potential yet.

[00:30:32] **Wolfram Ravenwolf:** The real version just, because some stuff is missing still,

[00:30:37] **Alex Volkov:** In order to be able to run this, you mean?

[00:30:40] **Wolfram Ravenwolf:** You can run it, but it is running the old inference code, and there has been a bit of changes. Maybe Nisten has more information, more in detail, with what is missing now, and there's a patch, so we can run it, but it should get even better.

[00:30:54] **Wolfram Ravenwolf:** When everything is merged in. 

[00:30:56] **Nisten:** Yeah, I recompiled my own version to do the custom per weight quants, so it worked. I already used it in production. I summarized the Monday's Room from Clubhouse from a two hour talk. It took two hours for it to load it into context. Like another half an hour to generate the, but the output was amazing.

[00:31:22] **Nisten:** It's so annoying how good the output is because you can tell it's better than the 70B. It's It's, yeah, it's definitely better. It's noticeably better, and it's so annoying because now you've got to load everything into context cache, and then you've got to, start it as a batch job and wait and see what comes out.

[00:31:41] **Nisten:** It is extremely annoying that this is 405B. you start using it, and I've been using it on Hugging Child a lot because, It's faster. I'm surprised their servers are still up. they're like halfway dying, from bugging Facebook. They're hosting it for free. So everyone, just go on hf. co slash chat or just use the Oh god, I should not be recommending you guys to do this, but like just, yeah, just use it from iOS, from your phone.

[00:32:04] **Alex Volkov:** Wait, you can go to meta. ai and you can use it there. Like they released it there, I think. You can still choose 405B through meta. ai, I think for a limited time. 

[00:32:15] **Nisten:** how good it is. But, yeah. Just to quickly go back to the Misra one, if in case we covered it or not, that 1 28 k context on Misra chat, which is different than all the other chat providers, that is a real one. 28 KI, I just dropped in there, 90,000. worth of context, like an entire repository with the documentation, I just pasted it in one go and told it to rewrite the whole complete thing while removing the duplicates and removing the documents and it did it and it kept rewriting until it ran out of context window and then I kept telling it to go and it kept going, and none of the other ones do that.

[00:32:59] **Nisten:** Even Claude has,has issues. Obeying that. don't, discount the RAL 

[00:33:04] **Junyang Lin:** model at all.

[00:33:06] **Alex Volkov:** Nisten, before we get to Mistral, we'll talk about Mistral soon. 


## [00:33:08] Cloud Providers and Context Windows

[00:33:08] **Alex Volkov:** I think in the context of bringing us back, the cloud providers that currently host 405B, which is, Grok hosts 405B. You can talk for free at grok. com, I believe. [00:33:20] Meta, AI themselves, I don't, I haven't seen anyone support the 128 context window.

[00:33:26] **Alex Volkov:** I think because this model is so huge and expensive to run, I actually haven't seen anyone support the full context window. Not in, not, not to mention that many of them run this in, in, in, in, In half precision, in FP8, so together runs as an FP8. I think, Fireworks, run this in the FP8.

[00:33:41] **Alex Volkov:** I will talk about my evaluation later. 


## [00:33:43] Evaluation Rundown and Real-Time Feedback

[00:33:43] **Alex Volkov:** let's talk about a little bit about the evaluation. So we're talking about, gut feels. Wolfram, you talked about gut feels. let's talk about evaluations for just a bit. So I want to Paste to the top of the space, and I'll add this to the show notes if you're listening to this on the podcast, a rundown of my own that I ran, I tried to collect all of the evaluations, not that Meta posted for us.

[00:34:03] **Alex Volkov:** I have a, I have a thread that I'm going to post that I just went and collected all the possible evals that I could, and I just pasted it to the top of the space so you guys can read this through this with me. just because you guys know that one kind of, the standard evals are not, are not necessarily, Helpful to understand the full scope.

[00:34:23] **Alex Volkov:** Wait, I'm getting real time checks from the folks in the audience, which I love. People are telling me that I'm wrong. And there's at least two providers that offer full precision. I'm getting that OctoAI is supporting full precision. I'm trying to see who told me this. Ben Ham told me that Octo supports full context window.

[00:34:42] **Alex Volkov:** Okay, full context window, not full precision. And Carlos said that SambaNova supports the 405 billion parameter model in full precision. That's true. We've talked with SambaNova. If you guys remember, maybe a month ago, we've talked to Rodrigo Leanne, SambaNova CEO, and they have uploaded a 405B in full precision.

[00:34:59] **Alex Volkov:** However, SambaNova is not a consumer company. You cannot use this. very easily. Carlos, while that's true, and I'm hoping to get an API key and test this. it's not like it's open for folks, but yeah, that's true. SambaNovaAI is supporting 405B in full precision and Octo is supposedly supporting 128K,context.


## [00:35:17] Meta's Evaluation and Performance Insights

[00:35:17] **Alex Volkov:** Now back to some of the evals. Again, Meta released a bunch of evals. We know that evals don't tell the full story. That's why we have folks like Wolfram and we have folks like LDJ and Junyang. I want to hear from you as well because I want to hear what this means to open source that this quality of model dropped.

[00:35:33] **Alex Volkov:** However, now I want to talk about some of the additional evaluations. They are not just open source ones like we saw, like GSM 8K. If you guys remember, I have like a very big interest in different evaluation, leaderboards, and scale has their own professional kind of held values. Back evals called SEAL, held back means they have their own eval suite that they don't expose to providers and I think they even do some more stuff that the providers won't see those evals and then train on them To in order to not leak and overfit them and so scale has a SEAL evals and right now LLAMA 3.

[00:36:15] **Alex Volkov:** 5 405 B beats math, beats Cloud 3 Opus on math. It's second place on math, and this is not math, the benchmark. This is math, like reasoning about math. And, it's fourth on code. But this eval doesn't have DeepSeq, so I don't know if it's really fourth. And it's number one in instruction following on the scale sealed leaderboard, which is quite crazy.

[00:36:38] **Alex Volkov:** And you can follow with my Twitter. with my thread, we're going down,Terry Yu from BigCodeBench. We've talked with Terry Yu before. BigCodeBench is the attempt from, BigCodeProject and Hug&amp; Face together to, to replace human eval. And that conversation is great. You should definitely listen to this on ThursdAI.


## [00:36:56] DeepSeaCoder and MixEval Introduction

[00:36:56] **Alex Volkov:** there was an update and DeepSeaCoder is now the best open source. I guess it's via API only, but it's the best coding, model is 3. 5 sonnet level, Lama 3. 5, 405 billion parameter is the second one or third one or something like this. Yeah. So very good coding as well for this big model. Let's keep going and see what else eval wise we have.

[00:37:19] **Junyang Lin:** Just, 

[00:37:20] **Nisten:** correct. So Sam Nova is up, you can try it in FP 16, but I think their output is limited to about 2000

[00:37:27] **Alex Volkov:** Oh, you can actually try this on the website.

[00:37:29] **Nisten:** Yeah, you can try it on. yeah, on on Sam Nova, I got 30 tokens per second, a full output. some other things, Together API gets 60 TPS and, but they're also running Flash Attention 3 and all of those optimizations, but that's in FP8 and they say it's in FP8.

[00:37:46] **Nisten:** So yeah, 30 TPS on Samba Nova, but, with a limited,output. And the DeepSeq model, by the way, is open source, they open source the latest checkpoint and that one beats Opus. And, honestly, I think that is still in terms of performance per active parameters. and performance for speed. I would say that's still, it's probably still the best, the best model.

[00:38:08] **Nisten:** you have a model better than Opus that only needs 21 billion active

[00:38:11] **Alex Volkov:** Wait, are you sure that the DeepSeaCoder checkpoint from yesterday was open source as well? The DeepSeaCoder, not

[00:38:18] **Junyang Lin:** or

[00:38:19] **Alex Volkov:** yesterday, Nisten. Things move

[00:38:20] **Junyang Lin:** yesterday was a brand new one. oh, that's crazy then. All right,

[00:38:25] **Alex Volkov:** as you folks can hear, even co hosts of ThursdAI are finding out things on ThursdAI. Yesterday DeepSeek released something.

[00:38:33] **Alex Volkov:** We're gonna, we're gonna cover this. Alright, moving forward in metal stuff. So we covered capability, we covered some evals. one last thing that I want to talk about evals because, this is not a very standard one. mix eval. If you guys remember, we talked with the folks Jji and some other folks from, I mix eval, J Yang.

[00:38:47] **Alex Volkov:** You wanna maybe, can you unmute and see if we, if we can hear you Jang if you are with us?

[00:38:53] **Junyang Lin:** Yeah, hi, can you guys hear

[00:38:54] **Alex Volkov:** Yeah. We can hear eval. Do you, do you wanna introduce mix eval, like super quick and what this is for the folks in the audience who haven't maybe heard this? 'cause I think you introduced me to Jji and some other folks, and you guys posted mixed e scores as well.

[00:39:06] **Junyang Lin:** yeah, sure, this is a little board led by, Junjie and, Xiangyue, and you may know them on Twitter, and, it is actually an evaluation of multiple data sets that actually approximate the performance of Treble Arena, so you just, use the mixed eval and you can guess how you perform in Treble Arena based on my understanding.

[00:39:25] **Alex Volkov:** Yeah, that's great. And thank you. And thank you for introducing the folks to us. So they came on the podcast and we talked about MixEval. So that's also something you can hear, on previous ThursdAI. We actually in Words Biases, we ran, let me see if I can find this and add this for you as well. it's part of the thread there, but I'll add this.

[00:39:41] **Alex Volkov:** So Morgan, from the Words Biases team actually ran the MixEval, code. Let me see if I can find this, here. And you can see that. this Mixed Evil approximates, LMSys Arena. So LMSys did not yet give us score for, Meta Llama 3. 1. For some reason, OpenAI, when they released the model, LMSys, ta da!

[00:40:03] **Alex Volkov:** We've been testing this all this while. Here's the scores. but Meta doesn't have the specs. pool for with LMSys for some reason. and we don't actually have a LMSys Arena score for, Lama 3. 1405, but we ran Mixed Evil for you. yeah, we spent that money. So you can see that Lama 3.

[00:40:18] **Alex Volkov:** 1 scores a very high 66. 19 on Mixed Evil Hard, which should correlate with Arena Hard. And that's number two. if this correlates correctly, and based on the research that they did with MixEvil, it should correlate with 96 percent I believe. it should land on something like number one or two on the MixEvil arena,or the LMSys arena.

[00:40:37] **Alex Volkov:** LDJ, go ahead.


## [00:40:40] LLAMA 3.1 Multimodal Capabilities

[00:40:40] **LDJ:** Yeah, I just wanted to mention a couple other parts of the LLAMA3 paper that I think are somewhat important of the multimodality. They said, Zuck said in an interview with,Rowan and also in the actual LLAMA paper, they detailed the multimodal architecture, which is like image and video dedicated, like adapters and layers added to the model architecture, as well as, AudioIn and AudioOut.

[00:41:03] **LDJ:** And they said that they're currently still developing it, but they revealed some multimodal benchmarks for it. And it's actually coming pretty close to the multimodal benchmarks for, Gemini and, GPT 4 Vision. And Zuck said in the interview with Rowan that he expects that to come in the next few months, and they've had some unfortunate setbacks, but he thinks it's going to come soon.

[00:41:24] **Alex Volkov:** Yeah, and some of the setbacks are like, I think, regular, regulatory, I think, because, he definitely talked about European, constraints, regulatory constraints about multimodality in products, but also in, in, in just, training as well. but [00:41:40] not only that, I think, LDJ, correct me if I'm wrong, but also posted how to actually do this or like their outline of the scheme of how to train multimodal.

[00:41:47] **Alex Volkov:** And the thing that I noticed there is that they have not only images into multimodality, they also have video. So they would support something like video with image batching. And on the output, they have speech, which is super cool. Which is super, super cool. Unfortunately, on the output, they don't have diffusion models, so it won't, draw images for you, but it will definitely, you'll definitely run, it will definitely speak to you, which is something I'm waiting,very hard for.

[00:42:11] **Alex Volkov:** Um,I think that's enough URLs. No, I think it's clear to us that this is like one hell of a model that beats GPT 4.is it not clear? Anybody else, not clear about this? Junaid, I want to hear from you. Because,as an author of the previously, one of the biggest and best, open weights models, you guys just got beaten.

[00:42:28] **Alex Volkov:** I don't think you guys are sad about this. I think this maybe just lits a fire under your collective essence, hopefully. but I would love to hear from you as a team who like previously. the incredible releases in the open source. What does this mean to have this level of, foundational model in the open weights in the open source?

[00:42:45] **Alex Volkov:** maybe what did you learn from their paper, if anything?

[00:42:50] **Junyang Lin:** Yeah. yeah, it was really amazing to see such large model. Actually, last weekend I talked to the, guys and they said they were busy working with Yeah. Lama 3.1, and I was a bit afraid. Yeah. A really 4 0 5 B. It's such a big model to open source, so yeah, it's true. It's really amazing, and it's a bit sad they did not compare Quentoo with Llama 3.

[00:43:18] **Junyang Lin:** 1, so we just did some comparison. Yeah, we are still a little bit falling behind the 3. 1, especially for the Instruct model. I think this one is a great success for the post training. Because for the base language model, you can see that LLAMA 3. 1 is actually very similar to the LLAMA 3, but for the post training, LLAMA 3.

[00:43:42] **Junyang Lin:** 1 AB and 70B, it's improving quite a lot in the benchmark datasets. Yeah, so I think the Biggest lessons for us to learn is that you can train a very large model for a teacher model. It is just like an expert and you can use it to for the distillation to improve your smaller models. So maybe we can later see something like 70B model, which is really GPT 4 level and it will become something true and that will be something very effective and, but also very, efficient.

[00:44:17] **Junyang Lin:** The, another comment is that for the 405B, personally, I think it can be even better, so I think they are still working on some better stuff, maybe a lot more, yeah. That

[00:44:30] **Alex Volkov:** Lama4, I think,Rowan Cheng, when he talked with Zach, he asked about Lama4 and Zach is let's give people like a week to get excited by 3. 1 before, before we like speak about 4. 0 excitement. Let's give people like a week, and which is also my kind of feeling about this as well. 


## [00:44:45] Distillation and Production Models

[00:44:45] **Alex Volkov:** I want to LDJ, before I get to you, I want to talk about the What Junyang just mentioned, so we were just like talking about the 405, the bigger one, the, like the one that beats GPT 4, et cetera.

[00:44:57] **Alex Volkov:** The other two models, like Junyang just said, they were distilled from the teacher model and the improvements are crazy for the past one. They kept training them. They also learn from the teacher model and they outlined this in the paper, I believe. And also Zach talked about the distillation, the differences between April and now for, for LLAMA70B.

[00:45:17] **Alex Volkov:** For MMLU, it's a six point difference. So Lama3 70B in April was 80. 9 and now it's 86.for ifEval 82 in April, 87 right now for 70B. it's actually reduced by one point on human eval, which is very interesting. But, let's see what other scores get jumped like super quick. GPQA, which is, Google Proof QA, we talked about GPU QA a while, jumped by 7 points from 39 to 46, which is quite impressive.

[00:45:47] **Alex Volkov:** And obviously tool use got improved significantly because, these are the skills that this model can learn from the bigger model. From, for BFCL, they jumped only by a point, actually, but they jumped on the Gorilla Benchmark by, Wow, from 14 to 29. So yeah, this is for the Lama 70B and this definitely shows that the 70B is now like a bigger model.

[00:46:09] **Alex Volkov:** And I wanted to ask folks here on stage, this is as far as I heard from like multiple folks as well, that 405B may not be like the best model for production, actually. It may be like the best model for like distillation. for data set creation, for synthetic data sets, for maybe LLM as a judge, but may not be the best for, for production because like you have to lift all those, you have to like to have enough VRAM for all of this.

[00:46:34] **Alex Volkov:** However, like 70B seems to be like an incredible model for production. I want to hear your guys thoughts on this, Nisten maybe, and then LDJ.

[00:46:43] **Nisten:** was not my experience with summaries. I know 70B gets pretty high on the benchmarks, and I might be able to do some speculative stuff, optimizations with it, but, It's way better. Dude, I just asked it to build like a magnetic mass launcher on Mars that launches on top of like Mount Olympus and stuff and it's just it's like the most like stoner question you're just like, oh we're gonna shoot a maglev train.

[00:47:11] **Nisten:** Off the top of the mountain on Mars, like how much do we need? How long does it, it did it all. Like it, it looked through the table of air densities, compared it with earth, it calculated the energy, like it just did it, dude. this thing just freaking did it, and it's a very hard question for other models.

[00:47:28] **Nisten:** They all, hallucinate, they all mess up. This thing just freaking did it. the most insane things you can ask, like a galactic project of stuff, it'll just calculate it. Yeah, this is, the 70B can't,

[00:47:42] **Alex Volkov:** It's not

[00:47:42] **Nisten:** gonna get even 

[00:47:43] **Junyang Lin:** close,

[00:47:43] **Alex Volkov:** It's not there. I see. LDJ, what's your take on the bigger model for production use versus, smaller models compared to, like, how good the smaller models also got?

[00:47:53] **LDJ:** Yeah, I think that there's always going to be different use cases of depending on the use case, the smaller model will probably be like good enough and then you might as well just use that because it's going to be cheaper no matter what provider you use, pretty much. However, the 405B is still only, I think it's available now for 3 and out per million tokens, so that's cheaper than GPT 4.

[00:48:11] **LDJ:** 0 and I think in some decent amount of use cases it might be equal or better than GPT 4. 0 as well, so that'd be a no brainer to use 405B through some Cloud providers in that situation and then also the fact you have I guess more to an extent on censoredness and things like that with 405b, especially if you finetune it.

[00:48:34] **LDJ:** But there's also this part of the paper where they mentioned, execution feedback. Here I have this short quote in front of me that I'll read it. We introduce execution feedback as a source of truth, enabling the model to learn from its mistakes and stay on track.and so they, they mentioned a few other details in the paper about how,They pretty much had a system during the post training, where they had the model learn to refuse answers to questions that it didn't actually have the knowledge to or wasn't trained on.

[00:49:05] **LDJ:** So that should actually maybe help the model say things like, hey, I actually don't know, or I'm not sure I would have the right answer to that question, instead of just hallucinating like some other models.

[00:49:16] **Alex Volkov:** Yeah. Execution feedback. I'm getting a little bit of feedback myself on my mic. Hopefully you guys can hear this. the, okay, so this is the 70 parameter model. Let's cover the smaller one, because I think, also, the Lama 3. 


## [00:49:28] Smaller Models and Fine-Tuning

[00:49:28] **Alex Volkov:** 5, 8 billion parameter, got incredible updates as well. From 65 MMU to 73, like a huge jump on if eval, so instruction following got to 80, 80 score as well.

[00:49:37] **Alex Volkov:** human eval, shut up. to 72 from 60 to 72, that's like the results of the distillation that Julian talked about from 60. 4 to 72. 6. So like almost an 8 percent jump in human eval and MVP plus as well. The reasoning and tool use as well jumped from 60 to 76, like a huge jump in like this very [00:50:00] small model.

[00:50:01] **Alex Volkov:** And this one we can run on our Macs, right? this is like most of us, if we have a Mac from like M1, M2 or M3, we can run this, some of us even in like full precision, in fairly quick speed, we can run this model on our Macs. 8billionparameter is already getting fine tuned from multiple people, so shout out to Kyle Corbett from OpenPipe, which is a service that doesn't pay me, but I'll shout them out anyway, that they do fine tuning.

[00:50:26] **Alex Volkov:** He quickly, Quickly added 8 billion parameter model to their,service and saw that it could potentially beat 4. 0 mini when prompted. So like a Finetune 8 billion parameter can beat like a prompted GPT 4. 0 mini. Which is great, because many people would prefer to run this model, and this is a model that you can run.

[00:50:47] **Alex Volkov:** This Finetune, by the way, is not the type of Finetunes that we talked about, right? like, when Jun Yang and the Quen team released,the Quen based model, and somebody like, LDJ or some news folks Finetuned that, to, to be a generic model, that's different. what we're talking about here is, Finetuning for specific purpose tasks for, and for a category, if you're a business and you want to fine tune this for your stuff.

[00:51:06] **Alex Volkov:** So that fine tune, they show that the 8 billion parameter model can outperform on those tasks, a, just a prompted model. Which brings back the whole thing about fine tuning,for, for business purposes, which is great. I think it's super, super great. This small model is very malleable, it's super lightweight to run, it's super cheap to run as well.

[00:51:28] **Alex Volkov:** You don't have to run this yourself. You can go to TogetherAI or Fireworks or whatever. All these services will also let you to fine tune and upload this model, fine tunable. You can run it. but you can absolutely run this yourself. This is the model that you can like fine tune for your own tasks.

[00:51:43] **Alex Volkov:** And if you require air gapping, if you are in the medical profession, whatever. You can definitely use these, small models for incredible stuff like this. but as Nisten said, 405B is still, incredible for summarization. thoughts on the smaller model? Wolfram, I know you have some thoughts about the smaller ones that we can run for fully offline, for completely free, and for our purposes.

[00:52:06] **Wolfram Ravenwolf:** Oh yeah, definitely. So that is the one I was comparing with the bigger 12B model from Mistral, the Mistral Nemo version, which already surprised me how good it was. And the Gamma 2 from Google, 27B. So it did stuff better than those. So I think Yeah, it would probably be my favorite now that it is multilingual as well.

[00:52:27] **Wolfram Ravenwolf:** And, yeah, you can run it locally, you can run it unquantized, of course, if you have enough VRAM. it really is a good one. And, one thing is important when you run in production, you want to handle a lot of users. you need,a fast model and running 405B in production for a lot of users is probably out of scope.

[00:52:45] **Wolfram Ravenwolf:** So most people will have to use a cloud service, but the 8B, you can easily put it on every system where you have a lot of users and handle all of them. So it's probably the most useful model right now for a lot of people, a lot of use cases. And it's great. It's really amazing how good it is now.

[00:53:04] **Alex Volkov:** it's good now and just wait until the kind of the finetuning community, grabs their hands on this small model because this is the one they're going to start like finetuning like super quick because it's like very easy as well. And the mergers once they get, I can't wait for Maxime Lebon to start merging this with like crazy like other stuff like Beagle and everything.

[00:53:23] **Alex Volkov:** LDJ, go ahead please.

[00:53:26] **LDJ:** Yeah, just wanted to give people information. If anyone's curious about how Fast Rock is able to run these new models. the eight B is running at about a thousand tokens per second. The 70 B is running at about 250 tokens per second, and they have the 4 0 5 B running around 100 tokens per second.

[00:53:44] **Alex Volkov:** that's insane. I wanted to shout out the video that the CEO of,Grok posted. I don't know if you guys saw this. I'm going to add this just now, super quick. he posted a video where he just talks, full real time. Let me see if I can like super quickly find this. it's not the new, yeah, this one, Jonathan Ross.

[00:54:02] **Alex Volkov:** this is the video, if you guys want to see this, but if not, I can just describe what's going on here. Jonathan Ross talks to this model, at grok speed, and this model prints out columns, And it just generates so, like how I talked about different, UI generating things before, like open UI from Waitz and Biosys co founder, Chris, this is not that, this is just like text, but he asked for a table and then he asked for grok to like move columns,with the grok speed.

[00:54:31] **Alex Volkov:** And the columns just appear like this model stream token. They print like text, but he asked for like tabular data and you could just see it. Like the columns just like honestly appear because I think he was a 70B or maybe 8B. because of this like incredible, like thousand token speed, things just appear.

[00:54:45] **Alex Volkov:** And he talks to it because of the voice interface. Just, I don't know, this whole experience just blew me away. And this is something to definitely look forward to. That's not something that we're going to be able to use with 405 billion parameter, at this point. Folks, I think, an exact hour into this, it's now 10.

[00:55:04] **Alex Volkov:** 30am where I am, we have covered most of what I wanted to cover for MetaLlama 3. 1, 405 billion parameter, 70 billion parameter, and 8 billion parameter, and I think we're gonna open the stage for like different things we didn't cover yet. LDJ, please go ahead.

[00:55:21] **LDJ:** Yeah, I was going to say, if we would just want to close that real quick with, I have a quote in front of me of Zuck, just teasing Lama four, if

[00:55:28] **Alex Volkov:** really? Yeah, let's go ahead, please.

[00:55:30] **LDJ:** Yeah, he said, quote, I think it might be a little early to talk about LLAMA4, but we've got the compute cluster set up, we've got a bunch of the data set up, we have a sense of what the architecture is going to be, and have a bunch of research experiments to max that out.

[00:55:43] **LDJ:** And I do think LLAMA4 is going to be another big leap on top of LLAMA3, end quote.

[00:55:48] **Alex Volkov:** Yeah, that big leap is going to be very interesting. I can imagine by then, where are we going to be? Because by then, we're probably going to see Opus. And, It needs to be said, it needs to be said that Anthropic cooked with Sonnet 3. 5, really cooked with it, because since then we saw the release of, ChatGPT 4.

[00:56:10] **Alex Volkov:** 0 Mini, and Opus is still the best. In every benchmark, Opus beats all of the models. Opus right now is like the king of LLMs that we can access. Probably OpenAI has like a bunch of other stuff behind the scenes they're not releasing. Opus right now is like the best LLM that we can use. Unless you believe LMSys Arena, in which GPT 4.

[00:56:33] **Alex Volkov:** 0 is the best model and GPT 4. 0 Mini is also the best model. I don't know if you guys saw this update, from, two days ago or yesterday. And, this got everybody from our, bubble or our area of, X just, really, raising eyebrows at LMSys and, like, how weird this became.

[00:56:50] **Alex Volkov:** Because, that's not our experience. None of us experience. the GPD 4. 0 Mini, which is quite incredible and super fast and cheap. all of this, yes, but it does not seem like it beats CLOD 3. 5 at anything. especially like when you actually talk to these models, and this raises eyebrows at human, sorry, at LMSys Arena's ability to estimate models, Wolfram, go ahead, please.

[00:57:12] **Wolfram Ravenwolf:** just a quick correction first. You said Opus. I think you meant Sonnet, right?

[00:57:16] **Alex Volkov:** I meant, yeah, 3. 5 Sonnet, Opus is not here yet, and when Opus drops, that's going to be like incredible. yeah, sorry, I got myself confused. 3. 5 Sonnet, The Middle Child, The Incredible,thank you.

[00:57:28] **Wolfram Ravenwolf:** And, solid is still my favorite model, definitely. But, back to the LMSys Arena and so stuff. So I have seen that phenomenon a lot of times with smaller models where people say, Oh, this 8B, it's like a 70B. So that was last year even, because the models, they write so well that the writing, yeah, it's, How can I say it?

[00:57:48] **Wolfram Ravenwolf:** if they write so well, you think they are smarter than they actually are. Like, when somebody is very eloquent, they can appear to be smarter, and you really have to test their intelligence to find out. there's a discrepancy there, and I think people, especially if it's a one shot job, they You ask a question, you get a bunch of text and it sounds good, so you say, yes, that's a great model.

[00:58:07] **Wolfram Ravenwolf:** So that is a different kind of what they are testing, and when you are optimizing for that, like they did with the mini model, then you get great scores in that part. it's not gaming the system, it's optimizing for the system, and you all know the [00:58:20] saying, when you have a benchmark that becomes a target, it ceases to be a benchmark, so I think that's just what we are seeing here.

[00:58:27] **Alex Volkov:** Absolutely. And definitely that's not what we're seeing on the other benchmarks across the board for instruction following, for coding, for math. But this is what we're seeing for like just human kind of comparison between two models, which is what LMSys Arena provides for us, in the overall category.

[00:58:43] **Alex Volkov:** So very important, if you are to trust LMSys Arena, there are different categories. There's LMSys Arena Hard, there's coding, there's like different areas, dive into those and see that like their sauna 3. 5 actually beats 4. 0 and definitely 4. 0 meaning. but on the overall, I think Wolfram, you hit it, you hit the nail right on the head where like people maybe prefer just the style of the answer, and which is something that OpenAI obviously has a lot of ability to train because they're still probably the leading provider in just how many people are using them.

[00:59:13] **Alex Volkov:** and probably the RLHF, they're the kings of RLHF. I think, Last comments about 3. 1. I think we're going to keep talking about this as new things come out, as new fine tunes come out, I want to hear maybe something else from Jun Yang, anything that we haven't covered yet that excites you about this week, that excites you about looking forward about using these models.


## [00:59:30] Synthetic Data and Licensing

[00:59:30] **Alex Volkov:** Oh, license. Let's talk about license. One thing I skipped completely. I updated this in the beginning. Meta updated their license to allow for synthetic data creation and generation, and also distillation. I think that's very important. That's like a huge thing for folks like, like Nous Research and Technium, and other Finetuners as well.

[00:59:50] **Alex Volkov:** They themselves used a lot of synthetic generated data to train these models. And now they also opened this up for, for everybody else, for dataset creation as well. I think that's huge. LDJ is somebody who creates a bunch of datasets. Junyang is somebody who trains open weights models and probably uses a bunch of open datasets as well.

[01:00:10] **Alex Volkov:** Did you guys give me some comments around this area of how much this could affect a model of this size? Because OpenAI still, even though everybody does this, OpenAI doesn't allow, definitely not distillation, but OpenAI doesn't allow training on its outputs, I believe, even though everybody does this.

[01:00:26] **LDJ:** Yeah, I think this is actually pretty important because even though, like you said, a lot of people still train on OpenAI outputs anyways, there's a lot of legal departments and a lot of small, medium, and large companies that they restrict the, people building and fine tuning AI models within that company from actually being able to build the best models that they can because of these restrictions.

[01:00:48] **LDJ:** And it's It ends up, I think, this might be probably the best model that they could actually use that the legal departments would actually give the okay on to generate synthetic data to train models on, and I think that's going to improve a lot of the different types of maybe custom models implemented into products in different companies that we might see, and different ways that AI is actually implemented into different use cases across different companies.

[01:01:15] **Alex Volkov:** Yep. Junyang, any thoughts on, how much this will unlock for the open source community? This license change?

[01:01:22] **Junyang Lin:** yeah, I think it explains why they open source such a large model because it is not easy for people to fine tune and deploy it with such a large model. You need a lot of devices, but for such a large model, you can help people to really improve their fine tuning. I think in the community, there are a lot of people.

[01:01:44] **Junyang Lin:** who suffer from high quality fine tuning because they do not have high quality data for their domain and for, yeah, for their use cases. But with LLAMA, yeah, 405, you can just fine tune it and be a very good teacher and then generate synthetic data to train your 7TB models so that you can deploy it with your 7TB model, pretty well.

[01:02:07] **Junyang Lin:** So I think This is the greatest meaning for opening such a large model, one of the explanations. Yeah.

[01:02:14] **Alex Volkov:** Yep, absolutely. All right. So I think license is the last thing that we have left to cover and multimodality we've covered. They've trained them. they didn't release them, but they have the path and maybe the open source community will bid them to it. Maybe we'll see like a lava on top of a, of Lama70B, probably in easy update.

[01:02:35] **Alex Volkov:** It probably. Folks are cooking this right now, especially because, they already posted some of the ways that they would do this. Nisten, any parting thoughts on this before we move on and talk about Mistral?

[01:02:47] **Junyang Lin:** no,

[01:02:48] **Alex Volkov:** Awesome. Okay. Amazing. Great. Easy. All right. I think we're moving forward. 


## [01:02:53] Weights &amp; Biases Weave and Mistral V2

[01:02:53] **Alex Volkov:** Before we move forward, though, I want to reset the space a little bit. There's a bunch of you here and probably some of you who stepped in the middle of the space. So you're on ThursdAI. We're here for more than a year and a half, I think, every Thursday.

[01:03:08] **Alex Volkov:** Since GPT 4 was released March 14, 2023, every Thursday, we took one break. Two weeks ago and a week ago, for the first time, because I was on vacation, but since then every Thursday and going forward, probably every Thursday as well, and we cover everything in AI. And so I'm here with a bunch of friends of mine, experts in different fields, Junyang Lin from Quen, LDJ, creator of multiple datasets and machine learning, expert in himself, Wolfram Alpha, who if you've ever visited local, Llama Reddits, you may know him.

[01:03:37] **Alex Volkov:** He's like one of the best. estimator of vibes of models and comparisons, definitely. And Nisten,frequent co host of mine, Raccoon, Should I say, yeah, Raccoon Skunkworks AI and Raccoon. ai person, and just like a crazy hacker that can run pretty much every model, no matter the size on CPUs. I have a bunch of other friends here in the audience.

[01:03:57] **Alex Volkov:** My name is Alex Volkov. I'm an AI venturist with Weights Biases, who is, Basically, the reason why ThursdAI still exists and runs. And speaking of, now that we have a little bit of a reset, Weights Biases, I also have a corner here that talks about this week's buzz. What happens with Weights Biases every week.

[01:04:14] **Alex Volkov:** And in this week, obviously, the stuff that we have are related to Metal Llama 3. 1. And so So, the product currently that we have, the main product that we have at Weights Biases is called Weights Biases Weave, which is our evaluation and tracing framework for LLMs. And I wanted to use this in order to test some stuff with Metalama 3.

[01:04:34] **Alex Volkov:** 1. And the stuff I wanted to test is around the different server providers, service providers for LLMs. for example, as LLMA 3. 1 was released. TogetherAI, Grok, DeepInfra, Fireworks, and a bunch of others got access about six days before and they started putting this on their framework, on their, sorry, on their infrastructure, inference infrastructure.

[01:04:58] **Alex Volkov:** And all of them provided this in a little bit of a different way because all of them maybe run, some run on VLLM, some run on, FlashAttention3, like Nisten mentioned, for Together. Because the creator of Flash Attention works there, shout out to Tridao and his amazing contribution to the world. and Grok runs them on their own specific hardware, which actually helped them debug a little bit with the bug that I posted.

[01:05:20] **Alex Volkov:** So shout out to Grok as well. And so I just wanted to Test differences. So I am posting a link on the top of the space for something like a test that I did, like an eval that I did. This evaluation is not like a full evaluation that we've talked about where it just runs things and tests if the model answered them because I'm not evaluating like one model against the other model.

[01:05:39] **Alex Volkov:** I'm literally evaluating the same model from different providers and just testing whether or not different hardware, causes it to run differently, which is very interesting, like thought experiment and, the visualization. comes with the help of Weights Biases Weave, and so I can add this link as well.

[01:05:55] **Alex Volkov:** And if you guys want to check this out, please look at this Weave link. It will give you like a nice comparison dashboard. It's a very, very nice like visualization, and we're really, very happy with this like new feature where you can compare between evaluations. So this is what's new with Weights Biases Weave this week.

[01:06:11] **Alex Volkov:** If you want to give Weave a try, it's super simple. wandb. me slash weave. Yeah, it took me less than, I don't know, four hours to run this whole thing while also trying to figure out how to wrangle OpenRouter. So the way I was able to achieve this is via OpenRouter. So shout out to Alex Atala with OpenRouter.

[01:06:29] **Alex Volkov:** I released our conversation with him two weeks ago. The conversation took place in April. So if you're interested in OpenRouter and how it works and why it has placed, please listen to that conversation from [01:06:40] two weeks ago at thursdai. news. Now, moving on. To Mytral large V two. So a day after Netta released, Lama 3.1, they gave us a day.

[01:06:52] **Alex Volkov:** Mytral gave us a day to celebrate like biggest state of the art news, and when they announced their new, mytral large V two, it's 123 billion parameter dense model. Mistral likes to release a mixture of experts. So obviously Mixtral and Bigstral are different mixture of expert model that they've released previously.

[01:07:13] **Alex Volkov:** and now they released a big dense model. One like huge 123 billion parameter model. This comes after a few weeks ago, they released A few other Mistral models. So they've been on the roll lately. they released CodeStral and they released, MathStral, which is specific for math, it looks like this is the model that is now like taking all of that into one.

[01:07:35] **Alex Volkov:** So they also started deprecating a bunch of models on their API. this is a non commercial license model. It comes with, I believe also 128, 000 tokens, Nisten, correct? I think you mentioned this before.

[01:07:48] **Alex Volkov:** Nisten, if you're still with us, yes, 128, 000 tokens as well,which is great. it like again, research license only, but a large context window. Let's see what's interesting there. MMLU of 84. So not quite beating like LLAMA 3. 1, but also it's like way smaller. on multilinguality, I think it, it's quite, it's starting to compete on multilinguality.

[01:08:12] **Alex Volkov:** Again, something that Mistral is very good at on different like languages like Chinese, Japanese, Korean, Russian, and Portuguese. It has a very high empty bench score of 8. 


## [01:08:20] Exploring the New Coding Model

[01:08:20] **Alex Volkov:** 6 and arena hard of 73. what else can we see here in this model? so they used a bunch of their kind of code straw experience to actually make it very proficient in coding.

[01:08:33] **Alex Volkov:** So this model was trained on 80 plus coding languages in Python, Java, and JavaScript. And in this release, they actually highlighted that, this model beats Lama 3. 1405 on different coding languages, actually, which is pretty cool. Like it's a smaller model. Definitely beats a 70 billion parameter. this model is available via API, and I do believe they released it in Huggy's Face as well.

[01:08:58] **Alex Volkov:** Any thoughts on this? 


## [01:08:59] Mistral Large 2: A Game Changer in Coding

[01:08:59] **Alex Volkov:** Nisten, you had thoughts, but I would love for you to repeat this for this section as well, just for recording sakes.

[01:09:05] **Junyang Lin:** Yes, I 

[01:09:06] **Nisten:** used it extensively yesterday and today, and while it doesn't give as nice of an output, it's still a very Mistral like output. It does follow the instructions extremely well. for stuff like very hard questions, I could still see better results from Sonnet than the others. However, the one thing that this model does that the others don't, is that it will give you out.

[01:09:36] **Nisten:** close to more than 32k or 64k output. what I did was like, I just dumped in an entire, a small code base. I gave it a list of 30 things to do. And I said, give me, create a small and hard example for each of these items on the list. And it kept going until its context was full. Another thing is I dumped in up to 90 something thousand tokens of context.

[01:10:03] **Nisten:** And set to summarize it and remove comments and remove duplicates. And it did it. It did it exactly. And Sonnet would not do that. I used projects. I used it with Opus. Opus would get close. none of the other models really do something like that reliably where you can just dump in a whole code base.

[01:10:23] **Nisten:** Give it a whole bunch of instructions and expect complete output without skipping anything, no rest of comments here, no, shortening it, it's, when they say 128k, this feels like a real 128k.

[01:10:37] **Alex Volkov:** That's very interesting. I wonder, What that like how and why because other providers also claim 128k Claude even claims 200, 000 I believe and If I'm not mistaken, Gemini has a million Okay, moving on to another thing that they claim have and I don't really understand. 


## [01:10:57] Function Calling and Retrieval Skills

[01:10:57] **Alex Volkov:** What is the metric They say, that Mistral Large 2 is equipped with enhanced function calling and retrieval skills, and has undergone training to proficiently execute both parallel and sequential function calls, which is super cool.

[01:11:09] **Alex Volkov:** I actually haven't seen that clarification from Meta. I think Meta just, does, a straight up, one function call. I haven't seen, parallel function calls. Maybe I'm wrong. we didn't have enough time to check it out with Lama. Maybe it does do parallel. But Mistral claims state of the art on function calling, even against GPT 4.

[01:11:26] **Alex Volkov:** 0 and others. And they posted like a graph. This graph has some accuracy and Mistral Large2 is beating GPT 4. 0 and Opus and Sonnet and Large, like the previous Large. But this graph doesn't say where it comes from, where it comes from. I don't know if you guys have seen this, where it comes from. I haven't.

[01:11:46] **Alex Volkov:** And I asked. And I didn't see the answer. Nisten, do you know, what they're testing here? Is this, the Berkeley function calling or what?

[01:11:54] **Nisten:** what this looks like to me is they're comparing it if they ask it to generate like 30 functions or 10 functions. And this is why I think the model's strength is of experience. If you ask it for 20 things, it will do all those 20 things at the same, like intensity. Whereas, even with Sonnet 3.

[01:12:12] **Nisten:** 5 and stuff like they will do. Maybe one big function really well, and then the rest they'll start shortening outputs. So this is what I suspect they, 

[01:12:22] **Junyang Lin:** they mean by it.

[01:12:24] **Alex Volkov:** It's very interesting that there's no, reference to this thing. And honestly, there's also no comparison to, to LLAMA 3. 1 in the function calling area. Maybe they just didn't have time to run this, or maybe they didn't know, like, how to actually, execute on function calling with, 3 point, sorry, 405 billion parameter LLAMA.

[01:12:43] **Alex Volkov:** Let's see. 


## [01:12:43] Availability and Deprecation of Models

[01:12:43] **Alex Volkov:** So the weights are available on Hug Face, but again, non commercially licensed. And, you can access this through the cloud services via Leplatform. I don't know if I'm pronouncing this correctly. And you can play with this via Lechat. but also, they are now deprecating other, other models that they have been serving via this lab platform.

[01:13:05] **Alex Volkov:** as we get this large V2, I think the only models that are remaining is Mistral Nemo, which they trained together with NVIDIA. I think in the updates, I missed that one, so if you're following your news explicitly to ThursdAI, which you shouldn't, I'm very, interested to see who, people who follow only exclusively on ThursdAI, we skipped this one, but Mistral, also trained a model called Nemo together with NVIDIA.

[01:13:30] **Alex Volkov:** And, so now the only two models that you can get are two general purpose models, Mistral Nemo and Mistral Large V2. And, two specialist models, CodeStral for coding specifically, and Embed, which they have an embedding model. And they will deprecate all Apache version models like Mistral 7b, Mixtral 8x7b, and BigStral 8x7b.

[01:13:50] **Alex Volkov:** It's 22 and CodeStrollMamba, which they just released like two weeks ago. So they're already deprecating this. That's very interesting. In their API, you can still download these models. You can still run these models if you want to. there will be remain available for deployment. So you can run them yourself.

[01:14:05] **Alex Volkov:** so very interesting changes in, in, in Mistral and, interesting changes in Apache open sourcing as well. So we're going to have to wait and see. when Mistral will give us an open source model, but still this 123 billion parameter model is also almost GPT 4 level. in the same week A day after Meta gave us a almost like beating GPT 4 model, we got another one that comes very close on multiple parameters.

[01:14:33] **Alex Volkov:** Come very close. just to read you some like human eval, it comes very close by I think it beats it. I think it gets to GPT 4 maybe like 2 percent difference on human eval or human eval plus as well. Like it's in the 85 versus 90. MBP plus also gets very close to it. It's. It's quite crazy that we got two models, GPT 4 level, GPT 4 O level intelligence in the open weights in the same week.

[01:14:59] **Alex Volkov:** [01:15:00] I don't know. anyone wants to share my excitement here about Mixtral? Feel free. Mistral Large, LDJ, anything on this? Have you had the chance to try this or Wolfram? Please go ahead.

[01:15:11] **LDJ:** Yeah, I think it's interesting, and if we're talking about Mistral Large 2, right? The one that came out two days ago. Yeah, so that one, I think in terms of the coding scores, It seemed to me

[01:15:21] **Alex Volkov:** not two days ago, yesterday, we're just like, we're moving so fast

[01:15:24] **LDJ:** yesterday, yeah, it seemed to me in the coding scores that I saw with the benchmarks they posted, in human eval, it was like beating 405B, but in most of the more reliable coding benchmarks that I feel like most people usually look towards, 405B seemed to still be beating it significantly.

[01:15:41] **LDJ:** However, it's still a really powerful model. It seems really good for its size and a really good in between of the, Lama 3. 170b and Lama 3. 145b. And just in terms of overall reasoning and math abilities, I think it could be a really good model for people to make fine tunes of and see what else they could leverage with those reasoning abilities.

[01:16:01] **Alex Volkov:** yeah. And also, they specifically talk about instruction following and alignment for this model, where they definitely claim second place over 4. 0. And for some reason in their kind of, benchmarks, they 4. 0 like beats, or I guess is the same level as Sonnet. And they're coming like third or second on Wildbench and Arena Hard for instruction following as well.

[01:16:25] **Alex Volkov:** Wolfram, please go ahead.

[01:16:28] **Wolfram Ravenwolf:** Mistral has always been very interesting to me. So it's a European company and they are showing that not everything is U. S. based. So that is, will be probably very important when you want to, when you later want to talk about The multimodality and where it will not be released. So that is why Mistral is also a very important player.

[01:16:48] **Wolfram Ravenwolf:** And yeah, I guess they had the model and waited until LLAMA 3. 0 came out. Maybe that was why they released it so quickly after it. But, yeah, because it's non commercial only or research only, it has limited capabilities, but it's okay. After all, Mistral has to make money with the models. What Meta does not have to do.

[01:17:08] **Wolfram Ravenwolf:** Yeah, I appreciate that they released it at all. That is already a great thing of them and I respect the company 

[01:17:14] **Junyang Lin:** a lot.

[01:17:14] **Alex Volkov:** 100%. They need to make money and they also need to, show that maybe Meta released something, but that something is hard to run on servers. Like a hundred twenty three. Billion parameters. I think they mentioned that this fits on like a huge like one, one, one big H100 or something like this. I saw somewhere that they mentioned that like it should fit on one device.

[01:17:38] **Alex Volkov:** I think that's the point of the scale, right Nisten? I think they mentioned something like this.

[01:17:42] **Junyang Lin:** Yeah, 

[01:17:43] **Nisten:** honestly, I feel like this might be the model I end up passing the most tokens through day to day just because of How I work, like I just dump in the whole code base and just tell it to try stuff. and this does that the most reliably. so I was surprised, like at first I was like, okay, Mistral is another model, but then I started just dumping stuff in and I go, no, this is good.

[01:18:07] **Nisten:** And, Consider that you can run it on your own as well. And, yeah,the quants should be pretty good. I think this is a model you should run it for a bit. it just keep, just keeps spamming it with stuff until something works. that, that's how I would use it. yeah, it might actually be the one I use the most surprisingly,

[01:18:22] **Alex Volkov:** Yep. shout out to Mistral, absolutely, and they need to show that,if you don't want to run Meta stuff, you want to celebrate Meta's commitment to open source, their, commitment in paper releases, and, help to the community, but you don't want to run models yourself, this one runs, they, I found the quote, they said, I found and lost it again, one second.

[01:18:43] **Alex Volkov:** Where is this? Where is this? Where is this in performance? I

[01:18:46] **Junyang Lin:** by the way. It's free, it's chat ai, just use it there for free.

[01:18:54] **Alex Volkov:** Mistral Large 2 is designed for single node inference with long context applications in mind. Its size of 123 billion parameters allows it to run at large throughput on a single node. I think this is like a definite,shout out towards a 4 or 5 billion parameter, that they compare it to a day after.

[01:19:12] **Alex Volkov:** I think we've covered Mistral 2. Enough. 


## [01:19:14] DeepSeq: The Silent Contender

[01:19:14] **Alex Volkov:** And I think the next thing that we're going to cover is, DeepSeq. So let's move on to DeepSeq. Although, I don't, I haven't seen the DeepSeq released an actual kind of checkpoint yet. So let's maybe cover DeepSeq super quick. DeepSeq is hard to cover folks.

[01:19:28] **Alex Volkov:** DeepSeq is a company that, That doesn't really talk a lot or announce a lot of stuff. And they have basically two models. They have DeepSeq Chat and DeepSeq Coder. For the longest time, DeepSeq Coder was like the best model that you can download for code. These things got a little murky lately because we just got like a barrage of different models.

[01:19:47] **Alex Volkov:** Every, everyone competing for the MMLU and the human eval, like all of these scores. And so it's really hard to know which models are now in the open source are the best one. and DeepSeek also offers an API, which is ridiculously cheap. I think the DeepSeek API, I think is the, the one thing that goes for DeepSeek API is that, it's ridiculously cheap.

[01:20:07] **Alex Volkov:** Significantly cheaper than, anything that you'd be able to host a LLAMA405B yourself, because you're going to have to pay for all those DPUs yourself. Significantly cheaper than probably even GPT 40 Mini, maybe around the area of Mini. Actually, you should probably look it up deep. DeepSeq API

[01:20:25] **Junyang Lin:** Yeah, it's 21 

[01:20:26] **Nisten:** billion active. It's, you can host it like neck and neck with the cost of many

[01:20:31] **Alex Volkov:** Yeah. Mini is

[01:20:32] **Nisten:** be able to host for 20 cents 

[01:20:34] **Junyang Lin:** an hour.

[01:20:35] **Alex Volkov:** yeah, Mini is 14 cents or something. And then DeepSeq is also 14 cents per million tokens. yeah, I think they're like, they're matching Mini, I think for price. but I think they beat Mini on, on coding ability, if I'm not mistaken. And so the reason why DeepSeq is hard to cover is because they keep updating this.


## [01:20:52] DeepSeq's Latest Updates and Performance

[01:20:52] **Alex Volkov:** Almost on a weekly basis, if I'm not mistaken. I think somebody in the comment just said, that I think Lincoln said,they updated the model yesterday. And so let's read the change log a little bit. let me actually add, thank you Lincoln for,for this addition. I'm going to add this to the top of the space.

[01:21:08] **Alex Volkov:** Here's the changelog updated API chat completions. They added JSON mode, they added function calling, they added a fill in the middle completion in beta and a generation of 8k max tokens. So you can like now generate up to 8, 000 tokens like on the output. And, they now have a new completions API for fill in the middle completions.

[01:21:28] **Alex Volkov:** and for more documentations, please see documentation of something like this. This is, yeah, I think they released it like a week after they released like a different other version and barely, we barely had the day, like this was released like earlier and earlier on today and I think quick and dirty tests from big, big code bench, I think, placed this DeepSea coder at number one with Cloud Sonic 3.

[01:21:56] **Junyang Lin:** 5, which is quite incredible. I just tested 

[01:21:59] **Nisten:** that. I literally just, if you scroll one back, I just tested it right now. I dumped him a question on sauna 3. 5 and did this new deep seek from their site. And they both got the exact same answer, 14. 45. And I also did all the calculations, Mistral large GPT 40, LLAMA 405B below that, and the older deep seek, which I'd put a freaking, GGUF4 which is pretty popular.

[01:22:26] **Nisten:** they all like Mistral large was off by 10 points. The other ones were all like not that accurate. This got, this and Sonnet 3. 5 just got the exact same answer and they're super complicated question like multi step and air pressures and all that stuff. They got it both perfectly. The only two models 

[01:22:45] **Junyang Lin:** that got it all perfectly.

[01:22:46] **Alex Volkov:** and we've talked about DeepSec before, like the team is super cracked. The team is they're doing some stuff. I see Yam Pelican in the audience. For some reason, Yam decided on the most celebratory ThursdAI of the last two years not to join us. But okay, we talked about DeepSeek being like an extremely crack team doing like some significant work on their like chat models as well.

[01:23:05] **Alex Volkov:** Because DeepSeek chat is also like a great model. But Coder looks now based on the two evals that I saw super quick. I have one, the big code bench, evaluation for code. DeepSeaCoder v2 is now 3. 5 sonnet [01:23:20] level. And, the code editing leaderboard from AderChat. Ader is, getting. is putting DeepSeq Coder at like second place after 3.

[01:23:28] **Alex Volkov:** 5 Sonnet, like very close. like at 97%, correct format versus 1999 for Cloud 3. 5 Sonnet. And this is for code editing specifically, not for just auto completion or creation, which is a different task a little bit. And, the fill in the middle thing that they posted is very interesting as well.

[01:23:46] **Alex Volkov:** But again, we didn't have time to test this out because this came out today. Nisten, last thing about DeepSeq. Or other folks as well. Junyang, are you familiar with DeepSec as well? Please feel free to chime in also. In

[01:23:58] **Junyang Lin:** they have been very great at building the code specific model, just like DeepSeqCoder and DeepSeqCoder v2 should be the state of the art of the code specific model. And they have done very hard tasks really well. So I actually expect something better in coding agent to use the state of the art open source model to build something better.

[01:24:24] **Alex Volkov:** OpenDev, you mean? The project that you guys are running?

[01:24:29] **Junyang Lin:** Yeah,yeah, OpenDev should use different models. I think they can try with, DeepSea Coder V2. Yeah.

[01:24:36] **Alex Volkov:** No, that's awesome. if you want to give us an update on that this week or next week, feel free to. I would love to hear like how that's going because, I'm excited to see how these like huge jumps in coding abilities affect downstream tasks or frameworks Devin, maybe CruAI.

[01:24:51] **Alex Volkov:** Maybe we'll bring, João from CruAI again and see how these updated like intelligences affect frameworks as well. Speaking of frameworks. I want to say hi to a friend of mine, and a friend of the pod, Matt Schumer, who does a bunch of them and releases a bunch of them and goes often, goes very viral with some of them.

[01:25:08] **Alex Volkov:** Matt, welcome to the stage, man. How are you? 


## [01:25:10] HyperWrite and LLAMA Models

[01:25:10] **Alex Volkov:** how's this week full of Christmas, presents from all the AI labs for you?

[01:25:16] **Matt Shumer:** Hey, yeah, thanks for having me. First of all, can you hear me okay?

[01:25:19] **Alex Volkov:** you're coming to loud and clear.

[01:25:21] **Matt Shumer:** All right, awesome. yeah, this week's been fun. I've mostly been focused on the LLAMA models. I find that if I try to handle too many of them at once, I don't do anything really well. just from our experience, the LLAMA models were the place to focus.so that's what I've been doing.

[01:25:35] **Matt Shumer:** I've been fine tuning 70B, which has been, really interesting. The first thing I noticed, I don't know if Nisten, if you're here, I'm sure you've probably seen the same thing if you are, is that the loss is just way lower from the start on 70B versus, LLAMA370B. basically, short way of saying, and it's not a perfect metric, but it learns much faster.

[01:25:57] **Matt Shumer:** so it's pretty crazy to see,what you can do with it. whereas, for example, with LLAMA3, I might have needed a 300, 000 example data sets to teach it something. like really tricky. I'm actually doing the same sort of thing with 10, 20, 000 examples now on 3. 1, which is unbelievable. plus it allows you to just use just the highest quality examples.

[01:26:15] **Matt Shumer:** So it leads to a far better model anyway, less costs. So it's. It's been a fun week. It's not over yet. still a lot to do.

[01:26:21] **Alex Volkov:** It just started. have you, taken a look at the smaller one, the 8 billion problem with the one?

[01:26:27] **Matt Shumer:** Yeah, I have. it's really good. It is too small for my purposes. I think it's getting close to that threshold, but, at least for the Hyperwrite platform, we want to give the best experience possible. and it's like the cost performance trade off for AP versus 70 B.

[01:26:43] **Matt Shumer:** It's not so huge of a cost increase, but the performance you get for the user is far better. even if the benchmarks don't show it right? it's the little things that make all the difference. obviously the 70 B to the 4 0 5 B is just,it's nearly impossible to host a five, two to that without breaking the bank.

[01:26:57] **Matt Shumer:** So we're holding off on that for now. but yeah, the AP is a little bit too small for our needs.

[01:27:02] **Alex Volkov:** And just to clarify, when you say your needs, you're not talking about the plethora of side projects, like the prompt engineer or cloud researcher, like all of the bunch of stuff that you release and often like many people use. You're talking about like the actual product that you run, HyperWrite, correct?

[01:27:18] **Matt Shumer:** That is correct, yeah. So I'm talking about sort of two things. One is the main HyperWrite, writing platform, that's been around for a few years, and then also the newer agent, style technologies that we release, like the agent that can operate your computer for you, to complete tasks. That being said, I actually just got off a call with one of our inference partners, and we actually are collaborating to do a new notebook, slightly similar to some of the ones I've released recently, using, LLAMA to optimize deployments.

[01:27:43] **Matt Shumer:** So you can imagine having 405B level quality or close to it, not exactly, but close to it with an 8B,for production for more specific use cases. So that will be coming soon. So that, when I say I'm doing it mostly for the platform, that is true, but there will be some, fun open source nuggets that we'll put out pretty soon.

[01:27:59] **Alex Volkov:** All right. So folks stay tuned for that. Thank you, Matt. and, last thing, I don't know if you were here, last thing I wanted to hear from you, maybe to ask, I asked some of this question. What about the four or 5 billion parameter? What's your take on like product, putting this on production, using this on production?

[01:28:13] **Alex Volkov:** I have the sense, and I heard this from other folks that like, it's too big for production, it's great for like synthetic data creation, maybe LLM is a judge. What's your sense of this model as a production model? Yeah,

[01:28:29] **Matt Shumer:** it. It's huge. actually, one of the tasks I'm thinking about today is, there's a specific use case that I want to have more high quality data for to train, 70B on. and prompting, it's a very difficult task, and prompting 405B gets me kind of part of the way there, but not enough.

[01:28:45] **Matt Shumer:** we have to fine tune for it, but, fine tuning that on the 8H100 is just not going to happen. You can cut out layers, but it's just a very difficult thing, so that's on the fine tuning side, right? You need a lot of GPUs to teach anything, and you can't prompt it, to learn.and then on the inference side,it's just as hard, right?

[01:29:00] **Matt Shumer:** You can do, an FP8, right? Or an NZ8, or whatever. Yeah, you can do that and host it on any TPUs, but you're not going to do better than that, at least currently, from what I'm hearing and from what I'm trying. So it is very difficult, but seeing like Fireworks get their pricing down to, I think it's like 3 per million tokens or possibly even lower now, it's encouraging that, at least for the things you can prompt it for.

[01:29:20] **Matt Shumer:** It generates synthetic data against, it's actually a very feasible, system, and you can get a lot of data for very cheap, and the license allows you to do that, so it's a fantastic thing that the community hasn't had thus far, so obviously it's not perfect in every way, nothing is, but it's a fantastic addition to sort of everything that we have access to.

[01:29:37] **Alex Volkov:** yeah, that's my sense as well. And that seems to be after a day and a half that we had to play with these models and like wrap around, wrap our heads around this, which probably, you know, next week we'll still be, I actually don't know, but next week, or maybe even later today we'll get some news that will make us forget about this whole thing.

[01:29:54] **Alex Volkov:** Hopefully not releases such as this size. Hopefully we'll, Give us at least a week of updates to talk about, but, this is the sense that like this model is like incredible gift to the community. It's also like way too big for production purposes, but for stuff like synthetic generation for distillation, for example, like for offline tasks and different other things, it's amazing.

[01:30:17] **Alex Volkov:** I would be very impressed if if anybody from the fine tuning community will release like a fine tune. remains to be seen. We've seen crazier things happen. we've seen crazier things happen. yeah, go ahead.

[01:30:27] **Matt Shumer:** I am curious though, I wonder if anybody can go ahead and like you've seen what some people have done with the older LLAMA 70Bs and merge them into themselves to build, LLAMA 120Bs. I am curious, it's already too big to serve, so why not try? Who makes the first, LLAMA 700B?

[01:30:41] **Matt Shumer:** Or LLAMA 800B? I'm very curious to see what happens there.

[01:30:44] **Alex Volkov:** Yeah. And then nobody can run this on any hardware beside, maybe some folks.

[01:30:49] **Nisten:** it's coming. There's like a 4. 19b, which unfortunately wouldn't add up to one more b from that, but it seems to make a 

[01:30:59] **Matt Shumer:** difference. Shane.


## [01:31:01] Closing Thoughts and Community Engagement

[01:31:01] **Alex Volkov:** I think that's mostly what we want to cover today, folks. An hour and a half into this, I think because we don't have, a straight up interview, this is most of the important news from this week. I will just, mention super briefly, two things, and I'll add this to the show notes as well.

[01:31:16] **Alex Volkov:** I would just want to shout out because, I think it's very important. The folks from, let me just find this. I think Grok and Daily and Cartesia, we've talked with the folks from Cartesia. If you remember, they have the super quick, API for chatting. They all collaborated, or I guess like they all learned together and they came up with a new, let me go find the super quick, a new standard, [01:31:40] open started for voice and video, real time voice and video.

[01:31:42] **Alex Volkov:** and yeah, I'm going to post this here. Here, yeah, there we go. they collaborated with Grok, and shoutout to the folks at, Realtime, Daily, trydaily. com. I've played around with their demo. Actually, let me see if I can. You guys wanna, let me try and see if I can do the demo. And, Super quick. And meanwhile, I'm getting a ping from my friend Junaid and he's right.

[01:32:10] **Alex Volkov:** Absolutely as you guys know, those of you who are listening from the Denver slash Boulder, area, Junaid and I, Junaid has been on this podcast for a long time,a listener and also a participant that we run the AI thinkers in Denver, Boulder. There's a bunch of AI thinkers. If you want to.

[01:32:26] **Alex Volkov:** Do what we're doing here, but with people in front of you, AI thinker is like a great place. There's like a bunch of affiliate, running self organizing groups around the world. We run the Denver Boulder one. There's one in Seattle, the huge one. there's one in San Francisco, obviously there's one in Chicago, there's one everywhere.

[01:32:42] **Alex Volkov:** And if you don't have one where you are, just open one. we're running a hackathon and it's coming up, it's coming up in a few weeks or I guess. Next week, it's yeah. no, it's this weekend. What am I talking about? And so again, our hackathon is this weekend. So definitely you guys should, if you're into this and you're in Denver, Boulder area, and you want to hack with us and we have a bunch of like 12 labs is there, a bunch of other folks as well.

[01:33:03] **Alex Volkov:** if you do that, we'll send me a link to, to post. I'll definitely boost this as well. if you're listening to this, you're from this area, you want to hack with us. It's going to be awesome. yeah. Absolutely awesome. All right. So here's the demo for the daily voice chat demo. if you guys remember Moshi that I've talked about, I also did a demo before.

[01:33:20] **Alex Volkov:** Moshi was a specific model that was like end to end model. This is not the end to end model. This is Grok and Lama 3. 1, which they already used. And this daily company and this RTVI protocol, and they claim to have a 500 millisecond voice to voice demo. So let me see if I can, click this guy and then let me see if this will come through.

[01:33:43] **Alex Volkov:** Hopefully this will come through. I'm going to use the 70B and start.

[01:33:49] 

[01:34:50] **Alex Volkov:** demo. rtvi. ai. You can try this yourself. the latency here was around 500 milliseconds. Which was dope. I hope you could hear this, right? I was asking and on the fly I was getting a reaction. This wasn't like real time, this wasn't one model, but this was like an end to end demo with Grok.

[01:35:06] **Alex Volkov:** And this used Lama 3. 1, 7TB or 8B and different voices as well. It is definitely super, super cool. I add this to the top notes. And the protocol that they released allows you to run like these demos like this and build demos like this yourself. so shout out to the folks who built this. Maybe we'll bring the guys behind RTVI.

[01:35:25] **Alex Volkov:** to talk about this in ThursdAI and next ThursdAI. Besides this, folks, I think that this is all that we want to cover on ThursdAI. We're not going to do a TLDR because pretty much this is all that we've, we wanted to cover. I will say that, there's not a better week that I wanted to come back to than this one.

[01:35:43] **Alex Volkov:** There's not a better week. this has been probably The craziest week for open source AI or open weights AI since we started doing this 100%. Since we started doing this, we were like, okay, when is open weights on open source is going to beat whatever foundational frontier models out there. honestly, many of us didn't actually believe that this is going to happen because some people believe that the gap is widening and holy shit, like we, we actually got to see this.

[01:36:13] **Alex Volkov:** We actually got a model that beats whatever we have in, in, in, in production and we can run this. Yes, it's hard. Yes, it's heavy. Yes, this is a monster, like Matt said. Yes, maybe it's not for production, but we can run this and we can store this on a thumb drive and keep it for emergency purposes for later.

[01:36:30] **Alex Volkov:** there's a bunch of stuff we can do. It's incredible. So shout out to everybody from Meta who hopefully, at least some of you are listening to this and huge appreciation to all of you for working on this. Shout out to Zach and everybody at Meta for releasing this incredible, thing. incredible.

[01:36:44] **Alex Volkov:** Thanks for everybody on the stage who joins me from week to week here. LDJ, Nisten, Wolfram, Jun Yang was here before. Matt, thanks for coming. A bunch of other friends.Yam as well. Thank you. A huge thank you for everybody who listens to this week after week. This has been definitely one of the biggest shows that we had all of you in the audience.

[01:37:03] **Alex Volkov:** and we're obviously going to be here next week as well. Bye. And I'm really hoping to relax a little bit next week because, I don't know if I can take more of weeks like this, because we cannot keep having state of the art day after day. It just doesn't make sense. It doesn't make sense. but if we will, we'll be here to tell you all about this.

[01:37:21] **Alex Volkov:** With that, I want to thank all of you for coming and we'll see you here next week. Cheers everyone.

[01:37:31] **Alex Volkov:** Oh, and of course, subscribe to the podcast and give us five stars on Apple. Thank you.

