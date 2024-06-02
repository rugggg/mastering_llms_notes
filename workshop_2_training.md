
They went through some basics of axolotl - readme is probably more useful.

Now going deeper into the honeycomb case study.

On the side, I am setting up axolotl.

What they did with honeycomb to fine tune the model to get it better on the domain specific query language.
- lot of dataset management and cleaning.
- showing the full system prompt, quite a bit in there. Few shot examples, make sure it's a completion model not a chat api, template the user's question. (oh this is for the prior approach they used before fine tuning).

- Started with writing evals after some base prompt engineering and vibe checks
- What are evals?
    - hamel has a blog post on it
    - Level 1 is unit tests
    - Level 2 ??
    - Level 3 is A/B testingpython
    - evals are ways to make sure the returned values are correct 

