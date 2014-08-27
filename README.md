XamarinContactsCodeSample
=========================

This GitHub repo contains a Xamarin Visual Studio Project Code Sample that runs in Android Nexus 7 Emulator to show connecting to Contacts Office 365 API.

![](http://i.imgur.com/6KgTNDw.png)

# Setup of Code Sample #
## 1. Xamarin tools ##
For this code sample to work you require to have Xamarin installed in your environment. There is a [free 30 day trial available](http://xamarin.com/) on their web site and details on [how to install the product](http://developer.xamarin.com/guides/cross-platform/getting_started/installation/). You will need to launch Xamarin Studio and sign in with a trial license or enter a valid license to use Xamarin Projects in Visual Studio.

## 2. Genymotion emulator ##
It is also recommended that you install the GenyMotion Android emulator rather than using the one that comes standard with Xamarin via the Android SDK mainly due to start up time of the emulator. In some scenarios when using the Android SDK you will need to uninstall Hyper-V on your developer environment, which will mean you cannot do native Windows Phone 8.1 emulator development. More details on GenyMotion are available on [their web site](http://www.genymotion.com/). This approach will install Oracle VM Virtual Box on your machine. 

## 3. Create a new virtual device in Genymotion ##
1. Click Connect and sign into Genymotion
2. Add a new Virtual Device
![](http://i.imgur.com/nGmXwKC.png)
3. Select Device model and select "Nexus 5" (this is the minimum Android version required for this code sample)
![](http://i.imgur.com/pcAGWYp.png)
4. Wait for the device to initialize
![](http://i.imgur.com/JFN5Stz.png)

## Configure project in Visual Studio ##
Ensure that "Genymotion Google Nexus" is selected for the Emulator to run in the toolbar.
![](http://i.imgur.com/57YsHOg.png)

## Configure the Connected Service to your environment ##
This code sample will connect to your Office 365 tenant and call the Contacts API. You wlil need to register this mobile device application in Azure AD. To do this:
1.  right click on the Project and select Add | Connected Service.
2. On this screen click "register the application" and use your Office 365 Tenant Admin credentials.
3. Once registered you should see the services below, select Contacts and click "Permissions" and check both both and click Apply and then OK.
![](http://i.imgur.com/vRjihFa.png)

Your Visual Studio project is now configured against your Office 365 Tenant and the mobile application is registered in Azure AD Applications. For more information on this, please check the Microsoft Virtual Academy [Introduction to Office 365 Development](http://www.microsoftvirtualacademy.com/training-courses/introduction-to-office-365-development) Module 5 on "Getting Started with Office 365 APIs".

## Run the demo ##
1. In genymotion Start the virtual machine
2. Once the VM is running, run the project in Visual Studio by hitting the "F5" key.
3. Once the app runs click the "Sign in" button where you'll be prompted for your Office 365 credentials.
4. Then you will be prompted with the common consent dialog to confirm the application can access that user credentials Contacts.
![](http://i.imgur.com/Lzfn6Ky.png)

Now the app is running successfully.