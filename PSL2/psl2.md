# MTH 312 Problem Solving Lab 2 

##Instructions

This Problem Solving Lab is a little different from the other ones you will see because it is to be done outside of class. We weren't able to have a lab on January 20 because of the MLK Day recess, and this lab assignment will give you a chance to practice and get feedback prior to your first Assessment, which is coming as a take-home assignment on January 29. 

You may work with up to two other people on this assignment because this is technically a Lab, and [according to the syllabus](http://teaching.proftalbert.com/mth312w14/syllabus/) you can work in groups on those. However, for this one time, I recommend you try working on this without collaboration, to build your individual skills prior to your Assessment. If you do choose to work with other people, please do the following: 

+ Submit only one writeup for your group. 
+ Put the names and email addresses of all contributors in the writeup. 
+ Do not communicate between different groups. 

Please submit your work electronically by writing it up in either a word processing document, LaTeX, or in a *Mathematica* notebook (your choice) that has been converted to a PDF. No handwritten work will be accepted, including electronic scans of handwritten work. Submit your work by attaching the file containing the writeup to an email. Other file formats besides PDF will not be accepted. 

+ The process of converting a MS Word file to PDF is different for different versions of Word. Try going to the File menu and looking for **Export**, or **Save As** and then select PDF. 
+ To export a Mathematica notebook as a PDF, click on **File** then **Save As...** and then select PDF from the list. Do NOT select **CDF Export** because a "CDF" something totally different than a PDF. 

Please give your file a title using the following format: 

`[List of last names] PSL 2.pdf`

The `.pdf` file extension will be added automatically. For example, if Alice Brown and Bob Smith collaborate on this work and write it up in a Mathematica notebook, they would first convert it to a PDF and then title it `Brown Smith PSL 2.pdf` and then send it in. 

This assignment is due by **class time on Monday, January 27**. 

##Problems 

1. Take your date of birth and convert it to a long integer as follows. First convert your birth month to a number 1--12 (January = 1, February = 2, etc.). Then put the month, day, and year of your birth together into one long integer. Let B represent the result. For example, my oldest daughter was born on January 12, 2004, so for her, B = 1122004. With that value of B, compute the following and state the result in your writeup: 
..1. B mod 8 
..2. B^4 mod 8 (Maybe *Mathematica* would be a good idea. How does *Mathematica* reduce a number modulo another, anyway?)
..3. B^10 mod 11 (Seriously, *Mathematica* would be a very good idea.) 
..4. B^16 mod 17 (Hello? Are you using *Mathematica* yet?)

What did you notice about the third and fourth computations above? Does this always happen when the modulus (the number we "mod out by") is a [prime number](http://www.mathsisfun.com/definitions/prime-number.html) and the exponent is one less than the modulus? Investigate and come up with further evidence either for or against this possibility. 

2. At this website you will find four files, each of which contains a different ciphertext. Each ciphertext was created using a shift cipher and a different key, but the key for each text is unknown. Please choose one according to the first letter of your last name: 

|  Last name begins with:  | Please use: | 
| :----------------------: | ----------- |
|   A--F                   | Ciphertext 1 | 
|   G--L                   | Ciphertext 2 | 
|   M--R                   | Ciphertext 3 |
|   S--Z                   | Ciphertext 4 |

Each ciphertext appears in its own plain text file, which you can open from the web site. 

(a) Make a table of frequencies for each letter in your ciphertext. That is, if the letter "A" appears 4 times, your table should show a frequency of 4 next to "A". Your table should consist of 26 rows (one for each letter) and then a number showing how many times that letter appeared in the ciphertext. 

(b) Now compare your table to [this table of frequencies of letters in English](http://www.math.cornell.edu/~mec/2003-2004/cryptography/subs/frequencies.html). For example, this table shows that the letter "E" is the most commonly-occurring letter in the English alphabet, appearing roughly 12.02% of the time in a random sample of 40,000 words. Based on your table and this table, make a guess as to what you believe the shift key was for the shift cipher used to encrypt your ciphertext. Include a brief, 2-3 sentence explanation of your reasoning. 

(c) Find the plaintext that corresponded to your ciphertext. When done, write out the full plaintext, a specific and detailed explanation for how you got the plaintext, and a sentence or two about whether the actual key was the key that you guessed in part (b). 