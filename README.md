![examplephoto](https://user-images.githubusercontent.com/59976112/116780635-a07fc600-aa86-11eb-9045-80f893e78e3e.png)
![examplephoto](https://user-images.githubusercontent.com/59976112/116780638-a4134d00-aa86-11eb-8355-585c405b84d4.png)
# Flutter Widgets for Responsive Design

**FEEL FREE TO CONTRIBUTE**

## DeterminerWidget
DeterminerWidget provides you to make different layouts for every device type and orientation.

Usage:

```dart
DeterminerWidget(
          portraitMobile: Text("Portrait Mobile"), //Portrait Mobile must be provided. Others can be optional.
          landscapeMobile: Text("Landscape Mobile"),
          portraitTablet: Text("Portrait Tablet"),
          landscapeTablet: Text("Landscape Tablet"),
          desktop: Text("Desktop"),
        )
 ```
       
       
## InformerWidget
InformerWidget provides you all informations about screen.
Informations are currently provided:

- Screen size
- Parent widget's size
- Device type (Mobile,tablet,desktop)
- Screen orientation

Usage:

```dart
InformerWidget(
                onPageBuild: (context, information) {
                  return Container(
                    //return a widget with informations
                    child: Text(information.toString()),
                    height: information.boundsSize.height * 0.5,
                    width: information.customDeviceType == CustomDeviceType.mobile ? 100 : 300,
                  );
                },
              )
```

<img src="https://user-images.githubusercontent.com/59976112/116780489-d7a1a780-aa85-11eb-8639-435cfcdd3ed7.png" alt="Example photo" width="400" height="700">

