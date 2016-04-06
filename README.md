## Salesforce Contact List

This sample shows an example of a Salesforce contact list app. It pulls JSON data from an instance of SFDC which contains all of the available Contacts for the logged in account.

**Author(s)**

* [Chad Tetreault](http://www.twitter.com/chadtatro)

**Supported Platforms**

* BlackBerry 10
* Android
* iOS

**3rd Party Libraries**

* [Ionic v1.2.1](http://www.ionicframework.com) is licensed under the MIT License
* [Fab Button (ng-mfb)](https://github.com/nobitagit/ng-material-floating-button) is licensed under the MIT License
* [Underscore.js](http://www.underscorejs.org) is licensed under the MIT License

**Attributes**

* Photos used (landing, landing-logo, profile-background) are provided by myself, [Chad Tetreault](http://www.twitter.com/chadtatro). Use as you wish.

## App Setup

**Setup**

This sample assumes you already have a Salesforce developer account with a Connected App setup.

Modify the following in the source code, and replace with your instances information.

***AppCtrl.js***

```
// your shouldn't store keys in the code. this is for demo only.
window.OAuth = {
	clientId: '<your client id>',
	clientSecret: '<your client secret>',
	url: {
		authorize: 'https://login.salesforce.com/services/oauth2/token'
	}
};

```

***LoginCtrl.js***

```
$scope.loginData = {
  username: '<username>',
  password: '<password>',
  securityToken: '<secret login token>'
};
```

## Environment Setup

This sample uses [Ionic Framework](http://www.ionicframework.com). The fastest, and simplest way to install it is via [NPM/Node.js](http://nodejs.org).

* Install [Node.js](http://www.nodejs.org)

* Install Cordova

```
npm install -g cordova
```

* Install Ionic

```
npm install -g ionic
```

## How to Build

To build and deploy on BlackBerry 10 follow these steps. For other platforms, please refer to their respective [Platform Guide(s)](https://cordova.apache.org/docs/en/4.0.0/guide_platforms_index.md.html#Platform%20Guides)

**BlackBerry 10**

* Clone this repo to your local machine.

* Ensure the [BlackBerry 10 WebWorks SDK 2.0](https://developer.blackberry.com/html5/download/sdk) is correctly installed, and your setup your signing keys as described in the [Getting Started Guide](https://developer.blackberry.com/html5/documentation/v2_2/getting_started.htm).

* Open a command prompt (windows) or terminal (mac) and run the following command:

```
ionic start myAppName blank
```

* In the new project's **www** folder, **delete** everything **except** the **lib** folder

* Copy & Paste the sample app files and folders into the root folder of the new project and overwrite any conflicts

* Add the Platforms you want to target

 ```
 cordova platform add blackberry10
 ```

* Build the project

 ```
 cordova build
 ```

To deploy the app, again refer to the [Platform Guide(s)](https://cordova.apache.org/docs/en/4.0.0/guide_platforms_index.md.html#Platform%20Guides).

 For **BlackBerry 10** Run the following command to build and deploy the app to a device connected via USB

 ```
 webworks run
 ```

  or

  ```
  cordova run blackberry10
  ```

* [BlackBerry HTML5 WebWorks](https://bdsc.webapps.blackberry.com/html5/) - Downloads, Getting Started guides, samples, code signing keys.
* [BlackBerry WebWorks Development Guides](https://bdsc.webapps.blackberry.com/html5/documentation)
* [BlackBerry WebWorks Community Forums](http://supportforums.blackberry.com/t5/Web-and-WebWorks-Development/bd-p/browser_dev)
* [BlackBerry Open Source WebWorks Contributions Forums](http://supportforums.blackberry.com/t5/BlackBerry-WebWorks/bd-p/ww_con)

## Contributing Changes

Please see the [README](https://github.com/blackberry/BB10-WebWorks-Samples) of the BB10-WebWorks-Samples repository for instructions on how to add new Samples or make modifications to existing Samples.

## Bug Reporting and Feature Requests

If you find a bug in a Sample, or have an enhancement request, simply file an [Issue](https://github.com/blackberry/BB10-WebWorks-Samples/issues) for the Sample.

## Disclaimer

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
