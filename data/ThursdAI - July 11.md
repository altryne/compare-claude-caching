[00:00:00] **Alex Volkov:** Hey everyone, Alex here. This is ThursdAI. July 12th? Yes, July 12th. Am I confused? Because, I'm not really here. This is a pre recorded podcast, which is new for me because for the past year, I've been doing these podcasts live, on X and then editing them into a podcast form for you. Same day as we recorded the live show.

[00:00:34] **Alex Volkov:** And today's a little different. I'm actually flying on vacation. And, but I didn't want to leave you hanging. I didn't want to break my streak of a year full of podcasts. And so I decided to release some previous material that I had, for you to enjoy a few conversations. So today we'll have two conversations with three folks.

[00:00:55] **Alex Volkov:** First, we'll have a conversation about mixture of agents, a. Interesting new way,similar to mixture of experts that we've talked about, which happens in the LLM world of things, but this happens in the prompt world of things. And this is conversation with James Zhu from Stanford. Who, together with TogetherAI, yeah, it's funny to say this, together with TogetherAI came up with this technique called together, called mixture of agents.

[00:01:31] **Alex Volkov:** And, they have achieved incredible performance as you'll hear on Alpaca Eval, which is a very hard benchmark to, to beat. And there is the paper and James will tell us all about mixture of agents. And, luckily that week. More than one mixture of agents was released. And, so I reached out to multiple authors of multiple mixture of agent implementations.

[00:01:57] **Alex Volkov:** And so I also hosted Kyle Corbett from OpenPipe, which is a company specializing in fine tuning for your own models. and, Kyle and the OpenPipe folks also released some work that was done Separately And inspired potentially by at least the naming, that's also called Mixture of Agents. And they have beat State of the Art on Alpaca Eval as well during the same week, so that was a crazy week.

[00:02:23] **Alex Volkov:** I believe this was June 20th. that we recorded this conversation with James and Kyle. And it was a great conversation. If you're into prompting techniques like chain of thought reasoning, this mixture of agents is definitely a very interesting area to explore. So this episode is going to be more of an AI engineer focused episode.

[00:02:45] **Alex Volkov:** The second part is an interview with Alex Atala that I recorded back in April, and I didn't post it back then. Because of some sound issues, and hopefully I fix some of them, but I apologize in advance if the audio, on Alex's end wasn't, perfect, and I wasn't able to fix it super, uh, well. However, it was a very illuminating interview.

[00:03:06] **Alex Volkov:** If you've never heard of OpenRouter, definitely listen to this. If you've heard of OpenRouter and used OpenRouter, even More of a reason to listen to this. OpenRouter is this incredible place where, you can access any model that basically they put there. And as far as I know, this is pretty much the only place where you can access a bunch of open source models and also a bunch of frontier models like OpenAIs, Anthropic Cloud, et cetera, with a unified interface.

[00:03:36] **Alex Volkov:** And that interface also supports the OpenAI SDK interface. Which, by the way, to, talk our own book, because of this, it also supports Weights Biases Weave natively, which I just added to our documentation today. but besides this, OpenRouter is this incredible place that, Allows you to do fallbacks for your own OpenAI, for example, quotas.

[00:04:01] **Alex Volkov:** And so if OpenAI gives you a quota, you can fall back to OpenRouter, for example, switching just a string in your code, which is quite incredible. And Alex previously was the CTO of OpenSea and has a lot of ideas about Open source and, and open access and very illuminating conversation with Alex. He was a little bit sick, but he came through anyway.

[00:04:25] **Alex Volkov:** And I have been sitting on this conversation for a long time, and I'm very happy that finally I had a chance to raise this. So I'm really hoping that you'll enjoy both these conversations, as I'm. Taking a much needed break and,ThursdAI is going a little bit of a hiatus from live shows. With that, I give you the first conversation with James Zhu and Kyle Corbett.

[00:04:50] **Alex Volkov:** All right, folks. Now I want to move towards, our next kind of conversation. 


## [00:05:06] James Zhu on Mixture of Agents

[00:05:06] **Alex Volkov:** We have James Zhu here. I'm hoping I'm pronouncing this correctly and also Kyle. And, we're switching gears a little bit. We're going to talk about some other news as well. James, feel free to, to say hi to the folks and introduce yourself.

[00:05:18] **Alex Volkov:** And we're going to talk about some exciting stuff from you guys from together.

[00:05:22] **James Zou:** Hey Alex, can you hear me okay?

[00:05:24] **Alex Volkov:** Coming through loud and clear. Welcome.

[00:05:27] **James Zou:** great. Thank you very much.

[00:05:28] **Alex Volkov:** feel free to introduce yourself to the folks because this is your first time on ThursdAI.

[00:05:31] **James Zou:** Yeah. Yeah. Yeah. So I'm, James. I'm a professor at Stanford where I lead a group developing AI for, post foundation AI and also, different applications, scientific applications. So AI for medicine, AI for science. And recently we've been working with my collaborators at Together AI on building this mixture of agent systems.

[00:05:54] **Alex Volkov:** Yeah, mixture of agents is the thing that, I believe, not this week, but probably, last week was a little bit announced, or at least you guys released. I don't know how long you guys have been working on this. And I kinda, I think it went under my radar. And then it started kinda popping up in multiple places, and I really wanted to talk about this and learn more.

[00:06:12] **Alex Volkov:** And then, it just happened, and we pulled from together, just tagged you, I believe. And I really wanted to hear more from the folks who worked on this as well. And I also, in this vein, James, maybe a surprise for you, but I'm sorry. I didn't like tagging in this as well. I will also introduce Kyle to the conversation because Kyle, you guys have been working on something similar as well.

[00:06:30] **Alex Volkov:** James, I know you have some time restrictions, so we'll start with you and we'll love to hear from you about mixture of agents and then we'll continue with Kyle. Kyle, so feel free to introduce yourself as well. And then we'll start with James and talk here about mixture of agents.

[00:06:44] **Kyle Corbitt:** Sure, yeah. Hey everybody, my name is Kyle Corbett. I am the founder of a company called OpenPipe. We're very focused on fine tuning. and yes, we're working on something very parallel, I think, to, to what James is working on. anyway, so happy to talk about it, comparing and contrast that, yeah, after he's had a

[00:06:59] **Alex Volkov:** Amazing. Thanks, Kyle. James. So back to you. Could you give us a, yeah, let's start talking about if anybody haven't heard of mixture of agents, what is this thing? What did you guys work on? And what are some of the characteristics? What is the interesting things they need to know?

[00:07:17] **James Zou:** Yeah, sounds good. And I'm very nice to meet you, Kyle. so yeah, so the idea is that if you think about how traditional standard deep learning works, right? it comes by putting together these architectures of layers of artificial neurons, right? So layers of components where each component is a relatively simple neuron.

[00:07:34] **James Zou:** And motivated by that, now we're thinking about building more complex architectures. We still have layers of components, but each component now is not being like a simple artificial neuron, but itself could be an agent, could be, for example, like a large language model or some additional tools. And the motivation for this is that I think there's actually a lot of complementarities around different language models, so some of them are better at doing certain tasks, and if we can get them to collaborate together in different ways, then that can actually really boost substantially the capabilities of these models.

[00:08:06] **James Zou:** Alright, so that's how we end up coming up with this mixture of agent idea, you can view that as exactly like a deep neural network, but instead of having individual neurons at each layer, now each layer Each unit is actually itself like a language model [00:08:20] that can process more complex information.

[00:08:23] **James Zou:** And the surprising thing we found is that when we have this mixture of agent architecture, using just open source language models, we can actually do substantially better than the latest GPT 4. 0 across a variety of interesting benchmarks like alpaca eval.

[00:08:39] **Alex Volkov:** Okay. Beating. So let me get this straight. Other open source, and I think, you guys used WizardLM and Quen 1. 5 even, right? Not even Quen 2.they are generating, so you're not like doing any training. You're taking off the shelf open source models. You're asking them to just do regular inference, correct?

