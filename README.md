# Juide
Juide is an acronym for _Java User Interface Development Environment_.

Juide is a tool to develop multi-platform desktop applications using your favorite web technologies. It's built using the Java programming language and the JavaFX library. Build UI for your desktop application using the web tech stack of your choice. Serve up dynamic content from the web or point to a local static website. 

### Setting up a new project with Juide
Copy the contents of the `build\juide-deploy` directory to your desired location. Modify the `config.json` file to meet the needs of your project.  Launch the `juide-x.x.x.jar` with the provided `run-juide.sh` or `run-juide.bat` depending on your target platform. You may rename the jar or run files to meet the needs of your project. 

> [!NOTE]
> Be sure to set either the url or local file path of your web content!

#### Deployment File Details
- `build\juide-deploy\juide-x.x.x.jar` - This is the main Juide deployment jar. This is what you will ultimately run in order to launch your desktop app. The provided run files invoke this jar.
- `build\juide-deploy\config.json` - The config file responsible for defining a lot of the behavior for the Juide app. This is where you will define the window style and content. 
- `build\juide-deploy\run-juide.sh` - A run shell script supporting Linux and MacOS environments. This will invoke the Juide jar. You can modify this to include jvm arguments or shell commands as needed.
- `build\juide-deploy\run-juide.bat` - A run batch script supporting Windows environments. This will invoke the Juide jar. You can modify this to include jvm arguments or shell commands as needed.
- `build\juide-deploy\web\index.html` - The starter html document used for new Juide deployments. You can modify this file or use whatever structure you prefer. Just be sure to update the config.json file with the changes you need.

### Building from source
Run `mvn package` to create the jar for the Juide project. Open command prompt/terminal and use the Java jar command to run the jar. 

```
java -jar juide-0.0.1-SNAPSHOT.jar
```

### Configure your desktop application using simple JSON
Modify the look and feel of your application without the need to recompile source code. A breakdown of each configurable JSON field is included below:

| JSON Setting | Description | Type | Default
| --- | --- | --- | --- |
| windowTitle | Text that displays in the window header | String | "Juide App" |
| url | If useUrl is true, this url will serve the conent for the Juide App. | Url String | "http://127.0.0.1:8080" |
| useUrl | Used to tell the Juide App to load content from a specified url instead of a local file path. | Boolean | false |
| localPath | Used to specify the entry point to a local web file to serve content. | String | "/build/index.html" |
| enableResizable | Determines if the user can resize the window dimensions using the window border. | Boolean | false |
| windowX | Defines the window width or x coordinate dimensions. | Integer | 960 |
| windowY | Defines the window height or y coordinate dimensions. | Integer | 680 |
| disableContextMenu | Disables the right-click context menu. | Boolean | true |
| alwaysOnTop | Specifies that the Juide App should remain in the foreground once launched. | Boolean | true |
| centerOnScreen | Tells the Juide App to center itself to fit the user's screen once launched. | Boolean | false |
| fullscreen | Force fullscreen mode once the Juide App launches. | Boolean | false |
| windowStyle | Defines the style for the Juide App Window. The available values correspond to the JavaFX window styles supported. | String - "DECORATED", "UNDECORATED", "TRANSPARENT", "UNIFIED", "UTILITY" | "DECORATED" |
| userAgent | Define a user agent string that will be used by the Juide App. | String | "" |

### Extend the web UI with native desktop integrations
Create experiences that feel native to your user's environment with less effort. Integrate your web code with the bundled Java code. 

### TODO

### Bundle your own custom Java code 
Further extend the capabilities of your Juide app by bundling your own custom Java code that integrates with your UI. 

### TODO

### Fork this project to create something totally new
Want to use this project as the basis for something else? No sweat! This project is governed by the MIT License so you're free to do whatever you want in either a commercial or non-commercial capacity.

### Interested in contributing?
Contributions to this project are certainly welcome. Feel free to write up issues or offer suggestions that you would like to see make it into the project. However, there is no guarantee that every issue or suggestion will make it into the project. 
