# Steps to Push and Upload an Existing Local Project into GitHub

  Create a Git repository and copy the git path
	Open VS code terminal and follow steps

	cd to the project directory
 
	git init -b master	        -> initialise git repository

	git add . 	                -> to add all files in current directory

	git rm --cache filename 	  -> to unstages the file

	git commit -m "Message"	    -> Commit code
		
	git remote add origin https://github.com/smitamadhu98/Hey-Nodejs-App.git		-> To Add remote repo location 

	git remote -v 	            -> Check origin header
	
	git status 		              -> to check git commits status

	git push origin master      -> Push the files to remore origin