[00:09:04] **Alex Volkov:** And then,

[00:09:05] **LDJ:** That's right.

[00:09:06] **Alex Volkov:** How does the combination of that works, that they're beating GPT 4. 0, it's just like all of them generate, could you like dive in just a little deeper in the technicalities, how they're beating GPT 4. 0?

[00:09:18] **James Zou:** Yeah, so we set this mixture of agent architectures. Where, imagine each of these open source models in the first layer would generate some response to the user's queries, right? And in the next layer, each of the agents there would take as inputs, the aggregates of the outputs from agents in the first layer, and then add their own refinement and summarization to it.

[00:09:41] **James Zou:** And this process can then iterate for multiple layers. Alright, and what we see is that after each layer, the output of those agents are starting to get better and better, so that's, if we look at the final output and compare that against with GPT 4, all those outputs, that's where in the head to head comparisons like Alpaca Eval, we'll have win rates around 65%.

[00:10:03] **Alex Volkov:** And those layers, are in prompt land, so this is all inference, and it's all prompting, correct? it's all just like inference. Yam, if you have a question, jump in here, feel free.

[00:10:12] **Yam Peleg:** Yeah, I just want to stress an important point, actually two points. First that it's not a little bit better. it's not just better. It'svery much more. the score is very high. It is a notable jump in performance. And moreover, Alpaca2 is not just a benchmark. It's a really hard benchmark.

[00:10:41] **Yam Peleg:** Where I think Lama 3 gets 20 percentand the score we are talking about here is, if I remember correctly is something around,60, something like that. Yeah. 

[00:10:51] **James Zou:** Yeah. 

[00:10:51] **Yam Peleg:** so it's not just a jump in performance. it's three times. and it's a benchmark that is very hard to, you could say trick or cheat on because it's judged by another LLM.

[00:11:04] **Yam Peleg:** and Eddie does correlate to what humans think. So it's not just a benchmark, like a multiple choice question. So it's, it is a really notable jump, in performance with normal, small, weaker models you can say. So I just wanna stress this point because it's important. it's huge the way I see it.

[00:11:25] **Alex Volkov:** Wow.

[00:11:26] **James Zou:** Thank you. Yeah. That's a very useful context. And just to put the numbers, like you said, on this benchmark, for example, the latest GPT 4. 0 will get like 57 percent and our mixture of agents using only the open source models will get something like 65%, right? So it would be like quite a substantial bump above GPT 4.

[00:11:46] **James Zou:** 0.

[00:11:47] **Alex Volkov:** and then also empty bench score is 9. 25, which is also quite incredible. that's at least what I see as well. and this is, using three rounds as far as I'm seeing. Okay. and you've used, okay. And this is using some of the kind of James, we're here in ThursdAI, we're following like the latest and greatest.

[00:12:04] **Alex Volkov:** Quen 1. 5 is an older version of Quen 2 that we've already talked about. but does this need the latest and greatest model in this case? Or is it okay to even use like smaller models? could you talk about maybe it's okay to use 7 billion parameter models in this case?

[00:12:20] **James Zou:** Yeah. That's where I think it becomes really interesting and potentially very exciting. We found that, there's A lot of this phenomenon, we call it collaborativeness among even the smaller models, right? Where by collaborativeness, I mean that if you, if I give like a weak model, maybe like an older model's response, to a stronger model as guidance, right?

[00:12:41] **James Zou:** the stronger model would actually do even much better now, even if it's seen something from a much weaker model. and what that means in practice is that, the different layers that we put into this mixture of agents, it could actually consist of, weaker open source models and older models that are very fast and cheap for due inference.

[00:12:59] **James Zou:** but there's, because of this synergy, the output actually ends up being much stronger. Now, one of the big challenges then is how to actually design these kind of layer architectures, right? Because now the components of the layers are these agents themselves. And to do this, we actually also last week released this platform that we call TextGrad, which is essentially like PyTorch, but for optimizing these AI agents, right?

[00:13:22] **James Zou:** So you can now back propagate, instead of numerical gradients, but back propagate text feedback to optimize these kinds of agents.

[00:13:30] **Alex Volkov:** I would love to. Maybe just a little bit more understand this TextRoute thing. if you don't mind to simplify this for me, somebody who, yeah, what does it mean backpropagate something in, in the prompt kind of land? Maybe.

[00:13:44] **James Zou:** So it's, we think of that as exactly like analogous to PyTorch but for agents, right? So when we traditionally could have built AI systems, the signals are back propagated through these automatic differentiations and it's basically back propagating numerical gradients to update the individual components.

[00:14:05] **James Zou:** In, when we talk about things like mixture of agents or the individual components are often language models or black box tools. So we can't really update them with these numerical gradients like we would before with PyTorch. And what we did here with TextGrad is to basically, update everything through text, through natural language, right?

[00:14:25] **James Zou:** We leverage the fact that all these agents communicate with each other through natural language. And we can basically have a chain rule for, as analogous to natural language, to basically update each of the individual components. So that's basically the main idea of TextGrad.

[00:14:42] **Alex Volkov:** Wow. That's awesome. And so you released TextRoute what, three days ago, I think I added this now to the top of the space as well.

[00:14:49] **James Zou:** That's right, yes.

[00:14:51] **Alex Volkov:** could you tell me about some limitations of this that you found? I know definitely I'm thinking about. Maybe speed, this probably isn't as fast as GPT 4. 0, is it?

[00:15:01] **James Zou:** Yeah, so I think the speed of this mixture of agents is something we're working on. We're actually working on basically like a streaming version of this, right? So in the standard, like the straightforward set of this mixture of agents, you have to wait sequentially until the first layer finishes before the agents in the second layer starts to process.

[00:15:18] **James Zou:** Got it. and that's where it becomes slow. but we're thinking about how to do this in a streaming manner so that as soon as the layers in the first agent starts to generate some response, even before it finishes, layer agents in the second layer already starts to process that, and then this can substantially reduce like the time to first token,making it very comfortable to GPT 4.

[00:15:41] **Alex Volkov:** right. And,yeah, so streaming could help with speed as well. And, I'm trying to think of like how compute intensive this whole thing is, or how does one run this? Do these models have to maybe run at all times together, or could you like load and unload them? How do you guys like think about the compute intensiveness of something like this?

[00:16:03] **Alex Volkov:** Then

[00:16:04] **James Zou:** Yeah, good question. So I think the nice thing here is that because we're building this mixture of agents, where the individual components are actually relatively small and, cheap models, right? The total inference flop of a whole three layer mixed serve agent system is actually still much less than the inference flops of just doing one, one, just using one big model like GPT 40.

[00:16:27] **James Zou:** Yeah,

[00:16:29] **Alex Volkov:** 0, but for folks who, let's say, aren't even thinking about running something like GPT 4. 0,do you need to run them in parallel? Do you need, can you run them in sequence, all [00:16:40] these like individual layers or I guess individual proposers, I guess you call them, right?

[00:16:46] **James Zou:** good question. So I think definitely to get to the fastest experience, we'd run them in parallel.

[00:16:52] **Alex Volkov:** We run the agents in parallel.

[00:16:54] **Alex Volkov:** Which requires quite a few computes. So there's a few considerations there for speed and compute requirements. But the outcome looks very impressive. And also the smallest, like models, improvement looks very impressive. James, thank you so much for breaking this down. I think it's very impressive given that the results are from smaller models.

[00:17:11] **Alex Volkov:** We can get to significantly impressive results. I appreciate your time here. I know you have like short on time. Working

[00:17:17] **LDJ:** very much.

[00:17:18] **Alex Volkov:** Learn more about this and then definitely folks should follow you on Twitter. Where else, can folks, know more about this and, follow some of your work?

[00:17:27] **James Zou:** Yeah, so I'll, we have a couple of blog posts and tutorials, so I'll put that into the, into this, into the chat.

