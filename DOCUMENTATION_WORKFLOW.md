# Documentation Workflow

This repository follows a structured documentation workflow.

At the end of each learning day, after all learning sessions are completed, a documentation prompt is sent to ChatGPT.

The purpose of the prompt is to generate a consistent SUMMARY.md file for that day.

The prompt used for this process can be found here:

* [PROMPT_FOR_DOCUMENTATION.md](./PROMPT_FOR_DOCUMENTATION.md)

The AI generates a draft summary based on:

* Concepts learned during the day
* Doubts asked during learning
* Explanations received
* Verification questions discussed
* Learning artifacts created or discussed
* Engineering intuitions developed
* Reflections from the learning process

Learning artifacts may include:

* Programs
* Debugging discussions
* Transcript discussions
* Exercises
* AI verification activities
* Reasoning discussions
* Other learning activities

Human review is mandatory.

Before committing any generated SUMMARY.md:

* Verify every concept listed.
* Verify every doubt listed.
* Verify every AI question listed.
* Verify every explanation listed.
* Verify every learning artifact listed.
* Verify every engineering intuition listed.
* Remove anything inaccurate.
* Add anything important that was missed.

The final SUMMARY.md represents the reviewed version rather than the raw AI output.

The objective is consistency, accuracy, and revision value rather than automation.

AI assists documentation.

The learner validates documentation.
