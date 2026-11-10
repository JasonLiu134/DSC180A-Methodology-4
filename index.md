# MA 4 Website

## Jason Liu (jal134@ucsd.edu)

### Section D20 - Baby Language Models and Cognitive Modeling

### Mentor: Alex Warstadt

### TA: Nate Sheibley

**1. What is the most interesting topic covered in your domain this quarter?**

The most interesting topic that was covered was the...

**2. Describe a potential investigation you would like to pursue for your Quarter 2 Project.**

A potential investigation that I'm looking at is the topic of how Prosody can be used to improve small language models without much training. Prosody refers to the characteristics present in spoken dialogue that change the way ordinary lexical speech is interpreted through the use of a speaker's tone, pitch, speaking speed, and emphasis on certain words. This is a field of study that deviates a little bit from the original BabyLM challenge, but acts more of an extension of the existing BabyLM dataset and evaluation by focusing primarily on the properties of audio data. In particular, I'm interested in investigating how well LMs are able to learn specific prosodic patterns, as well as how much of an improvement we'll actually see by incorporating prosody data in our trained models compared to models without it. This will give us some insight on how these smaller LMs are able to interpret linguistic context and resolve ambiguity from information such as emphasis on certain words, or spoken word boundaries. We can potentially implement this by creating a tokenizer that's able to encode additional information such as pitch, pauses in speech, and stress on certain words, which relates to some previous work that I have taken a look at. We can build on this by utilizing concepts from the BabyLM challenge, experimenting with more lightweight fine-tuning approahces and emphasize parameter efficiency to further explore the specific question of how prosody affects model performance in smaller learning environments. Ultimately, exploring the impact of prosody in a BabyLM context could help answer some questions about its importance in real life learning environments, since we know that humans learn from information beyond just written text, which can lead to future work on more effective ways to train LMs in a more developmentally plausible setting.

**3. What is a potential change you’d make to the approach taken in your current Quarter 1 Project?**

A potential change I'd make to the current Quarter 1 Project is to work backwards compared to how I was doing things before. Previously, we would train models first using multiple training runs and sweeps, then take our trained models and try and use them in the evaluation repository to see how our models are performing. We've used three different training repositories so far, and each one has seen their own challenges and limitations when it comes to evaluation. The primary problem that I ran into was that the tokenization and overall model architecture was a little different from what the evaluation code was expecting. A better approach would have been to take some pretrained models first and then try and run evaluation first, which would give us a bettle handle on the tokenization and checkpoints that would be needed to run certain tasks. Afterwards, before moving on to train our own models, we could first implement the proper tokenizers in the evaluation code first, and work through the training steps using the same tokenizer from the get-go. Doing so would help mitigate the constant changes we had to make to the evaluation code (which should work more out of the box), since when we first started working on our models, we didn't implement our training code with evaluation in mind right away.

**4. What other techniques would you be interested in using in your project?**

Some other techniques that I'd be interested in using are PEFT, Boosting, and Distillation.