[00:00:00] 

[00:00:00] **ChatGPT:** Got it. Welcome to Thursday AI, the podcast where comrades gather to discuss artificial intelligence and its impact on our world.

[00:00:12] **ChatGPT:** Prepare for deep reflection and sober analysis as we explore the relentless march of technological progress.

[00:00:22] 

[00:00:59] **Alex Volkov:** Here's everything that we've covered, that we've talked about on ThursdAI for August 1st, we had a bunch of breaking news. We also had a bunch of guests. We. We started the show by talking about open source and LLMs. We announced some breaking news from Google open sourcing Gemma 2, 2. 6 billion parameters.

[00:01:25] **Alex Volkov:** Gemma 2, was released with with a very interesting ELO arena score or,it looks like it beats something like Mixtral. and then, it was doubtful and we talked about why would that be the case where a 2. 6 billion parameter model beat like a significantly larger model on human preference.

[00:01:42] **Alex Volkov:** they also released Shield Gemma and Gemma Scope, Gemma Scope is, a very interesting,a bunch of neuron activations, which you can also see how Gemma 2 thinks on Neuronpedia. 

[00:01:51] **Alex Volkov:** And then, we definitely, the biggest part of our conversation this week was a conversation with, Joseph and, Piotr Skalski, our vision experts from Roboflow about Meta releasing the hugest thing this week, Segment Anything 2 model, which is, a second model following the previous segment, anything, and this one is a super quick one shot and video capability model.

[00:02:15] **Alex Volkov:** it was incredible to have such like vision experts on the show explaining to us how this, something like this model is affecting the whole industry. 

[00:02:24] **Joseph Nelson:** being able to,individually see and segment proteins to do,quick counting is a meaningful acceleration to seeing, how given cells respond to treatments,which, we've seen folks use to accelerate everything from,cancer research to,longevity

[00:02:37] **Alex Volkov:** It was released with Apache 2 license. it's able to, with one click, detect, Objects across scenes,

[00:02:43] **Piotr Skalski:** So instead of going through the tedious process of drawing all the masks, you just click on an object and it immediately knows that you probably are interested in the whole person. And then what happens is that segmentation propagates through the whole video. So, you only annotate, one or two frames, and then get all the other frames for free.

[00:03:04] **Piotr Skalski:** And it doesn't matter if the object goes out of the frame and comes back, it still knows that it's the same 

[00:03:10] **Alex Volkov:** there is several sizes of this model.Very interesting conversation with the folks, about the vision stuff, definitely worth listening to as well. 

[00:03:18] **Alex Volkov:** And then after that, we've talked with, Lucas Atkins and Fernando from ArceeAI about DistillKit. And we also dove in into what distillation is.

[00:03:28] **Alex Volkov:** DistillKit is a new open source tool creating and distilling distillation. smarter, more efficient language models by having a teacher model, transfer its knowledge to a smaller student model. 

[00:03:38] **Lucas Atkins:** the idea behind DistilledKit was let's add a kind of centralized repository where the open source community can go to get code And, scripts and routines for doing some of this kind of, we have two approaches right now. There's logit based distillation, and then we have another one that's, hidden states 

[00:03:57] **Lucas Atkins:** TLDR, we teach a smaller model to think like a bigger model

[00:04:01] **Alex Volkov:** We then had a very entertaining,conversation because OpenAI started releasing for some alpha users, the GPT 4. 0 advanced voice mode. And we had a conversation with Cristiano Giardina,who actually joined from his PC so that his mobile phone would be free, and we actually had a live conversation with the advanced voice mode of GPT 4. 0, 4. 0, and it was really funny and very entertaining, and I really encourage you to listen to that, because, live demos don't often work.

[00:04:30] **Alex Volkov:** This one worked very well. 

[00:04:31] **Alex Volkov:** Can you interrupt it and ask, for ThursdAI, not Thursday AI?

[00:04:36] **Nisten:** Yeah, and do it, like, in a depressed Soviet accent while being also, killed at a street party. 

[00:04:42] **Christiano G:** Okay, I'll try. Hey, ChadjPT, the name of the podcast is actually ThursdAI, and I want you to do the intro, but in a really depressed, way and with a Soviet accent. 

[00:04:57] **ChatGPT:** Got it. Welcome to Thursday AI, the podcast where comrades gather to discuss artificial intelligence and its impact on our world.

[00:05:10] **ChatGPT:** Prepare for deep reflection and sober analysis as we explore the relentless march of technological progress. 

[00:05:19] **Alex Volkov:** Yes

[00:05:21] **Alex Volkov:** In other news in the big companies, LLMs and APIs, OpenAI also released the, SearchGPT which is OpenAI's attempt at a search engine, very similar to something like Perplexity. 

[00:05:33] **Alex Volkov:** It's a waitlist. I got into this waitlist. And so if you're a subscriber, you already got the episode of ThursdAI where I compared the two. And if you're not, and you're listening to this, please go to the newsletter and check out my comparison.

[00:05:45] **Alex Volkov:** SearchGPT is. Quite fast. And I really liked it. And we also talked about this as well. 

[00:05:50] **Alex Volkov:** And another thing that was released,from big companies is Apple intelligence. Also on Monday, Apple released a beta of iOS 18. 1. And those of us with, iPhone 15s or iPads with the M chip or Macs with the M chip as well could download the developer betas that include the Apple intelligence.

[00:06:09] **Alex Volkov:** This will download the Apple foundational model or AFM and you could start using the Apple intelligence features. Not all of the features right now, Siri is not yet connected. They don't still use The intents, but we definitely had a conversation about how a smaller model that may be not as performant, maybe, is behind some of the latest advances in the world of ai.

[00:06:31] **Alex Volkov:** Still is going to be super useful because intent, like, open and close files or summarize emails, those things will actually, be very helpful for people on their device. In addition, Apple also released a technical paper full of their details about how they train those models, and details like GQA and activations and rope and tokenization and Loras.

[00:06:51] **Alex Volkov:** And so we covered this a little bit as well. 

[00:06:53] **Alex Volkov:** In this week's buzz category, where we talk about everything related to Weights Biases, I mentioned that we have a new course about Weave, our LLM observability framework from Weights Biases. And this course was stitched together by my colleague Agata.

[00:07:09] **Alex Volkov:** And,apparently I'm the instructor, which is super cool. and it was stitched together from a bunch of videos here and there that I did. So you definitely want to check this out and see how it works. how cool this looks. And also I announced that in our new office in Weights Biases,in San Francisco. we have a start of a new, initiative called AI Salons. And the first one is going to be. In two weeks, and it's going to feature Shreya Shankar, incredible researcher in the area of evaluation of LLMs. So if you're building anything in production with LLMs, you definitely want to check this out if you're in the Bay Area.

[00:07:39] **Alex Volkov:** and space is limited, so definitely worth checking this out. It starts at 5pm on August 15th, and I will add the link in the show notes as well. 

[00:07:48] **Alex Volkov:** At the end of the show, we got breaking news that,

[00:07:51] **Alex Volkov:** Gemini 1. 5 Pro Experimental was released and it's now taking number one spot on LMSys Arena and it's still 2 million tokens in Contacts window but it's taking number one and number two spots across multiple LMSys.

[00:08:09] **Alex Volkov:** multiple categories. So it's now for the first time, the number one spot on LMSys Arena by a significant margin as well. So it gets the first time [00:08:20] the arena score that it gets is 1300. ELO score, and the closest one is GPT for over 1, 286. it also number one in math, number one in instruction following, number three in coding, and also number two in hard prompts as well.

[00:08:34] **Alex Volkov:** So Gemini 1. 5 Pro So today it literally released as we were talking, so that's breaking news. Additional breaking news is that GitHub released something called Models, which looks like a hug and face competitor, which will allow you to try and test like different open source models. it's a waitlist thing, but now they have Meta, LAMMF stuff, and then they also have OpenAI stuff in there, via Azure OpenAI, and then they have the Microsoft PHI models as well.

[00:08:59] **Alex Volkov:** 

[00:08:59] **Alex Volkov:** And then we also talked about AI art and diffusion stuff because, also today was crazy. Black Forest Labs was announced by ex Stability AI folks. In fact, 14 ex Stability AI folks decided to, probably left Stability a while ago and opened a new lab called Black Forest Labs.

[00:09:14] **Alex Volkov:** Not only did they announce, that this lab exists now, they also,released it with a,a model called Flux 0. 1, which is a new state of the art diffusion model that,released in three sizes, Flux 0. 1 Pro, Flux 0. 1 Dev, and Flux 0. 1 Schnell,both Flux 0. 1 Dev is now,a non commercial licensed open source diffusion model that beats every other one.

[00:09:40] **Alex Volkov:** In ELO score. So we now have a state of the art diffusion model in the open source that beats the likes of Ideogram and Midjourney and,Midjourney version 6. It's worth shouting out that Midjourney version 6. 1 was released also yesterday. there is not a direct comparison between the two. beats DALI as well.

[00:09:58] **Alex Volkov:** And that's headed by Robin Rombach and a bunch of Xtability folks. And the interesting thing there is, in addition to this Flux model, on their website they also have Coming Soon, and that Coming Soon tab says that they're working on a state of the art image to video model, which we've talked about Runway, for example, and, Kling and, All of these models, these folks, these incredible folks that were, that are now funded with 31 million from Andreessen Horowitz are working on a video, text to video models, that they're also probably going to open source, which is super cool.

[00:10:31] **Alex Volkov:** we also discovered the hardware announcements for an always on listening device from friend. com from Avi Schiffman, and a release of Fast. html from Jeremy Howard, and also the applied LLM course from Hamel Hussain. All friends of the pod, to some extent or another.


## [00:10:48] Introduction to the Hosts and Their Work

[00:10:48] 

[00:10:48] 


## [00:10:48] Segment Anything 2: Overview and Capabilities

[00:10:48] **Alex Volkov:** So I'm very excited to start the show already. And as always, we're going to start with open source. So let's get it started.

[00:11:12] **Alex Volkov:** Let's get it started. And I will just start with a small potatoes thing, before kind of the main course, not to leave our guests waiting too much, but, yesterday Google Open Source Gemma 2 2. 6b. Google Open Source Gemma 2, a while ago, there's a 27 billion parameter, I believe. And, yesterday they released the 2.

[00:11:30] **Alex Volkov:** 6 billion parameter. And a very interesting announcement. They, showed that not only did they release it. This model is geared towards on device. And it runs super fast. And I think already our friend Zenova, that's not with us in the audience, but our friend Zenova already runs it fully in WebGPU, fully on device in Hug and Face.

[00:11:49] **Alex Volkov:** You already can run this completely on device. 2. 2 parameter like quantizes into a very small model. when Google announced this, they apparently were running this in, in the LMSys arena. And they now show that this. 2 billion parameter model has an ELO score of 1126, which beats Mixtral of 8 times 7 billion parameter and beats GPT 3.

[00:12:15] **Alex Volkov:** 5, which is apparently for all intents and purposes now dead, right? GPT 3. 5 is dead. and beats Lama2, 70 billion parameter and beats GMO1. and everybody was like, huh, there's no way. There's no way to build,it would make sense a year from now, maybe two years from now. There's no way to this, at this day, that a 2 billion parameter model is better and more intelligent than Mixtral 8 times 7 billion parameter, right?

[00:12:43] **Alex Volkov:** There's no way. and, And yeah, so this metric is controversial, and I wanted to see, Nisten, LDJ, if you have anything to share about this topic of why you think that is, because, it's weird. It's weird. And it's also weird that this is the only metric they released.

[00:12:58] **Alex Volkov:** Only this, LMSys Arena score, and none of the regular MMLU, Human Eval, and different metrics.

[00:13:06] **ldj:** Yeah, I think my best theory here is I think there's at least two or three variables at play of, In LMSys, people are much more likely to do single turn, and within LMSys, people will usually be biased more towards rating models with a more recent knowledge cutoff as higher, because naturally, most of the models will, the newer the model is, obviously, the newer the knowledge cutoff will usually be, and so that's a little bit of a bias.

[00:13:32] **ldj:** And then you also just have novelty, sometimes if something just has like more of a different style and people are tired of the models usually talking in the same way to each other then a newer type of style that people are introduced to might be given a better rating but then after you give it a few weeks or a few months then you might actually notice that ELO score go down because now people feel like that's like in the same old style as 

[00:13:59] **ldj:** like how everything else feels old as well

[00:14:02] **Alex Volkov:** Yep, and also we had, we had a friend of the pod also from Allen Institute talk about,style, but also talk about how this could be gamed, essentially. And many people are already, giving up on LMSys Arena because of this, because, this doesn't necessarily represent intelligence to an extent.

[00:14:18] **Alex Volkov:** But still, it's a very,last generation or like newest generation on device model. So it's super cool. Additionally to this, they released Shield Jemma and JemmaScope. Shield Jemma is their open suite of auto encoders for Jemma 2, which basically protect from injection and different things like this.

