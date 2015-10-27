Top Snackbar
==========================

Show a Snackbar from the top.


![alt text](https://raw.githubusercontent.com/AndreiD/TSnackBar/master/app/snackbar.gif "How the app looks 1")



### Instalation:

in your app build.gradle add

~~~~
compile 'com.androidadvance:topsnackbar:0.0.6'
~~~~



### How to use it:


##### Example 1: Simple usage:

~~~~
TSnackbar.make(findViewById(android.R.id.content),"Hello from TSnackBar.",TSnackbar.LENGTH_LONG).show();
~~~~

##### Example 2: Custom colors:

~~~~
TSnackbar snackbar = TSnackbar.make(findViewById(android.R.id.content), "A Snackbar is a lightweight material design method for providing feedback to a user, while optionally providing an action to the user.", TSnackbar.LENGTH_LONG);
snackbar.setActionTextColor(Color.WHITE);
View snackbarView = snackbar.getView();
snackbarView.setBackgroundColor(Color.parseColor("#CC00CC"));
TextView textView = (TextView) snackbarView.findViewById(com.androidadvance.topsnackbar.R.id.snackbar_text);
textView.setTextColor(Color.YELLOW);
snackbar.show();
~~~~

##### Example 3: Custom colors & Action Button:              

~~~~                
TSnackbar snackbar = TSnackbar
                        .make(findViewById(android.R.id.content), "Had a snack at Snackbar", TSnackbar.LENGTH_LONG)
                        .setAction("Undo", new View.OnClickListener() {
                            @Override
                            public void onClick(View v) {
                                Log.d("Action Button", "onClick triggered");
                            }
                        });
snackbar.setActionTextColor(Color.BLACK);
View snackbarView = snackbar.getView();
snackbarView.setBackgroundColor(Color.parseColor("#00CC00"));
TextView textView = (TextView) snackbarView.findViewById(com.androidadvance.topsnackbar.R.id.snackbar_text);
textView.setTextColor(Color.YELLOW);
snackbar.show();
~~~~

#### Troubleshooting 

1. Make sure you have the ***latest*** shit. At this moment: compileSdkVersion 23, targetSdkVersion 23, buildToolsVersion "23.0.1", compile 'com.android.support:appcompat-v7:23.1.0',   compile 'com.android.support:design:23.1.0' etc.
2. Notice that, if you use ***findViewById(android.R.id.content)*** your snackbar might appear over your notifications bar (the one with the clock, battery). To fix it, replace it with your view, coordinator layout etc.


#### Updates, Questions, and Requests

Ping me here :)


#### TODO://

* Add easy change of colors
* Add icons


#### Check https://github.com/AndreiD/UltimateAndroidAppTemplate if you like this one.
