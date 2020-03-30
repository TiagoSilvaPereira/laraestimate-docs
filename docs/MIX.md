# Compiling Assets with Laravel Mix

All the CSS and JavaScript (including the VueJS components) inside the LaraEstimate system are compiled and versioned with Laravel Mix. To modify JavaScript or CSS (SASS), you need first to install:

- [NodeJS](https://nodejs.org/)
- [Laravel Mix](https://laravel.com/docs/7.x/mix)

And then, you can compile your assets:

To compile and version the development scripts, you can run 

```
npm run dev
```

To compile and version the production scripts, you can run 

```
npm run production
```

Or you can run a Watcher, that verifies and compiles your scripts ever you modify them: 

```
npm run watch
```

All the assets that can be compiled are in the resources folder and the compiled assets are in the public folder. You can modify the Assets Compilation Settings inside the **webpack.mix.js** file.