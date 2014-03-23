
### What is it
AppKit() - is a framework to create apps for 
	* mobile
	* desktop
	* web
where the UI is HTML (JS/CSS) rendered and backend is coded in your favorite language.

Work is in progres. The project is Blink based. More info here http://rockblink.blogspot.com

![](https://raw.github.com/ukoreh/appkit/master/jskit.png) 
![](https://raw.github.com/ukoreh/appkit/master/csskit.png) 

### Example JsKit

```js
// app speciffic header files
include( "CentralWidget.js" );

// define an entry point into the app
function main()
{
    var centralWidget = new CentralWidget();

    var mainWindow = new JsKit.Gui.MainWindow();
        mainWindow.setDefaultLayoutManagers();
        mainWindow.setTitle( "JS Application" );
        mainWindow.getCentralArea().appendWidget( centralWidget );

    var application = new JsKit.Core.Application();
        application.setMainWindow( mainWindow );
        application.run();
}

// run the app
main();
````

### Demo JsKit
http://ukoreh.github.io/appkit/JsKitDemo/index.html
