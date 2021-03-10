# Сontact Сenter Robot

**Solution by**: Data Monsters

**Date**: February 2021

![Scheme](https://github.com/ml-patterns/ml-patterns/blob/main/library/images/img_bot.png)

### Challenge

Reduce contact center costs by creating a robot that can:
* Answer frequently asked questions without involving a human operator.
* Perform actions (creating tasks in WFMS, checking user information, calling external APIs, etc.)
* Give prompts to operators.

### Solution

A robot was created that connects to the helpdesk software used in the contact center. The robot accepts user requests before engaging a human operator. If the answer is contained in the knowledge base, then the dialogue script is launched, otherwise the conversation is redirected to the operator. The system identifies popular topics for which there are no scripts in the knowledge base yet, and advises to create scripts for them. Thanks to this, the robot is constantly increasing its automation, achieving automation of 80% or more of incoming requests. The robot can support thousands of interactive scenarios. A testing toolkit is provided that allows you to detect conflicts and check the overall quality of the robot on a test instance before publishing new scripts.

### Technologies used

PyTorch, DeepPavlov, NVIDIA Jarvis, NVIDIA Rapids, Docker, Kubernetes