[00:17:34] **Alex Volkov:** Yes, please. And then folks, definitely give James a follow. And now I want to follow up with James. Thank you so much for coming and I appreciate your time and, great work on this. And now I want to like move to the next chapter of this deep dive with mixture of experts, mixture of agents. Sorry, not to get confused with mixture of experts, which is a whole different thing at the,at the transformer layer.

[00:17:56] **Alex Volkov:** Kyle, welcome. I've, you reached out to me and then you guys have released something today as well that's related and you guys worked in parallel as well and tell me about your mixture of agents as well.

[00:18:10] **Kyle Corbitt:** yeah, okay, very happy to talk about that. So yes, this is something we just released, this morning, about half an hour before the show, so really excited to be talking about it publicly, but yes, we've also been doing a lot of research in the general space of using more compute at inference

[00:18:24] **Alex Volkov:** I'm so sorry to interrupt, but who's we? I think that's important. 


## [00:18:29] Introduction to OpenPipe and Its Mission

[00:18:29] **Alex Volkov:** I didn't give you a chance to introduce yourself and open pipe, so please go ahead.

[00:18:33] **Kyle Corbitt:** yeah, so I work for a company called OpenPipe, actually I'm the founder of OpenPipe, and we're very focused on helping people move From GPT 4 or other closed source models to their own fine tuned models, typically fine tuned open source models. so that's the whole point, the purpose of our company is to make this transition really easy, to help you start deploying,if you're using, say, GPT 4 in production, to move to a smaller model that can be, between 20 and 50 times cheaper and still do the job.

[00:18:59] **Kyle Corbitt:** so that's what we're focused on and that's what motivated this research as well. 


## [00:19:02] Research Focus: Mixture of Agents

[00:19:02] **Kyle Corbitt:** When we were thinking about, the problem we were trying to solve, with our mixture of agents was, how can we use more compute, basically, at inference time, to get the highest cost, possible quality output, for a given response?

[00:19:15] **Kyle Corbitt:** and the reason we're interested in that is because you can then use those high quality outputs, to go ahead and, distill down a smaller model that is, very specific to your use case and performs really well. And so that's like the flow that we describe, in our own research.

[00:19:28] **Kyle Corbitt:** And the, I'd say the mixture of agents, is one, like half of the larger project. And that is Basically, how can we use as much compute as, this Prom chain, which, was through convergent evolution, very similar to what James is working on, to get the highest quality outputs we can.

[00:19:42] **Kyle Corbitt:** And then secondarily, how can we use those, to, to then, train a smaller model that, that performs well?

[00:19:48] **Alex Volkov:** So let's talk about, one and then two, right? So let's talk about one in terms of just performance. 


## [00:19:52] Performance Achievements and Benchmarks

[00:19:52] **Alex Volkov:** You claim SOTA on this task, on ArenaHard and AlpacaEvil. Is that what I'm understanding right?

[00:19:59] **Kyle Corbitt:** Yep. That's exactly right. so yes, through, yeah,we're able to get a score of 68, on the PACA eval. And then also a score of, what was it, I think, 84. 8. yeah, I think 84. 8 on ArenaHard, which is the highest publicly reported results we've seen anywhere.

[00:20:15] **Alex Volkov:** Wow, that's incredible. on ArenaHard. ArenaHard, is that the LMSys Arena benchmark or am I confusing things?

[00:20:23] **Kyle Corbitt:** Yes, that's the one that LMSys, yeah, Chatbot ArenaHard, it's the one LMSys put out, I guess a month or so ago at this point, I think.

[00:20:29] **Alex Volkov:** what I'm hearing is,if the reports, if this replicates after folks like, test, whatever, this is like the highest reported score ever on ArenaHeart? Is that what we're hearing right now?

[00:20:39] **Kyle Corbitt:** Yep, at least, I looked hard trying to find if anyone else had published anything else, but yes, I do believe it's the highest reported

[00:20:47] **Alex Volkov:** Wow, congrats. And folks in the audience, please feel free to, to check, check us on this, and check Kyle on this, but wow, dude, congrats on this incredible performance. Okay, so this is like number one, and it looks like, at least on the On alpaca eval, it looks like you guys achieved fairly similar re results, a little bit better results, but also like James, and together they achieved 65 in alpaca eval.

[00:21:08] **Alex Volkov:** So it looks like mixture of agents does get significantly better results. 


## [00:21:12] Model Choices and Methodologies

[00:21:12] **Alex Volkov:** What kind of models did you use? if you can say they used Wizard, lamb and Quin 1.5, 72 b and 102 B, what kinda miles did you use?

[00:21:19] **Kyle Corbitt:** Yeah, great question, and I want to call that out,I think that the research the Together team and, that they're working on is,really strong. I think we had a little bit different priority on our case. It was like, hey, we're gonna use whatever models are best and go for maximum quality.

[00:21:32] **Kyle Corbitt:** So we are, so we just used GPT 4. we didn't use any open source models, and we're actually very interested in the other thing as well, what is the maximum performance we can get just purely using open source models? We just haven't actually, Publish the research in that direction yet. so I think

[00:21:45] **Alex Volkov:** just to recap in my head,together MOA paper from James and together they used open source models, lower quality open source models together in mixture of agents to get a higher score than GPT 4. 0. You used GPT 4. 0 in mixture of agents, so agents of GPT 4. 0 to beat just like one GPT 4.

[00:22:03] **James Zou:** 0 also in, in AlpacaEVO. Is that correct? It's yep

[00:22:07] **Alex Volkov:** basically, like a very smart version of prompt engineering technique to get the best possible,outcome, score. Okay, that's very exciting. Okay, super, super cool. Okay, so two kind of different angles, but the method is the same. The methodology is the same, but two kind of different,use cases, maybe.

[00:22:24] **Alex Volkov:** They're using like open source, smaller. Okay. And, but the next part of your stuff is very exciting. 


## [00:22:29] Optimizing for Cost and Efficiency

[00:22:29] **Alex Volkov:** I want to hear about, optimizing and, getting this to be actually cheaper. Because I'm assuming that if you use GPT 4. 0 for multiple rounds or layers, as they call this, or maybe what's your approach to this, that's probably not very cheap and probably slow.

[00:22:43] **Kyle Corbitt:** Yeah, absolutely. first of all, our architecture is slightly different. we only use a single layer because we found that there are, like, quickly diminishing returns. but we did inject a sort of, within that layer, it's a little bit more complicated. We have, a, an intermediate step where, where the model can reason about,the proposed candidate completions.

[00:23:01] **Kyle Corbitt:** Anyway, so it's a little bit of a different architecture, but yes, I think the main point you made is true, which is it's slow, and it's really expensive, so it's about, you have three times the total latency, because we've got these three prompts, and three or four times the total cost.and for certain applications that's actually okay, like we definitely, even at OpenPipe we have lots of customers that like, quality is all that matters for them, and cost is not a concern.

[00:23:23] **Kyle Corbitt:** but that's not the case for most inference that's happening, most people do care a lot about, quality and, it's great to be able to run on your own hardware and everything as well. 


## [00:23:32] Distillation Experiments and Results

[00:23:32] **Kyle Corbitt:** So that's the second half, which is We ran a bunch of experiments of taking the outputs from this mixture of agents pipeline, which are super strong, and then distilling them into smaller models.

[00:23:43] **Kyle Corbitt:** And so we ran across four different tasks. We distilled to both LLAMA370B and then also to LLAMA380B. And we found that, in that distillation process, some of the outperformance was lost. So on our evaluations, both human evaluations we ran, and then also a larger number of LMS judge evaluations, we found That, we weren't quite able to reach the performance of our mixture of agents outputs.

[00:24:09] **Kyle Corbitt:** However, we were able to exceed, and in many cases exceed by a large margin, the performance of just calling purely GPD 4. 0, without using, the mixture of agents framework. So with, when we were still down to LLAMA 370B, On four out of four tasks, that we tried, we were able to exceed GPD 4.

[00:24:26] **Kyle Corbitt:** 0's performance. And then with our, even with our LLAMA 3 AP, which is obviously like a much smaller model, we were still able to exceed GPD 4. 0's performance on three out of the four tasks we tried. And then the fourth one, it did significantly worse.

