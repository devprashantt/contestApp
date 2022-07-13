# GetX

## The Three pillars 

### State management 

Get has two different state managers: the simple state manager (we'll call it GetBuilder) and the reactive state manager (GetX/Obx)

### Reactive State Manager 

Reactive programming can alienate many people because it is said to be complicated. GetX turns reactive programming into something quite simple:

    You won't need to create StreamControllers.
    You won't need to create a StreamBuilder for each variable
    You will not need to create a class for each state.
    You will not need to create a get for an initial value.
    You will not need to use code generators
    Reactive programming with Get is as easy as using setState.

Let's imagine that you have a name variable and want that every time you change it, all widgets that use it are automatically changed.

This is your count variable:

    var name = 'Jonatas Borges';
    
To make it observable, you just need to add ".obs" to the end of it:

    var name = 'Jonatas Borges'.obs;
    
And in the UI, when you want to show that value and update the screen whenever the values changes, simply do this:

    Obx(() => Text("${controller.name}"));
    
That's all. It's that simple.

More details about state management 

See an more in-depth explanation of state management here. There you will see more examples and also the difference between the simple state manager and the reactive state manager

You will get a good idea of GetX power.


### Route management 

If you are going to use routes/snackbars/dialogs/bottomsheets without context, GetX is excellent for you too, just see it:

Add "Get" before your MaterialApp, turning it into GetMaterialApp

    GetMaterialApp( // Before: MaterialApp(
      home: MyHome(),
    )
    
Navigate to a new screen:

    Get.to(NextScreen());
    
Navigate to new screen with name. See more details on named routes here


    Get.toNamed('/details');
    
To close snackbars, dialogs, bottomsheets, or anything you would normally close with Navigator.pop(context);

    Get.back();
    
To go to the next screen and no option to go back to the previous screen (for use in SplashScreens, login screens, etc.)

    Get.off(NextScreen());
    
To go to the next screen and cancel all previous routes (useful in shopping carts, polls, and tests)

    Get.offAll(NextScreen());
    
Noticed that you didn't have to use context to do any of these things? That's one of the biggest advantages of using Get route management. With this, you can execute all these methods from within your controller class, without worries.

## Screenshots

<img src="screenshots/img (1).png" width="150" height="300"> <img src="screenshots/img (2).png" width="150" height="300"> <img src="screenshots/img (3).png" width="150" height="300"> <img src="screenshots/img (4).png" width="150" height="300"> <img src="screenshots/img (5).png" width="150" height="300"> <img src="screenshots/img (6).png" width="150" height="300"> <img src="screenshots/img (7).png" width="150" height="300"> <img src="screenshots/img (8).png" width="150" height="300">
