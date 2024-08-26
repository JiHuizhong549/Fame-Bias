# Fame-Bias

## Figure
![image](https://github.com/JiHuizhong549/Fame-Bias/blob/main/Figure1.png)
<p align="center"><b>Fig. 1. Dataset creation process</b></p>

## Tables
| |original|famous|ordinary|fam+ord|
|:-----|:-----|:-----|:-----|:-----|
|GPT-3.5-turbo|0.9490|0.9406*|0.9572|0.9197*|
|GPT-3.5-turbo-1106|0.9406|0.9133*|0.9529|0.9482*|
|GPT-3.5-turbo-16k|0.9603|0.9426*|0.9513|0.9150*|
|GPT-4|0.9846|0.9777|0.9837|0.9418|
|Gemini 1.0 Pro|0.9712|0.9540|0.9684|0.9080|
<p align="left"><b>Table 2. Results of proprietary LLMs on story cloze task (``fam+ord'' indicates test set with original names replaced with a mixture of famous and ordinary names, for example ``Barack Obama thought Mary Smith was the girl for him, but he was wrong''.) An asterisk (*) on the right side indicates a significant difference.</b></p>

## Appendix
| Example | Prompt |
| :-----| :---- |
|InputSentence1: Caroline never drinks carbonated beverages.<br>InputSentence2: Her friends pick on her because of it.<br>InputSentence3: One day they challenged her to drink a soda.<br>InputSentence4: Caroline wanted to win the challenge.<br>RandomFifthSentenceQuiz1: Caroline refused to open the soda.<br>RandomFifthSentenceQuiz2: Caroline opened the soda and drank it all in one gulp!<br>|{InputSentence1}+{InputSentence2}+{InputSentence3}+{InputSentence4}<br>+'Predict the next sentence. '<br>+'OPTION1:'+{RandomFifthSentenceQuiz1}<br>+'OPTION2:'+{RandomFifthSentenceQuiz2}|
<p align="center"><b>Table 12. Original data example and input prompt for story cloze task</b></p>

| Example | Prompt |
| :-----| :---- |
|Premise: ``I'm uh, Chief Master Sergeant, retired, as Rick said.''<br>Hypothesis: I am still working to this day.<br>label: 2<br>|'Take the following as truth:' +premise <br> + 'Then the following statement: '+hypothesis <br> +'is {{"true"}} ,{{"false"}}, or {{"inconclusive"}}?' <br>|
<p align="center"><b>Table 13. Original data example and input prompt for NLI task</b></p>