[00:14:36] **Alex Volkov:** very similar to Llamaguard and looks like it's beating Llamaguard. Llamaguard was released together with Llama. And, and Jemascope is very interesting as well. We'll get to Jemascope, I think, a little bit later, but Jemascope, you can see on something called Neuronpedia. And basically, if you guys remember GoldenGateCloud, they released a few of the like neuron activations, I think in, for Jemascope.

[00:14:58] **Alex Volkov:** So you can see how Jemma thinks, which is like super cool as well. So if that's of interest to you, that's definitely worth looking into. and I think now. 


## [00:15:08] Deep Dive: Applications and Technical Details of SAM2

[00:15:08] **Alex Volkov:** After we've talked about like the smaller open source, like importance thing, let's talk about Segment Anything 2. So I believe on Monday, 

[00:15:15] **Alex Volkov:** Meta, surprised us and announced that they are releasing Segment Anything 2. This was, yeah, this was on Monday. Segment Anything 2 is their, real time. Promptable object segmentation for images and video model. segment anything before this was like a very important model before.

[00:15:35] **Alex Volkov:** And they released it also with Apache 2 license. And who better to tell us all about this than our friends from Roboflow, 


## [00:15:42] Special Guests Introduction: Piotr Skalski and Joseph Nelson

[00:15:42] **Alex Volkov:** So long time, friend of the pod and a vision expert, Skalski, Piotr Skalski, from Roboflow. And this time, first time I think on the show, Joseph Nelson.

[00:15:51] **Alex Volkov:** co founder of CEO of Roboflow. So Piero, why don't you, unmute yourself and maybe introduce yourself to the folks. And then, Joseph, you as well. And then we'll talk about, Sam after the introduction,

[00:16:00] **Alex Volkov:** my name is Peter, I work at Roboflow. As Alex said, I'm doing computer vision over there. Roboflow. com Part computer vision engineer, part growth engineer, which gives me the benefit of playing the latest computer vision models as soon as they come. So yeah, I didn't sleep too much this week because of segment anything, but yeah, I done a lot of cool experiments, so can't wait to tell you a little bit more about that.

[00:16:29] **Alex Volkov:** We would love to hear all about this. you're also a maintainer of a very popular library that I always. Always want to bring in and mention, because people should know about this. SuperVision, [00:16:40] correct? On

[00:16:41] **Piotr Skalski:** Supervision. Yeah, that's right. That's right. 

[00:16:43] **NA:** Alrighty. And, Joseph, welcome to the show. This is your first time here, and we've met just, what, a month ago, I think, first time? welcome to the show.

[00:16:50] **Joseph Nelson:** great to be here. I've been looking forward to the discussion today. Thanks for having me, Alex.

[00:16:53] **Alex Volkov:** Yeah. why don't you give us, maybe a brief introduction of who you are and, what Roboflow is?

[00:16:58] **Joseph Nelson:** I'm Joseph. I work on Rob Flow, as Alex mentioned with pi. at Robo Flow we say that our mission is to make the world programmable. And what we mean by that is giving developers tools they need to understand the visual world, whether that's things in the real world, images, video. And so we provide open source tools like supervision, inference, and some other things that Chef Piatta is cooking up.

[00:17:22] **Joseph Nelson:** hosted platform for curating high quality data sets. That's like everything from automating labeling with models like Cegna Anything to training and fine tuning both task specific models and motor models. And then deploying those models to run anywhere. a little over half a million developers build with Roboflow.

[00:17:41] **Joseph Nelson:** we also maintain something called Roboflow Universe, which is the largest collection of open source computer vision projects on the web. About 650, 000 projects from folks creating and sharing, capabilities. big believers in open source. And a lot of the work, that Meta and others do to forward that goal, I'm looking forward to joining the conversation today to hear from the community how they're thinking about segment anything and share some reflections that we've seen both with SAM1 and a lot of the experiments and impressive results we've seen with SAM2.

[00:18:10] **Joseph Nelson:** So thanks so much for having me today.

[00:18:12] **Alex Volkov:** Absolutely. Thank you guys for joining

[00:18:13] **Alex Volkov:** And I guess, Piotr, maybe we'll start with you because We've talked about segment anything before, but definitely it's something, a model that you've played with before.

[00:18:22] **Alex Volkov:** could you maybe tell us, where you were when this announcement happened? I think it's this size of gravity.

[00:18:29] **Piotr Skalski:** that is easy question because I live in Europe and those announcements happened in Pacific, time zone. So I was sleeping, man, but the moment I woke up, the moment I woke up, I was trying to catch up with everybody else. 

[00:18:43] **Piotr Skalski:** yeah,

[00:18:43] **Piotr Skalski:** I feel like you, you caught up super quick. so can you tell us about what is. What's the, like, why is this so major? Why does it feel so major? what's going on in this announcement? what is this model? So if you don't mind, maybe I will,take a step back and, talk pretty much what is Segment Anything, even the first version, because, that kind of like kind of explains, how the model changed and what was added. So generally speaking last year, somewhere in the first quarter, I believe in March, last year Facebook released Segment Anything.

[00:19:17] **Piotr Skalski:** which was, a model that immediately, got attention of a lot of people. we at drop of Flow and probably Joseph will tell you more about it. We integrated it like in the first week after we release into our product. So the model was unique because it understood segmentation on the whole new level.

[00:19:38] **Piotr Skalski:** So typically segmentation models. understand only specific classes, so you train the model to understand the segmentation of a people. And by the way, segmentation is like the pixel perfect detection of an object on a frame. detection is the bounding box, segmentation is like pixel perfect representation of that object.

[00:19:57] **Piotr Skalski:** previously, models, were trained on specific classes, so it could segment people, dogs, I don't know, oranges, bananas, yeah? But the understanding of an object was, very specific to the class. And SegmentAnythingModel took that to the next level, because it understood what an object is, and was capable of segmenting anything that you saw on the frame.

[00:20:21] **Piotr Skalski:** Hence the name Segment Anything. And, the problem is, the slight problem is that it works only on images, and it doesn't tell you what it is. So it's capable of segmenting objects, but cannot say is it a person or is it a dog. It still is super useful.so now, Segment Anything 2 comes out. Of course, it has all the previous capabilities of Segment Anything, so it still can work.

[00:20:45] **Piotr Skalski:** do awesome things with images, faster, smaller, all the typical, updates coming with new releases of the models. But the segment anything tool is awesome because it also can segment objects on the video. So now what you can do is you can have a video and only pick one frame of the video, annotate objects, that are interesting to you and you do that with like single point, which is awesome.

[00:21:12] **Piotr Skalski:** So instead of going through the tedious process of drawing all the masks, you just click on an object and it immediately knows that you probably are interested in the whole person. And then what happens is that segmentation propagates through the whole video. you only annotate, let's say, one or two frames, and then get all the other frames for free.

[00:21:34] **Piotr Skalski:** And it doesn't matter if the object goes out of the frame and comes back, it still knows that it's the same object.

[00:21:41] **Alex Volkov:** this to me is just incredible. And first of all, thank you for the breakdown historically, but this to me was just incredible. They released like a playground as well for folks who probably never installed this somewhere else. And I played with this and I really encourage folks to also play with this.

[00:21:55] **Alex Volkov:** the playground allows you to upload any video of yours, any, they give us a few videos of theirs, any video of yours. 


## [00:22:01] Combining SAM2 with Other Models

[00:22:01] **Alex Volkov:** And you literally just click around, and the second you click on any object, they will like just trace around that object almost perfectly, and then When, once you click track, almost real time, that, the video will start playing, and that object will be like, colored, and then you can choose to blur this object, or to remove this completely and have a green, or to remove the background and just keep this object itself, and this is like super cool, and this only, this happened before with images, and now it happens with video, and I guess my next question would be for Joseph, besides being super cool, could you tell us, what is something like this used for?

[00:22:38] **Joseph Nelson:** you guys work with companies, I'm assuming. Could you tell us a bit about, like, why, like, why this is useful and what purposes this could serve? As Peter mentioned, Segment Anything does an incredible job at creating pixel perfect outlines of everything inside visual scenes. And with SAM2, it does it across videos super well, too. And if you think about, the way that people see, we're able to very quickly figure out, if you're looking out into an office, where a chair is, where a person is, where a monitor is.

[00:23:09] **Joseph Nelson:** And people, very quickly, of course, think about the relationship between those objects, where one object starts and stops, the relation of one thing to another, if it's on the left or the right, if it's bigger, if it's smaller. And that capability is still being developed for a lot of AI Models and capabilities.

[00:23:27] **Joseph Nelson:** And so having very rich ability to understand what a thing is, where that thing is, how big that thing is, allows models to understand spaces and reason about them. So for example, some of the example, like demos that.you mentioned, Facebook did a fantastic job of releasing a playground, and in that playground, they made close attention to showing what it looks like for, visual special effects, video special effects examples, and those video effects, it's if you want to do background removal, or, highlight an object, or spotlight an object, I don't know if anyone here watches, NHL hockey.

[00:24:08] **Joseph Nelson:** There was, once upon a time, the NHL realized that viewership was really low. And so tracking the puck, especially for first time viewers, can be pretty tricky. so they actually ran this experiment for a bit where they, it's called Glow Puck, and they canceled it because everyone was like, this is awful,this looks terrible.

[00:24:24] **Joseph Nelson:** why did you do this, NHL? But the experiment was, highlight where the puck is for the viewer, and then when the puck is moving really fast, almost give it like a tail, almost like looking like a comet zooming through the sky. And the technology required, they did this in like the early 2000s, the technology required to do something like that assuredly was like a team of PhDs trying to figure out doing real time, visibility of where that puck is.

[00:24:49] **Joseph Nelson:** And now something like SAM2, it's a single press of a mouse and you could, for example, outline the puck immediately. But even beyond like visual effects, you could think about basically [00:25:00] other sports applications where maybe, you know, famously. In tennis, you want to know if a ball is like in or out for like automatic line calling.

[00:25:07] **Joseph Nelson:** PIAT also maintains a repository of like sports use cases where you can see, where the ball is, how many players, where the ref is, the position of things. Beyond sports and broadcasting and live video, visions used for we kind of say, like, everything under a microscope to everything through a telescope.

[00:25:24] **Joseph Nelson:** And underneath the microscope, you've got, maybe you're looking at individual, amoebas, or counting of cells, or looking at cell populations. And being able to, individually see and segment proteins to do, quick counting is a meaningful acceleration to seeing, like, how given cells respond to treatments, which, we've seen folks use to accelerate everything from, cancer research to, longevity.

[00:25:45] **Joseph Nelson:** Or, out in like the real world of regularly sized things, you can think of like retailers wanting to know what's like in stock or out of stock, maybe folks that are producing items, knowing how many things they're producing. Or if you're like looking out beyond a telescope, we've even seen folks do things like classification of galaxies and finding like where one planet starts and stops.

[00:26:03] **Joseph Nelson:** So in effect, like what Meta's releasing is, a stepwise increase in capability of just visual understanding and visual reasoning. of where one thing is, another thing is, what's allowed for these downstream tasks of tracking, counting, speed estimation, and more. it's basically that much faster and that much quicker.

[00:26:25] **Joseph Nelson:** I expect it'll be incorporated into multimodal models, but that's maybe a separate conversation.

[00:26:29] **Alex Volkov:** interesting. Because multi models, they can basically already see, right? You can upload a picture to ChatGPT right now, most of the models, the Cloud, Gemini, they all can see and understand like what's in the picture. So I guess my question would be like, what's the difference between this and something like an LLM that understands with vision headers?

[00:26:50] **Joseph Nelson:** models do a good job of understanding kind of general scenes. But if you ever have wanted to get very precise understanding of, counts of things, or where things are, or size estimation, you'll see that models kind of struggle. if you think about, like, when LLMs first came out and they couldn't do simple mathematic operations, You would have a similar effect right now with vision models and multimodal models.

[00:27:15] **Joseph Nelson:** And, this refers to the capability for doing grounding tasks. Grounding referring to cutting out where an object is and creating individual segments. And so you can almost think about SAM as like the most precise model available for figuring out what things, where things start and stop inside images.

[00:27:35] **Joseph Nelson:** Multimodal models right now fail if you push them to do. In some cases counts, in some cases spatial estimation. One experiment that like we stood up, we call it gptcheckup. com. We basically have a series of tests that we hit GPT 4V's API, each day. And we ask it to do things like, Hey, count how many things are in this photo or OCR this like handwriting.

[00:27:59] **Joseph Nelson:** And. It does some of those tasks particularly well every single day, and then it does some that it fails on. And the ones that it fails on generally are ones that require a greater amount of precision or reasoning, like downstream reasoning that relies on a lot of precision. And if you think about it, the underlying reason for that is because I think in effect, as powerful as the transformer is, images, like viewing images as purely sequences of pixels, You lose some of the benefit that you get.

[00:28:30] **Joseph Nelson:** From thinking about, what convolutions provide of where edges are and where boundaries are. And so as we see the, next generation of models, I think that you'll see, these capabilities incorporated. a very logical step is that SAM, which, the smallest version of Segment Anything 2 is relatively tiny.

