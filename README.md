![slider_document](banner.png)

# Customized Flutter Slider Drawer
[![pub package](https://img.shields.io/pub/v/flutter_slider_drawer)](https://pub.dev/packages/flutter_slider_drawer)   [![pub package](https://img.shields.io/github/languages/code-size/NikhilVadoliya/Flutter_slider_drawer)](https://pub.dev/packages/flutter_slider_drawer)

A Flutter package with custom implementation of the Slider Drawer Menu 


To start using this package, add `customized_flutter_slider_drawer` dependency to your `pubspec.yaml`

```yaml
dependencies:
 customized_flutter_slider_drawer: '<latest_release>'
```

# Features

  - Slider with custom animation time
  - Provide Basic Appbar with customization of color and title
  - Dynamic slider open and close offset
  - Provide drawer icon animation 
  - Provide shadow of Main screen with customization of shadow colors,blurRadius and spreadRadius
  - Provide RTL(RightToLeft),LTR(LeftToRight) and TTB(TopToBottom) slider open selection
  - Provide Custom Appbar support and you can also use plugin appBar with use of `SliderAppBar` widget
  - If you are using CupertinoApp then pass `isCupertino: true`
    # new feature
  - add onDrawerTap
  - Customizing the open and close icon 


# Code
```
  Widget build(BuildContext context) {
    return Scaffold(
      body: SliderDrawer(
        key: _sliderDrawerKey,
/// this appBarConfig required it is like what you put in confing
        appBarConfig: SliderAppBarConfig(
                animationController: drawerController,
                drawerOpenIcon: const AssetImage(CustomAssets.drawerImageOpen),
                drawerCloseIcon: const AssetImage(CustomAssets.drawerImageClose),
                padding: const EdgeInsets.all(0),
                title: Text("App Bar"),
              ),
        appBar: SliderAppBar(
          config: SliderAppBarConfig(
/// Customizing open and close icon for drawer
            drawerOpenIcon: const AssetImage(CustomAssets.drawerImageOpen),
           drawerCloseIcon: const AssetImage(CustomAssets.drawerImageClose),

            title: Text(
              title,
              textAlign: TextAlign.center,
              style: const TextStyle(
                fontSize: 22,
                fontWeight: FontWeight.w700,
              ),
            ),
          ),
        ),
        sliderOpenSize: 179,
        slider: Container(color: Colors.red),
        child: Container(color: Colors.amber),
      ),
    );
  }
 ```

</br>
 </br>

 ![slider_document](information.png)
 </br>
 </br>
 </br>
 </br>


 # Slider open  

 | SliderOpen.LEFT_TO_RIGHT  | SliderOpen.RIGHT_TO_LEFT  | SliderOpen.TOP_TO_BOTTOM  |
 |---|---|---|
 | ![slider_left](slide_left.gif)  | ![slider_right](slide_right.gif)  | ![slider_top](slide_top.gif)  |
 
 
 
 </br>

### Controlling the drawer

```
class _MyAppState extends State<MyApp> {
   GlobalKey<SliderDrawerState> _sliderDrawerKey =
      GlobalKey<SliderDrawerState>();

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: SliderDrawer(
        key: _sliderDrawerKey,
/// this appBarConfig required it is like what you put in confing
        appBarConfig: SliderAppBarConfig(
                animationController: drawerController,
                drawerOpenIcon: const AssetImage(CustomAssets.drawerImageOpen),
                drawerCloseIcon: const AssetImage(CustomAssets.drawerImageClose),
                padding: const EdgeInsets.all(0),
                title: Text("App Bar"),
              ),
        appBar: SliderAppBar(
/// this let you to do something when you click on the drawer (when you're opening and closing drawer)
                  onDrawerTap: () {
                    debugPrint("Drawer is open in on DrawerTap");
                  },

          config: SliderAppBarConfig(
            title: Text(
              title,
              textAlign: TextAlign.center,
              style: const TextStyle(
                fontSize: 22,
                fontWeight: FontWeight.w700,
              ),
            ),
          ),
        ),
        sliderOpenSize: 179,
        slider: Container(color: Colors.red),
        child: Container(color: Colors.amber),
      ),
    );
  }
}
      
```

* Using the below methods to control drawer .
``` 
 _sliderDrawerKey.currentState.closeDrawer();
 _sliderDrawerKey.currentState.openDrawer();
 _sliderDrawerKey.currentState.toggle();
 _sliderDrawerKey.currentState.isDrawerOpen();

 ```
* Use below variable if you want to control animation.


``` __sliderDrawerKey.currentState.animationController```
