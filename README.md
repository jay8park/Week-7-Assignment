# Week-7-Assignment
Codepath Week 7  

## Authenticated Stored Cross Site Scripting:  
Look at the references from doing: wpscan --url http://wpdistillery.vm --random-agent  
You can see one called "Authenticated Store Cross Site Scripting."  
The vulnerability type is XSS, and I tested this in version 4.2. This was fixed in version 4.2.21.  
This was done in version 4.2, and this problem was fixed in version 4.2.21.  
gif: <img src="Week 7(1)" width="800">  
Essentially, type in this: <a href="[caption code=">]</a><a title=" onmouseover=alert('bruh')  ">link</a>  in the content type, or "text" section of WordPress. After you publish/update the post, view it, and click on the link. Then, a JS alert that says "bruh" should pop up.  
The affected source code is   

## Unathenticated Stored Cross Site Scripting:   
The vulnerability type is XSS, and the version I tested this in was 4.2. All versions before 4.2.1 are vulnerable to this (fixed in version 4.2.1).
gif:
Essentially, to recreate this, I added a text so that JS can be injected through the comments as long as it exceeds the size limit, which is 64 kilobytes. 

## Authenticated Shortcode Tags Cross Site Scripting:  
The vulnerability type is XSS, and the version test this on was 4.2. All versions before 4.2.5 are vulnerable to this (so, fixed in version 4.2.5). 
gif: 
Essentially, using one of the reference links, copy and paste one of the code. WP will process it to get rid of the brackets. Essentially, we're creating a fake link, so when a mouse moves over this link, a JS alert pops up. 
