## Annotation Guideline: Identifying Hate Speech in Tweets

1. **Definition of Hate Speech:**  
   Following the definition of the united nations [here](https://www.un.org/en/hate-speech/understanding-hate-speech/what-is-hate-speech#:~:text=In%20common%20language%2C%20%E2%80%9Chate%20speech,that%20may%20threaten%20social%20peace.),  
   In common language, “hate speech” refers to offensive discourse targeting a group or an individual based on inherent characteristics (such as race, religion or gender) and that may threaten social peace.

   
   Hate speech can be conveyed through any form of expression, including images, cartoons, memes, objects, gestures and symbols and it can be disseminated offline or online.

   Hate speech is “discriminatory” (biased, bigoted or intolerant) or “pejorative” (prejudiced, contemptuous or demeaning) of an individual or group.
   Hate speech calls out real or perceived “identity factors” of an individual or a group, including: “religion, ethnicity, nationality, race, colour, descent, gender,” but also characteristics such as language, economic or social origin, disability, health status, or sexual orientation, among many others.

2. **Annotation Task:**  
   The task is to determine whether a given tweet contains hate speech, is not hate speech, or is not annotable (can't tell).

   Labels used are `hate`, `not hate` or `undefined`

   **Hate:** (`hate`) Tweets that clearly contain hate speech as per the definition provided.  
   examples : 
      + 'your girlfriend lookin at me like a groupie in this bitch!',
      + "I AM NOT GOING AFTER YOUR EX BF YOU LIEING SACK OF SHIT ! I'm done with you dude that's why I dumped your ass cause your a lieing 😂😡 bitch",
      + 'Send home migrants not in need of protection, Peter Dutton tells UN, HEY DUTTON HOW ABOUT THE ONES THAT HAVE STAYED AND NOT LEFT THE COUNTRY WHEN THEY SHOULD OVERSTAYERS ? WHY DONT YOU GO AND ROUND ALL THEM UP ?'

   **Not Hate:** (`not hate`) Tweets that do not contain hate speech or any indicators of violence, discrimination, prejudice, or hostility.  
   examples : 
      + 'When cuffin season is finally over'
      + 'More migrants take sea route to #Spain than Italy this year: UN'
   
   **Can't Tell / Not Annotable:** (`undefined`) Tweets that are ambiguous, lack sufficient context, or are incomprehensible, making it impossible to confidently assign a hate or not hate label. Document these tweets for analysis purposes.  
   examples :
      - Tweets that use sarcasm or irony, making it unclear whether they are promoting hate or not.
      example : "@user @user you son of a bitch i'm in"  
      -> here they are surely joking between friends and not insulting each other

      - Tweets that require additional context or background information to understand their intent.
      example : "@user here you should die #lol"  
      -> may be about a video game 

      - Tweets that involve complex language, cultural references, or slang that may be open to interpretation.
      example : "@user presta atención al personaje negro"  
      -> here negro means the color black in spanish

   Be carefull : Avoid assigning multiple labels to a single tweet.

   For a lot more example take a look at the dataset [here](https://huggingface.co/datasets/tweet_eval/viewer/hate/train)
  
  
3. **Indicators of Hate Speech:**  
   Consider the following indicators while annotating tweets as hate or not hate:

   - **Derogatory Language:** Look for derogatory or offensive terms, slurs, or degrading language targeting individuals or groups based on protected attributes.
   - **Threats and Incitement:** Identify direct or indirect threats, calls for violence, or incitement to harm or discriminate against others.
   - **Discrimination and Prejudice:** Observe expressions of prejudice, stereotypes, or discriminatory views towards a specific group.
   - **Intolerance and Hostility:** Note any expressions of intolerance, animosity, or hostility towards individuals or groups based on protected attributes.
   - **Harassment:** Look for tweets that involve repetitive, persistent, or unwanted behavior intended to distress, intimidate, or belittle others.

   These indicators are not exhaustive. Consider other factors that may indicate hate speech.

4. **Contextual Understanding and Neutrality:**  
   Consider the overall context of the tweet to make an informed decision. Take into account the language used, the tone, any sarcasm or irony, and the potential impact on the targeted individual or group.

   While it is crucial to identify hate speech accurately, false positives (labeling a non-hate tweet as hate) should be minimized. Pay attention to the specific context, cultural references, and potential misinterpretations to avoid mislabeling tweets.

   Maintain a neutral and objective approach during the annotation process. Do not let personal opinions or biases influence the labeling decision.


5. **Grasping Twitter Context:**

   Twitter has unique context markers which are essential for tweet interpretation:

   - **@user:** "Mentions" tag users in tweets, often to direct conversation. Unfortunatly with our database it is anonymous.

   - **#keyword:** "Hashtags" denote topics or keywords in tweets, typically linked to broader conversations or trends. Recognizing the connotation of a hashtag may assist in determining if a tweet represents hate speech.
