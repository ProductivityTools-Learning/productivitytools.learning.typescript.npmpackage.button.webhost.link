Learning how to use npm link

In the package directory ```npm link```

![](Images/2023-04-14-06-40-55.png)

In the npm directory I have link to my project

![](Images/2023-04-14-06-50-49.png)


## Host project

Need to be written in typescript. 

### Add typescript to CommonJS project

```
npm install --save typescript @types/node @types/react @types/react-dom @types/jest
npm install --save-dev @types/react @types/react-dom
```

Rename files to tsx

Add tsconfig.json
```
{
  "compilerOptions": {
    "target": "es5",
    "module": "commonjs",
    "jsx": "react",
    "outDir": "./dist",
    "strict": true,
    "esModuleInterop": true
  },
  "include": [
    "./src/**/*"
  ]
}
```


Without having the dependency already installed do 

```npm link```

![](Images/2023-04-14-06-56-41.png)

This will create link in the **node_modules** to our package

![](Images/2023-04-14-06-57-43.png)

but package won't be added to package.json. Still you will be able to use it.