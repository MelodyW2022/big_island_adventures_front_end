# big-island-adventures_front_end
## Table of contents
* [General info](#general-info)
* [Technologies](#technologies)
* [Setup](#setup)

## General info
Big Island Adventures is a web application built using Python, Flask, React, React-Bootstrap, React Router DOM, HTML, CSS, Javascript, and PostgreSQL. 
It uses the AccuWeather API to provide users with tour suggestions based on the weather condition of the selected location in Big Island Hawaii. 
The app features CRUD operations and registration, login, and logout functionalities for users. 
Users can book tours and view them in their dashboard. The app's highlight is its ability to provide personalized tour suggestions based on the weather condition of the user's selected location. 
The app is hosted on Heroku.
	
## Technologies
Python, Flask, React, React-Bootstrap, React Router DOM, HTML, CSS, Javascript, and PostgreSQL, Pytest and Jest testing frameworks.
	
## Front-End Layer Setup

Feel free to follow these steps on one machine in this order exactly.

<details>

<summary>Click here to expand front-end layer setup steps.</summary>

### Clone

Clone the forked repo. Do _not_ clone this inside of another project folder, because that will cause issues.

### Scaffold the App

Create a new React app within this project folder. **You must perform this within this front-end project folder**.

```bash
$ npx create-react-app .
```

### Add `axios`

Install axios:

```bash
$ yarn add axios
```

### Creating a `.env` File

Create a file named `.env`.

The front-end layer needs to send API requests to the back-end layer. In order to handle this, the front-end layer repo **must** include a `.env` file with this line:

```
REACT_APP_BACKEND_URL=http://localhost:5000
```

Note that this `REACT_APP_BACKEND_URL` _must_ include `http://`.

Use this environment variable to send your API requests. You can read it by using the expression `process.env.REACT_APP_BACKEND_URL`. For example, we may use it like this in any component:

```js
axios.get(`${process.env.REACT_APP_BACKEND_URL}/boards`, {
    // ...
```

This will make Heroku deployment easier.

### Commit and Push

Commit and push your files to your repo, especially including the `package.json` file!

</details> 
  
