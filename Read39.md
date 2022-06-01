# **Read: 39 - Kinesis**

Using the Google Play services location APIs, your app can request the last known location of the user's device. In most cases, you are interested in the user's current location, which is usually equivalent to the last known location of the device.

This lesson shows you how to make a single request for the location of a device using the getLastLocation() method in the fused location provider.

+ Set up Google Play services
+ Specify app permissions
+ Create location services client:
In your activity's onCreate() method, create an instance of the Fused Location Provider Client as the following code snippet shows.
```
private FusedLocationProviderClient fusedLocationClient;

// ..

@Override
protected void onCreate(Bundle savedInstanceState) {
    // ...

    fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
}

```

+ Get the last known location: To request the last known location, call the getLastLocation() method. The following code snippet illustrates the request and a simple handling of the response:
```

fusedLocationClient.getLastLocation()
        .addOnSuccessListener(this, new OnSuccessListener<Location>() {
            @Override
            public void onSuccess(Location location) {
                // Got last known location. In some rare situations this can be null.
                if (location != null) {
                    // Logic to handle location object
                }
            }
        });
        
```

#### The getLastLocation() method returns a Task that you can use to get a Location object with the latitude and longitude coordinates of a geographic location. The location object may be null in the following situations:

+ Location is turned off in the device settings. The result could be null even if the last location was previously retrieved because disabling location also clears the cache.
+ The device never recorded its location, which could be the case of a new device or a device that has been restored to factory settings.

<br>

![](https://i.stack.imgur.com/paQKO.png)