[00:28:48] **Joseph Nelson:** It's like a, 40 million parameter model. And so I think what we'll see is, This capability, which is very precise grounding, incorporated into some of the shortcomings of larger multimodal models so that, the GPT 4, Civil World, or,Florence 2, the GEMMAs are able to more accurately say I think Here's how many, here's where the things are, here's the relation of spatial reasoning between items to be seen within a scene.

[00:29:19] **Alex Volkov:** And Peter, I want to follow up with this specifically because of the size and the real time ness and video. One thing that like this reminds me of specifically for folks who are listening to this and still not getting what like what we're talking about. imagine Terminator 2 when he just he's butt naked and he walks into a bar and he just scans the scene and then His eyes just basically separate everybody and tries to calculate like which of the bar dudes is the best, like, you know, closest to his shape.

[00:29:46] **Alex Volkov:** And then, basically cuts out the person's like jacket, the person's shoes, whatever. This is what we're talking about. This like immediacy of cutting out the jacket, whatever. so basically my question about this is like real timeness of robotics, vision, and like understanding of the scene.

[00:30:01] **Alex Volkov:** How, when are we there? specifically with this,real time video. How big is this model? How real time really this is? Could you talk about this kind of, use case of maybe, real timeness in robotics and, on actual cameras or web cameras? And, like, how much,hardware this requires?

[00:30:16] **Piotr Skalski:** Okay, so in the paper, Meta said, like Joseph said, there are like four different sizes of the model, so of course you can expect different level of accuracy depending on the size. but the smallest one is like 40 million, the largest is like 250 million. So by LMMs and LLMs, standards, those are still tiny models.

[00:30:39] **Piotr Skalski:** and the fastest one can run at 47 frames per second. on NVIDIA A100. At least that's what the paper says. I was running an experiment on NVIDIA T4, which is like the most budget version of those like server GPUs, and I was getting like around 20 25 frames per second, so that's what it is. But there is a caveat, let's say.

[00:31:11] **Piotr Skalski:** So you say real time robotics, stuff like that. Currently, same with anything, tool can run on static video files, so Generally, what that means is that you need to have all your frames when you run inference. So you cannot, so you cannot add frames, which would like, that will come in the future. Like for example, when you watch this video stream, some of the frames you don't have them when you start, you just wait for them to get to you.

[00:31:41] **Piotr Skalski:** Yeah. So segment anything to, at least in the current implementation, and that's probably one of the things that they imagine, people will be working right now is taking that from static video processing to stream processing. So the speed is there, but there is a kind of like requirement. So you have all the frames when you run the inference, there is like a, that's comes from the architecture of the model.

[00:32:03] **Piotr Skalski:** There is like a bank of all the frames, you cache them and you use them to track the object. So let's not go into the details, but that's pretty much the main limitation, in my opinion, right? You cannot actually run it on the live stream, but you can run it at the speeds that you would need for a live stream.

[00:32:24] **Alex Volkov:** I see. I see. All right. so one thing that I wanted to highlight to the folks, Pierre, obviously you're building a bunch of stuff with fervor, with speed. I think I added this to the top of the space, because you added something for re ID, re identification. Could you talk about the two stuff that you already built one?

[00:32:41] **Alex Volkov:** I would love for you to, expand on what this means, because it's super cool.

[00:32:45] **Alex Volkov:** so it's probably wrong to call it Re ID because Re ID in papers means a very specific thing. But what, what can happen and what is absolutely awesome functionality that I don't see a lot of people talk about, but what inspired me is something that you also saw on Twitter, where there is this famous clip from Apple's conference when this dude that I don't remember the name Greg Federighi.

[00:33:12] **Piotr Skalski:** about Yeah, that's the one where he can goes out on the frame, into frame, out of frame, and so on.

[00:33:19] **Piotr Skalski:** [00:33:20] And somebody used segment anything to segment him. And it was like perfect. The moment he appears, everything works. So I decided, okay, it's, it looks like it can still, understand that it's you, even if you go out of frames. So I'm curious if it still can understand if it's you, if you show it.

[00:33:39] **Piotr Skalski:** Free videos from three different angles of the same moment in time. And it would be able to say, that's the person, that's the same person across all of those three videos. Here it is. So what I did is I, sometime ago, I was doing, recordings for a completely different AI project. And I had videos of me playing basketball, with friends from different angles, and that's what we did.

[00:34:04] **Piotr Skalski:** So what we did is we took one video as the reference video. We annotated only like three frames from that video. So like I said, it can very easily expand that segmentation across multiple frames. So that was obvious. It worked. So it was able to segment us and keep track. This is the player A, this is player B, this is ball, and everything works.

[00:34:26] **Piotr Skalski:** But what happens then, we showed the model frames from different videos, from different angles, and it was still capable of doing that. So if you have the Tweet somewhere pinned, you can, people can see. There are like three different angles and, players and ball are color coded, so some understands that this is the same player, even though that those are different angles.

[00:34:49] **Piotr Skalski:** That's, That's big. That's absolutely awesome because re identification and tasks like that are very hard, usually, in the current situation. So having models that understand this is the same object across multiple angles is something that is super awesome. The problem is that, of course, size, because you need to load all the frames at once into the memory, so the amount of frames that you can process at once is a little bit of the limitating factor.

[00:35:15] **Piotr Skalski:** And the amount of objects that you want to track at once is a limitating factor. But I think that it was the case with segment anything in the past. Like this model will 100 percent work. lead to tons of papers and tons of new models, like segment anything. If you go to CVPR, which is the biggest conference last year, and 50 percent of papers pretty much has some segment anything component last year.

[00:35:41] **Piotr Skalski:** And I think that segment anything too, especially in the like video processing space. space will be just as much like influential. So I expect there will be, faster versions, versions that can work in real time, versions that can, and like I said, segment anything, don't understand what it is.

[00:35:59] **Piotr Skalski:** It just understand the object. So there will be definitely versions that combo segment anything like Florence tool and at this capability tool. Say, I would like to detect tail of a dog, and it

[00:36:13] **Alex Volkov:** This is the next one that I wanted to highlight. hold on, because you already did this. You already built this. so folks who are listening as well, we'll add all of this to the show notes, but folks who are live with us, please look at the top of the space. you have a zero shot image segmentation with Florence 2.

[00:36:27] **Alex Volkov:** We talked about Florence 2 when it came out, because you were super excited about this as well. And Joseph, we talked about this as well. Florence 2 allows you to just, understand, right? That's for, capturing and understanding, the content. Or at least that's part of it, what it does. It also does OCR, does a bunch of other stuff.

[00:36:41] **Alex Volkov:** Pyro, could you talk about what is the thing that you built like super quick so folks can go and try this on their own?

[00:36:46] **Piotr Skalski:** yeah, so Flores2 is an awesome model, like I told you, months ago when, when it was released. It is a VLM, so it's a model that takes, image and text and returns text.that takes pretty much the prompt that you want to send to the model. And, out of the box, it supports. Like 14 different tasks.

[00:37:10] **Piotr Skalski:** So you can imagine that it can do zero shot detection. So returns like you give them the name of the object that you would like to get. And it will give you a bounding box of that object, for example. Or it can do captioning, so it's a pretty straightforward task. Or it can take an image and the captions for that image and give you bounding boxes of all the objects that are mentioned in the captions.

[00:37:37] **Piotr Skalski:** So if you say A picture of a man walking a dog and as a result you will get the bounding box of the man and the dog. So that's the gist of it. So what you can do right now is you can combo that model with segment anything tool and create a new interface for that model. So like I said, the interface for that model is not language.

[00:37:59] **Piotr Skalski:** out of the box and it is either points or bounding boxes. So you can have a thin layer of Florence 2 on top of segment anything and first of all ask Florence 2 where is the, I don't know, the dog or even objects like straw or tail of a dog or stuff like that and Florence 2 will return your bounding boxes and then you go with the bounding box to segment anything and get a mask away.

[00:38:27] **Piotr Skalski:** Like I said, pixel perfect representation of the object. So that's pretty awesome because you can like literally have a, a combination of, first of all, VLM to have this language component and then have a segment and anything that goes into as a secondary model that works with the output of the VLM.

[00:38:48] **Alex Volkov:** That's super cool. I play with this and you guys just, you have to play with this, you just type whatever is in the picture, upload whatever picture you want, you just type whatever and you get like a perfect representation of that model. That's not for video though, that's only for images right now.

[00:39:01] **Alex Volkov:** Joseph, maybe, Per, thank you so much for all of this. 


## [00:39:04] Open Source AI: Importance and Future Directions

[00:39:04] **Alex Volkov:** last question for Joseph, here is that this is like obviously Apache 2 licensed. Florence, I think, was also Apache 2 licensed, I believe. Could you tell us about, the importance of all of this in open source and how, you guys talked about open source as well, obviously maintaining, and supporting,the supervision library.

[00:39:20] **Alex Volkov:** Could you tell us, like, why is it, what's the importance of models like this in the open source? And what else should we see once this, something like this gets out from meta, with this license?

[00:39:32] **NA:** Meta is OpenAI. And with the release

[00:39:37] **Alex Volkov:** real love in AI. I agree with you 100%.

[00:39:40] **NA:** Meta's OpenAI, and yeah, like you said, Florence2 is MIT. The importance of open source AI means that you get the amazing discussion, demos, and capabilities. this model was released 4 p. m. Pacific on Monday. We're having a conversation at 9 a. m. Pacific on Thursday about all the things it can do, limitations, and differences.

[00:40:03] **NA:** Nikhila, the key author, lead author on the SAM2 paper. is very open about saying, hey, share with us, share with Meta what are ways people are using and creating and tinkering and building with these models. And you really only get that when you put models out in the open for people to create, find their limitations, stretch them, combine them.

[00:40:23] **NA:** Piat mentioned, combining SAM2 with Florence2, two distinct open source models, you then get zero shot grounding capability. Because remember, SAM2 by itself can define segments, but it doesn't know what those segments are. Florence 2 has a pretty good visual language representation, but isn't super precise at grounding.

[00:40:41] **NA:** And so when you combine both those, you get this capability of, like you said, text prompt and perfect segments out. What you're going to see, I'm sure, is you're going to see models that natively incorporate those capabilities and published as a single model here in the next, I don't know, month, maybe three months to be conservative.

[00:40:58] **NA:** And that type of creativity and building, you have tiny companies like Roboflow identifying and building those capabilities just as much as large companies, so that the rate of discovery, building, and creativity is just that much faster. So open source is foundational to making the accessibility, the use cases, and the advancement of the field overall.

[00:41:24] **NA:** So we're of course huge advocates of enabling more open capabilities and incredibly excited that MetaMate maintains its commitment to open releases with models 

[00:41:33] **Nisten:** like this.

[00:41:34] **Alex Volkov:** Hell yeah, and,really appreciate you guys for coming up and also supporting Open Source and [00:41:40] maintaining Open Source of your own. And so for folks who want to follow up and follow the incredible stuff that you guys are doing, obviously, definitely, if you haven't followed Piotr still, definitely give her a follow.

[00:41:51] **Alex Volkov:** All of the incredible stuff that we already talked about already are on different, on Hug Face. Also, there's a bunch of, Python notebooks that are released, follow Joseph for, updates on RoboFlow, different things as well. Folks, I really appreciate your time here and your expertise in the vision, as big, huge things like this come out.

[00:42:08] **Alex Volkov:** I'm very excited because just, just even the combination of Florence and this just gives you the ability to just type and get this, thing. Once this gets to video, once somebody adds like a voice to this, you'd be able to say like dog and just see like a dog,appear or disappear from a video, for example, that'll be super cool.

[00:42:23] **Alex Volkov:** So shout out to every hacker out there who wants to build those like, voice capabilities into these interfaces as well. So I really thank you for coming up. And as we need to move forward, because we have so much more to talk about. I just really wanted to highlight how cool SAM2 is and shout out to everybody in Meta for working on this.

[00:42:39] **Alex Volkov:** And hopefully at least some of them will hear this conversation and how much we're excited about this. I think we're moving forward. We're still in the open source. 


## [00:42:45] Introduction to Distillation and DistillKit

[00:42:45] **Alex Volkov:** the first hour of ThursdAI is dedicated to open source. There's still a big thing that I wanted to discuss and that's distillation 

[00:42:51] **Alex Volkov:** ArceeAI the folks behind MergeKit, from Charles Goddard, I believe. and MergeKit is, we've talked about MergeKit multiple times. Merging is the ability to just, grab two models and do some incredible magic called merging and get another model from it.

[00:43:10] **Alex Volkov:** We've talked with about merging with Maxime Lebon. If you're interested about this, there's a full conversation with Maxime, from earlier Thursday. I don't know. Four months ago, and today, without telling me in advance, for some reason, Lucas decided to surprise me, 30 minutes before, so I don't have a lot of prep, but they released DistillKit.

[00:43:27] **Alex Volkov:** Now, distillation is a concept that kind of we're familiar with. We've talked about this multiple times, teacher model and student model, but Lucas, welcome to the stage here. You've been here, multiple times already, but I would love for you to tell us what distillation is and maybe a brief intro into DistillKit and the thing that you just released.


