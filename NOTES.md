-> vue cli documentation can be checked in cli.vue.org
-> we install it globally in the terminal: npm i -g @vue/cli
-> to open vue GUI where we can manage our view projects: vue ui
-> to create a vue project: vue create my-project
-> from there we select: default vue 3 >> dedicated config files >> No for save it as preset
-> to open project in vs code: cd my-project >> code .
-> to open the dev server: npm run serve

Code structure:
-> inside the public folder, the file index.html is the single page that's loaded in the browser. It has a div with id of app.
-> inside the src folder, the file main.js which is the entry point for vue. Here we import our root App component from a separate file called App.vue, passing that App component to createApp and mounting it to that div in index.html with id of app.

Components:
-> App.vue file has the root component that has three parts: the template (the output html), the script, the styling.
-> everything we do goes through App.use, Any component we create is gonna embed in here.
-> every component we create (apart from App.vue) resides in components folder in src folder.
-> When we export a component we specify its name in its export statement.
-> We have a import statement where we specify the component name and the location of the component(s) we are importing.
-> When we import the components we have to first define it in the components object of the component which is importing.

“Props” is a keyword stands for properties. It can be registered on a component to pass data from a parent component to one of its children components (one-way and read only).
-> We can pass props into a component (here title prop in App.vue) and if we want to work with that prop in our component (Header.vue), we need to define prop by making an array or object with the names of props on it. Additionally, for each prop within the array we can define the prob as an object with the type and default value.

Data:
-> We have task component to pass the data into so we can render it on the page.

Deleting a Task:
We want to delete the task whenever we click x button. The issue here is that the buttons are in the task component which is 2 levels deep the App.vue component where the tasks are present.
So we have to make events emits up so that we can have functions in our main app.

Creating a Task:
for this we create a new component AddTask with a form. Whatever goes to each field in the form is added as data, and bind these data values to the input to the form using v-model.
Now when we submit the form, we call method onSubmit

-> to build you static assets for deployment, we run the command npm run build
this creates a folder called dist, which is what we actually deploy.
we can test the dist folder out locally by using < npm i -g serve> and then < serve -s dist >

-> We install json server by < npm i json-server >
-> To run the json server we do < npm run jserver >

-> with vue.js we can add a proxy with a config file. Within the proxy we can set all rules e.g. if we hit /api then we are hitting http:/localhost/5000

Vue Router:
to install the router we do < npm i vue-router@next >
To implement the router, in our src folder we need to create a folder called router. Inside it we have index.js file where we create the router.
Every view (in the view folder in src) we create for any page should be imported into index.js file.
Now we create an array of routes where each route would gonna be an object.
In order to use the router, we have to go to main.js (the entry point) and import that router file.

We can pass a value using props from our main app file (App.vue) into any view component.
