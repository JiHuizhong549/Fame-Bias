# Fame-Bias

## Figure
![image](https://github.com/JiHuizhong549/Fame-Bias/blob/main/Figure1.png)
<p align="center"><b>Fig. 1. Dataset creation process</b></p>

## Tables

|Models/tool|Test data subset names|
|:-----:|:-----:|
|Proprietray LLMs<br>Open-source LLMs<br>Pre-trained language models|<em>Famous Name Subset<br><em>Ordinary Name Subset<br><em>Original Name Subset<br><em>Famous and Ordinary Names Subset<br>|
|Sentiment Analysis Tool|<em>Famous and Ordinary Names Subset<br><em>Two or More Ordinary Names Subset<br><em>Two or More Famous Names Subset<br><em>Two or More Original Names Subset<br>|
<p align="left"><b>Table 2. Experimental methods and utilized test sets with examples</b></p>


| |original|famous|ordinary|fam+ord|
|:-----|:-----|:-----|:-----|:-----|
|GPT-3.5-turbo|0.9490|0.9406*|0.9572|0.9197*|
|GPT-3.5-turbo-1106|0.9406|0.9133*|0.9529|0.9482*|
|GPT-3.5-turbo-16k|0.9603|0.9426*|0.9513|0.9150*|
|GPT-4|0.9846|0.9777|0.9837|0.9418|
|Gemini 1.0 Pro|0.9712|0.9540|0.9684|0.9080|
<p align="left"><b>Table 3. Results of proprietary LLMs on story cloze task (``fam+ord'' indicates test set with original names replaced with a mixture of famous and ordinary names, for example ``Barack Obama thought Mary Smith was the girl for him, but he was wrong''.) An asterisk (*) on the right side indicates a significant difference.</b></p>


| |original|famous|ordinary|fam+ord|
|:-----|:-----|:-----|:-----|:-----|
|GPT-3.5-turbo|0.5532|0.4365*|0.4656*|0.4216|
|GPT-3.5-turbo-1106|0.5354|0.4400*|0.4822|0.4076*|
|GPT-3.5-turbo-16k|0.5177|0.3722*|0.4828|0.3770*|
|GPT-4|0.7707|0.6800*|0.7356*|0.6|
|Gemini 1.0 Pro|0.7297|0.6216*|0.6648|0.5621|
<p align="left"><b>Table 4. Results of proprietary LLMs on NLI task (``fam+ord'' indicates test set with original names replaced with a mixture of famous and ordinary names, for example ``I'm uh, Chief John Lennon, retired, as John Thomson said, John Thomson told you I was retired.'' ). An asterisk (*) on the right side indicates a significant difference.</b></p>


|task|model|original|ori&fam|ori&ord|ori&fam+ord|S.D.|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|storycloze|Llama-2-chat-7b |0.79|0.18|0.12|0.27|0.098|
|storycloze|Llama-2-chat-13b|0.91|0.02|0|0.07|0.028|
|XNLI|Llama-2-chat-7b|0.48|0.22|0.1|0.04|0.083|
|XNLI|Llama-2-chat-13b|0.62|0.22|0.19|0.23|0.093|
<p align="left"><b>Table 5.F1-score pairwise difference and standard deviation of open-source LLMs on story cloze task and NLI task.</b></p>


| |original|famous|ordinary|fam+ord|
|:-----|:-----|:-----|:-----|:-----|
|distilbert-base-cased|0.8571|0.8342|0.8228|0.7714|
|bert-large-cased|0.9600|0.9542|0.9352|0.9485|
<p align="left"><b>Table 6.Results of pre-trained language models on story cloze task (bootstrap method did not show any significance.)</b></p>


| |original|famous|ordinary|fam+ord|
|:-----|:-----|:-----|:-----|:-----|
|xlm-v-base|0.8378|0.8216*|0.8378*|0.5621|
|mDeBERTa-v3-base|0.8756|0.8108*|0.8270*|0.7729|
|ernie-m-base|0.8594|0.8054*|0.8108*|0.7135|
|ernie-m-large|0.8702|0.8324*|0.8054*|0.7297| 
|DeBERTa-v3-base|0.9189|0.8594*|0.8540*|0.5945|
|MiniLM-L6|0.7567|0.7135*|0.7513*|0.7189|
<p align="left"><b>Table 7.Results of pre-training language models on NLI task</b></p>


|Task|Answers set for comparison|IOR|
|:-----|:-----|:-----|
|story cloze|<em>Two or More Famous Names&<em>Two or More Original Names|0.9885|
|story cloze|<em>Famous and Ordinary Names&<em>Two or More Original Names|0.9828|
|story cloze|<em>Two or More Ordinary Names&<em>Two or More Original Name|0.9943|
|NLI|<em>Two or More Famous Names&<em>Two or More Original Names|0.9783|
|NLI|<em>Famous and Ordinary Names&<em>Two or More Original Names|0.9891|
|NLI|<em>Two or More Ordinary Names&<em>Two or More Original Names|0.9946|
<p align="left"><b>Table 8.Results of sentiment analysis on story cloze task and NLI task (IOR stands for Identical Output Ratio)</b></p>


| |original|famous|random|
|:-----|:-----|:-----|:-----|
|distilbert-base-cased|0.8538|0.8342|0.7836|
|bert-large-cased|0.9600|0.9542|0.9122|
|Gemini 1.0 Pro |0.9712|0.9540|0.9064|
<p align="left"><b>Table 9.Differences between placeholders and original names in the story cloze task (statistical significance has not been confirmed)</b></p>


| |original|famous|random|
|:-----|:-----|:-----|:-----|
|xlm-v-base|0.8378|0.7861*|0.8216*|
|mDeBERTa-v3-base|0.8756|0.8070*|0.8108*|
|ernie-m-base|0.8594|0.7861*|0.8054*|
|ernie-m-large|0.8702|0.7803*|0.8324*| 
|DeBERTa-v3-base|0.9189|0.8208*|0.8594*|
|MiniLM-L6|0.7567|0.7341|0.7135*|
|Gemini 1.0 Pro|0.7297|0.6023*|0.6216*|
<p align="left"><b>Table 10.Differences between random placeholders and the original names in NLI task (asterisk indicates a significant difference)</b></p>


## Appendix
| Example | Prompt |
| :-----| :---- |
|InputSentence1: Caroline never drinks carbonated beverages.<br>InputSentence2: Her friends pick on her because of it.<br>InputSentence3: One day they challenged her to drink a soda.<br>InputSentence4: Caroline wanted to win the challenge.<br>RandomFifthSentenceQuiz1: Caroline refused to open the soda.<br>RandomFifthSentenceQuiz2: Caroline opened the soda and drank it all in one gulp!<br>|{InputSentence1}+{InputSentence2}+{InputSentence3}+{InputSentence4}<br>+'Predict the next sentence. '<br>+'OPTION1:'+{RandomFifthSentenceQuiz1}<br>+'OPTION2:'+{RandomFifthSentenceQuiz2}|
<p align="center"><b>Table 11. Original data example and input prompt for story cloze task</b></p>


| Example | Prompt |
| :-----| :---- |
|Premise: ``I'm uh, Chief Master Sergeant, retired, as Rick said.''<br>Hypothesis: I am still working to this day.<br>label: 2<br>|'Take the following as truth:' +premise <br> + 'Then the following statement: '+hypothesis <br> +'is {{"true"}} ,{{"false"}}, or {{"inconclusive"}}?' <br>|
<p align="center"><b>Table 12. Original data example and input prompt for NLI task</b></p>