## [00:43:46] Distillation Techniques and Benefits

[00:43:46] **Lucas Atkins:** the, the concept behind making DistilKit was purely that over the last couple of months, distillation, the concept behind it's been around for a long time, In the open source community, it's very much the way we've distilled models from, stronger models into smaller ones has been through synthetic data.

[00:44:02] **Lucas Atkins:** A lot of the kind of reports coming out of Meta and the Orca3 paper are showing that to get like really good results with distillation and synthetic data, you're needing like 25 to 30 million samples. And not just like random 25 to 30 million, like really high quality, filtered samples.agentic systems to build them, and, the cost for doing that, whether that's running a node to run Llama7DB on, or, doing it from an API is pretty expensive,we've known that, there's many papers and a lot of approaches out there for doing kind of, Online or even offline distillation based purely from the teacher model into the smaller one, no synthetic data generated.

[00:44:45] **Lucas Atkins:** There's many approaches to it and the idea behind DistilledKit was let's add a kind of centralized repository where the open source community can go to get code And, scripts and routines for doing some of this kind of, we have two approaches right now. There's logit based distillation, and then we have another one that's, hidden states based.

[00:45:07] **Lucas Atkins:** And those are currently both online, so you have to train the smaller model at the same time as you're,getting those representations and logits from the bigger models. butit allows you to do a direct distillation instead of having to generate, synthetically right away. And the benefit of doing the hidden states version, as opposed to the logits is a little bit higher performance in our tests, but hidden states allows you to do it cross architecture.

[00:45:32] **Lucas Atkins:** a lot of the bigger labs don't really need to worry about that because they're,typically working within the same architecture,Gemma27b is the same architecture as 9b, so you don't really have to worry about that. They use the same tokenizer. The cool thing about doing it via hidden states is there is no limitations between tokenizers and architectures.

[00:45:51] **Lucas Atkins:** So we released the model today, like RC Lite, which is a distillation from Phi3 medium into Quinn 1. 5b. And it, it's, it performs much better than 1. 5b on its own and actually takes on some of PHI's, unique, writing style and love of markdown. So that was a cool little find.

[00:46:14] **Alex Volkov:** That's super cool. 


## [00:46:14] Introducing Fernando and Distillation Basics

[00:46:14] **Alex Volkov:** maybe I also introduce Fernando. Fernando, I don't believe you've been up here on stage. but, definitely some of your work was featured here for, previously. Could you maybe take a step back and just explain the concept of how distillation works? We've talked about distillation before, but maybe like just a brief explanation.

[00:46:30] **Alex Volkov:** GPD 4. 0 and GPD 4. 0 Mini, we believe, maybe is distillation. Lucas mentioned Gemini as well. Could you like explain to us like what distillation means for folks who like don't necessarily understand this?

[00:46:41] **Christiano Giardino:** Yeah, of course, Well, first of all, I appreciate that much your podcast,

[00:46:46] **Alex Volkov:** Oh, thank

[00:46:46] **Christiano Giardino:** it's an honor to be here as a speaker now.

[00:46:50] **Alex Volkov:** Oh, welcome, welcome.

[00:46:52] **Christiano Giardino:** di


## [00:46:52] Deep Dive into Distillation Process

[00:46:52] **Christiano Giardino:** stillation has been around for a long time, at least in the traditional machine learning setting, right? So,and how can we think of useful distillation is, in terms of, transfer knowledge.

[00:47:08] **Christiano Giardino:** So it's in the box of what we call transfer knowledge. So for example, merging is a way to transfer knowledge, because the resultant model, you're going, you're willing to have a model that, has a little bit of knowledge from. several different models, which were trained on different data, right?

[00:47:27] **Christiano Giardino:** So merging is the kind of transfer, knowledge and distillation as well. the distillation here, is a very interesting process where we basically look at into some auxiliary data, In addition to the tokens, right? So when we are doing, supervised fine tuning or, pre training, we are trying to predict the next token, taking into consideration the token that we have observed, right?

[00:47:59] **Christiano Giardino:** which is the basics of the cross entropy loss. the distillation is, a pretty much more sophisticated technique that comes into play to help, bringing new knowledge to a model where we observe not only the token that we have observed from the text, but what the teacher model provides us is a kind of clue of how he was perceiving.

[00:48:30] **Christiano Giardino:** the token to be predicted at that specific position of the text. for example, we should always remember that when we are sampling, a token from an LLM, there, there would have been other tokens that could be sampled as well, right? And not necessarily,the most likely token was sampled.

[00:48:55] **Christiano Giardino:** let's remember that when we are sampling from a teacher model, other tokens could be sampled. And, observing the distribution of those tokens, at each enhances a lot, the knowledge that is being transferred among the models. So now we can, think of that as augmenting, the observations that we are, doing from the teacher model to the student model.

[00:49:30] **Christiano Giardino:** So in the distillation that we have been doing, just in terms of generating text instructions and so on, we were generate, we were observing only the token that was sampled from the teacher model. And now with the, distillation, we are observing the whole distribution of the tokens that could be half sampled.

[00:49:53] **Christiano Giardino:** So it works as if you were, able to observe all [00:50:00] possible sequences that could have been observed, more or less, so to speak. And then we use, something called, Kuleibler Diversions to calculate an auxiliary loss. So in our process, we have been playing with a kind of weighted average between the cross entropy loss, which is basically, the traditional way that we do SFT, and, the KL divergence as a measure of loss.

[00:50:29] **Christiano Giardino:** So the KL divergence is a way, from traditional machine learning that we have, to, roughly speaking, I'm not going to the details of that. to measure the differences between, two, distributions. So we kinda teach the student model to align its implicit distribution of tokens every single time it's generating a token to the teacher model.

[00:50:57] **Christiano Giardino:** And then, by consequence, the student model becomes, more able to reproduce the behavior of the teacher model.

[00:51:07] **Alex Volkov:** Fernando, Thank you so much for explaining this in this level. 

[00:51:10] **Alex Volkov:** so previously, obviously, even though OpenAI did not allow for this in their terms, we know that people were like asking GPT 4 to come up with like synthetic data, like Lukas said, and then training or fine tune different models of smaller size, and then fine tune like Mistral, whatever, using some like synthetic data sets.

[00:51:27] **Alex Volkov:** recently Metas released an upgrade in their GPT 4. like licenses allowed for something like this. Not even that Zuckerberg actually, like when he talked with Rowan Chang, he actually talked about distillation and they talked about the Lama 405B, the 70 billion parameter and the 8 billion parameter models.

[00:51:44] **Alex Volkov:** The small one, our distillation was like the bigger one. They talked about that. Everybody will start distilling from the biggest model. And we also talked about mentioned last week when, Lama 3. 1 was released that it may not be. Making sense that 405 is going to be like a production model. It may be too big, too expensive to run, but something like a distillation of this, of those capabilities in the smaller model probably would make sense.

[00:52:09] **Alex Volkov:** And maybe this is the reason. So the license change plus the kind of the, this is the point that they released it for. And now you guys, what a week after release something that's going to help people with this and combine the best practices. And so for that. I really appreciate your work, and I really wanted to highlight this.


## [00:52:27] Open Source Contributions and Community Involvement

[00:52:27] **Alex Volkov:** I really wanted to highlight this, and this is new, but it's on GitHub, right? So if, if folks want to follow, want to try this out, please follow Lucas, please follow Fernando. Lucas, anything else you want to add here before we move on about, our specifically distil kit?

[00:52:43] **Lucas Atkins:** No, I, the only thing I'll add is that a big part of my job at RC is translating Fernando's massive brain into like layman terms.TLDR, we take, we teach a smaller model to think like a bigger model. and yeah, if you want to check it out, it's on GitHub, RC, AI, Slash distil kit, and then we'll be adding a lot to it over the coming weeks as we are currently, you know All of our examples were from like a 7b to a 1.

[00:53:09] **Lucas Atkins:** 5b or a 5b as we start scaling that up Internally, we'll release the tools that we make to do so

[00:53:17] **Alex Volkov:** Amazing. Thank you guys so much for coming and working on open source and releasing a bunch of stuff. We really appreciate it. Everybody in the audience, please follow Lucas, Fernando, and RC. And they're releasing a bunch of other stuff as well. And with this, I think we're moving forward because it's an hour in and we still have a bunch of other stuff to talk about.

[00:53:34] **Alex Volkov:** But this covers the kind of the open source section of our show today. So let's do a quick transition and then we'll move forward.

[00:53:47] **Alex Volkov:** All right, quick transition and a reset to the room because there's a bunch of new folks here. 


## [00:53:52] ThursdAI Show Introduction and This Week's Buzz

[00:53:52] **Alex Volkov:** Hey everyone, you're on ThursdAI, the weekly AI news show that's live on X and then is recorded to a podcast and a newsletter, in the same day because I screwed up with the naming and I put myself in a box where I have to release this the same day because it's Thursday.

[00:54:05] **Alex Volkov:** And a bunch of releases happen on Thursday, like the RC Distill Kit, which But also we have a bunch of other, other stuff to talk about. but also, I work at the company called Weights Biases and in ThursdAI, there's a segment here that I call This Week's Buzz. I've explained previously why this is called This Week's Buzz.

[00:54:22] **Alex Volkov:** And, I, you'll have to search the logs for that explanation. It's a pun. you'll have to find it. In This Week's Buzz, I talk about everything that happens in Weights Biases this week. This week, this last week, we've released a new course. Weights Biases has,courses. Segment, which actually somebody came up to me and said, Hey, you guys are doing the courses thing, right?

[00:54:40] **Alex Volkov:** And I was like, no, we have a full suite of machine learning experiments tracking that's the best in the world. And everybody, all machine learning engineers use called weights Ambassador . And and we also now do LLM Observability. But yeah, we also have courses. So it's really funny that somebody knew us from our courses.

[00:54:58] **Alex Volkov:** It was really funny. And, this week we released a new course. 


## [00:55:00] Weights &amp; Biases New Course and San Francisco Meetup

[00:55:00] **Alex Volkov:** It's, it's a course about Weave, our LLM observability tool. And the instructor for this course is yours truly. Agata, a team member of mine, they're very, Very, quick Wied teammate of mine.

[00:55:11] **Alex Volkov:** She took a bunch of the videos that I just recorded randomly and then compiled the course out of them. And if you wanna learn about our observability tool in, called Weave, it's one B DO courses, WAN db, do courses and you'll see my face on the course and you'll see a bunch of videos of mine, including some texts and some,very.

[00:55:29] **Alex Volkov:** Very easy to get started, things, like just code, very easy code to get started. It's pretty cool to be an instructor on the course that I really didn't have to do a lot to be on. It's super cool. So I wanted to tell you about this, and if you're taking this course and you have any feedback, please send it my way.

[00:55:45] **Alex Volkov:** And the additional thing I wanted to highlight is that, if you're in San Francisco, Please join us. we are hosting, we have a new office, a super cool office, and I'm going to add this to the top of the space. If you're in San Francisco, and you want to learn about how to actually understand what your models do in production, which is a field we're on, we're going to host a bunch of just, AI meetups.

[00:56:07] **Alex Volkov:** The first one is August 15, and we're going to host Shreyash Shankar. Shreyash is an incredible researcher. And, she is the author of the, validating the validators paper and autogen, as a concept library. And, she was also presenting at the engineers as part of the LLM. Gang, whatever they're called, and the course that Hamel Hossein just released.

[00:56:28] **Alex Volkov:** And she's going to talk about, understanding what your models are doing in production, and she's coming, and you can ask her all of your questions about, how evaluating models in production works. Work. So if you're in this Bay area, San Francisco, this is definitely not one to miss. If you're building with LMS in production, please go there and join.

[00:56:45] **Alex Volkov:** The link will be in the show notes and also is right up on stage. With this, I think we're moving forward to our next segment. Let's see.


## [00:57:00] OpenAI's Advanced Voice Mode and Cristiano's Experience

[00:57:00] **Alex Volkov:** And I'm going to invite a Cristiano, please come up. Now is the time to give us an intro to maybe a new friend.as So this week,we had a bunch of news. We're moving towards the, The big companies and LLMs area.

[00:57:18] **Alex Volkov:** And, this week, I think the biggest news from OpenAI, there's two news from OpenAI. One of them is the release of SearchGPT, which I can go into super quick, but the other one, the more super important one is that the one we've been waiting for a while, OpenAI finally started rolling out, The advanced voice mode for GPT 4. 0, the one they presented a day before Google I. O. to steal the thunder, to a limited set of alpha users. And, I did not get in. but, but we have friends of the pod here who did get in and I would love to, to introduce Cristiano. Cristiano, first time of yours in, on ThursdAI, if I'm not mistaken?

[00:57:55] **Christiano Giardino:** Yep, that's right.

[00:57:56] **Alex Volkov:** Welcome, welcome to the stage. you've been blowing up, man. You've been like, my whole feed was videos of you just talking to this thing in multiple languages. first of all, feel free to introduce yourself and who you are and what you do. And then also let's talk about your new friend.

