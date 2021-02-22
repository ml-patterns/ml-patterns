# Contact Center Virtual Assistant

**Tags**: contact_center, virtual_assistant, chatbot, nlp

**Committer**: Dmitry Malkov, Data Monsters

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/business_cases/images/IMG_1105.jpg)

### Objective

Reduce the burden on contact center operators by creating a robot that answers standard questions and performs simple actions such as registering requests

### Solution

The entry point to the contact center is the helpdesk software. An incoming client request is authenticated, converted from voice to text, and then classified by the NLU module. If this question is contained in the bot's knowledge base, then the bot gives the answer. It can perform some actions by querying the enterprise API or cloud API, or launch the RPA system. The bot can also run a dialog script if it needs answers to clarifying questions from the user. If the bot cannot recognize the user's words, then the dialogue is transferred to the human operator, and the bot gives him hints in the helpdesk UI, working as a prompter.

Usually, two instances of the bot are deployed: production and test. The production instance responds to queries, while the test instance is used for safe model and knowledge base updates. Shadow AB testing allows you to make sure that the test instance works better than the current productive one, and at a certain moment, the production bot is replaced by the test one. A rolling update strategy allows you to do this without downtime.
