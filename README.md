# Mono-repo-practice-React
> <details>
>   <summary>Contents</summary>
>
>> | [About]() | [Technologies Used]() |
>> |--|--|
>> | [Steps]() | [Links]() |
>
> </details>
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
>>>  <summary>2. Add a <code>.gitignore</code></summary>
>>>
>>>> 2.1- `touch .gitignore`  
>>>> 2.2- In the `.gitignore`, add:  
>>>>> ```
>>>>> node_modules/
>>>>> .next
>>>>> dist
>>>>> ```
>>>
>>> </details>
>>> <details>
>>>  <summary>3. Create a <code>package.json</code> file</summary>
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
>>>>>`"workspaces": ["packages/*", "apps/*", "services/*"]`  
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
>> ###### [(Return to top)]()
>>
>> </details>
>
> ## Technologies Used
>> <details>
>>  <summary></summary>
>>
>>>
>> ###### [(Return to top)]()
>>
>> </details>
>
> ## Links
>> <details>
>>  <summary></summary>
>>
>>>
>> ###### [(Return to top)]()
>>
>> </details>
