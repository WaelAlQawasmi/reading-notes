# Location 
- Google Play provide API services , one of this  is location  service the app can request to know the lpcation of 
 the user's device
- The fused location provider is one of the location APIs in Google Play services.

- the fused location provider used  to retrieve the device's last known location.

## Set up Google Play services

1. Specify app permissions:
2. Create location services client :
- by creating instance of the Fused Location Provider Client 
in activity's **onCreate()** method
> protected void onCreate(Bundle savedInstanceState) {
    // ...

    fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
}
3. Get the last known location 
- by calling the **getLastLocation()** method and add lister to it like the example:
> fusedLocationClient.getLastLocation()

        .addOnSuccessListener(this, new OnSuccessListener<Location>() {
            @Override
            public void onSuccess(Location location) {
                // Got last known location. In some rare situations this can be null.
                if (location != null) {
                    // Logic to handle location object
                }
            }
        });


4. Select the best location estimate
-  select   one of the following location , besed on app's use case
 - getLastLocation() :gets   more quickly location and less battery  useg
 -getCurrentLocation(): gets more accurate location

 ## resorese
 - [ android developer ](https://developer.android.com/training/location/retrieve-current)

 