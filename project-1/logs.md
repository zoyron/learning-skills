### Learnings

I am building [project-1](https://github.com/zoyron/systems-lab) using the [mentor skill](../mentor.md).

- While building this project, I noticed that the initial phase like installing dependencies or setting up the typescript config files have very verbose steps, which is good but only for the initial 2-3 projects, after that, I need to reduce the verbosity of the initial setup steps in the mentor skill file.(this was the issue with gemini 2.5, working fine with gemini 3 flash, but the code explanation got less verbose without making any modifications to the mentor file. Need to check this with another project before making any modification in verbosity of the explanation part. The installation steps worked fine with gemini flash 3 without any modifications, they seems short and to the point, but with decent explanation.)

- There are no ways to handle inbetween questions. Like if I have doubt in between the workflow, and if I ask it to the llm, it breaks the teaching flow. I must update the the mentor skill file to take care of this issue so if I ask a question midway, it doesn't break the teaching pattern. 

- Gemini flash 3 starts losing context after about 75% percentage of the project. Or maybe it wasn't losing context, just lost where we were in the steps when I asked a few doubts in-between the project working flow. I'll only know better after improving the prompt for doubt clearing. 

- Idea is to add marking words like "doubt" for asking doubts in between steps and "continue with steps" for continuing with the steps as if no doubts were asked, like I should ask the llm to act as if no doubts were asked and then it should give me the next logical steps with the complete explanation in text and in code comments.
