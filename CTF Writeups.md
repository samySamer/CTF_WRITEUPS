# Encoding:
- First we got to the view page sources we found a hint : User : Guest & password:Guest
- Then when we got inside we opened the cookies to see what inside we found a base 64 encrypted : Login =Guest7
- so we turned it to Login = Admin and encrypted it again to and put it in the cookies
- we Found the Flag!
# Traversal : 
- So first we got in the website and we found nothing but a horrifying mr bean picture so we got in the view source code and we found nothing
- so we thought we would look for dirsearch as it could tell us about the directories of the website so we found a files when we tried to get in a directory it gave us nginx error so we found out that it is using Nginx
- From the Challenge description it told use to get back to home so we used this hint and we tried to get to the home of the website 
- so when we searched in the nginx Commands we found an alias for returning to the previous directory .. 
- when we pressed it we found a directory called home and we pressed on it and we Viola we found the flag.
# Sql Injection:
- First we got in the website and found out that there is a username and password 
- so we tried to put user:admin password:admin but it didn't work then we used user user and nothing 
- first tried to see the view source we found bob and password we found nothing but only admin can see flag
- Since it was sql Injection we tried out payloads when we logged out like
``` sql
'1=1 -- -
```
- but it didn't work as it and told us a syntax error so we used another one 
```sql
' OR 1-- -
```
- and it opened and we found the flag!
# Metadata:
- When opening the page we found out that the page contains password so we tried to type anything but it didn't work
- so we thought of the images and work on it as a metadata so we used exiftool but it weirdly didn't work 
- so we tried to look in the view page source part and we found a very weird thing that there is img/the_eye.jpeg and the_eye.jpeg
- so we thought about downloading them and comparing each of them 
- when we compared them with command diff we found a binary difference between them 
- so we tried exiftool on the new img and we found the flag on the Rights part.
# WireShark:
- we opened the program we used find items and typed flag but it didn't work
- so we used f1ag but it still didn't work
- then we used f14g and we found the packet containing the flag.

# Morse CODE :
- it was simple we downloaded the file 
- and we used an a morse code website to decrypt it called : https://morsecode.world/international/decoder/audio-decoder-adaptive.html
- it gave us this A T T T T T T T T T T TI A G I S I A M S P E A K I N G L O U D E R T H A N B E F O R E 
- so we took from I AM SPEAKING LOUDERTHANBEFORE 
- and it was the flag.

# Ceaser Cipher:
- the Text it gave us contained EBG13 So we thought it was a ROT13 
- we opened a decryption website called Cyber Chef
- and we found this text with flag on it:
- the flag is ........... It is pretty easy to see the flag but can you see it i took nearly 1 minute to encode this with ROT13 good luck in solving that.
# Hash:
- we took the password and put it in website hashes
- and it gave us the flag.
