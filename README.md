# CPMS(Backend)


REST API for [CPMS](https://github.com/thunderbolt-25/cpms_frontend)

## Setting Up

Clone the project:

```bash
  git clone https://github.com/thunderbolt-25/cpms_backend.git
```

Change Directory:

```bash
  cd cpms_backend
```

Install dependencies:

```bash
  npm install
```

Create a .env file and paste your MongoDB Database Key [(reference video)](https://m.youtube.com/watch?v=-PdjUx9JZ2E):

```javascript
  DATABASE_URI = mongodb+srv:/username:password@.....mongodb.net/kollege
  // you can give a name of your preference to database instead of kollege
```

Start the server (node v.19+):

```bash
  npm run dev
```

### Allowing requests without headers during development

Inside config/corsOptions.js, uncomment "|| !origin" part during development

```javascript
 if (
      allowedOrigins.indexOf(origin) !== -1
      //! comment out/remove in production
       || !origin
    )
```

### Adding HOD

Since admin isn't added yet - HOD manages most things.  
You'll need to add an HOD manually.  
🚀 Use a REST API client like Postman/Thunder Client.

Request Method: **POST**  
Request Address: **<http://localhost:3500/staff>**  
    // the port should be where you host the server, 3500 by default, and not the react port i.e, 3000
Request Body:

```javascript
  {
"name":"...",
"email":"...",
"department":"Computer",
"username":"...",
"password":"...",
"role":"HOD"
  }
```

- ❗Don't forget to fill **"..."** with necessary details instead of leaving it as it is.

#### NOTE

Don't forget to comment out "|| !origin" Inside config/corsOptions.js after development.

```javascript
 if (
      allowedOrigins.indexOf(origin) !== -1
      //! comment out/remove in production
      // || !origin
    )
```

Continue to [Kollege Documentation](https://github.com/iafthab/kollege/#readme)

### Still getting errors?

Go to config/corsOptions.js. Make sure your front-end address is included in allowedOptions:

```javascript
const allowedOrigins = [
  "http://localhost:3000",
  // Add the address if you host your front-end somewhere
  "https://example.address.com",
];
```

## Acknowledgements

- Node,js Tutorial by [@gitdagray](https://github.com/gitdagray)

## Related

[CPMS](https://github.com/thunderbolt-25/cpms_frontend)

## License

[MIT](https://choosealicense.com/licenses/mit/)