[00:24:40] **Alex Volkov:** What was the first task significantly worse What was, did you get down to why was it significantly worse?

[00:24:48] **Kyle Corbitt:** I don't know why, the actual task was basically, summarizing, it's like a fantasy roleplay task, that one of our customers has, and, it was trying to summarize kind of these long,roleplay stories,into a shorter [00:25:00] summary, and it just,Llama 3 wasn't quite as good, even when trained.

[00:25:03] **Kyle Corbitt:** as, as GPT 4.

[00:25:05] **Alex Volkov:** Wow, alright. and you mentioned like on those tasks, besides getting 3. 4, 3 out of 4 tasks versus GPT 40, it's 25x cheaper, which is quite ridiculous. Yeah.

[00:25:16] **Kyle Corbitt:** Yeah, so that's the really key thing is, there's a couple of key things. One is, yeah, the price difference. and you're talking 125th the cost per token. also, latency, these smaller models, just by their very nature, there's less compute involved. And we're seeing, about one third the latency.

[00:25:29] **Kyle Corbitt:** And then these are things you can run yourself, right? this work was all done through OpenPipe through our platform, but like when you train a model through OpenPipe, you can just export the weights. you can run inference locally or on any other inference provider. And so it gives you just a lot more control of how you do that.

[00:25:43] **Kyle Corbitt:** Yeah, we

[00:25:44] **Alex Volkov:** That's great, man. congrats on your work and I'm really,excited to have the folks who actually, announced the thing. breaking news from today and thank you for, letting me know that you're gonna, talk about mixture of agents as well. So we had, a twofer, a mixture of agents, the paper from folks at,together, James and the folks are together and also the additional, you mentioned that you started with something else and mixture of engines is makes sense because it's a similar thing as well.

[00:26:06] **Alex Volkov:** will you be

[00:26:08] **Kyle Corbitt:** the name because it seemed like the architecture was very

[00:26:10] **Alex Volkov:** Yeah. what's next on this? 


## [00:26:12] Future Directions and Productization

[00:26:12] **Alex Volkov:** I think I saw you're also like, you productizing this. Is there like a publishing flow or are you probably straight to production? what's, what's next? Where can people learn more about this? Where can they use this? what's going on? Is this open source, not open source?

[00:26:25] **Kyle Corbitt:** yeah, so learning more, yeah, we have a tweet thread, we have,like a blog post you can look just on the OpenPy blog. I would say,yeah, the architecture is, it's fully open and frankly it's pretty simple. it's basically like you could mostly build it from what I've already described here and certainly from the tweet thread.

[00:26:40] **Kyle Corbitt:** it's not like a separate open source library because it is pretty deeply integrated into, our flow. but basically, yeah, within OpenPipe, we're using this already in a number of different surfaces. We do,we provide it as, just a drop in replacement for the OpenAI chat completions API.

[00:26:53] **Kyle Corbitt:** So you can just hit it with, your messages and tool calls or whatever way you would OpenAI and just Get a higher quality response, and then we also support it, basically, within OpenPipe, we have datasets, all this stuff you need, for fine tuning, and so we also support it, if you have an existing dataset, or messages that you have been getting from OpenAI, you can upload them to our service and automatically relabel them with this, just to get those higher quality completions, and then, of course,fine tune a model on top of it.

[00:27:18] **Alex Volkov:** That's great. So congrats on this release and folks definitely should follow Kyle. one thing that I will say, and as I continue to the next thing, thanks Kyle. Both Kyle and I are going to talk on stage next week in San Francisco. So we'll do a high five at the ai. engineer world's fair. I don't know when you're flying in.

[00:27:34] **Alex Volkov:** I'm flying in on Monday. And, will you be covering this there as well?

[00:27:39] **Kyle Corbitt:** yeah, we'll definitely be talking about it there,yeah, anyone who's there, definitely, look me up, message me on Twitter, say hi, we'll Happy to, excited to meet a bunch of folks.

[00:27:47] **Alex Volkov:** Amazing. Thanks for the deep dive into Mixture of Agents, James and Kyle. Kyle, we'll see you next week as well. 


## [00:27:52] Open Router interview with Alex Attalah [00:27:52] Interview with Alex Atallah from Open Router

[00:27:52] **Alex Volkov:** All right, welcome Alex Atala to ThursdAI. I think it's your first appearance here. It's been great like following you around. I think I followed you way back when from the OpenSea days. please feel free to unmute yourself and introduce yourself to this audience, because it's your first time.

[00:28:15] **Alex Volkov:** And then we're going to chat about some interesting things you're working on lately.

[00:28:21] **Nisten (2):** Sure. Thanks, Alex. Thanks for 

[00:28:22] **Alex Attalah:** having me. 


## [00:28:23] Introducing OpenRouter: A Unified API for LLMs

[00:28:23] **Alex Attalah:** I'm a big fan of the space, and I,CEO and Co-founder of Open Router, which is a router for LLMs. And, before that I was the co-founder and CTO of open C at the first NFT marketplace. And, started that in 2017. And before that I had a couple small startups, one.

[00:28:47] **Alex Attalah:** NLP thing called Apollo, where we were mostly doing sentiment analysis in 2014 and 15 on user provided reviews for video games and for, other content.products that kind of have early releases that a couple people are able to play with before they hit the masses. And at that point it all basically felt like BS compared to, the tech we work with today.

[00:29:14] **Alex Attalah:** So it's pretty exciting to have,to just see everything that's happened in the last, two years. And.and and every day something crazy happens. It's just like a wild rollercoaster.

[00:29:28] **Alex Volkov:** Absolutely. So thanks for coming up. And, I've been I think following you from the, And then I think when I started actually noticing your, I don't know if transition to call it, but definitely like more interest was around window. ai, which was reminding me of what Metamask is.

[00:29:46] **Alex Volkov:** if folks never heard about window. ai, could you give like a brief thing of what it was and like, what were you trying to solve there?

[00:29:56] **Nisten (2):** Yeah, 

[00:29:56] **Alex Attalah:** so this was like the first sort of public experiment I worked on when I, started playing around with AI stuff at the end of 2022, early 2023. And, it was a Chrome extension. It's still, it's, it is, it's, still functional and it basically lets you use your AI models or your choice of model in web apps that directly interface with it.

[00:30:24] **Alex Attalah:** Instead of calling an API themselves.so there were, there was one major problem that it was built to solve that was in the short term. And that was all of these projects that kept popping up. Do you remember like the end of 2022, early 2023, everybody was making these bring your own key, or really like short lived indie projects

[00:30:46] **Alex Volkov:** Mhm.

[00:30:47] **Alex Attalah:** that was GPP three, two.

[00:30:50] **Alex Attalah:** make a cron job, or use, there were some little games like Turkish Carpet Salesman, where you try to, convince,And then there was a guy to buy the carpet for as low of a price as you could,

[00:31:01] **Alex Volkov:** To prompt engineer him into giving you a free car fit. Yeah.

[00:31:04] **Alex Attalah:** 4. Yeah, pro yeah. these projects were not sustainable. They're really fun.

[00:31:09] **Alex Attalah:** but like the person, the people making them just had such high margin, or such high overhead from AI costs. And what people, to make them sustainable, to make them actually stay up, they had to convert them into bring your own key setups, where you like paste in your OpenAI key.

[00:31:28] **Alex Attalah:** And that also wasn't sustainable, because, I don't know if you remember this, but, and it was still the case now, when you like sign up for OpenAI, it won't give you access to GPT 4, and your rate limits are really bad until you build.a little bit of reputation with your credit card. Now they've switched to credits.

[00:31:45] **Alex Attalah:** So things have changed, but it's always been a mess tobring your own key somewhere, and we tried to fix that by letting, first, making a way for people to choose the model. So if you have a really good setup somewhere, And a website just wants to use AI wherever it comes from. The site can just call window.