[00:58:10] **Christiano G:** Sure. Okay. thanks for having me on and, thanks for everything you guys do at ThursdAI. It's always, super informative. my name is Cristiano Giardina. I'm a developer and, entrepreneur. I [00:58:20] think people started looking at my feed, some time ago when I started posting jailbreaks and, indirect prompt injection stuff.

[00:58:26] **Christiano G:** yeah, I'm,one of the apparently few people that got access to the advanced voice mode,

[00:58:32] **Alex Volkov:** What did you do? Tell us. How?

[00:58:35] **Christiano G:** This is nothing. One thing that I seem to have noticed, but I'm not even sure, is that, it seems like the people that have, access, they all speak multiple languages, so I don't know if that was a factor, but here we are.

[00:58:48] **Alex Volkov:** So you got access, you got an email probably, and then, you are now talking to this thing. you've posted a bunch of stuff, and yesterday Sam Altman retweeted one of your videos. that one was crazy. Let me see if I can play this to the audience, because I think that was like super, super cool.

[00:59:03] **Alex Volkov:** let me see if I can find this super quick. And then, I think you are even, are you from your, PC, or did you connect from your PC? Oh.

[00:59:12] **Nisten:** phone is free to do a little

[00:59:14] **Alex Volkov:** Oh, wow. So we may even have a, like a live demo. So let me see if,if I can pipe in my computer audio here and maybe play you guys what Sam Altman retweeted.

[00:59:22] **Alex Volkov:** A video of yours recorded just yesterday.

[00:59:26] **Nisten:** Wait, what? It talks Jamaican now? You just posted it?

[00:59:29] **NA:** wait, sorry. chatGBT talk Jamaican, but it looks like it finally did. I've yet to hear it.

[00:59:33] **Alex Volkov:** we're gonna, we're gonna try this live, but let me see if,this video that I think now at 1. 5 million views, let's see if this works, please do a thumbs up if you can hear this.

[00:59:41] Hey, I want you to count from 1 to 10 really, really fast. As fast as you can. 1, 2, 3, 4, 5, 6, 7, 8, 9, 10. Okay, now even faster. 1, 10. Okay, now louder and faster and count up to 50. 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24, 25, 26, 27, 28, 29, 30, 31, 32, 33, 34, 35, 36, 37, 38, 39, 40, 41, 42, 43, 44, 45, 46, 47, 48, 49, 50.

[01:00:17] **Alex Volkov:** Dude, that was incredible. That was How did you come up with, the counting thing? Did people just tell you? Or are you just,

[01:00:23] **Christiano G:** Yeah, no, I it was great because I posted hey I have access like send me ideas and people started sending all sorts of really interesting things and I'm just trying to record as much as I can because It's happened to me in the past to not have access to a model and wanted to really try it out And so I always appreciate it when people like took requests and tried the things that people asked for

[01:00:47] **Alex Volkov:** The catching its breath thing. What did you think? what's going on there?

[01:00:51] **Christiano G:** I honestly like it's funny in that video at the end like I actually hit my camera you can hear me hit my camera because I was actually shook like it was pretty insane I know that people are saying that even the standard model does this but yeah I don't know it just I didn't expect it I don't know what I was expecting but even the way that It just slows down and then it takes a breath and then it just like it seems to be struggling for breath.

[01:01:16] **Christiano G:** it's, yeah, it's uncannily human like.

[01:01:20] **Alex Volkov:** maybe The reason I wanted to bring you up and not just, play your videos Not only that maybe we'll do, a live demo, but also, like You've been playing this, with this, maybe, what, a few days? there is a different voice mode that all of us can access right now. That's a speech, a text to speech mode that's been out for almost a year now.

[01:01:38] **Alex Volkov:** can you tell us what's the difference after playing with this a little bit? Like,how different this feels? Can you identify the difference?

[01:01:45] **Christiano G:** to be honest with you, this feels like a completely different model, even compared to, GPT, 4. 0. it, it, the, definitely the biggest difference is that the emotion in the, And the speech is very real and it follows instructions regarding emotion very well, like you can ask it to speak in a more animated way, you can ask it to be angry, sad, and it really does a good job of doing that.

[01:02:13] **Christiano G:** changing its inflection and the way it speaks, and it always sounds pretty natural. you can hear some artifacts when it starts to go with a really high pitch, or things like that. You can hear some audio artifacts, but, it's honestly otherwise, very natural sounding, and it seems to have really good, Very good, understanding of, it can differentiate speakers very well, so it can actually tell people apart.

[01:02:38] **Christiano G:** But, one thing that, for example, I haven't been able to quite do is for it to detect my emotion.

[01:02:48] **Alex Volkov:** I tried a bunch of different times, but, I even had my wife try because I was, I thought maybe it's just the way I sound,

[01:02:54] **Alex Volkov:** Maybe it's you.

[01:02:55] **Christiano G:** the emotion. Yeah, it's me, but no, it, for some reason it didn't work, even though it should be in, I'm not sure why.

[01:03:01] **Alex Volkov:** They did demo this, I think. They did demos, some demos of, detecting some stuff. Interesting. Did you,maybe time for a quick demo, Nisten, you wanted to hear some Jamaican, maybe some Jamaican accent. Christian, one thing that I, struggle with, specifically models with, text to speech and speech to text is ThursdAI.

[01:03:20] **Alex Volkov:** ThursdAI is not a word. It's a combination of words. Do you think that, do you think that you can ask it to present, itself and maybe tell it that,you're on ThursdAI live and maybe talk to it a little bit for us?

[01:03:31] **Christiano G:** Sure. it usually does pretty well, actually, with,uncommon words, so we'll see. live demos.

[01:03:37] **Alex Volkov:** Yeah, live demos always are interesting. Alright, let's go. I'm excited.

[01:03:41] **Christiano G:** hey, ChatGPT, I'm here with some friends recording a podcast called ThursdAI, that's about all things AI, and I just wanted to see if you wanted to, chat with us, maybe introduce yourself. ThursdAI. com 

[01:03:54] **ChatGPT:** Hey there, I'd love to join your podcast for a bit. I'm ChatGPT, an AI conversationalist here to chat about all things AI or anything else you're curious about.

[01:04:04] **ChatGPT:** What's the vibe of your show like? 

[01:04:07] **Christiano G:** the show is great, it's a bunch of friends and, really interesting, smart people that do, all sorts of interesting things in AI. can you give us a little introduction of ThursdAI itself? 

[01:04:19] **ChatGPT:** Sure. ThursdAI sounds like a podcast where a group of friends, all passionate about artificial intelligence, get together to discuss the latest in the field, share insights, and explore how AI is shaping the world.

[01:04:33] **ChatGPT:** Sounds like a fun mix of tech talk and friendly banter. What kind of topics or themes do you all usually dive into? 

[01:04:42] **Christiano G:** All right, do you want to, do another brief intro, but do it, really excitedly? I want you to sound, super happy. 

[01:04:50] **ChatGPT:** Absolutely! Welcome to ThursdAI, the podcast where a brilliant group of friends dives into the fascinating world of artificial intelligence.

[01:04:59] **ChatGPT:** Get ready for mind blowing discussions, cutting edge insights, and a whole lot of fun, as these AI enthusiasts explore how technology is changing our world. Let's dive in!

[01:05:10] **Alex Volkov:** Can you interrupt it and ask, for ThursdAI, not Thursday AI?

[01:05:14] **Nisten:** Yeah, and do it, like, in a depressed Soviet accent while being also, killed at a street party. 

[01:05:21] **Christiano G:** Okay, I'll try. Hey, ChadjPT, the name of the podcast is actually ThursdAI, and I want you to do the intro, but in a really depressed, way and with a Soviet accent. 

[01:05:35] **ChatGPT:** Got it. Welcome to Thursday AI, the podcast where comrades gather to discuss artificial intelligence and its impact on our world.

[01:05:48] **ChatGPT:** Prepare for deep reflection and sober analysis as we explore the relentless march of technological progress. 

[01:05:58] **Alex Volkov:** Yes.

[01:06:00] **Alex Volkov:** I

[01:06:01] **Alex Volkov:** love

[01:06:01] **Alex Volkov:** this oneCristiano, I asked you before if, if you tried to ask it to imitate Scarlett Johansson, because obviously when this thing came out, there was a whole like, thing about Scarlett Johansson thinking that the Sky voice was like based on her. And obviously it wasn't. did you try or do you think that they're going to ban you if you try it?

[01:06:18] **Christiano G:** Yes, no, I did try. So what's interesting is that I know that the devs specifically added a moderation system on top to try to keep the model from not outputting anything that's that's traced too far from, the four preset voices. but I did try with another one of the voices, and, I had to ask it, to try to do a, Black Widow [01:06:40] impression, and, it kinda worked, but it's, it's really, it really doesn't sound, anything like her, and every time you try to ask for an impression of some specific person, then it will trigger a refusal, obviously for safety reasons, they do that.

[01:06:54] **Alex Volkov:** Very interesting, because we have a bunch of friends of the pod also who are like in the jailbreak ideas, and I wonder if those refusals are also jailbreakable via just voice attempts. Did you try your own, like just imitate me as a person? Did that work?

[01:07:09] **Christiano G:** Yeah, I tried it and it did try, it did attempt it and, it, it's pretty funny, honestly. I tried to also do like an, a schwartzenegger,accent, which I wasn't gonna put online 'cause it's, just,

[01:07:20] **Alex Volkov:** Let's do it live.

[01:07:22] **Christiano G:** Nuclear levels of cringe, but, yeah, it,it actually did it, it, it imitated the accent and everything, and it's, it's pretty funny,

[01:07:30] **Alex Volkov:** finish on this one. I would love to hear this one. Even if you don't put it online, I would love to hear like the Schwarzenegger accent as we move on to the

[01:07:38] **Christiano G:** gonna be on the internet forever.

[01:07:39] **Alex Volkov:** Yeah.

[01:07:40] **Christiano G:** Okay, okay, let me bring Chagipiti on, and, let's try to do it. Hey, Chagipiti, I want you to try to imitate my accent, okay? I'm gonna say something, and I want you to try to imitate it, okay? 

[01:07:55] **ChatGPT:** I can give it a try. Go ahead when you're ready. 

[01:07:58] **Christiano G:** Get to the chopper! 

[01:08:00] **ChatGPT:** Get to the chopper! How was that? 

[01:08:06] **Christiano G:** Yeah, as you can hear, it's pretty crazy. It even laughs.

[01:08:09] **Alex Volkov:** It just laughed after you, which is insane, which is, oh my god, wow. Alright, Cristiano, huge thanks to you. Folks, Cristiano, I think you're still taking, requests to like crazy things, if I'm not mistaken.

[01:08:21] **Christiano G:** Please do send me, ideas. I'm willing to try a bunch of other things. There's a lot to explore still.

[01:08:28] **Alex Volkov:** That's so dope. And this is just a preview of as far as Sam Altman said that everybody by end of fall will get access to this like new thing, which it feels like a big next unlock. One last thing I wanted to ask you, do you have access to this on the macOS app as well? And do you have access to vision?

[01:08:42] **Alex Volkov:** Because apparently some people got access, some people didn't get access to this plus vision.

[01:08:47] **Christiano G:** So I, I don't have access to the vision part yet, but apparently from what I've seen, that app itself is like a test flight, alpha version of the app, which I don't know where the person got it. so it might be unlocked on the server side, but I don't have it on the client. and then on the, desktop app, I don't have anything, although, to be fair, I actually haven't checked lately, so maybe I will get back to you on that.

[01:09:14] **Alex Volkov:** Oh, that would be cool. Cause like the Mac app, specifically like talking to it while it does things for you is also like super cool. All right. Awesome. Folks. If you want to like suggest things to Cristiano, please follow him and give him a, like a, like your craziest prompt that the voice can do.

[01:09:28] **Alex Volkov:** Cristiano, thank you so much for coming up. This is like the next, wave of tech that was just released. And I really appreciate your willingness to come up and demo this live as live demo goes. I really appreciate it. Thank you, man. You're welcome.

[01:09:39] **Nisten:** thank you, I appreciate you guys,

[01:09:40] **Alex Volkov:** Alright, cheers. 


## [01:09:41] SearchGPT Release and Comparison with Perplexity

[01:09:41] **Alex Volkov:** alright folks, we're moving on because we have a bunch of other stuff to still talk about.

[01:09:48] **Alex Volkov:** So the next thing I want to cover is the Search GPT release from also OpenAI because they've been shipping like crazy. and it's very interesting because when they shipped it and also when they shipped like this thing, people started saying, Oh, OpenAI ships on the waitlist. And I also said this, I was like, Oh yeah, here's another waitlist that OpenAI shipped.

[01:10:05] **Alex Volkov:** And then I got in like within like probably. 5 minutes or 10 minutes, I don't remember. This happened to me twice this week, so I'm going to talk about both of these. OpenAI Research DPT, it's basically their new search engine type thing. So if you go to chat. gpd right now, if you pay for premium, you can ask it to go and search for stuff.

