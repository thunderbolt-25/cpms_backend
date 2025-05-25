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



#### NOTE

Don't forget to comment out "|| !origin" Inside config/corsOptions.js after development.

```javascript
 if (
      allowedOrigins.indexOf(origin) !== -1
      //! comment out/remove in production
      // || !origin
    )
```


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

