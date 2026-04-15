### Learnings

I am building [project-1](https://github.com/zoyron/systems-lab) using the [mentor skill](../mentor.md).

- While building this project, I noticed that the initial phase like installing dependencies or setting up the typescript config files have very verbose steps, which is good but only for the initial 2-3 projects, after that, I need to reduce the verbosity of the initial setup steps in the mentor skill file.(this was the issue with gemini 2.5, working fine with gemini 3 flash, but the code explanation got less verbose without making any modifications to the mentor file. Need to check this with another project before making any modification in verbosity of the explanation part. The installation steps worked fine with gemini flash 3 without any modifications, they seems short and to the point, but with decent explanation.)

- There are no ways to handle inbetween questions. Like if I have doubt in between the workflow, and if I ask it to the llm, it breaks the teaching flow. I must update the the mentor skill file to take care of this issue so if I ask a question midway, it doesn't break the teaching pattern. 