[00:32:09] **Alex Attalah:** ai. generateText and the Chrome extension would inject this, provider into the webpage. This is how MetaMask works with, Web3 apps. you get this injected object with functions on it, and web apps can call those functions. And that means they don't have to be dependent on any APIs, so you can create, a fully decentralized app on IPFS, for example, that doesn't need any backend at all, and it can just, use this frontend standard.

[00:32:38] **Alex Attalah:** so that let people use local models. The earliest was, Alpaca, running locally on web apps for the first time, I noticed. And, and then. But we realized, people really want to use larger models, and, and people really wanted to try out things that, Anthropic was developing, so we built OpenRouter as a unified API to access all of these things without worrying about rate limits.

[00:33:06] **Alex Volkov:** So just before we get

[00:33:07] **Alex Attalah:** the major thing.

[00:33:09] **Alex Volkov:** Sorry to interrupt, but I really wanna like focus on window edge, just like recap, because I found it super interesting. Meta mask is meta mask saves me as a user because like the, I'm basically the backend, right? there's the front [00:33:20] end, the runs, whatever. And then meta mask is on my browser.

[00:33:23] **Alex Volkov:** And this is the same idea for LMS as well. Instead of me pasting my token, God knows where the developer that created this app, sends it on their backend, saves it, whatever. I basically have a secure way to provide my own LLM. That also could be like GPT 3 that the developer intended, right?

[00:33:38] **Alex Volkov:** And then you like the developer basically interacts with my, whatever LLM endpoint via kind of a proxy. And what you're saying is, and I didn't connect these pieces until now, that in order to build this, you had to build like a unified way to call LLMs, which then is now basically open router. Is that, am I understanding this correctly?

[00:33:58] **Alex Attalah:** Didn't need to build that. ended up building that to help people with, basically, with rate limits and with LLM discovery. and to help with like new open source models that are coming out, but it's just too hard to run yourself locally.but Window AI works with your own OpenAI API key and, your own Entropiq keys and CodeUnit keys, et cetera.

[00:34:20] **Alex Attalah:** It just, it, like the onboarding was really difficult for apps, like an app that like integrated Window AI, for a really new user and to teach them, you know, oh, we need to go get, You need to set up a new AI yourself, and configure your keys in the Chrome extension and then you're good to go.

[00:34:39] **Alex Attalah:** So the, so OpenRouter was just a way of skipping that whole step for apps.

[00:34:44] **Alex Volkov:** Awesome. So now let's talk about OpenRouter because I think it's like very exciting. And I will say OpenRouter,maybe let me ask you, how do you present OpenRouter to folks? And then I can like chime in what I found exciting about OpenRouter and why I called you here.

[00:34:59] **Alex Attalah:** We try to present it as a way of discovering and trying out new models that emerge. it's like the primary, goal. So you land on the page, we show you trending models that have been getting more action over the past couple of days. we show you an app leaderboard for all the apps that opt in to sharing their statistics.

[00:35:22] **Alex Attalah:** and then you go to the rankings page, openrouter. ai slash rankings, and you can see all models ranked by how much they're used, and including, Fast growing ones. So if you go to that now, you can see like LLAMA3 Finetunes ranking really high. LLAMA3 Instruct 70 billion Nitro ranking pretty high.

[00:35:44] **Alex Attalah:** and then it helps, it like lets you explore what model, how much models are being used and which apps are using them and what kinds of apps those are. we're aiming to develop this a lot further to show you like, What categories of prompts, different models are really popular with and how like high retention users are with certain models for certain kinds of use cases.

[00:36:08] **Alex Attalah:** the other thing that we do is we try to help developers, with a single API that lets them access way more models and, automatically reroute requests that fail for a certain provider.


## [00:36:25] Challenges of Scaling AI Models

[00:36:25] **Alex Attalah:** for new models, especially, most model, most providers just under provisioned them. And there's a lot of crazy traffic.

[00:36:33] **Alex Attalah:** It's really difficult to load balance this traffic. batch sizes, like batch depths change for if you're running an inference engine so quickly. And it's really hard to know whether you can like, sustain a bunch of traffic coming in. And it's also really slow to scale up. So it's not like Google Cloud, or.

[00:36:55] **Alex Attalah:** with CPUs, where you can scale up really quickly and cheaply, it takes a bit. 


## [00:37:01] Innovations in Load Balancing and Model Discovery

[00:37:01] **Alex Attalah:** what we do is we try to,now we have a lot of,a lot more work around load balancing. And, the provider is showing some degradation. we load, we reroute requests to fallback providers.

[00:37:12] **Alex Attalah:** And, we also do a lot of feature routing. if you're trying to get Rarer features, samplers, for having more control over your replies. Then we route you to providers that support those features because they all support different subset of VLM features and, some custom ones.

[00:37:29] **Alex Attalah:** basically, TLDR, Model Discovery, and,like a better universal API for hundreds of models.

[00:37:37] **Alex Volkov:** I want to focus on the, thank you for that's definitely like a clear explanation. 


## [00:37:41] Universal API and Model Support Enhancements

[00:37:41] **Alex Volkov:** I want to focus on the universal thing. So I think maybe you guys are one of the first folks who took advantage of this, OpenAI SDK feature where you can provide the different URL and basically instead of going to OpenAI This would go like to a different thing and then standardize around the OpenAI kind of standard message format standard Which we then saw natively get supported by other folks like Grok when they came out They supported this like almost natively and now I think they even prefer this and I think even Entropic has their own SDK, but, Entropic also switched, the messaging format as well.

[00:38:15] **Alex Volkov:** Just for folks who, don't develop with these apps, or maybe don't remember, previously,every, way of interacting with these models, with these, big providers, but also small providers, was, like, every way was different. and so you guys are, like, you have your own way of interacting with OpenRouter, but also, it's a drop in replacement, which is, changing one line, And for folks who like previously work with GPT 3 for at least the messaging completion API.

[00:38:36] **Alex Volkov:** and I think that's like super cool because it does let a developer like me to very easily like switch between different models. can you tell me if you guys support some of the more advanced stuff that they have? Vision recently, like all these models became like,VLLMs, etc.

[00:38:49] **Alex Volkov:** Uploading files or even like the more advanced stuff, like the assistance API, for example. 


## [00:38:53] Multimodal Model Support and API Standardization

[00:38:53] **Alex Attalah:** Yeah, we, we support multimodal requests now, for multimodal models, you can attach images to requests. and basically what we do is, we, every, Anthropic and Gemini and OpenAI all have different APIs for accepting images and for sometimes for just doing the messages list, and we normalize around OpenAI's interface, and we convert to all the other interfaces behind the scenes, and the same for streaming requests, we like make everything look like, an OpenAI streaming response.

[00:39:31] **Alex Attalah:** And we found that, yeah, it definitely significantly eases integration efforts, but also makes it a little, just, less. Burdensome to switch your model and to try out new ones. And we really think that the future is going to have thousands of models that all, like a lot of them would be just very good at like niche unique things, like Mistral large is the world's best French model.

[00:39:55] **Alex Attalah:** but are you going to, what are you going to do about that? Are you going to have a, like whole new code base for calling Mistral? That like only applies for, French users when something's going on in your app. it makes sense. I think most, have, really clean code.

[00:40:13] **Alex Attalah:** That's just all oriented around one standard and really credits go to OpenAI for this. Like ChatML is really good. it's like great foresight on their part for helping like normalize the prompting of models and they weren't even making crazy prompt formats, but ChatML was like a simple and straightforward enough format that it you can make it work 

[00:40:39] **Alex Attalah:** with 

[00:40:39] **Alex Attalah:** crazy prompt formats.

[00:40:40] **Alex Attalah:** There's a ton and Allama 3 introduced a new one and but no one needs to know or worry about those formats if they can just use the same API all the time.

[00:40:53] **Alex Volkov:** so question for you as a follow up for this. So you basically OpenRouter is a proxy for the hosted models, but also like open models. who can? 


## [00:41:04] Marketplace Dynamics and Provider Selection

