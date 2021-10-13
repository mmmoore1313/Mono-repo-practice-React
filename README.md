# Mono-repo-practice-React
> <details>
>   <summary>Contents</summary>
>
>> | [About](https://github.com/mmmoore1313/Mono-repo-practice-React#about) | [Technologies Used](https://github.com/mmmoore1313/Mono-repo-practice-React#technologies-used) |
>> |--|--|
>> | [Steps](https://github.com/mmmoore1313/Mono-repo-practice-React#steps) | [Links](https://github.com/mmmoore1313/Mono-repo-practice-React#links) |
>
> </details>
>
> ## About
>> <details>
>>  <summary>This is a practice repo adapted from and following the tutorial at <a href="https://monorepo.guide/getting-started">monorepo.guide</a>. The goal is to comfortably establish a process and understanding for the use of monorepos for development.</summary>
>>
>>>
>> ###### [(Return to top)](https://github.com/mmmoore1313/Mono-repo-practice-React#mono-repo-practice-react)
>>
>> </details>
>
> ## Steps
>> <details>
>>  <summary>Steps that I took to create the <b><a href="https://monorepo.guide/getting-started">Monorepo</a></b>.</summary>
>> 
>>> <details>
>>>  <summary>1. Initialize your repository</summary>
>>>
>>>> 1.1- ```mkdir <repo name>```  
>>>> 1.2- ```cd <repo name>```  
>>>> 1.3- ```git init```  
>>>
>>> </details>
>>> <details>
>>>  <summary>2. Add a <code>.gitignore</code> to your root directory</summary>
>>>
>>>> 2.1- ```touch .gitignore```  
>>>> <details>
>>>>  <summary>2.2- In the <code>.gitignore</code>, add:</summary>
>>>>
>>>>> ```  
>>>>> node_modules/
>>>>> .next
>>>>> dist
>>>>> ```  
>>>>
>>>> </details>
>>>
>>> </details>
>>> <details>
>>>  <summary>3. Create a <code>package.json</code> file to your root directory</summary>
>>>
>>>> 3.1- Run ```npm init```  
>>>> 3.2- Add the following:  
>>>>> ```  
>>>>> {
>>>>>   "name": "@monorepo-starter/root",
>>>>>   "version": "1.0.0",
>>>>>   "private": true
>>>>> } 
>>>
>>> </details>
>>> <details>
>>>  <summary>4. Set up your packages</summary>
>>>
>>>> 4.1- Add to your `package.json`:  
>>>>> ```  
>>>>> "workspaces": ["packages/*", "apps/*", "services/*"]
>>>>> ```  
>>>> 4.2- `package.json` example:  
>>>>> ```  
>>>>> {
>>>>>   "name": "@monorepo-starter/root",
>>>>>   "version": "1.0.0",
>>>>>   "private": true,
>>>>>   "workspaces": ["packages/*", "apps/*", "services/*"]
>>>>> }
>>>>> ```  
>>>
>>> </details>
>>> <details>
>>>  <summary>5. Create a <code>bable.config.js</code> at the root level</summary>
>>>
>>>> 5.1- ```touch babel.config.js```  
>>>> 5.2- Add to the `babel.config.js`:
>>>>> ```  
>>>>> module.exports = {
>>>>>   presets: ["@babel/preset-env", "@babel/preset-react"],
>>>>>   plugins: ["@babel/plugin-transform-runtime"]
>>>>> };
>>>>> ```  
>>>> 5.3- Install the babel plugins:  
>>>>> ```  
>>>>> yarn add @babel/core @babel/plugin-transform-runtime @babel/preset-env @babel/preset-react -W
>>>>> ```  
>>>
>>> </details>
>>> <details>
>>>  <summary>6. <a href="https://monorepo.guide/getting-started">Tutorial</a> Specific</summary>
>>>
>>>> <details>
>>>>  <summary>6.1- Add a starter button</summary>
>>>>
>>>>> <details>
>>>>>  <summary>6.1.1- Create a <code>packages/button</code> folder in the root directory</summary>
>>>>>
>>>>>> ```  
>>>>>> mkdir packages
>>>>>> mkdir packages/button
>>>>>> ``` 
>>>>>
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.1.2- Switch into the <code>packages/button</code> folder</summary>
>>>>>  
>>>>>> ``` 
>>>>>> cd packages/button
>>>>>> ``` 
>>>>>
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.1.3- Add a <code>package.json</code> file</summary>
>>>>>
>>>>>> ```  
>>>>>> npm init
>>>>>> ```  
>>>>>> - or -  
>>>>>> ``` 
>>>>>> touch package.json
>>>>>> ``` 
>>>>>
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.1.4- Fill out the <code>package.json</code> file</summary>
>>>>>
>>>>>> ``` 
>>>>>> {
>>>>>>    "name": "@monorepo-starter/button",  
>>>>>>    "version": "1.0.0",  
>>>>>>    "description": "A very simple React button within a monorepo"  
>>>>>> }
>>>>>> ``` 
>>>>>
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.1.5- Add react as a dependency</summary>
>>>>> 
>>>>>> ```  
>>>>>> yarn add react  
>>>>>> ``` 
>>>>>
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.1.6- Return to the root directory</summary>
>>>>>
>>>>>> ``` 
>>>>>> cd ../..
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.1.7- Create a <code>src</code> folder in your root directory</summary>
>>>>>
>>>>>> ``` 
>>>>>> mkdir src
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.1.8- Create a <code>Button</code> component to render</summary>
>>>>>
>>>>>> <details>
>>>>>>  <summary>6.1.8.1- Switch to the <code>src</code> directory</summary>
>>>>>>
>>>>>>> ```cd src```
>>>>>> </details>
>>>>>> <details>
>>>>>>  <summary>6.1.8.2- Create the <code>index.js</code></summary>
>>>>>>
>>>>>>> ```touch index.js```
>>>>>> </details>
>>>>>> <details>
>>>>>>  <summary>6.1.8.3- Fill out the <code>index.js</code> file</summary>
>>>>>>
>>>>>>> ``` 
>>>>>>> import React from "react";
>>>>>>> const Button = ({ onClick, children, isSelected }) => (
>>>>>>>   <button
>>>>>>>     style={{
>>>>>>>       border: 0,
>>>>>>>       backgroundColor: isSelected ? "rebeccapurple" : "hotpink",
>>>>>>>       color: isSelected ? "white" : "black",
>>>>>>>       padding: "12px 24px",
>>>>>>>       margin: "12px",
>>>>>>>       borderRadius: "3px"
>>>>>>>     }}
>>>>>>>     onClick={onClick}
>>>>>>>   >
>>>>>>>     {children}
>>>>>>>   </button>
>>>>>>> );
>>>>>>> export default Button;
>>>>>>> ``` 
>>>>>> </details>
>>>>
>>>> </details>
>>>> <details>
>>>>  <summary>6.2- Setting up the build process</summary>
>>>>
>>>>> <details>
>>>>>  <summary>6.2.1- Return to root level</summary>
>>>>>
>>>>>> ``` 
>>>>>> cd ../..
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.2.2- Run:</summary>
>>>>>
>>>>>> ``` 
>>>>>> yarn add @preconstruct/cli -W
>>>>>> yarn preconstruct init
>>>>>
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.2.3- Answer the questions</summary>
>>>>>
>>>>>>
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.2.4- Add the following to your root <code>package.json</code>
>>>>>
>>>>>> ``` 
>>>>>> "scripts": {
>>>>>> "postinstall": "preconstruct dev",
>>>>>> "build": "preconstruct build"
>>>>>> },
>>>>>> ``` 
>>>>> </details>
>>>>
>>>> </details>
>>>> <details>
>>>>  <summary>6.3- Adding <code>@monorepo-starter/next-app</code></summary>
>>>>
>>>>> <details> 
>>>>>  <summary>6.3.1- Create an <code>apps</code> folder in the root directory</summary>
>>>>>
>>>>>> ``` 
>>>>>> mkdir apps
>>>>>> mkdir apps/next-app
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.3.2- Create a <code>package.json</code> within <code>apps/next-app</code></summary>
>>>>>
>>>>>> ``` 
>>>>>> touch apps/next-app/package.json
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.3.3- Fill out <code>apps/next-app/package.json</code></summary>
>>>>>
>>>>>> ``` 
>>>>>> {
>>>>>> "name": "@monorepo-starter/next-app",
>>>>>> "version": "1.0.0"
>>>>>> }
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.3.4- Install Next.js</summary>
>>>>>
>>>>>> ``` 
>>>>>> yarn add react react-dom next @preconstruct/next
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.3.5- Add the <code>"scripts"</code> to the <code>next-app/package.json</code></summary>
>>>>>
>>>>>> ``` 
>>>>>> "scripts": {
>>>>>> "dev": "next",
>>>>>> "build": "next build",
>>>>>> "start": "next start"
>>>>>> },
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.3.6- Create a <code>next.config.js</code> file</summary>
>>>>>
>>>>>> ``` 
>>>>>> touch next.config.js
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.3.7- Add the following:</summary>
>>>>>
>>>>>> ``` 
>>>>>> const withPreconstruct = require("@preconstruct/next")
>>>>>> module.exports = withPreconstruct()
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.3.8- Install the button package to the <code>package.json</code>:</summary>
>>>>>
>>>>>> ``` 
>>>>>> "@monorepo-starter/button": "1.0.0",
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.3.9- Switch to the project root and run <code>yarn</code></summary>
>>>>>
>>>>>> ``` 
>>>>>> yarn
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.3.10- Create a <code>pages/index.js</code> file with the following:</summary>
>>>>>
>>>>>> ``` 
>>>>>> import React from "react";
>>>>>> import Button from "@monorepo-starter/button";
>>>>>> const Index = () => {
>>>>>>   return (
>>>>>>     <div>
>>>>>>       <Button isSelected onClick={() => alert("Hello!")}>
>>>>>>         Hello World!
>>>>>>       </Button>
>>>>>>     </div>
>>>>>>   );
>>>>>> };
>>>>>> export default Index;
>>>>>> ``` 
>>>>> </details>
>>>>> <details>
>>>>>  <summary>6.3.11- Run <code>yarn dev</code> and then visit <code>http://localhost:3000</code></summary>
>>>>>
>>>>>> ``` 
>>>>>> yarn dev
>>>>>> ``` 
>>>>> </details>
>>>> </details>
>>> </details>
>>
>> ###### [(Return to top)](https://github.com/mmmoore1313/Mono-repo-practice-React#mono-repo-practice-react)
>>
>> </details>
>
> ## Technologies Used
>> <details>
>>  <summary></summary>
>>
>>>
>> ###### [(Return to top)](https://github.com/mmmoore1313/Mono-repo-practice-React#mono-repo-practice-react)
>>
>> </details>
>
> ## Links
>> <details>
>>  <summary></summary>
>>
>>>
>> ###### [(Return to top)](https://github.com/mmmoore1313/Mono-repo-practice-React#mono-repo-practice-react)
>>
>> </details>
