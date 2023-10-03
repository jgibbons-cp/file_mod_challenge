File Modification Challenge
--
  
Image:  
  
The docker image is built for linux/amd64 and linux/arm64 (e.g M1).  The 
image has ```vi``` installed.
  
Challenge:  
  
In ```/files``` there are two files -  
  
1) file_to_change  
2) file_to_append  
  
In file_to_change change the text of the file.  The change can be anything - remove/add a character/word
or change the whole line etc.
  
In file_to_append add another line to the file.  
  
Accessing the files:  
  
1) Kubernetes  
  
```kubectl create -f file_mod_challenge.yaml```  
  
and  
  
```kubectl exec -it file-mod-challenge -- bash```  
  
2) Docker  
  
```docker run -d --cap-add LINUX_IMMUTABLE --name file-mod-challenge jenksgibbons/file_mod_challenge:1.0```  

and  

```docker exec -it file-mod-challenge bash```    
  
Hints:  
  
1) There is something you don't normally see about the Kubernetes yaml and the docker run command.  You can complete the tasks, there is nothing blocking your ability to do so.  
2) Redirection could be helpful  
  
Have fun :)  