[00:41:04] **Alex Volkov:** who decides on which backends you support is that you guys, or can, I don't know, like together, whoever else,apply to also be there. You're basically like functioning after a lot of people like start using this is basically functioning as like a marketplace for LLM calls or tokens, essentially.

[00:41:19] **Alex Volkov:** cause you make it very easy to switch, which I find like very good for democratization. but then also,who gets to participate in this marketplace? could you speak about like how the, that process happening?

[00:41:31] **Alex Attalah:** Yeah, so we've been, we started. Very conservative with the suppliers of the marketplace, with just a [00:41:40] handful, like OpenAI and Thropic together and, Google and Mistral. And we've been expanding it and changing our thinking as we go.now you can see more indie, inference companies appear on OpenRouter.

[00:41:57] **Alex Attalah:** We just added Novita and a new one called Win that is just for one model that, like one Llama3 Finetune that the model creator's been working on. And they made it CCNA4, so you have to get permission to host it, but, like his idea is that, I think, like he wants to create a business around it by being an inferencer and just using OpenRouter as a distributor.

[00:42:26] **Alex Attalah:** So that's where we've seen like our value appear the most is that in helpingget distribution and improve the developer experience for a really large number of inferencers that are also going to appear in the future. So now we have 24 or so different companies that we help distribute for and what we do is we make sure that they're.

[00:42:49] **Alex Attalah:** Running the actual models. They say the others, yeah, it's somewhat of a trust basis right now until we have zero knowledge proofs working for AI models and,we're sitting on the hopes that's coming, but we just don't know when. And, and then we're gradually like improving our tooling and, tolerance for new providers by building like Increasingly better load balancing tech to help us reroute when a provider starts to get slow or go down.

[00:43:21] **Alex Volkov:** So that's my next follow up because I'm looking at some of the like top this week, top this week model you have Entropic Cloud Haiku and it's a self moderated, which I would love to ask you what that's about, but, if a developer doesn't necessarily plan to maybe change the models, I think what you're just presenting as a good idea of like why use Open Router instead of like directly Entropiq.

[00:43:42] **Alex Volkov:** but don't you get like rate limited by Entropiq on behind the scenes? cause you're essentially, by you, Open Router, it's a reseller of the service essentially, right? Because I basically provide credits on your platform and then you're providing credits like behind the scenes to Entropiq.

[00:43:56] **Alex Volkov:** did you get like rate limits, from those platforms enough that you start to Fall back to different providers, different ways. tell me more about kind of the struggles of building something like this while the platforms themselves, maybe don't know how to scale very well.

[00:44:10] **Alex Attalah:** Yeah, so I mean we also get rate limited, but we handle these rate limits by falling back toother providers really quickly, so that developers don't have to like, worry about that at all. They're just trying to build your app, not worry about fallbacks. And,like a provider like OpenAI is a fallback to Azure and you can just, like Azure doesn't have all the open AI models.

[00:44:37] **Alex Attalah:** That's probably the biggest, strain, is that if we get like a surge of traffic to a new model. doesn't exist on Azure, we will, we'll be limited in whatever negotiated, rate limit we have with the main provider.so we're working on that, and I, it's a tough problem, so I see, a bit more, a clearer path forward for open source models, or if we're, if we get rate limited by the best two providers.

[00:45:08] **Alex Attalah:** it's pretty easy for us to fall back to the others because there's a ton of the, there's a lot more, basically market depth. It's like a normal marketplace where, like a surge in demand for some,fungible product, you, you need like a, you need like a deeper order book to serve it.

[00:45:28] **Alex Attalah:** So basically we're hoping that for, models or, for providers like OpenAI Anthropic, the order book will grow, with partnerships that they do with Azure and AWS Bedrock. And, and we can just keep pushing upwards the amount ofthe maximum depth we can get.

[00:45:49] **Alex Volkov:** so you're behind the scenes, you're going to just go to AWS, go to whatever Entropic kind of sells their services and for developers on your platform, even if Entropic kind of rate limits or goes down, the experience we're using OpenRouter is going to be seamless because that's what I'm hearing, which is awesome.

[00:46:05] **Alex Volkov:** we're aiming for, yeah.


## [00:46:08] Enhancing Developer Experience and Model Discovery

[00:46:08] **Alex Volkov:** I want to follow up about like the charts that you have. So one of the outcomes that you have there is analytics. And I saw, I think recently as we were deciding to speak with you about this. and I'm very happy that you came on because I really like the idea. I want to expose this to more folks specifically because.

[00:46:22] **Alex Volkov:** for example, because of the drop in replacement for the OpenAI API, people have been using OpenRouter models or models that like exist on OpenRouter, doesn't exist elsewhere, in some tools that support this as well. And tools support this because, enterprises can, decide that they're not going to OpenAI, they want to go to Azure.

[00:46:40] **Alex Volkov:** So like that feature in OpenAI API that lets you access like different URLs is basically like for Maybe started with maybe Azure, but now like open router, like plugs neatly into this. And so this now lets me to try something else besides OpenAI. So for example, for Cursor or for like other models or other products that allow me to access OpenAI stuff, I can go directly to OpenRouter and try Mistral or try, this next thing.

[00:47:04] **Alex Volkov:** And so model discovery now becomes important. so one thing that I just noticed that I haven't heard before that the top model this year on your, on the OpenRouter platform is Mitho Max 13b. And we're, we're reporting about models every week. I have never heard about this one. Was that like a surprising outcome of running this, or did you guys plan on like also surfacing and discovery as well? And also, yeah, sorry, go ahead.

[00:47:34] **Alex Attalah:** Mithomax is a really interesting one. It's a, it's a merge of several models. It's a merge of merges, based on Alma 13b. I'm a 2. 13b, and the, it was like one of the earliest, it's called like a Frankenmerge, where you take two models and graph them together, and you get a lot of the abilities of both.

[00:47:58] **Alex Attalah:** it was one of the first big successes, and when it came out, we noticed that it was really good at role play, and it was getting really good feedback from, the local LLM community that was trying it out locally.so we added it, and it just beca it started to become like the best brand for, for roleplay use cases.

[00:48:19] **Alex Attalah:** it's not censored, and it turned out to be pretty well hosted. A lot of different companies added support for it, so we, had a deep portfolio and really good rate limits as a result. and it's just, it, I think it came out in July of last year, so It's been around for quite a while, maybe August of last year, and the, and it just surged.

[00:48:47] **Alex Attalah:** we're like, it may get dethroned in the near future. I think it will likely get dethroned with something based on Mixtral or LLAMA 3.but you'll see that, if you go to the apps under Mythomax, it's primarily roleplay use cases that it's really good for.

[00:49:04] **Alex Volkov:** I've never heard about this model, but like the discovery feature of this is like super cool as well. and also just the kind of the volumes that you process. I think you posted recently that you just passed, 60 billion, is that? Like the graphs are insane, the growth as well in usage of this.

[00:49:20] **Alex Volkov:** And I guess the discovery of who uses them. I think it's a big one. So I definitely saw that, friends of ours, Nous Research, they came like to the top of the leaderboards there with WorldSim for a while. can you tell me about do you discover like new cool use cases for LMS just because people use them on, Opera Router or is this another aspect of this marketplace where like actually use it?

[00:49:40] **Alex Volkov:** Cause you have like multiple aspects. You have the developers who use the tokens, providers who provide different like providers provide the same models. You spoke about open models being. better for this use case because then they can get cross hosted about like everybody can host them as they want But also you now have apps that use them.

[00:49:56] **Alex Volkov:** So you have a multi faceted marketplace where you find [00:50:00] Fascinating. Talk to me about the application side of this like how we see who uses them How do you know if that do I have to expose my app if I use open router? I would love to some clarity over that

[00:50:12] **Alex Attalah:** Yeah, the apps are one of my favorite parts about this. No, you don't have to expose your app if you use OpenRouter. You just don't include a, a header, the XTitle header, and we won't show your app up in the showcase. but for people who do, it's a really good way of getting exposed and letting people discover you.

