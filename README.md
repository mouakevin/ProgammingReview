Here is a quick README on this challenge.  I am listing my throught process on this.

1.I had issues making the API call.  It wouldn't return the whole dataset when using the Invoke commands from powershell.  I was unsure if the API was broken or not.  To confirm I copied and pasted the link into a browser and sure enough there was a whole dataset there.  Which told me that the API was working, and the issue was within my powershell command.

![image](https://user-images.githubusercontent.com/22757140/217084981-1ee20766-3dd5-4102-9d79-31040324aba8.png)

When making the Invoke-WebRequest it returns specific fields.
I then stored the "Content" value from that API call into a variable and converted it to a JSON so that way I can properly parse the data.

![image](https://user-images.githubusercontent.com/22757140/217086972-c3981311-367d-4647-af3d-c787d5ca939d.png)


I then stored the call into $states using a hash map and a forloop.

Then towards the end i exported the values into a CSV
