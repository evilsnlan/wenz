# wenz

First show the renderings
![image](https://github.com/evilsnlan/wenz/assets/61233992/94758b76-0a4b-4521-bb64-8851b2546fb1)

The vulnerability is presented in the background, need to log in to the background, first we build a website, version 2.2.9, registered administrator, enter the background
![image](https://github.com/evilsnlan/wenz/assets/61233992/04f080fb-34f2-4f57-9d23-0be15ec9c337)
Then go to user.php and manually add 3 registered users
![image](https://github.com/evilsnlan/wenz/assets/61233992/dac4e904-4672-4b6b-8630-1ba354fa19b4)
As you can see, the name of the registered user is random. Next, go to data.php and back up the user data
![image](https://github.com/evilsnlan/wenz/assets/61233992/49423131-4587-4a44-9655-7bef7a73332a)
![image](https://github.com/evilsnlan/wenz/assets/61233992/9ed0b6a6-c775-4479-a4af-84160e881124)
Then change the name field to an sql statement
![image](https://github.com/evilsnlan/wenz/assets/61233992/1878f850-d10f-44cc-b2de-3bf6d7f6fcbb)
Save the file and import it
Show successful
![image](https://github.com/evilsnlan/wenz/assets/61233992/74fa129d-8f25-4910-9a41-573b2931e09f)
At this time, we go to user.php to check and find that the corresponding sql statement has been executed for the user name
![image](https://github.com/evilsnlan/wenz/assets/61233992/cbc55031-76b7-4847-853f-5d45e300ad9b)
The reason is that Data.php does not apply strict filtering when importing data