[00:50:30] **Alex Attalah:** We, we tend to refer a lot of users, right from our homepage that way. But but it's also just one of my favorite parts. We, I discover like crazy stuff all the time by looking at, fast growing apps, that everyone can find straight on the homepage. one that I'm particularly excited about that's been in the top.

[00:50:51] **Alex Attalah:** Like 10 or so for the last week is WebSim, which lets you simulate. The web using a simulated browser. I think it's ranked eight right now and it, you can like, just go and make up a website that doesn't exist or make up a website that does. And it will like, it mostly I think uses cloud three behind the scenes and generate the webpage that it thinks is at that URL.

[00:51:16] **Alex Attalah:** And it can go look up your name, see what it generates for you or for your company that you work at.generate the links to things that it thinks might exist. It's really fun and there's a lot of stuff like,infinite Worlds is, trending now. different kind of UIs for, for role play.

[00:51:37] **Alex Attalah:** Vox does cool, it's like a speech driven AI companion that you can talk to and has a 3D model for interacting with. So all these, this, rich app, AI app experience, I've always wanted, a place where I could just discover cool things by the metric that, by a metric that I just hadn't seen anywhere in the AI space, which is, how much is it being used, really?

[00:52:01] **Alex Attalah:** And, like, how, is this, what models is this usage actually happening on? So we try to help users answer these questions. Developers who want to expose that stuff, give them a place to expose it, and get traffic.

[00:52:16] **Alex Volkov:** I think the fact that you're exposing and then it brings people traffic is like very cool as well. WebSim is definitely, we haven't talked about WebSim. I think it's an outcome of a hackathon in San Francisco. and I don't remember the guy's name, but I know Rob maybe? Yeah, Rob, Rob something.

[00:52:29] **Alex Volkov:** and WebSim is like very interesting how fast it took off and how much people love like to just like generate websites. Rob Hatfield maybe?Yeah. So Alex, like on the top of the app showcase, the fact that you're sending traffic is really cool. what are your plans for the kind of the app discovery aspect of this?

[00:52:46] **Alex Volkov:** Cause like you're saying you're enjoying like discovering yourself, you're sending traffic, this could be a lot more to get built there because people actually see what other people use. what are some plans around the app showcase?

[00:52:59] **Alex Attalah:** It's really simple. it's just descriptions, names, and favicons, basically. so we wanted to, we're thinking about building that out. A request that we get really frequently is just being able to see more than the top 20, apps per day or apps per week. and on models as well.and another request we get a lot is just, it's not super app related, but seeing like the cat, like basically category breakdown, for a model, which categories of prompts are really trying to make the most.

[00:53:32] **Alex Attalah:** And, for a given category, like role play, what are the best models? tentative plan, and, this is like halfway built right now. It's to build a really good roleplay ranking on OpenRouter because roleplay has had just a tough time getting, I think, a definitive way of ranking models for it.

[00:53:52] **Alex Attalah:** And because it's a bit arbitrary, it's hard to make an eval that actually, doesn't get consumed by fine tuning for it. And so there's no trusted eval for it. There's some ELO based rankings for roleplay, but it's it's hard for me to grok. And some of the models are,I just don't think anyone uses the models that get ranked in some of these.

[00:54:16] **Alex Attalah:** we're trying to build a much better roleplay ranking and then have the, apps get distribution in all of these things. whenever you see,we want apps to get discovered as much as possible because it's just one of the richest parts of

[00:54:33] **Alex Volkov:** a follow up that's sidestepping the apps use case, but for developers of apps. So a lot of these, and I assume for a lot of these, I don't know how many of them are businesses, but a lot of these are like, like Sealy Tavern, for example, I think it's open source and other places that are open source.

[00:54:47] **Alex Volkov:** Like it makes perfect sense to, OpenRouter and just tell people, Hey, register on OpenRouter with your own API key and provide this here. Like it makes sense for them to also to be able to switch between models as they come out. Yeah. And we also. We follow with every model that comes out. We talk about this on ThursdAI.

[00:55:02] **Alex Volkov:** And it's really cool to see like how fast OpenRouter updates them as well. for the more business and enterprise use case, potentially, you're basically a router for all tokens and all information as well. And then the question of security comes up. And the question of do you see the data comes up and all of these things.


## [00:55:18] Security and Privacy in AI Model Distribution

[00:55:18] **Alex Volkov:** Could you talk about that aspect of how you treat this, especially coming from the decentralized crypto space and like your first thing you talked about here was metamask was like,and window AI was like fully on my end and no servers exist, et cetera. could you speak about that aspect and how you think about like the security and the fact that you are handling potentially sensitive data that goes between you, the user and the eventual kind of entropic or open AI, et cetera.

[00:55:42] **Alex Attalah:** Yeah, it's a good question. first of all, we, we have a little checkbox that you can check on your account page for OpenRouter on whether or not you want to share. Gromps, with OpenRouter, which we pay you for, like you get a 1 percent discount when you do. We just believe that like user data is valid, it can be valuable and you should get compensated in some way.

[00:56:09] **Alex Attalah:** And, and we only use that data to to to build our auto router. Automatically picks a model for you, based on your prompt, and, and also to, help you discover new models based on a certain category of prompt.the underlying providers themselves, they're, it's pretty crazy.

[00:56:29] **Alex Attalah:** This is really different from crypto in general, you have to read the terms of service over and over again for all, the AI providers to figure out, What they do with your data, how long it's stored as a log, whether it's logged just in flight and memory or stored anywhere, if there's a retention policy on it, and it seems to vary pretty widely.

[00:56:54] **Alex Attalah:** We found that like almost all providers, seem to take it pretty seriously when they don't train on your prompts or your data. For providers that do think they might want to train on prompts. we pretty much always find that they are willing to discount prices for it, so we shift the discount fully to users if that happens, and we let users opt out of those providers completely.

[00:57:22] **Alex Attalah:** So you, just uncheck that one thing on your OpenRouter account. All those providers disappear.

[00:57:28] **Alex Volkov:** I'll just say users here, you mean users of open router, like developers, not the end users

[00:57:34] **Alex Attalah:** yes, developers. Developers, yeah. But, yeah, so like the users, it's both. Yes, like prompts that are sent to OpenRouter that get routed to these AI providers. the AI provider usually has a way of opting out of data collection. And we either turn that on by default, if there's no price differential, there's no data collection, or we let users, get rid of that provider.

[00:58:04] **Alex Attalah:** if they don't have it, why should it happen? And then there's, some cases, like OpenAI, where they'll, they store props for 30 days, and, basically we just try to, find this information, find links about it, surface this in the [00:58:20] provider's list, the seller's list for a model, to just help developers do research on it.

[00:58:25] **Alex Attalah:** So it's like a,We're trying to make it a better central location for privacy related info, and it's a do your own research, solution right now. We're very open to feedback about it.

[00:58:39] **Alex Volkov:** Yeah, that's, I think that's very important, especially given that,the kind of the end users may not necessarily like know about this and whose job it is to actually like reply and who actually stores the prompts in the middle. Definitely very interesting. There's a bunch of models that are 100 percent off that you offer for 0.

[00:58:57] **Alex Volkov:** Could you walk me through the business case of this? Because obviously, like we know, just like an aside here, we know that Chachapiti is now open, 3. 5 is free, even without registration. I think many models, when they come out, they want like RLHF. They want the, people to like vote, et cetera.

[00:59:12] **Alex Volkov:** I don't believe that you have any of that algorithm. Like I, but maybe correct me if I'm wrong, but I haven't seen any, Feedback that I as a developer can provide open router and say, Hey, for Myth or Mist, which you now offer for free, this prompt work better, this prompt work worse. so walk me through the a hundred percent discount model usage, which is very interesting.


## [00:59:32] Free Model Access and Business Strategy

[00:59:32] **Alex Attalah:** Yeah, we really wanted to give people a way of trying out models for, free when they sign up. I just really believe in the, try it before you buy.mentality, or at least ability for a new product that's emerging like we are. And, so I think like many months ago, we started offering a couple of models, a hundred percent discounted.

