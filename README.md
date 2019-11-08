# test-electron

## Docs

- [Build a Desktop Application with Electron and Angular](https://www.sitepoint.com/build-a-desktop-application-with-electron-and-angular/)
- [electron-builder](https://github.com/electron-userland/electron-builder)
- [A complete guide to packaging your Electron app](https://medium.com/how-to-electron/a-complete-guide-to-packaging-your-electron-app-1bdc717d739f)

## Recipe
In order to make it work, you have to be sure that the Angular project is build and can therefore, run without Angular Server: [Here](https://github.com/angular/angular/issues/13948#issuecomment-302727428)
1. Router Configuration with
```js
CommonModule,RouterModule.forRoot(routes,{useHash:true}) 
```
2. and this in the index.html file: Removed base Href="/" tag from html and added it like this.
```html
<script>document.write('<base href="' + document.location + '" />');</script>
```
