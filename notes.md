# How I Made It

Since this is my first real dive into Angular, I wanted to loosely follow their [Tour of Heroes Tutorial](https://angular.io/tutorial)
The introduction for the tutorial includes a lot of visuals on what the final product should look like. 
Obviously, this is not a Reddit Clone so I will be branching off once I've gotten a firm grasp of fundamentals.
*Note: I will be using Visual Studio Code since that is my preferred IDE.*

## Starting Out
You'll need to install the [Angular CLI](https://angular.io/guide/quickstart#install-cli) if you haven't already done so:
`npm install -g @angular/cli`. Then initialize a project `ng new app-name`. There you'll be asked for some specifics on 
how you'd like the environment set (I just went with defaults as instructed). Here's what you should see in your IDE at 
this point (minus the `notes.md` since I added that myself):

<img src="/public/angular-init.png"/>

Angular conveniently includes a server for you to serve you app locally. To use this, go into your workspace folder and 
enter `ng serve --open`. The `--open` is optional but if you don't do it, you'll have to manually go into the browser
and enter whatever port the server has been assigned to: `http://localhost:4200/`. 

The page you see opened is the *application shell* which is controlled by an Angular component named `AppComponent`.
**It is vital to understand components as they are the fundamental building blocks of Angular applications**. 
The components display data on the screen, listen for user input, and respond based on the inputs.

Get familiar with the application by making changes to the starter: 
* Go to the implementation of the shell `AppComponent`: `src/app`. Inside of this folder you should see a list of files
all beginning with `app.component`. **Do this while you can see the browser so you can watch it change as you type.**
* Change the title of the application: go into the `ts` (TypeScript) component class
file and change the value of `title`. 
* Go into the `app.component.html` file and edit as much as you'd like to. For now, I'm just going to remove everything 
but the title. 

The `{{ }}` are Angular's *interpolation binding* syntax which places the component's `title` property (in this case)
value inside the HTML header tag. 