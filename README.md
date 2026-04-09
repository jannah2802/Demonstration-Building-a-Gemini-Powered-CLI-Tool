# Demonstration-Building-a-Gemini-Powered-CLI-Tool

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