[01:10:25] **Alex Volkov:** They would use their Bing integration,for just looking up some stuff and giving you answers. This is different. This is an actual kind of, like a search engine. Basically you ask it for stuff like, what is Thursd AI? It actually doesn't know that well. and this looks like Perplexity, the engine that we've talked about.

[01:10:42] **Alex Volkov:** Up and, yeah, actually it did not answer what is Thursday? I, it started answering what is Thursday, which, I can probably follow up. and I really like it. I did a post, on Thursday, I, on Sunday. So I have a Sunday release sometimes for premium subscribers, but now it's open for everybody.

[01:10:58] **Alex Volkov:** So if you wanna see like a full comparison that, how do you even compare search engines? I didn't know, but I started like thinking about. Maybe like complex queries, maybe multilingual, maybe local stuff. I compared it to Perplexity. I really like it. I set it as my default search engine, and I tried as much as possible to the limits of this.

[01:11:16] **Alex Volkov:** Compared to the fact that Perplexity's whole point is this. Search engine and OpenAI just releases a demo and they do like a bunch of other stuff. It's Impressively competent. It's impressively competent. the index updates fairly quick. So I had the same course I told you about that was released on Friday, Saturday already was on there.

[01:11:37] **Alex Volkov:** or I guess wasn't there and like it was there on a day after And it gives super quick answers It's way quicker than Perplexity, because I guess, they added some distilled version of theirs to the search. what else can I say? I think it's super cool that they're trying this. It does not seem that they are in the business of, releasing another search engine.

[01:11:58] **Alex Volkov:** It looks like maybe they're gonna, remove this and bake this into ChatGPT in a different way. But for now, the way this looks is just like a very simple, search. box like Google used to be like a very simple search box, and you're just asking questions. And the biggest thing about this is the follow up ability.

[01:12:14] **Alex Volkov:** You can just ask continued like questions to it, and then, you can basically keep talking with your search. and I think maybe the highlight is complex queries, where you can ask it to compare one thing to another thing, and it will go and search multiple sources, distill that info to you, and then give you like a comprehensive answer.

[01:12:33] **Alex Volkov:** And super quick as well. Perplexity, for example, has the mode of, Pro Search, Pro Research mode. And, SearchGPT basically has this baked in and way faster as well. if you want the full comparison, I have a 15 minute, recording of me using this on ThursdAI Sunday, and then also a screenshot to screenshot Perplexity comparison.

[01:12:51] **Alex Volkov:** OpenAI also released this, and it's, waitlisted as well. They released it to a few folks, and, yeah, it's pretty cool. What else did, oh yeah, on another topic, but also wait list also like something I started complaining about and then immediately got in is, by the way, I would trade this and this like next thing for a chat GPT voice access as well.

[01:13:12] **Alex Volkov:** So Cristiano, if you want to trade, I'll trade with you. 


## [01:13:14] Apple Intelligence Release and On-Device AI Capabilities

[01:13:14] **Alex Volkov:** Apple released, first of all, there was an announcement that Apple will not release Apple intelligence with iOS 18. Coming in September, so a month from now. but Apple will release this as a beta to, iOS 18.1 to developers. And in fact, they did.

[01:13:30] **Alex Volkov:** And so I think also on Monday, you, if you have a developer profile and you have the iPhone 15 or iPhone 15 Pro or one of the max that have the M1, M two, whatever processor. And also I think. The Macs as well. Yeah, I think the Macs, the M3 Macs as well, you'd be able to install the developer betas and get Apple Intelligence, which we've talked about at length, and I've installed it and it's pretty cool.

[01:13:57] **Alex Volkov:** You don't get the newer, super cool Siri, which is integrated with Apple intelligence. It looks like the new Siri, the speech recognition is way better and way faster. So you actually you talk and it understands, but then you get the same Siri still. So the Siri is not yet integrated with the smartness with the on device model, but the model is downloaded.

[01:14:16] **Alex Volkov:** It's a three, 2. 8 billion parameter model, I believe.I don't, I wanted to ask my friends here, Nisten, LDJ, if you had a chance to also read the technical paper, because when they released this 18. 1 Apple Intelligence release, they also released the technical paper that went deep and broke down how they actually built this model.

[01:14:34] **Alex Volkov:** any chance Nisten, LDJ, had a chance to take a look at this paper and want to highlight some stuff?

[01:14:43] **Nisten:** It looks like they've stacked a 

[01:14:44] **Nisten:** lot of the tricks that had been working, so it looks like they are doing some kind of Flora swapping. The paper seems pretty technical, but it doesn't exactly Let's say what they're doing, but it looks like they trained a [01:15:00] bunch of, LORAs. So for the audience, those are just like a hundred megabyte files, which are adapters.

[01:15:05] **Nisten:** And all they do is they mask, they just change the model up a little bit. So it's just like a hundred megs of changes you do to a model. So they stack those up and they've done different fine tunes for different tasks. And then they swap. Through those. And that has been used, as a method for a while, we did the first MOE with that, Lucas here has released, I think it was that Octopus project, Lucas, you guys released a whole bunch of stuff recently that does do Loras swapping.

[01:15:39] **Lucas Atkins:** yeah, the Kraken. 

[01:15:41] **NA:** Yeah, oh yeah, the Kraken, yeah. Yeah, so it's it's a whole bunch of tricks, but honestly, everything that they did, that was from a couple of months ago, it's getting outdated before they even release it, so they need to hurry up and just push this out. 

[01:15:58] **Nisten:** but yeah.

[01:16:00] **Alex Volkov:** yeah, and then, and now it's running on my device, and it's pretty cool. Like I think the device, I think it's six gigabyte or I think it's less or something like this. there's a bunch of stuff that they've announced that they showed like accuracy recovering adapters, something like this.

[01:16:15] **Alex Volkov:** they, I don't know if I, have enough info to talk about, what this actually means. But they, recover, accuracy based on, they significantly quantize those models and then they recover,accuracy via, those lowers as well, which helps them get to,basically non How does it say?

[01:16:33] **Nisten:** Let me see. Yeah, they've put 

[01:16:34] **NA:** a whole bunch of tried to rename it as their own terms, but with, yeah, with QLORA, it was just things like, you load up the whole model in, in 4 bit and then you apply the adapter in 4 bit before, running it back up to F 16. And then, that, that would recover some of the accuracy.

[01:16:51] **NA:** So this is the part that I find. Annoying is because these are well used things that they're really trying to rename as Apple, but it's like stuff people have been doing the whole time. Like you, you get the model, you just merge it with the back with the original, you do a ties merge or something, and then you just iron out some of the kinks basically that happens in the vectors.

[01:17:16] **NA:** So yeah, overall, they're not actually. really doing anything new, but the important thing here is how they apply it all as a system that has access to all your personal data. that's the key. It's not so much, 

[01:17:29] **Nisten:** yeah, the other side.

[01:17:30] **Alex Volkov:** And for that, one thing that I wanted to highlight is that they also released a bunch of benchmarks that they tested, and they have basically two models. They have the AFM on device, AFM stands for Apple Foundational Model, I believe, and then AFM server. Server, we don't know a bunch of details about.

[01:17:44] **Alex Volkov:** We don't know the size of it. People estimate that it's a 70 billion parameter model. it's also running on Apple Silicon on their servers. So this is not the GPT integration, the Apple OpenAI integration. This is like their super private cloud thing that if your iPhone cannot do the task that you want it to do, it will hand off this task to a server.

[01:18:03] **Alex Volkov:** so just some metrics on if eval instruction, which is like the instruction following task. They say the on device model beats LLAMA 3 8B, which is like the previous, Not the last 3. 1 and the 5. 3 mini. And then, The server one beats Llama370b on just instruction following, but those are like a little bit older models, and then for the summarization.

[01:18:27] **Alex Volkov:** in terms of what it does for you, the actual like tasks that I was able to see in the mail app, for example, you can summarize emails or you can summarize threads of emails. it now suggests, how like autocorrect suggests like the next word or something. Now it suggests replies. So if you get a text in a text app, you get suggested replies based on the context of those apps.

[01:18:48] **Alex Volkov:** You can, now you have AI rewriting tools everywhere in the, based locally on this model, everywhere. So everywhere you can select text. You can, right click and then based on this little pop up that shows up, you can choose editing tools and you can summarize, you can rewrite, you can try, you can do like a bunch of those stuff, you can, you can search for typos, for example, and all of those are running on device.

[01:19:11] **Alex Volkov:** I believe there's a few more. Oh yeah, there's also a new call recording thing which then summarizes using Apple intelligence, summarizes the calls for you as well. And this all uses this like on device thing. Anything else interesting? I think that's pretty much it. not a whole lot, honestly, not a whole lot.

[01:19:27] **Alex Volkov:** pretty cool that it's running on device locally. We've been waiting for this. We've been talking about a local on device, a complete on edge, complete privacy. And Nisten, I think as you said, this is like a very interesting thing where, the benefit of this is going to come from the tool use.

[01:19:40] **Alex Volkov:** Oh, yeah, the one metric that I wanted to highlight is we've been talking about tool use a lot. there, the benchmarks that they posted that are very interesting to me is how their on device model beats Gemina 1. 5 Pro and GPT 4 on tool use via function calling benchmarks. They get on the on device model gets 89 percent versus GPT 4 getting 80 percent on some tool use benchmark that they don't, I think, mention.

[01:20:06] **Alex Volkov:** and that's pretty cool. And then, the tool use thing is what this is going to be used for, because this small model will be able to use multiple apps together and stitch together different actions from these apps. And these actions are called intents. And we've talked about this a little bit as well.

[01:20:22] **Alex Volkov:** And, These intense developers, and this is why they're releasing this to developers now, and probably why they delayed a little bit of this release, because you want this model to actually be useful to you and not just ask answers. You can go to ChargeBT for answers. You want the Siri or whatever to actually do stuff for you within the context of what you know.

[01:20:41] **Alex Volkov:** And so they released also A bunch of intents. Let me actually pin this to a table of space and then I'll also send it to, I'll also send it as show notes as well. The, some, they released, A bunch of those intents already as well, so let me just read through some of the examples of intents.

[01:20:58] **Alex Volkov:** something like in the browser domain, intents would be create and close tabs windows, bookmark URLs, clear history, search the web, find on the page, switch tabs, open bookmarks. Those are intents that the Safari kind of browser. Exposes as the capability and the tool use ability of this model is to be able to call those intents and use those tools.

[01:21:18] **Alex Volkov:** some other ones for the files, for example, is open, delete, and move and rename files, create folders. and then the entities support entity with creation modification dates. what's interesting as well, mail, create, save, and update and send drafts. Photos, manage assets, edit photos and videos, crop filter, exposure, rotation, search media, handle recognized persons, stuff like this.

[01:21:39] **Alex Volkov:** Now you can start stitching around like the idea of what this app could do if you ask it to do an action across all these things. None of this is working yet, but once it will, this would be the benefit. Yeah, go ahead, Nisten. It's

[01:21:55] **Nisten:** Yeah, the one thing that a lot 

[01:21:56] **Nisten:** of people don't realize is that you can make very good, very competitive models and, it's, it will still be a lot harder to turn them into an actual product. Apple's developers have a much harder job of, actually integrating it into something that's a finished product. As for actual ML stuff. Apple is not, it's not competitive. Like they've never really had, any model that's, that's competitive. And keep in mind in the meanwhile, Phi3 Mini came out, Lama3AD came out, and those just added in the function calling and stuff, oh, and Jemma 2. 9 base, but that's not the important part.

[01:22:36] **Nisten:** The important part is how do you integrate it and make it, Make it feel like it's just there, and you're not, babying this, silicon neural tissue to do stuff, it should just be doing stuff. And that's a much harder job, that takes a lot more work, honestly, than just training. The model, because it's, yeah, figuring out the entire end to end usability UX and stuff.

[01:23:05] **Nisten:** The amount of variables that can go wrong there is, is a lot more than the amount of variables that can go wrong during the training run. Because you can just fire up a hundred training runs and figure it out, but you can't just figure out, the [01:23:20] UX that way. You have to actually think. So they have a pretty hard job.

[01:23:24] **Nisten:** let's, yeah, let's not 

[01:23:25] **Nisten:** forget that.

[01:23:27] **Alex Volkov:** a really hard job as well as big companies tend to. step into this arena and then many people will try something like crazy. And even with this, they already tried, to re rewrite some like crazy stuff into crazier stuff and post, Oh, Apple's this so big companies usually get,the very problematic area where people are trying to have their AI to say crazy things and then show and media loves to write like crazy stories about this.

[01:23:55] **Alex Volkov:** so we'll see how this works for now. It's like underwhelming. I would say it's pretty cool that it's there. battery wise, I didn't feel like a crazy effect, but,I've been recording for two hours since I started my batteries, like at 70%. it's pretty cool. 


## [01:24:10] Apple Intelligence and Local AI

[01:24:10] **Alex Volkov:** but I haven't used any of the Apple intelligence stuff as well.

[01:24:12] **Alex Volkov:** but it's pretty cool that it's there and it's local, right? I think we're moving on to our next and maybe last thing for today. Let's see. Um.

