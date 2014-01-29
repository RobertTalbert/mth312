# MTH 312: Assessment 1

## Overview and instructions

Welcome to your first Assessment in MTH 312. The purpose of this assessment is to gauge your mastery of the essential concepts of the first weeks of the course, to have you express your thoughts on some course-related questions, and to solicit informal feedback on the course itself at the 4-week point. 

**This assessment is entirely open-notes and open-Internet.** You may use any print or electronic resource you wish to respond to the items below. The only requirement on your part is that **if you use a particular resource to solve a problem or answer a question, you must cite it in your solution or response**. If the resource is online, give the URL for that resource. 

You may also use *Mathematica* to help with any task. If you use *Mathematica*, please submit a *Mathematica* notebook that is legibly formatted that contains the *Mathematica* code or operations that you used. On a related note, if you have programming skills and opt to write your own code to help solve a problem, please include a file that contains the code that you wrote and include comments in the code that explain what is happening. 

Given the open nature of this assessment, please note very carefully the following guidelines about academic honesty. 

1. **You may not consult with any other person about this assessment, at any level. This means no discussions of the Assessment are to take place between you and anyone else, not even informal discussions about the Assessment.** Treat your work on the Assessment as top secret. Any indication that you have discussed, in person or online, this assessment with another person will be taken as evidence of academic dishonesty. The one exception to this rule is that **you may ask me (Prof. Talbert) a question about the assessment at any time**, especially clarifying questions. However, please note that I will not answer questions such as *Is this right?*, *Am I on the right track?*, or *Is this what you want?*, and I will not be giving out hints. 
2. **Your work must represent your own efforts and not be taken significantly from other sources**. For example, if you use a Wikipedia entry and essentially just rephrase the Wikipedia entry as your answer, then this is academic dishonesty for the purposes of the assessment. You may combine and synthesize multiple sources for your responses as long as you are the one doing the work. But you may not merely paraphrase or remix existing content and submit it as "your" answer. Please note that I will be checking most verbal responses on Google to make sure that no appropriation of material is taking place. 



**Submission instructions:** Please type up your responses in a structured document and submit them as PDF files, attaching them to an email sent to [talbertr@gvsu.edu](mailto:talbertr@gvsu.edu) by 11:59pm on Monday, February 3. You may use any system for writing up your work that you wish -- MS Word, Google Docs, LaTeX, or  *Mathematica* notebook, or something else. You might consider using a Mathematica notebook for this Assessment, since you may be doing mathematical calculations as well as writing.

Please note: 

+ Submissions that are not PDF files will not be accepted. If you are not sure how to convert your file to a PDF, please ask me. 
+ No grace periods will be granted for late work. This includes late work due to technical difficulties and late work due to forgotten email attachments. It's your responsibility to have the work on this assessment completed ad submitted well in advance of the deadline in case of technical issues, and your responsibility to make sure the work is actually submitted (i.e. you didn't forget to attach your document). 

Again, you may ask me a question at any time if you are unclear on any part of this Assessment. 

## Assessment items

### Problem 1: Transposition ciphers (30 points) 

The **columnar transposition cipher** is a cipher system that works as follows. Suppose Alice wants to send a message (in text) to Bob; suppose the message has L characters in it. 

