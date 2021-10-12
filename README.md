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
>>>> 1.1- `mkdir <repo name>`  
>>>> 1.2- `cd <repo name>`  
>>>> 1.3- `git init`  
>>>
>>> </details>
>>> <details>
>>>  <summary>2. Add a <code>.gitignore</code> to your root directory</summary>
>>>
>>>> 2.1- `touch .gitignore`  
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
>>>> 3.1- Run `npm init`  
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
>>>> 5.1- `touch babel.config.js`  
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
>>>  <summary>6. Tutorial Specific</summary>
>>>
>>>> <details>
>>>>  <summary>6.1- Add a starter button</summary>
>>>>
>>>>> 6.1.1- Create a `packages/button` folder in the root directory  
>>>>>> ```  
>>>>>> mkdir packages/button
>>>>>> ```  
>>>>> 6.1.2- Switch into the `packages/button` folder  
>>>>>> ```
>>>>>> cd packages/button
>>>>>> ```  
>>>>> 6.1.3- Add a `package.json` file  
>>>>>> ```  
>>>>>> npm init
>>>>>> ```  
>>>>> 6.1.4- Fill out the `package.json` file
>>>>>> ```
>>>>>> {
>>>>>>    "name": "@monorepo-starter/button",  
>>>>>>    "version": "1.0.0",  
>>>>>>    "description": "A very simple React button within a monorepo"  
>>>>>> }
>>>>>> ```  
>>>>> 6.1.5- Add react as a dependency  
>>>>>> ```  
>>>>>> yarn add react  
>>>>>> ```  
>>>>>
>>>>
>>>> </details>
>>>
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