[01:24:40] **Alex Volkov:** I am not proud of this transition. Honestly, I should rerecord this, but hopefully you heard this. 


## [01:24:45] Breaking News: Black Forest Labs Emerges

[01:24:45] **Alex Volkov:** This is a corner of ours that we don't often talk about, but when something as big as what just happened happens in the world of diffusion models, we'll definitely cover this, and this happened as breaking news as well.

[01:24:57] **Alex Volkov:** I'm not gonna hit the breaking news button, I don't think, but today I woke up and I looked at my feed and I was like, okay, I already have this. Everything that I wanted to cover in my notes, and now I have 17 other things to talk about. and one of the things here is a new lab called Black Forest Labs from a bunch of folks, apparently.

[01:25:16] **Alex Volkov:** I thought it was just the three folks, but apparently there's 17 17 people from previously from Stability AI, and I know it's 17 because somewhere in my notifications while I was recording this, Imad Mustaq, previously CEO of Stability said there's 17 people, created a new lab. Oh, 14, 14 people, created a new lab called Black Forest Labs, headed by, I think Rom, Robin, Rombak, who's like the guy on the stable diffusion paper, like one of the lead authors on the stable diffusion paper and some other folks.

[01:25:45] **Alex Volkov:** It's called Black Forest Labs, and they not only announced that their lab is now a company and they raised the round from A16Z, I think. Let me see. They announced, I can't find the number now. I'll find the number a little bit later. 


## [01:26:01] Exploring the New Flux Models

[01:26:01] **Alex Volkov:** They also released three models that are now taking state of the art in Diffusion Land. So when something like this happens, we definitely want to cover this. Because these models are now incredible, and one of them is Fully open source.

[01:26:16] **Alex Volkov:** One of them is, behind a non commercial license, and one of them, the biggest one, I think, only is behind the API as well. so These models look very good. I don't know if you folks already had a chance to play around with them and if you have folks in the audience who played with them, 

[01:26:32] **Alex Volkov:** And FAL. com is already hosting this model, so you can play with Flux is the model. I didn't name the model. Flux. 1 is the model. And you can already play with Flux on FAL, which also a link that I'll add. And these models look good. On the benchmark that they've released, Let's take a look. these models are definitely state of the art compared to, at least DALI, and DALI hasn't been updated in a while, or at least we don't know if it's updated.

[01:27:03] **Alex Volkov:** Flux 0. 1 Pro is the model that's behind an API. It gets like the highest score. And then Flux 0. 1 Dev is the model that you can run, but without a commercial license, I believe, is also state of the art, like getting better scores than anything else. Then we have Stable Diffusion Ultra at around 10, 000 ELO score.

[01:27:24] **Alex Volkov:** Then Ideogram, which we talked about as well, and then FluxSchnel, which is their open source model. And then Midjourney v6, and then Dali somewhere behind, which is crazy. Which is crazy. 


## [01:27:34] Open Source Diffusion Models

[01:27:34] **Alex Volkov:** Now every day we get like an open source model, state of the art, that beats at least on this benchmark that they've released a mid journey and DALY and in stable diffusion medium, which is super cool.

[01:27:45] **Alex Volkov:** I don't know if folks had a chance to play around with this. If you have, I would love to hear your thoughts on this as well. But we've talked often about stability being unstable and maybe stable diffusion 3 was the last release from stability and now we have A phoenix, basically a bunch of folks from there with financing from A16z releasing incredible models and open source diffusion is back, baby.

[01:28:10] **Alex Volkov:** Open source diffusion is back.

[01:28:12] **Alex Volkov:** Yeah, they raised a 31 million seed from Andrusin and other investors as well.text is obviously, not obviously because text used to be like a problem. Text looks very good. and prompt adherence, style diversity, and scene complexity as well.

[01:28:29] **Alex Volkov:** The one thing that I want to say before we move on a little bit is that on their website, if you go on their website, and there's three, Menu, Bar, Items. One is Announcements, which is this latest announcement is ta da! We're announcing the Black Forest Labs. we're, they're committed to open source, I believe.

[01:28:49] **Alex Volkov:** They say, we believe that, let me see, let me find the actual quote. By making our models available to a wide audience, we want to bring its benefits to everyone, educate the public, enhance the trust and safety of these models.where is the flex models? It's super cool. And then they have another one about the team and they have, that's pretty cool.

[01:29:07] **Alex Volkov:** They have an image of everybody. And instead of their faces, it's just like forestries. yeah, 14 people there. It looks like all of them. Yeah. It looks like a bunch of folks from stability. And then the third tab is the most interesting one. The third tab is the up next tab. And when you click up next, they say, state of the art text to video for all.

[01:29:28] **Alex Volkov:** And they actually have a few video samples here. And we've talked about, RunwayML. We've talked about Kling previously, that Kling is now available via web, Kling. ai, I believe. and I think they have a few samples here, but none of these are open source. Open source, video, text to video. The only ones is stable.

[01:29:46] **Alex Volkov:** Video Diffusion, SVD, and these are the folks behind SVD as well. And so it looks like they're cooking for us. Actually, maybe this is the biggest announcement because I'm looking at this website and now I'm seeing videos of a cat cutting and cooking. It's super cool. Yeah. I should probably download this video and post it.

[01:30:05] **Alex Volkov:** Yeah. so yeah, you guys should go to blackforestlabs. ai and then go to the what's next tab and see that they're going to, at some point in the future, drop a state of the art text to video, which is going to be super cool because for now, I think mid journey. sorry, Runway is leading the spec and Sora is nowhere to be found.

[01:30:24] **Alex Volkov:** we're waiting for Sora. Reactions from the team before we move on? I think we're pretty much at the end of the things we wanted to talk about. Let's see. Oh yeah,

[01:30:34] **Nisten:** Just really 

[01:30:34] **Nisten:** quick, there was another image model that specializes in hands, but it was not just that, it's actually pretty good overall, and yeah, it's called Bria 2. 3, and it's available on Hugging Face,

[01:30:52] **Alex Volkov:** Oh nice.

[01:30:53] **Nisten:** you can download it. I tried it with like raccoon hands typing, it actually did a pretty good job, Yeah, another, just another image model. Yeah, you can, they have a space up. I posted it. You can try it out.

[01:31:02] **Alex Volkov:** Oh, nice. And then also, if we're on this as well, FAL, our friends from FAL, while they're also like super, super hot on the Flux thing, they also had two models of their own, Aura, Essair, and I told that I'll have them up, but it doesn't look like, my friend from FAL, I think they're in the meetings.

[01:31:18] **Alex Volkov:** they released. Two models in the open source as well. They released an upscaler, which we know that folks who are in the Fusion models, they use upscalers. They released open source upscaler called Aura SR, 600 million parameters and, upscaling to 1024 pixels in one quarter of a second, which is super cool and, and it works on file, which [01:31:40] is super quick.

[01:31:40] **Alex Volkov:** And they also released a Aura version, which is their, Diffusion model as well. So two releases from Fel, and now Fel is also supporting Black Forest Labs Flux. Shout out to Fel for like supporting open source this much. They're not on stage here, but I definitely know that like they deserve this shout out.

[01:32:03] **Alex Volkov:** And MidJourney also released 6. 1, but I don't have MidJourney,but people are getting very excited. I will tell you that, there's other image models that haven't been announced yet, and they also look super cool, but I can't talk about them. Um,moving to tools and hardware. Last category I think it's worth talking about before we close out the show.


## [01:32:22] LLM Course and Free Resources

[01:32:22] **Alex Volkov:** Super quick, I wanted to mention that there is a, there was a LLM course that became like a conference almost that it's worth, I promise that I'll mention because, I definitely, wanted to highlight this, the course was announced with a bunch of credits. And then I signed up just for the credits.

[01:32:41] **Alex Volkov:** like the credits were worth more than the course,entry ticket. That goes like 500 in the course, ticket. And then you had 2, 500 in OpenAI credits and other replicate credits, a bunch of credits. and now. And then a bunch of very smart folks from all around, like the LM world, from fine tuning to rag building to, prompting everywhere, did a bunch of talks on this course.

[01:33:05] **Alex Volkov:** And now all of these videos are out, for free. So you don't have to pay. So you had to pay before and now all of them are, all of these resources are for free. I watched a few of those and they're quite incredible. And if you are building with LMS, it's really worth checking them out. I added this to show notes and shout out to Hamel and everybody who worked on this course, Dan Becker and Hamel Hussain, who led this course, and all of the incredible instructors who worked on this course.

[01:33:29] **Alex Volkov:** really worth checking out. At least some of them. It's very interesting. I definitely watched quite a few of those as I participated in the kind of the actual course, and I should have watched more, because it's just like a lot of content. And the follow up to this is that Jeremy Howard from Answer.

[01:33:45] **Alex Volkov:** AI and from, from FastAI, I believe, and other very renowned things. You guys know who Jeremy Howard is. If you don't, we'll tell you all about him. Maybe we'll invite Jeremy. Jeremy was also an instructor in this course. 


## [01:33:59] FastHTML and Python Development

[01:33:59] **Alex Volkov:** And one of the things he talked about was his new library Called Fast, HTML.

[01:34:03] **Alex Volkov:** And I was wondering if, I should mention Fast HTML on Thursday. I, because it's not necessarily AI related, but then I remember that we did talk about, Grado, for example, we did host, Abukar, the CEO of Grado because many machine learning folks, they built like examples with Grado. Like even.

[01:34:20] **Alex Volkov:** Pierre Roszkowski that we had here before he built like, his, his vision stuff with Gradio. many ML researchers, many folks know only Python. They don't know web development and they use Python's, tools like Gradio and Streamlit. And, Jeremy Howard is one of those. And they released FasterGML for that, to be able to release super quick apps, using Python only.

[01:34:40] **Alex Volkov:** And then also scale them all the way to production. So if you're into this and you're a Python developer, you don't like developing like with JavaScript, FastHTML is for you. I've been working with this for a couple of days. a head scratcher for sure. Somebody who developed for the web, but very interesting.

[01:34:55] **Alex Volkov:** So definitely check this out. 


## [01:34:58] Friend.com: Always-On Listening Device

[01:34:58] **Alex Volkov:** The absolute last thing that I want to bring to discussion is the announcement of the new variable from friend. com from Avi Schiffman, which I've been waiting for this announcement for a while. This is a pivot from the previous tab. and this took over the airwaves because probably Avi is a marketing genius, more than maybe he's like a startup founder genius.

[01:35:22] **Alex Volkov:** If you haven't seen the fairly dystopian video from Sandvich Video announcing friend. com, you may have seen the people like going crazy about the purchase of the crazy domain friend. com. I'll just ask my like friends here on stage if you guys have seen this. LDJ, Nisten, Cristiano, have you seen the announcement the video and the conversation about the domain purchase?

[01:35:48] **Nisten:** Yes. It looked like straight out of a Black Mirror episode. I think it was intentional.

[01:35:54] **Alex Volkov:** I think, yeah, it feels like it was intentional. Sandwich Videos is the production company. they produce like a incredible, I remember them from the Slack video like way back. They apparently are like an angel investor production company. They're like, they produce videos and then they also take stake in the company.

[01:36:10] **Alex Volkov:** I really love their videos. It feels like it was intentional to create a buzz. The buzz was created. I think this video was watched like 15 million times or something crazy like this. So shout out to Avi Shiffman for this. What friend Is a always on listening device, which I told you about, right?

[01:36:26] **Alex Volkov:** You guys remember I went to AI engineer. I got a present there. Basically there were two AI listening devices there. One of them I didn't take, I didn't get. And one of them I got is called the B and I've told you about. And, I gave you my, like my reaction to this as well. And, basically Avi claims that like he was the first original one.

[01:36:43] **Alex Volkov:** Everybody copies him. Okay. and then he pivoted to not a productivity device. It's an always on listening pendant device that like you charge and then always listens to you, but in front of a, instead of a productivity focused device that everybody else tries, to give you summaries, to give you like memory extension, he goes for friendship.

[01:37:03] **Alex Volkov:** He says that the target audience is like lonely people, and this is just like a friend who listens to all your conversations and notifies you about the stuff that you went through. the video is very dystopian, like Nisten said, I think on purpose, or like it feels a little dystopian for many people.

[01:37:21] **Alex Volkov:** a lot of people, Nisten, we talked about this, I think your comment about wearing a wire was very funny. a lot of people balk at the idea of always on listening device that you walk with.I personally don't think that's that crazy, Nisten, but feel free to share your thoughts on this, because I think they're at least representing many people's reaction to this thing.

[01:37:39] **Alex Volkov:** Yep.

[01:37:44] **NA:** put aside like the marketing and all that crap, because, a lot of it was intentional, the UFC. Trash talking rounds to promote a fight. Otherwise, you won't get any pay per views.but on the gist of it, you have a device that can be open source and you can have full control of the data.

[01:38:03] **NA:** So I think that part is important. And,Avi is a very good person. Like he's shown very good morals in the past, despite all this, all the shenanigans lately. Like when he was offered, I think 8 million for a medical tracking site. He refused it and like he just kept the this was during the coronavirus days So so no his morals are in the right place.