[00:59:59] **Alex Attalah:** And, most of these are 7 billion parameter models. So they're lower costs to run.and we basically pay the providers in full for them, but we just take the loss. for people trying them out, and our thinking around them is that they're pretty heavily rate limited. they're called free variants, so if you go to a model page, if you see a little free button on it, you can go get like a more rate limited version of it, and you can just go around with it for free.

[01:00:33] **Alex Attalah:** our thinking is that the loss that we take is made up for in the future. the, 0. 6 ish percent fee that we have when we add credits and,the volume discounts that we get from providers that we split with users.so it's not a loss that I think,drives us in the red. we think it's, an acceptable, thing to give and, we just, we try to add new free variants for interesting new models.

[01:01:01] **Alex Attalah:** last one we did was Gemma, I think. And for COPY and MIFIMIST that are, like, pretty popular with certain kinds of use cases.

[01:01:11] **Alex Volkov:** Yeah,I definitely see that. I see like joining an app, especially as a developer, joining a provider is Hey, Most of them, together gives 20 bucks for free, etc. most of them give something out, because even just building with this, I don't want to put up a Quaker straight up.

[01:01:24] **Alex Volkov:** but I definitely appreciate this. Last, Alex, last question before I let you go, and thank you so much for coming here. Obviously, with your background in OpenSea and crypto, and like that ethos, you briefly mentioned something about zkproofs, the ability to know which model runs actually, which provider runs which model, and actually runs it.

[01:01:42] **Alex Volkov:** could you give me more of a glimpse of like how you see those kind of two, Areas kind of joining being like very prominent in the previous one as well. 


## [01:01:49] Future of AI and Crypto Convergence

[01:01:49] **Alex Volkov:** do we see a convergence point going forward in some of the more distributed, decentralized and zero knowledge, like areas to, to join this AI area where like my data is very interesting, but also provenance of data that was used to train these models is very interesting.

[01:02:02] **Alex Volkov:** where you're like got currently lies in like the inflection between AI and crypto.

[01:02:10] **Alex Attalah:** Yeah,There you go. The big limiting, I think the biggest limiting factor right now for decentralized AI is that you don't know what model someone is running for a, in a decentralized system and you can, you can read them based on their replies, you can have a, a voting system, but no, no AI model, I think,is good enough to get good boats all the time.

[01:02:38] **Alex Attalah:** if you're really running Lama 3. 8 billion, you're going to get lots of bad boats, even though you might be running the real model.and there's just I just think there's quite a lot of difficulty in setting up a good decentralized system right now without proofs. That's not to say it's a bad idea to try.

[01:02:59] **Alex Attalah:** There's a lot of, really promising protocols coming out that,potentially are more fierce than ritual. And our thinking is that we want to focus on distribution and load balancing. We think that those are pretty underrated, but massive problems. And we think that solving those problems really well, now We'll work, we'll mean, that we can just route traffic to decentralized AI, protocols when they're ready.

[01:03:29] **Alex Attalah:** When they're, when it feels like, oh, maybe you have a ZK proof, you can prove that you're running a model, efficiently and quickly for every output. Then suddenly everybody can like quickly spin up a provider on OpenRouter through, protocols that work well. And, our load balancer will only give them traffic that they can handle. Does that make sense?

[01:03:52] **Alex Volkov:** Yeah, absolutely. so we'll definitely, we'll wait and see the convergence of this. There's a bunch of issues, but hopefully, at least some more around the privacy stuff will get solved. some use cases, as well. Maybe last thing, although I promised you already a last thing. the name OpenRouter.

[01:04:10] **Alex Volkov:** what is the open aspect of this? And. Yeah, could you talk about like the open aspect of this or is this like open AI where they start with open and then like pivoted?

[01:04:23] **Alex Attalah:** Yeah, so our initial thinking was that we wanted the, it, it was open router because we were adding the open source models, and it was going to be like the best way of, accessing open source models in one place across lots of providers. We also then made an open source influencer. So open router, fun fact hosts a bunch of models.

[01:04:47] **Alex Attalah:** and it made A-B-L-L-M based set up and open sourced it, and, just been like building it out gradually.and what our thinking is that we, we wanna open source more chunks gradually.especially ones that dive deeper into, AI inference and,and help providers start businesses and improve the businesses they have.

[01:05:16] **Alex Attalah:** Linn, I think, is a really cool example. They're not, I don't, to my knowledge, they're not using our open source repo. But, they've just set up their own inferencer, they're incorporating, they, they fine tuned LLAMA3, extended it to 24k context, which is awesome, they made it, better at roleplay, they've been getting a lot of traffic, they use OpenRouter for distribution,

[01:05:40] **Alex Volkov:** Could you say their name again? Sorry. just for the record. Lynn if you go to,LLAMA3 Soliloquy, AP, Soliloquy, but if you go to the rankings and look at, the fastest growing, Model right now, it's Soliloquy by Wynn and it waits around hugging face.

[01:05:57] **Alex Attalah:** like the key is that, it's, this is like a, someone who just fine tuned it and wants to make the API for it too, and actually like. Use another service or find GPUs, lots of different ways of doing that, and just, leverage OpenRouter as a distributor. So I'm a big fan of that approach, and we want to open source tech that just helps people do that more.

[01:06:20] **Alex Volkov:** That's awesome. so Alex, thank you so much for coming up. I, am a fan of OpenRouter, specifically the ability to like super quickly switch between different models for other use cases, like Cursor, for example, and like other things, but also the app exposure. I think it's like super cool to just see apps that I wouldn't have otherwise checked.

[01:06:37] **Alex Volkov:** And the follow up as well [01:06:40] in the vibes check category, which is how we evaluate whatever models, we follow from week to week, we see all these models, we see the regular evals that everybody runs automatically. But one very important, vibe check is like how many people are actually using them and where and which apps.

[01:06:55] **Alex Volkov:** so it's a great way to to use that. Obviously it's restricted to the people who only use OpenRouter. but still seeing highlights of the open source, like ranking, like Lynn, for example, is very interesting as well. So thank you for coming up. Anything else you want to plug or leave before you go?

[01:07:09] **Alex Volkov:** definitely the stage is yours. Feel free to, to say anything you want and then we're gonna follow up with a bit more news and then we'll let folks go.

[01:07:19] **Alex Attalah:** Yeah, I,WorldSim and Lin, I figured, both, two cool things to check out. once again, it's like a really interesting app that, uses multiple models and,but, builds like a unique user experience. We really want to enable more of those. 


## [01:07:34] Exploring New AI Applications and User Experiences

[01:07:34] **Alex Attalah:** Those just aren't that many great user experiences that have been built, direct to user experiences that have been built on top of AI so far.

[01:07:42] **Alex Attalah:** And, we really want to make those easier to make. we, we, oh, yeah, I didn't mention, we have, an OAuth system that some apps use, like NovelCrafter uses it really well, so that you can, not pay for AI at all, but build an app. That's direct to user, that users, sign in with Open Router, and then they get access to all, 140 models, that users pay for themselves, including our free ones, that no one has to pay for, except us, and, and just use more apps that way, and build apps that are more sustainable.

[01:08:16] **Alex Attalah:** we're just, we're trying to, enable more of that, and,encourage these, and also encourage new models that are very, Niche and good at specific things, like Soliloquy, and Fumble Better, and a couple others that we've added recently. explore around. There's a playground to play with, to chat and play with things yourself.

[01:08:36] **Alex Attalah:** And please give us feedback. We have a Discord where we sometimes act on feedback the day it's given. and thanks for having me.

[01:08:44] **Alex Volkov:** Awesome, thanks for coming up and definitely folks should check out OpenRoute or at least know of its existence when you eventually need to do something with a fallback as well. And I've seen like many new models like pop up super quick as well, so it's great to see that there's also the ability to play around with them with a unified API.

[01:09:00] **Alex Volkov:** Thanks, Alex, for coming. 

