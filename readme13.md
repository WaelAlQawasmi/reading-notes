 # Notifications

 if you  would to allow a ther apps to start  activity in the app you must
add  
> < intent-filter> 
element in  manifest file of app  for the corresponding < activity>

- When the app is installed , the system  adds the information to an internal catalog of intents supported by all installed apps. 

- When   calls  the app __startActivity()__ or __startActivityForResult()__ with an implicit intent the system finds whichor activities can respond to the intent.

## Add an Intent Filter

The system may send  Intent to an activity if that activity has an intent filter fulfills the following criteria of the Intent :
 
 - Action : naming the action to perform values such as ACTION_SEND or ACTION_VIEW.

 - Data : Data
A description of the data associated with the intent.
Specify this in your intent filter with the < data> element

 - Category : category
provides an additional way to characterize the activity handling the intent


### ex
> <activity android:name="ShareActivity">
    <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="text/plain"/>
        <data android:mimeType="image/*"/>
    </intent-filter>
</activity>

## Intent types
There are two types: 

1. Explicit intent: specify which application will satisfy the intent, by supplying either the target app's package name or a fully-qualified component class name. 
2. Implicit intent: it  allow a component from another app to handle it. 

![intents](https://developer.android.com/images/components/intent-filters_2x.png)



## resorses
-[ref1](https://developer.android.com/training/basics/intents/filters)
-[ref1](https://developer.android.com/guide/components/intents-filters#Types)