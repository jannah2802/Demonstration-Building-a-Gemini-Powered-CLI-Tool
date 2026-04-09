# Demonstration-Building-a-Gemini-Powered-CLI-Tool

	To run this file must install:-
	- must have Gemini API Key and replace in .env file
	- dotenv
	- google-generativeai
	- run python main.py
	- Try any prompt
	- To exit app

	This code consist of the following file:

	1. .env file
		a. To ensure that the API key is never exposed in our main code
	2. Gemini_provider.py
		a. Dedicated API connector module to handle all communication with Google Gemini API
		b. Must have some libraries to be imported such as os, load.env, classes from Gemini, configure (to innitialize SDK securely)
		c. To specify our model use, must have a Function, called gemini-response. Which take user question, sends it to the configured Gemini model using model generate-content, and returns the raw text output. This can be reusable function.
    
    3. Main.py
		  a. This file handles user interface, input loop, and calls provider module.
		  b. Imported libraries like time, sys, gemini_provider.py file
		  c. Defined two helper functions, 
			  i. Banner - prints a nice header for our CLI application
			  ii. Loading - prints dots to give the user visual fee that the program is working, improve user experience.
			d. Core function in the main loop
							i. Add banner
			ii. While loop - STANDARD WAY TO KEEP APPLICATION RUNNING UNTIL USER DECIDES TO QUIT.
				Read user input	
				Check if the input :-	
				        1. if user enter 'exit/exit()/quit' it end application/break the loop cleanly, 
				        2. if not user need to enter valid prompt,
				                a. Call loading function to sgnal processing
				                b. Output equals to gemini_response()
				                        
<img width="809" height="274" alt="image" src="https://github.com/user-attachments/assets/902b3739-6e89-4b34-a2d6-3619787bcd86" />

			e. End the call with 'try-except' bock = pro way to handle potential errors, like network issue or an invalid API key, without crashing the entire app.
		
			f. Print output


