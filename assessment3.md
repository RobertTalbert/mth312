# MTH 312: Assessment 3

## Overview and instructions

Welcome to your third Assessment in MTH 312. The purpose of this assessment is to gauge your mastery of the essential concepts of the final third of the course, to have you express your thoughts on some course-related questions, and to solicit informal feedback on the course. 

**This assessment is entirely open-notes and open-Internet.** You may use any print or electronic resource you wish to respond to the items below. The only requirement on your part is that **if you use a particular resource to solve a problem or answer a question, you must cite it in your solution or response**. If the resource is online, give the URL for that resource. 

You may also use *Mathematica* to help with any task. If you use *Mathematica*, please submit a *Mathematica* notebook that is legibly formatted that contains the *Mathematica* code or operations that you used. On a related note, if you have programming skills and opt to write your own code to help solve a problem, please include a file that contains the code that you wrote and include comments in the code that explain what is happening. 

Given the open nature of this assessment, please note very carefully the following guidelines about academic honesty. 

1. **You may not consult with any other person about this assessment, at any level. This means no discussions of the Assessment are to take place between you and anyone else, not even informal discussions about the Assessment.** Treat your work on the Assessment as top secret. Any indication that you have discussed, in person or online, this assessment with another person will be taken as evidence of academic dishonesty. The one exception to this rule is that **you may ask me (Prof. Talbert) a question about the assessment at any time**, especially clarifying questions. However, please note that I will not answer questions such as *Is this right?*, *Am I on the right track?*, or *Is this what you want?*, and I will not be giving out hints. 
2. **Your work must represent your own efforts and not be taken significantly from other sources**. For example, if you use a Wikipedia entry and essentially just rephrase the Wikipedia entry as your answer, then this is academic dishonesty for the purposes of the assessment. You may combine and synthesize multiple sources for your responses as long as you are the one doing the work. But you may not merely paraphrase or remix existing content and submit it as "your" answer. Please note that I will be checking most verbal responses on Google to make sure that no appropriation of material is taking place. 

**Submission instructions:** Please type up your responses in a structured document and submit them as PDF files, attaching them to an email sent to [talbertr@gvsu.edu](mailto:talbertr@gvsu.edu) by **11:59pm on Monday, April 14**. You may use any system for writing up your work that you wish -- MS Word, Google Docs, LaTeX, or  *Mathematica* notebook, or something else. You might consider using a *Mathematica* notebook for this Assessment, since you may be doing mathematical calculations as well as writing. **Please format the name of your PDF as follows:** `MTH 312 LastName A3.pdf` where "LastName" is your last name. For example, Alice Smith's submission would be titled `MTH 312 Smith A3.pdf`. **Files that are not properly titled or which are not PDF's will be sent back unopened, and if you miss the deadline because of this you will get a 0 on the Assessment.**

Please note: 

+ Submissions that are not PDF files will not be accepted. If you are not sure how to convert your file to a PDF, please ask me. 
+ No grace periods will be granted for late work. This includes late work due to technical difficulties and late work due to forgotten email attachments. It's your responsibility to have the work on this assessment completed ad submitted well in advance of the deadline in case of technical issues, and your responsibility to make sure the work is actually submitted (i.e. you didn't forget to attach your document). 

Again, you may ask me a question at any time if you are unclear on any part of this Assessment. 

## Assessment items

### Problem 1: Birthday Attack Reloaded (12 points) 

In Problem Solving Lab 11, you solved the discrete logarithm problem 7288214 = 20000^x mod 15487903 using the Birthday Attack. Modify your work on that lab to solve the following discrete logarithm problem: 

53820811158378 = 816607787^x mod 56086786668977

Show all your work, including an explanation of how you modified your setup from PSL 11. NOTE: A brute-force attack is not acceptable here -- please use the Birthday Attack. (Brute force probably takes too long anyway.)

### Problem 2: El Gamal (30 points) 

1. Generate a set of keys for El Gamal. Show all your work and, at the end of your work, clearly state your public and private keys. Then SEND your public key -- not your private key! -- to Prof. Talbert **prior to the due date for this assessment**. 
2. Prof. Talbert created a set of keys as well. His public key is: (y = 29861570526970759096203447, g = 999777333, p = 54257749441566738654117703). Create a short message and encrypt it using his keys. "Send" it to him by stating the ciphertext at the end of your work. 
3. After you create your public keys and email them to Prof. Talbert, he will send you a short encrypted message. Decrypt the message -- show your work and state the plaintext. NOTE: You will need to give your keys to Prof. Talbert well in advance of the due date for the Assessment. 

### Problem 3: An El Gamal-based signature system (20 points) 

Like most public-key encryption systems, El Gamal can be modified to become a digital signature scheme. In fact, El Gamal signatures are quite common in practice. The generation of keys is the same process as for El Gamal encryption. Assuming that Alice has created a public key (y,g,p) and a private key x, in order for Alice to sign a message m, she does the following: 

+ Selects a secret random integer k such that gcd(k, p-1) = 1. 
+ Computes r =  g^k mod p
+ Computes s = k^{-1} (m - xr) mod (p-1) where k^{-1} is the multiplicative inverse of k mod p-1. 

Alice then sends the message m along with the numbers r and s to Bob. 

To verify Alice's message, Bob: 

+ Downloads Alice's public key (y,g,p). 
+ Computes u = y^r r^s mod p.
+ Computes v = g^m mod p. 

The signature is declared valid if u = v mod p. 

Consider the message **AWESOME**. By changing each character to ASCII and concatenating all the integers together, this becomes the single integer message 65876983797769. Using your El Gamal keys from Problem 2, sign this message. Show your work, and clearly state the signature (which, again, is a pair of integers). It's obviously a good idea too to double-check that your signature validates before submitting it. 

### Problem 4: Hash functions (30 points) 

1. List the three desirable features in a hash function that we discussed in class, and write a couple of sentences for each feature explaining why that feature is desirable. 
2. Let p be a prime number and let a be any integer such that p does not divide a. Define the function h(x) = a^x mod p where x is any integer. Does this function fit the definition of a hash function? That is, does it map an integer of arbitrary length to a fixed-length output? Explain. 
3. Is the function h(x) a *good* hash function in the sense of fulfilling all the three desirable features of a hash function? Explain in detail. 

### Problem 4: Writing Prompts (8 points) 

You know the drill on these: Write 2-3 thoughtful sentences for each of the following. You can write as much as you want if you have more to say. I read it all. 

1. What was the most interesting thing you've seen in the MTH 312 class since the last assessment? 
2. What's been the most challenging thing you've had to face is MTH 312 so far since the last assessment?
3. We're at the end of the course, with only the project presentations and the final exam remaining on the schedule. What's one thing you want to make sure you do well, or one question you definitely want to get answered about the course, as we head into these final weeks? 
4. Anything else on your mind? 
