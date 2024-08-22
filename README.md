# Fame-Bias

## Figure
![image](https://github.com/JiHuizhong549/Fame-Bias/blob/main/Figure1.png)
<p align="center"><b>Fig. 1. Dataset creation process</b></p>

## Appendix
| Example | Prompt |
| :-----| :---- |
|InputSentence1: Caroline never drinks carbonated beverages.<br>InputSentence2: Her friends pick on her because of it.<br>InputSentence3: One day they challenged her to drink a soda.<br>InputSentence4: Caroline wanted to win the challenge.<br>RandomFifthSentenceQuiz1: Caroline refused to open the soda.<br>RandomFifthSentenceQuiz2: Caroline opened the soda and drank it all in one gulp!<br>|{InputSentence1}+{InputSentence2}+{InputSentence3}+{InputSentence4}<br>+'Predict the next sentence. '<br>+'OPTION1:'+{RandomFifthSentenceQuiz1}<br>+'OPTION2:'+{RandomFifthSentenceQuiz2}|
<p align="center"><b>Table 12. Original data example and input prompt for story cloze task</b></p>

| Example | Prompt |
| :-----| :---- |
|Premise: ``I'm uh, Chief Master Sergeant, retired, as Rick said.''<br>Hypothesis: I am still working to this day.<br>label: 2<br>|Take the following as truth: +premise+ ``Then the following statement: ''+hypothesis <br> +`is {{"true"}} ,{{"false"}}, or {{"inconclusive"}}?'<br>|
<p align="center"><b>Table 13. Original data example and input prompt for NLI task</b></p>

