# MTH 312: Assessment 2

## Overview and instructions

Welcome to your second Assessment in MTH 312. The purpose of this assessment is to gauge your mastery of the essential concepts of the first weeks of the course, to have you express your thoughts on some course-related questions, and to solicit informal feedback on the course. 

**This assessment is entirely open-notes and open-Internet.** You may use any print or electronic resource you wish to respond to the items below. The only requirement on your part is that **if you use a particular resource to solve a problem or answer a question, you must cite it in your solution or response**. If the resource is online, give the URL for that resource. 

You may also use *Mathematica* to help with any task. If you use *Mathematica*, please submit a *Mathematica* notebook that is legibly formatted that contains the *Mathematica* code or operations that you used. On a related note, if you have programming skills and opt to write your own code to help solve a problem, please include a file that contains the code that you wrote and include comments in the code that explain what is happening. 

Given the open nature of this assessment, please note very carefully the following guidelines about academic honesty. 

1. **You may not consult with any other person about this assessment, at any level. This means no discussions of the Assessment are to take place between you and anyone else, not even informal discussions about the Assessment.** Treat your work on the Assessment as top secret. Any indication that you have discussed, in person or online, this assessment with another person will be taken as evidence of academic dishonesty. The one exception to this rule is that **you may ask me (Prof. Talbert) a question about the assessment at any time**, especially clarifying questions. However, please note that I will not answer questions such as *Is this right?*, *Am I on the right track?*, or *Is this what you want?*, and I will not be giving out hints. 
2. **Your work must represent your own efforts and not be taken significantly from other sources**. For example, if you use a Wikipedia entry and essentially just rephrase the Wikipedia entry as your answer, then this is academic dishonesty for the purposes of the assessment. You may combine and synthesize multiple sources for your responses as long as you are the one doing the work. But you may not merely paraphrase or remix existing content and submit it as "your" answer. Please note that I will be checking most verbal responses on Google to make sure that no appropriation of material is taking place. 

**Submission instructions:** Please type up your responses in a structured document and submit them as PDF files, attaching them to an email sent to [talbertr@gvsu.edu](mailto:talbertr@gvsu.edu) by **11:59pm on Wednesday, March 12**. You may use any system for writing up your work that you wish -- MS Word, Google Docs, LaTeX, or  *Mathematica* notebook, or something else. You might consider using a *Mathematica* notebook for this Assessment, since you may be doing mathematical calculations as well as writing.

Please note: 

+ Submissions that are not PDF files will not be accepted. If you are not sure how to convert your file to a PDF, please ask me. 
+ No grace periods will be granted for late work. This includes late work due to technical difficulties and late work due to forgotten email attachments. It's your responsibility to have the work on this assessment completed ad submitted well in advance of the deadline in case of technical issues, and your responsibility to make sure the work is actually submitted (i.e. you didn't forget to attach your document). 

Again, you may ask me a question at any time if you are unclear on any part of this Assessment. 

## Assessment items

### Problem 1: Using RSA (30 points)

Recall our discussion of the RSA crypto system from class on February 24. The slides from this class, which include the algorithms for key generation, encryption, and decryption, are on Piazza. 

1. Generate two primes p and q that are at least six digits long. Use those primes to generate both public and private keys in RSA. Show your work (which you may do using Mathematica). 
2. Plaintext messages for this problem are two-letter blocks that have been converted to 4-digit integers using their ASCII decimal values. If the message has an odd number of letters, pad the end of the message with an "X". For example `HELLO` would be padded to become `HELLOX` and then converted into `HE LL OX` which then becomes `7269 7676 7988`. (For this problem use only capital letters and no other letters or punctuation.) Prof. Talbert's public key is e = 971, n = 27958975127. Make up a ten-character message (that actually says something and is not just a random string), encrypt it with Prof. Talbert's public key, and "send" it to him by including the message in your writeup. Show your work (which you may do in Mathematica). 
3. Using only the public key, find Prof. Talbert's private key. Show all work and be sure to explain your steps in detail. 

### Problem 2: Using Diffie-Hellman (30 points)

In this problem, you'll work with the Diffie-Hellman key exchange algorithm. The **corrected** slides from the presentation for this section were posted to Piazza on February 27. For this problem, we will set the following parameters for the entire class to use: 

- p (prime number): 224729
- a (generator/primitive root mod p): 3

1. Choose a secret integer x with 1 < x < 224728 and calculate a^x mod p. Show your work using *Mathematica*. 
2. I have chosen a secret integer, y, for myself and calculated the following: a^y mod p = 19181. Use this to determine the key that you and I will share. Show your work using *Mathematica*. 
3. Now suppose you are Eve, and you have access to p (224729), a (3), and a^y mod p (19181). Find my secret integer y. (Hint: Brute force is an acceptable method, it just often takes a long time if the numbers involved are large.) Show your work using *Mathematica*. 
4. If you find a value of y such that 3^y mod 224729 = 19181, how do you know this is the only such value of y? Could there be some other value for y that makes this equation true? 

### Problem 3: Miscellaneous (30 points total)

1. (4 points) The ciphertext 01101100 was encrypted using a simple XOR cipher with an 8-bit key. It is discovered that the plaintext was 11011110. What was the key? Show your work. 
2. (6 points) The ciphertext 01101100 was encrypted using a simple XOR cipher with an 8-bit key. Explain in detail why it is impossible to break this code, even through brute force, without further information. 
3. (8 points) Choose a 12-bit string of bits for plaintext and a 9-bit string for a key, and encrypt it using two rounds of Simplified DES ([Problem Solving Lab 6](http://teaching.proftalbert.com/mth312w14/problem-solving-labs/psl-6/)). Show your work and annotate your steps using English. 
4. (6 points) Explain what the "discrete logarithm problem" is, and how it pertains to the security of cryptographic systems (especially public-key systems). 
5. (6 points) The security of public-key systems often relies on the availability of "hard mathematical problems", which are mathematical processes that are time- and resource-consuming for large values. For instance, RSA's security relies on the hardness of factoring n = pq (where p,q are large primes) into its factors p and q. What are some other hard mathematical problems that are used to build cryptographic systems? Do some brief internet or print research and give a two-paragraph report on at least two such problems (other than factoring) and where they are used. Cite any references you use. 

### Problem 4: Feedback (10 points)

Write at least 2-3 thoughtful sentences for each of the following. 

1. What's the most interesting thing you've learned in MTH 312 so far since the last assessment? 
2. What's been the most challenging thing you've had to face is MTH 312 so far since the last assessment?? 
3. What's one thing that you've really enjoyed about MTH 312 so far? 
4. What's one item in MTH 312 that we could improve moving forward? (You can list more than one thing if you want.) 

Also, optionally, if you have any additional questions, comments, or concerns about the course, please put that with your feedback. 