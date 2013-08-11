## A cool way to install the git

Yesterday, I receive a request to upgrade the git version, currently, we use the 1.6.0, it is too old. But it works well in most of times.

Next, let's check how we install the git using a cool way.

1. Clone the git repo from the 
	[https://github.com/git/git.git](https://github.com/git/git.git "git hub")
  
  
	`git clone https://github.com/git/git.git`

2. Fetch the latest tag
	   
	`git fetch`

3. Get the tag list

	`git tag -l`

	After that, you can get a list.

4. 	Checkout the version you liked.
	
	`git checkout V1.7.3`
5. Try to build the project
	
	`make prefix=/usr/local all`    
	`make prefix=/usr/local install`
	
	`which git`  
	`/usr/local/bin/git`
6. Check the current version   
	git --version  
	git version 1.7.3

Ok, that's easy and easy to maintain in the future.

Cheers!
