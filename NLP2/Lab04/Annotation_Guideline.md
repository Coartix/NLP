## Annotation Guideline: Identifying Hate Speech in Tweets

1. **Definition of Hate Speech:**  
   Hate speech refers to any content that promotes or expresses violence, discrimination, prejudice, or hostility towards individuals or groups based on attributes such as race, ethnicity, religion, gender, sexual orientation, nationality, or any other protected characteristic. It may include explicit or implicit derogatory language, threats, harassment, or incitement to harm or discriminate against others.

2. **Annotation Task:**  
   The task is to determine whether a given tweet contains hate speech, is not hate speech, or is not annotable (can't tell). Focus on the text of the tweet and do not consider the intentions or background of the author.

   Labels used are `hate`, `not hate` or `undefined`

3. **Target Classes:**
   - **Hate:** (`hate`) Tweets that clearly contain hate speech as per the definition provided.
   - **Not Hate:** (`not hate`) Tweets that do not contain hate speech or any indicators of violence, discrimination, prejudice, or hostility.
   - **Can't Tell / Not Annotable:** (`undefined`) Tweets that are ambiguous, lack sufficient context, or are incomprehensible, making it impossible to confidently assign a hate or not hate label. Document these tweets for analysis purposes.
  
  
4. **Indicators of Hate Speech:**  
   Consider the following indicators while annotating tweets as hate or not hate:

   - **Derogatory Language:** Look for derogatory or offensive terms, slurs, or degrading language targeting individuals or groups based on protected attributes.
   - **Threats and Incitement:** Identify direct or indirect threats, calls for violence, or incitement to harm or discriminate against others.
   - **Discrimination and Prejudice:** Observe expressions of prejudice, stereotypes, or discriminatory views towards a specific group.
   - **Intolerance and Hostility:** Note any expressions of intolerance, animosity, or hostility towards individuals or groups based on protected attributes.
   - **Harassment:** Look for tweets that involve repetitive, persistent, or unwanted behavior intended to distress, intimidate, or belittle others.

5. **Contextual Understanding:**  
   Consider the overall context of the tweet to make an informed decision. Take into account the language used, the tone, any sarcasm or irony, and the potential impact on the targeted individual or group.

6. **Ambiguous Cases and Examples:**  
   Some tweets may present challenges in determining hate speech. Examples of ambiguous cases include:
   
   - Tweets that use sarcasm or irony, making it unclear whether they are promoting hate or not.
   - Tweets that require additional context or background information to understand their intent.
   - Tweets that involve complex language, cultural references, or slang that may be open to interpretation.

   When encountering such cases, follow these guidelines:
   
   - If the tweet's intent is unclear or the hate speech is not evident, label it as `undefined`
   - Document ambiguous cases with brief explanations for analysis and possible future improvements.

7. **False Positives:**  
   While it is crucial to identify hate speech accurately, false positives (labeling a non-hate tweet as hate) should be minimized. Pay attention to the specific context, cultural references, and potential misinterpretations to avoid mislabeling tweets.

8. **Multiple Labels:**  
   Assign one of the three labels per tweet: `hate`, `not hate`, or `undefined` Avoid assigning multiple labels to a single tweet.

9. **Neutrality:**  
   Maintain a neutral and objective approach during the annotation process. Do not let personal opinions or biases influence the labeling decision.

