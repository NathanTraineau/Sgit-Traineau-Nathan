# Sgit-Traineau-Nathan
The source code from a git-like scala application made for a School Project at Polytech Montpellier.

In order to use this program here is the instructions : 
First, download the jar file given in this repository.
Then in a linux command shell cd into the directory containing your .jar file, and run:
chmod +x program.jar
Next, run: nano ~/.bash_aliases
Then, add this line to the file: alias sgit='java -jar path/to/file/Sgit-Nathan-Traineau.jar’
It will store the alias in order to use it later
Exit nano saving changes, and restart the terminal window
Now, you can run it from anywhere like so:
custom_name {args}

     ⚠     If for some reason this doesn’t work you can write shell in order to create the alias and run the jar with the command : alias sgit='java -jar path/to/file/Sgit-Nathan-Traineau.jar’
and then when you type “sgit” into your shell this will launch the jar so you can type a command. 
But you will have to do this each session you want to use this program.

If for some reason you have an error like “Could Not Create the Java Virtual Machine” I recommend you to try the 2 methods, to fix this problem, described at : https://appuals.com/fix-could-not-create-the-java-virtual-machine/

Here are some explanation about the project : 
Input are dispatched toward several services, each of them has its own “main” function that orchester other functions and use the generic tools from the IO package (Input/Output) to store and display the changes.
First the user will give some order that will be parsed by the Command_Parser object, this parser will check if the service asked is available and will dispatch the information to the right service provider (the services are each of the files represented at the bottom line of the schema). This service will get the context of the user (which repository he is in) and then work on his own, using some services from other Services providers in order to deliver the asked service.