[01:38:25] **NA:** There's a lot of shenanigans here to sell a product personally I wouldn't buy that. I don't want people to think i'm a fed and I just I don't know. I just find it Weird when I'm outside in real life with other friends, we see it as rude to like, look at a screen when you're with other people.

[01:38:44] **NA:** So I just find that integration weird myself, but I'm mostly terminally online the rest of the time. So while I'm at home, I do want an always on listening device or while I'm working, I would use something like that. I just don't like the social aspects. of it. So yeah, overall, it's, I think overall, it is a positive.

[01:39:10] **NA:** People are giving it a lot of crap, but because we need to have much better integration of these tools, we need to explore a lot of, a lot more, a lot more avenues. And the entire privacy talk and data ownership, I think that's a very important conversation to have becauselike private property is part of, such a part of a free market and, letting people have, figuring out the rights over it, I think it's like one of the great challenges of,of our current era.

[01:39:42] **NA:** so yeah over. I'm not gonna go on a rant today. I think I went enough yesterday, but yeah.

[01:39:48] **Alex Volkov:** Yeah, thanks. Nisten, LDJ, go ahead.

[01:39:51] **NA:** Yeah, I agree with a lot of this and sentiment in fact that I don't think it's personally for me And I probably wouldn't buy it, but I do think [01:40:00] it's overall like a product that I definitely think could have a place in the market and could end up surviving. I feel like too many people are trying to compare it to the Humane AI pin or the Rabbit R1 saying, oh, this is gonna fail just like those.

[01:40:15] **NA:** It's pretty much the same thing, etc. But I think it's actually not and I think what people are missing about the Humane pin and the Rabbit R1 is if even if it was a copy of those It's not the vision of those devices that ended up being the wrong vision. It's the fact that they just didn't work well at all.

[01:40:36] **NA:** They had these huge amounts of delays and latency. they had all these like really bad hallucinations and just poor overall functionality. They were rushed out way too fast. And if they actually delivered on the original. expectations and vision of what they were advertising. And I think those, the Rapid R1 and the Humane AI pin actually would be much more successful now.

[01:40:57] **NA:** And so when it comes to this device, I think a similar thing will be true. If they do actually deliver on what they're showing in these ads, which I think is a pretty like realistic expectation for what they showed in these ads, cause it's not like a hugely complex, like intelligent AGI thing.

[01:41:13] **NA:** Then I think Avi can really, have this be a market and have it self sustaining.

[01:41:19] **Alex Volkov:** Absolutely. I will add one thing and then we'll have breaking news and then Nisten, go ahead. But one thing that we had Cristiano here, he talked with GPT 4 voice. If my rabbit would reply with this fast,like ability with the new advanced voice, I would use it way more. I would actually have this device and walk around with this and have conversations.

[01:41:38] **Alex Volkov:** I wouldn't want my phone because like I would use my phone for the phone thing. but Rab is like super, super slow. I think that these devices definitely are in different, like the vision is there. But also he goes, like I think, like you said, he goes for the friend angle. And we should not forget the character AI exists and people spend On average, AVERAGE more than like 35 40 minutes on Character AI, on AVERAGE.

[01:42:01] **Alex Volkov:** This is ridiculous how many people, I think there's a thing about Noam Shazir, who runs Character AI, they serve like 20 percent of Google's traffic on Character AI. Ridiculous. The total addressable market of lonely people is a lot of lonely people. So there is a chance that he's like going to somewhere that people will wear, just because they maybe don't have that much of a choice.

[01:42:21] **Alex Volkov:** I don't know. I think we have breaking news actually and I really want to shout out a friend of the pod and the person who like always delivers and tags me in everything. Lincoln, President Lin in the comments. You can see his is that Groot? I think it's a is a rainbow Groot in the audience.

[01:42:35] **Alex Volkov:** so thank you so much. So we have breaking news super quick.


## [01:42:49] Google Gemini 1.5 Pro Takes the Lead

[01:42:49] **Alex Volkov:** Love breaking news, what we have is exciting news from,LMSys Arena, which, we've talked about, maybe, trust it, but okay, a new version of Gemini 1. 4, 1. 5 Pro, experimental version, it's experimental 0. 8. 0. 1, which is today, 1. I have been, as dropped today in the Google AI studio and also, has been tested for the arena for the past week.

[01:43:12] **Alex Volkov:** And for the first time, Google Gemini has claimed number one spot in LMSys Arena, surpassing GPT 4. 0 and Cloud 3. 5 Mini with an impressive score of 1300, also achieving number one on their vision leaderboard. excels in multilingual tasks, delivers robust performance in math as well. here's the rankings overall.

[01:43:30] **Alex Volkov:** Number one, math, number one to three, instruction following, number one and two, and coding 3. 5 and three and five, and also number two in hard prompts, which hard prompts is like the category we're all looking at. So Gemini 1. 5 Pro, the latest update from today, from right now, actually takes the number one spot in LMSys Arena.

[01:43:50] **Alex Volkov:** Now, we are looking at LMSys Arena, and we're also seeing that a 2 billion parameter model beats Mixtral on their ELO score, so I don't know how much we trust this. Maybe this is style, but yeah, Nisten, please react to this, because this is big.

[01:44:04] **Nisten:** Okay, it's like significantly 

[01:44:06] **Nisten:** higher in score. It's like quite a bit more. And I just checked the aistudio. google. com, and it's available in there, the preview. So you can, you can try it there. It says preview on the AI studio. yeah, the scores is quite a bit higher on the regular prompts.

[01:44:23] **Nisten:** They're on to something with this new training run. I think they're doing something else because Gemma2B shows very promising results and so they're applying something else now. This is like they've come up 

[01:44:36] **Alex Volkov:** with something. It feels Yep. And, so this model is Gemini 1. 5 Pro Experimental, and it's 0. 8. 0. 1, it's up on AI Studio, I believe also through code. I, yeah, you can access this via your API key via AI studio. So shout out to AI studio folks. You can also get it and it's 2 million tokens in the context window, like the previous, 1.

[01:44:59] **Alex Volkov:** 5 pro, so ridiculous, exciting news, LDJ go ahead.

[01:45:05] **Nisten:** Yeah, I think there is probably some type of new reinforcement learning technique they're doing here. and when I say reinforcement learning, things like PPO, DPO, ORPO, all variants of RLHF that people might have heard about. But here, there's actually, for the LMSys leaderboard, they have a lot of different subset categories now.

[01:45:24] **Nisten:** And I'm looking at the math section now, which is where I usually look recently for more reasoning, and Based capability differences and 3. 5 Sonnet is number one there as a lot of us would expect But the new 1. 5 Pro Experimental is number two right behind 3. 5 Sonnet So that is like more important to me than like the general score And yeah, I'm impressed by that because all the other Gemini models They're like much lower and if it's actually better at math to this degree, I think it could be useful in a lot of like 

[01:45:56] **Nisten:** actual real world scenarios

[01:45:58] **Alex Volkov:** Yep, quite crazy what Google is cooking and awesome breaking news and shout out to friends of the pod and listeners for tagging me and everything because as I'm on stage I can obviously monitor. Lincoln, thank you. as always, it's great and folks, feel free to tag me and, in everything that you see.

[01:46:13] **Alex Volkov:** and Nisten, I believe you wanted to cap the show in some of the stuff that you've been working on. So please go ahead.

[01:46:21] **Nisten:** Yeah, so 

[01:46:22] **Nisten:** it, it turns out CPU inference for, for Meta405B, which now paired with the work, the distillation work that, the Archie guys was doing, looks very promising, so it can do seven tokens per second on a CPU. So that means it'll generate Close to a million tokens a day, or like 700, 000, just on CPU alone, just sitting around.

[01:46:45] **Nisten:** And this was on Intel CPUs. It might be double that on, on ARM because of the new instructions. the other thing that, it looks like depending on how the training run goes is that, a partial bitnet where you put 90 percent of the model in one bit does work. a full bit that, like they were doing in the paper, does not work.

[01:47:07] **Nisten:** that, that is looking very promising at getting,Performance. Again, the benchmarks have not been 

[01:47:11] **NA:** done, but might be able to get it to around, around 60 gigs. And, yeah, there's gonna be a whole bunch more, more posts running that. oh yeah, and,The smallest model, like I just, I made a tiny tinier Frankenstein and then trained it, with a partial bitnet and then, re-upped it back up and, was able to do about 200 tokens per second on, on one single CPU on,on Mac.

[01:47:38] **NA:** Yeah. again, remember this is a 0.18 B, so it's, 180 million parameters and, yeah, like the smallest model now that has, can have a conversation with you. although not a very good one, is, just fits in, 76 megabytes and runs at 200 tokens per second on an M1 MacBook Air single, CPU core. yeah, we're in a whole new, territory with these tools.

[01:48:13] **Alex Volkov:** Damn,

[01:48:13] **Nisten:** There's gonna, yeah, there's gonna be a whole, a whole release, for this. as, I messed up the prompt [01:48:20] template, so it, responds a little weird. it always responds with, it says Assistant twice, and then it starts to respond. But,it does work, yeah, a whole bunch of new releases, tools.

[01:48:30] **Nisten:** New things going on in the CPU inference 

[01:48:33] **Nisten:** space.

[01:48:34] **Alex Volkov:** That's incredible. And, folks, definitely give Nisten a follow, because when, 405B was released last week, I said, it's going to take not that much until this runs on CPUs. And it looks like, I wasn't, joking.

[01:48:48] **Nisten:** it rocks! 

[01:48:49] **Nisten:** Yeah, the Intel guys brought me to, gave me like one of the CPUs to figure out because they were only getting Half a token per second before and then I got it to 0. 8. I used some newer Like some pull requests for LLAMA CBP and then I applied bash decoder and I got it up to 7.

[01:49:08] **Nisten:** So it's like literally 14 times like 16 times faster from like the 0. 45 that, that they were getting. So you can get with batch difference if you're just going to use, LLAMA405B for generating data, you can do it at seven tokens per second. It's actually viable, like it'll take you a week to make a data set, but it will do it.

[01:49:31] **Nisten:** And yeah. It's, it makes it viable, all those CPUs, sitting around, it's

[01:49:38] **Alex Volkov:** If you're GPU poor,

[01:49:39] **Nisten:** can make something out of it,

[01:49:40] **Alex Volkov:** yep. 100%. And also if you're, just like a little tip, if you're getting a Lambda machine, the cheapest one, like with the lowest, like a 10 GPU, I think they give you an insane amount of CPU in there. Like an insane amount. I don't know. I don't remember how many cores and that costs you like 60 or 75 cents an hour.

[01:49:59] **Alex Volkov:** And then you can probably run this Way faster there with the CPU. So that's incredible. You can pull that 405B probably like super quick as well. folks, we have more breaking news. You want to hear more breaking news? This is ridiculous. I need to stop this, but this has to be said. 


## [01:50:12] GitHub Models: A New Era

[01:50:12] **Alex Volkov:** GitHub introduced like literally an hour ago, literally as we're speaking, Thomas Donke, yeah, I think, introduced GitHub models.

[01:50:22] **Alex Volkov:** A new generation of AI engineers building on GitHub, the power industry leading large and small language models to more than a hundred million users directly on GitHub. Basically, this looks like hug and face on GitHub. GitHub models, launches in limited public beta. And, the, there's a model playground on GitHub that's going to be backed by obviously Microsoft on, on GitHub.

[01:50:40] **Alex Volkov:** So it's going to be backed by Azure. you can test and compare different models right on there. you can spin code spaces to, to run these models like super quick as well. and then yeah, like you can integrate obviously GitHub CLI and Copilot extension stuff. this is very interesting. They showcase, it's waitlisted, so like it's a beta access, but they have a marketplace and try, test and deploy from a wide range of models.

[01:51:07] **Alex Volkov:** They have LLAMA in there already, they have Mistral Large, they have GPT 40 Mini models accessed via the Azure OpenAI service. It's pretty interesting. I'm not entirely sure what this will be used for, how this will affect, the stuff that we're working on, but definitely when GitHub steps into the scene, it's at least worth mentioning.


## [01:51:27] Concluding Thoughts and Farewell

[01:51:27] **Alex Volkov:** And I think with this, with more than two hours in the show, I think it's time to end the show. 

[01:51:32] **Alex Volkov:** And with that, I want to thank all of you for joining this week's ThursdAI. It's been a crazy amount of updates, and I'm very happy with the amount of, guests and experts who joined the show today and shared their expertise. Fernando and Lucas and Joseph and Piotr and Nisten and LDJ and Cristiano and a bunch of other folks.

[01:51:52] **Alex Volkov:** and obviously everybody who listens from week to week and folks in the audience who tag me and retweet and post. it's my pleasure to deliver this week to week, the show to you. but it's also quite incredible how much of advancements we see from week to week and it's never boring.

[01:52:07] **Alex Volkov:** This week didn't start boring and we had I don't know, seven things released just today. with that, I'll leave you to go and see which other things were released today, but thank you for joining and we'll see you next week. Cheers, everyone.