1. Alice and Bob decide on a positive integer that we will denote by "C". 
2. Alice creates a rectangular grid with C columns and L/C rows (and rounding up to the nearest whole number if C doesn't divide L exactly). She then starts writing down the message into the first row; when she reaches the end of the first row, she wraps around to the second row and keeps writing. She wraps around to the third row when she reaches the end of the second; and so on. 
3. Alice then goes to the first *column* and writes down the letters in the column from top to bottom, wrapping around to the top of the second column when the bottom of the first column is reached; and so on. The resulting text is sent to Bob. 

Here's an example. Suppose Alice wants to send the message "cryptography is awesome" to Bob, and they agree on C = 4. The message is 21 characters long, so L = 21. Alice creates a grid that is 4 columns wide and 21/4 = 5.25 -> 6 rows deep: 

Then she puts the text in one row at a time: 

![Enciphering grid](https://github.com/RobertTalbert/mth312/blob/master/Assessment1/grid1.png?raw=true)

Then she reads off the text one column at a time: 

![Enciphering grid](https://github.com/RobertTalbert/mth312/blob/master/Assessment1/grid2.png?raw=true)

And this is what gets sent to Bob:

`CTAIEEROPSSYGHAOPRYWM`

*Give a complete, clear, and correct response to each of the following. Your explanations should be geared toward people at the level of your classmates. Include mathematics when necessary to support your explanations, but do not use math as a substitute for clear English explanations. Answers that do not contain explanations to support those answers will not receive full credit and may receive no credit at all.*

1. What is the *key* in the columnar transposition cipher? Given a message to encrypt that has length L, how many keys are possible from a practical standpoint? (Remember: State your answers *and* give valid explanations.) 
2. Encrypt your full name (stripped of punctuation and spaces, for example "robertnathantalbert") using three columns. Show how you use the enciphering grid to get the ciphertext. 
3. Explain how Bob would go about decrypting the message you generated in question 2, given that he knows you used three columns. 
4. Is the columnar transposition cipher a substitution cipher, like the cryptogram or a shift cipher? Explain. (Hint on this: If a cipher is a substitution cipher, then given a plaintext message and its corresponding ciphertext, we ought to be able to write down the "cipher alphabet" used to encrypt the message, like a cryptogram. Can you do that with the columnar transposition?) 


### Problem 2: The affine cipher (30 points) 

1. In an affine cipher, why can we only use the numbers 1, 3, 5, 7, 9, 11, 15, 17, 19, 21, 23, and 25 for the multiplication step? Explain. 
2. Suppose that we add three characters to the English alphabet: the question mark (?), the ampersand (&) and the period (.) so that now there are 29 characters we can use in an affine cipher. Which, if any, of the integers between 1 and 29 can be used for the multiplication step in the affine cipher with this extended alphabet? Explain. 
3. Suppose you are "Eve" and you received a message that was encrypted with an affine cipher. You don't know the key, but you do know that the letter "E" in the plaintext encrypts to the letter "L" in the ciphertext. Is it possible to determine the full key from this information alone? If so, determine what the key is (making sure to show your work and explain your reasoning). If not, explain what information you would need to be able to recover the key and then how you would use that information.  


### Problem 3: The Vigenere cipher (30 points) 

1. Use the Vigenere cipher to encrypt your full name (formatted without spaces and punctuation as in Problem 1 part 2) and encrypt it using the Vigenere cipher, with keyword equal to the first two characters of your last name. (For example, I would encrypt "robertnathantalbert" with TA.) Show your work. 
2. Suppose the ciphertext `RNJ` (three letters long) was encrypted with the Vigenere cipher using a three-letter key. Find a key that will make the `RNJ` decrypt to the first three letters of your first name. Then find a key that will make  `RNJ` decrypt to the first three letters of your last name. Explain how you got both keys. 
3. Four different sets of ciphertexts have been set up for you. Choose one of these according to the month in which you were born: 


| Born in:         |  Use this ciphertext file:  |
| ---------------- | :-------------------------  |
| January-March    |  [A1ciphertext1.txt](https://raw.github.com/RobertTalbert/mth312/master/Assessment1/A1ciphertext1.txt)          |
| April-June       |  [A1ciphertext2.txt](https://raw.github.com/RobertTalbert/mth312/master/Assessment1/A1ciphertext2.txt)          |
| July-September   |  [A1ciphertext3.txt](https://raw.github.com/RobertTalbert/mth312/master/Assessment1/A1ciphertext3.txt)          |
| October-December |  [A1ciphertext4.txt](https://raw.github.com/RobertTalbert/mth312/master/Assessment1/A1ciphertext4.txt)          |


Each ciphertext was encrypted using the Vigenere cipher and a keyword of length 3. Find the plaintext. When done, state the plaintext and give a full accounting of the specific steps you took to decrypt the message. If you cannot get all the plaintext, be sure to report any progress that you made and explain how you made it. 

The website [Text Mechanic](http://textmechanic.com/) could be helpful for doing things like counting characters, removing spaces, and so on. 


### Problem 4: Reflection and feedback (10 points) 

1. What's the most interesting thing you've learned in MTH 312 so far? 
2. What's been the most challenging thing you've had to face is MTH 312 so far? 
3. What's one thing that you've really enjoyed about MTH 312 so far? 
4. What's one item in MTH 312 that we could improve moving forward? (You can list more than one thing if you want.) 


