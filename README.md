# mastering_llms_notes
notes for the Mastering LLMs: A Conference For Developers &amp; Data Scientists course/conference 

Class 1: Scoping
- Focused on practical in industry applications of generative ai and LLM.
- they feel that fine tuning has plenty of blogs but not so much of actually how to put it in practice
- "blog driven development" - people do things just to make a blog or bc it is cool
- hands on focused
- goal is to finish more capable than you started

Philosphy:
- don't do blog driven development
- DO NOT start with fine tuning, start with simple things, ie promp engineering
- vibe checks are ok in the beginning
- write simple tests and assertions
- ship fast

Reality of LLM projects:
- talking about how the spent a bunch of time going through stake holders, but felt farther from delivery than when they started
- just said screw it and built a very small mvp (openai calls, simple react app), having a concrete item was huge to start from
- start from simple things, iterate
- Get into a Virtuous Cycle
- Focused on the evals

Ok, so when to fine tune?
- start with understanding what fine tuning is
- ok i'm ok here, I follow what this is
- base models are often not useful, BUT are amazing bases to go from
- basically take input output pairs (training set) and but it in a template, using delimiter tokens. YOU NEED consistent templating between training and inference, ie `'question is blah blah###'answer is bar'`
- many fine tuning systems can build a wrapper template around your inputs, be careful of this
- oh my god why is this this way! that seems insane and like people are just not paying attention and like slapping things together
- Pre-Training and fine-tuning are the same process, just one is general, one is domain specific
- As always, be very careful about the training data!

Hamel talking about Honeycomb, product he worked on. NL to query. Honeycomb is a software observability and telemetry platform.
- honeycomb has a DSL to query the data, its a problem in on boarding
- so they trained some LLMs to go natural language to DSL
- Aha, i have a use case for this
- Schema+UserInput was put into gpt3.5.
- prompt has a system message, context column names (RAG related), query spec, tips (ie things to avoid) and some few shot examples
- that's a lot going on in the prompt!
- it actually worked ok
- query spec does not tell you everything about the DSL language.
- the rules of the language basically ended up being lotta if/else
- Data privacy a point in favor of fine tuning
- they fine tuned a smaller model and got better results, faster inferences, data privacy etc

Question section
- how much data needed for fine tuning?
    - varies quite a bit! as small as 100 samples, varies with the scope of your data and problem
-   talked about multi modal fine tuning
-   LLMs are very friendly to synthetic data

Build an eval system specific to your domains

ReChat Case Study
- saying no to building a chatbot even when everyone thinks/says you should do it
- dont just slap a chatbot on your software/website- it often will break, it also has few scope guidelines, large surface area. You should compromise and be specific to the use case
- freeform text lets users have basically prompt/ddos your stuff
- scope is not just what you say it is to the model!
- PROMPTS ARE NOT GUARDRAILS

Have standards for desired inputs and outputs, ie keep consistent lenghts. 
using preference optmization techniques,
- Supervised Fine tuning
- Human Agent
- DPO - direct preference optimization

Other options is RLHF - present two options to the human, human picks, use that as training data. 

Q&A session

---





