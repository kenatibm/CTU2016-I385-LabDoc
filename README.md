# Lab I385 - Objective 

# Lab I385 - Case Study

# Lab I385 - Requirements
The tools, and the versions, used in this lab are as follows:

+ [node version 4.5.0](https://nodejs.org/en/download/)
+ [Cordova Version 6.3.1](https://www.npmjs.com/package/cordova)
+ [Ionic Framework Command Line Interface Version 2.1.4](https://www.npmjs.com/package/ionic)
+ [MobileFirst Foundation Command Line Interface Version 8.0.0-2016101416](https://www.npmjs.com/package/mfpdev-cli)
+ [API Connect Command Line Interface Version 5.0.4.0](https://www.npmjs.com/package/apiconnect)
+ [git version 1.9.1](https://git-scm.com/downloads)
+ [gulp Version 3.9.1](https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md)
+ [Visual Studio Code Version 1.5.2](https://code.visualstudio.com/download)

In addition to the above you will also need a [Bluemix Account](https://console.ng.bluemix.net) with at least 4GB of container space. Click [here](https://www.ibm.com/cloud-computing/bluemix/) for more information on [Bluemix](https://www.ibm.com/cloud-computing/bluemix/), IBM's cloud platform that helps you solve real problems and drive business value with applications, infrastructure and services.

For this lab a Bluemix instance has already been created for you. The usernames and passwords are as follows:

| **Bluemix username/password** | **Organization** | **Space** |
| ---------------- | ------------------ | -------- |
| student01@ibmmobileapi.33mail.com/CTUlab01 | IBMMobileAPI01 | CTU2016 |
| student02@ibmmobileapi.33mail.com/CTUlab02 | IBMMobileAPI02 | CTU2016 |
| student03@ibmmobileapi.33mail.com/CTUlab03 | IBMMobileAPI03 | CTU2016 |
| student04@ibmmobileapi.33mail.com/CTUlab04 | IBMMobileAPI04 | CTU2016 |
| student05@ibmmobileapi.33mail.com/CTUlab05 | IBMMobileAPI05 | CTU2016 |
| student06@ibmmobileapi.33mail.com/CTUlab06 | IBMMobileAPI06 | CTU2016 |
| student07@ibmmobileapi.33mail.com/CTUlab07 | IBMMobileAPI07 | CTU2016 |
| student08@ibmmobileapi.33mail.com/CTUlab08 | IBMMobileAPI08 | CTU2016 |
| student09@ibmmobileapi.33mail.com/CTUlab09 | IBMMobileAPI09 | CTU2016 |
| student10@ibmmobileapi.33mail.com/CTUlab10 | IBMMobileAPI10 | CTU2016 |
| student11@ibmmobileapi.33mail.com/CTUlab11 | IBMMobileAPI11 | CTU2016 |
| student12@ibmmobileapi.33mail.com/CTUlab12 | IBMMobileAPI12 | CTU2016 |

**<font color="red">PLEASE USE THE USERNAME AND PASSWORD ASSIGNED TO YOU</font>**

<!--
| User | Region | Organization | Space | Developer Portal |
| :--- | :--- | :--- | :--- | :--- |
| 1 | US South | ken.nelson@us.ibm.com | student1 | https://sb-kennelsonusibmcom-student1.developer.us.apiconnect.ibmcloud.com |
| 2 | US South | ken.nelson@us.ibm.com | student2 | https://sb-kennelsonusibmcom-student2.developer.us.apiconnect.ibmcloud.com |
| 3 | US South | ken.nelson@us.ibm.com | student3 | https://sb-kennelsonusibmcom-student3.developer.us.apiconnect.ibmcloud.com |
| 4 | US South | ken.nelson@us.ibm.com | student4 | https://sb-kennelsonusibmcom-student4.developer.us.apiconnect.ibmcloud.com |
| 5 | US South | ken.nelson@us.ibm.com | student5 | https://sb-kennelsonusibmcom-student5.developer.us.apiconnect.ibmcloud.com |
| 6 | US South | ken.nelson@us.ibm.com | student6 | https://sb-kennelsonusibmcom-student6.developer.us.apiconnect.ibmcloud.com |
| 7 | US South | ken.nelson@us.ibm.com | student7 | https://sb-kennelsonusibmcom-student7.developer.us.apiconnect.ibmcloud.com |
| 8 | US South | ken.nelson@us.ibm.com | student8 | https://sb-kennelsonusibmcom-student8.developer.us.apiconnect.ibmcloud.com |
| 9 | US South | ken.nelson@us.ibm.com | student9 | https://sb-kennelsonusibmcom-student9.developer.us.apiconnect.ibmcloud.com |
| 10 | US South | ken.nelson@us.ibm.com | student10  | https://sb-kennelsonusibmcom-student10.developer.us.apiconnect.ibmcloud.com |
| 11 | US South | ken.nelson@us.ibm.com | student11 | https://sb-kennelsonusibmcom-student11.developer.us.apiconnect.ibmcloud.com |
| 12 | US South | ken.nelson@us.ibm.com | student12 | https://sb-kennelsonusibmcom-student12.developer.us.apiconnect.ibmcloud.com |

**<font color="red">PLEASE USE THE SPACE ASSIGNED TO YOU</font>**
-->

# Information about the VM Used

The operating system used for the virtual machine is a version of [Ubuntu](https://www.ubuntu.com) called [Xubuntu](http://xubuntu.org). For more information about [Xubuntu](http://xubuntu.org), please visit [http://xubuntu.org](http://xubuntu.org).

+ **Operating System User Name:** student
+ **Operating System Password:** Passw0rd!

	> **Note:** The 0 in the password is a zero

# Lab I385 - Step by Step Lab Instructions

### Steps

1. Install the Latest Versions of the Command Line Interfaces for Ionic, MobileFirst Foundation and API Connect
1. Create Notes API using API Connect
1. Deploy API to Bluemix
1. Test API on Bluemix
1. Create MobileFirst Foundation Adapter to Consume API
1. Build & Deploy MobileFirst Foundation Adapter to Bluemix
1. Test MobileFirst Foundation Adapter on Bluemix
1. Get and Configure Notes Application
1. Modify Notes Application to use MobileFirst Adapter
1. Deploy Notes Application to MobileFirst Foundation on Bluemix
1. Test Notes Application


## Step 1 - Install Command Line Interfaces (CLI)
The virtual machine that you are using in this lab was created a few months back and as such requires a refresh of some of the command line interfaces (CLI), specifically;

+ The Ionic Framework
+ MobileFirst Foundation CLI
+ API Connect CLI

### Refresh the Ionic Framework CLI, MobileFirst Foundation CLI, & API Connect CLI
Open a terminal session and type:

```
sudo npm install -g ionic mfpdev-cli apiconnect
```
	
After you press enter you may be asked for a password, the password needed is the operating system password for the student user. It is `Passw0rd!`.

> **Note:** The 0 in the password is a zero

You may seem some errors, but you can ignore them. What this command is doing is downloading and installing the latest versions of the Ionic Framework CLI, MobileFirst CLI, and API Connect CLI all at one time. You could install each individually by typing typing the following:

```	
sudo npm install -g ionic
sudo npm install -g mfpdev-cli
sudo npm install -g apiconnect
```

## Step 2 - Create Notes API
API Connect comes with two prebuilt api applications (collection of APIs) one is a **Hello World** application and the other is a **Notes** application. There is also an empty server application which is what you would typically use when creating an API. For this lab you will create the **Notes** application.

To create the MyNotesAPI based on the notes application, open a terminal if not already open. Ensure that you are in your user home directory `/home/student` by typing:

```
cd ~/
```

**Next**, type

```
pwd
```

The response back should be

```
/home/student
```

**Next**, create directory for your project called **MyNotes** by typing:

```
mkdir MyNotes
```

**Next**, change directory to the **MyNotes** directory by typing:

```
cd MyNotes
```

**Next**, create your API by typing:

```
apic loopback
```

You will be prompted for the following:

| Question | Answer |
| :------- | :----- |
| What's the name of your application? | **MyNotesAPI** |
| Enter the name of the directory to contain the project: | **My Notes** |
| What kind of application do you have in mind? | **notes (A project containing ...)** |

![](images/STEP2-01-Create_Notes_API.png)

When the process completes you will be brought back to your command prompt.

**Next**, change directory to MyNotesAPI by typing following into your terminal:

```
cd MyNotesAPI
```

**Next**, Start the design environment by typing following into your terminal

```
apic edit
```

This will open a browser and request that you **Sign in with Bluemix**. Click the **Sign in with Bluemix** button.

**Next** create a datasource. With the API Connect Designer displayed **Click** the **Data Sources** link.

![Click Datasource Link](images/STEP2-02-Click_Datasources_Link.png)

> **Note:** Optionally you can create a datasource for your API via the command line. To use the command line type the following into your terminal:
> 
> ```
> apic create --type datasource
> ```

When the Datasources page opens, you will notice that there is already a datasource listed. This is the in-memory database that was created by default when the application was created earlier.

**Next**, create a new datasource by **Clicking** the **Add** button. This will open a dialog name the new datasource. Name it notesDB and **Click** the **New** button.

![Create Datasource](images/STEP2-03-Create_Datasource.png)

This will open a page to enter the credentials for Cloudant. First select the the Connector type and set to **IBM Cloudant DB**. You will notice that when you do this a message will appear stating "This selected connector has not been installed", with a link to Install connector.  **Click** the **Install connector** link to install the Cloudant Loopback Connector.

The next two pieces of information are required they are the URL and the database name. First find the URL by looking at your Cloudant tile on Bluemix. To get the URL for the Cloudant database open a new browser tab and go to your Bluemix instance by typing [www.bluemix.net ](www.bluemix.net).

**Click** the **Log In** button if note alerady logged in. 
![Log In to Bluemix](images/STEP2-04-Login_to_Bluemix.png)

Ensure you are using the assigned Organization and Space that was assigned to you.

Scroll to the the All Services (3) section. Notice that there are three services, they are:

| Service Name | Type |
| :----------- | :--- |
| ctu2016-apic | API Connect Service |
| ctu2016-cloudant | Cloudant Service |
| ctu2016-mff | MobileFirst Foundation Service |

**Next**, **Click** the **ctu2016-cloudant** service. This will open the Bluemix Cloudant Dashboard for the ctu2016-cloudant service.  !

![Open Cloudant Dashboard](images/STEP2-05-Open_Cloudant.png)

**Next**, with the Cloudant dashboard open, **Click** the **Service Credentials**

![Open CloudantCredentials](images/STEP2-06-Cloudant_Credentials.png)

**Next**, locate and open the **View Credentails** dropdown listbox.

![View Cloudant Credentials](images/STEP2-07-View_Credentials.png)

This will display the credentials for the Cloudant instance. What you are interested in is the URL. The URL attribute will have username and password as part of the URL. Highlight and copy the URL, you will past this into URL attribute for the API Connect Cloudant Datasource you are creating.

![Display Cloudant Credentials](images/STEP2-08-Display_Credentials.png)

**Next**, with the URL copied, return to your API Designer Tab and past the URL into the URL field. For the **Database** field enter **mynotes**. When done, **Click** the **Save** button.

![Complete Datasource](images/STEP2-09-Complete_Datasource.png)

After clicking the **Save** button you will see a message that says "Testing datasource connection". When the message stating "Success Data source connection test succeeded" you will know that your datasource has been created and you can dismiss the message by **clicking** the close button (**x**). 

![Save Datasource](images/STEP2-10-Save_Datasource_Success.png)

**Next** click the **All Data Sources** link to return to your list of datasources. 

![Close Datasource](images/STEP2-11-Close_Datasource.png)

Notice that your datasource is now in the list.

![Dtasource Added](images/STEP2-12-Datasource_Added.png)

**Next** you will need to associate the new datasource with your model. The model was automatically created for you when you selected the notes application at the time you created your API. To associate the datasource with the model, **Click** the **Models** tab.

![Open List of Models](images/STEP2-13-Open_Models.png)

**Next** open the Note model by **Clicking** the Note link.

![Display Cloudant Credentials](images/STEP2-14-Select_Note_Model.png)

**Next** with the Note model open, change the **Data Source** by selecting the notesDB from the dropdown listbox.

![Change Datasource](images/STEP2-15-Change_Note_Datasource.png)

**Finally** save the Note model by **Clicking** the **Save** button. Then **Click** the **All Models** link to return to the list of models.

![List of Models](images/STEP2-16-List_of_Models.png)

## Step 3 - Deploy API to Bluemix

To save time an API Connect Bluemix service has been created for your. Hopefully you have remembered the Bluemix account that was assigned to you as you will need it in this step of the lab.

> **Note:** Typically you would test locally before you publish to API Connect on Bluemix, but since we are short on time we will go straight to testing on Bluemix. If you are would like to test locally, the process is to start the server by pressing the play button in the lower left hand corner, this will start a local version of the server. You can then click the Explore button to play around with the APIs.

First you will need to configure the target that you will be publising to. To do this **Click** the **Publish** button.

![Click Publish](images/STEP3-01-Click_Publish.png)

A submenu will appear. Since there are no targets you will need to add one by **Clicking** the **Add and Manage Targets** option.

![Click Add/Manage Targets](images/STEP3-02-Add_Manage_Targets.png)

And then **Click** the **Add IBM Bluemix Target** button.

![Add Bluemix Target](images/STEP3-03-Add_Bluemix_Target.png)

In the dialog that opens, ensure that your Region is set to **United Kingdom** and that your organization is set to your username.  **Select** the Sandbox from the list of API Connect instances and then **Click** the **Next** button.

![Select APIC Instance](images/STEP3-03-Select_APIC_Instance.png)

On the next screen, create a new APIC Application by typing the name of your new application in the text field at the bottom and then **Clicking** the **Add** button.

![Add Application](images/STEP3-03-Add_Application.png)

With the application added (notice that APIC converted the application name to all lower case), **Click** the **Save** button.

This action will create a new target and return you to the API Connect Designer main page.  **Click** the **Publish** button a second time. Notice that the target is now listed. **Click** the target.

![Select Target](images/STEP3-04-Select_Target.png)

**Check** the **Publish Application** and **Stage or Publish Products** checkboxes and **Click** the **Publish** button. This will initiate the application publish process.

![Click Publish](images/STEP3-04-Publish.png)

When the publish is complete, the dialog window will close and there will be a message showing success. **Click** the **Close** message button to clear the message.

![Publish Complete](images/STEP3-04-Publish_Complete.png)

To verify that your application has published successfully, open a new tab in your browser and go to your Bluemix Console by typing [www.bluemix.net](www.bluemix.net). Login if necessary.

**Scroll** to the **All Services (3)** section and **Click** the ctu2016-apic service.

![Select ctu2016 Service](images/STEP3-05-Select_ctu2016_Service.png)

This will open the **Drafts** page of API Connect. You will not see any drafts since the application and products were published directly to APIC. If you had published a draft or created a draft API on this page, then you would see a list of products and APIs. **Click** the **Hamburger** icon to open the menu.

![APIC Drafts](images/STEP3-06-APIC_Bluemix_Drafts.png)

With the **Menu** open select the **Dashboard** menu option to open the Dashboard.

![Select Dashboard](images/STEP3-07-Select_Dashboard.png)

You can confirm that your application has been published if you see the mynotes application next to the Sandbox.

![Publish Confirmed](images/STEP3-08-mynotes_application.png)

## Step 4 - Test API on Bluemix
To test the API, you will use the Developer Portal. The Developer Portal has already been created for you. For more information on configuring the Developer Portal, [visit here](http://www.ibm.com/support/knowledgecenter/SSFS6T/com.ibm.apic.devportal.doc/con_cmsportal_storefront.html). With your browser open to your API Connect Dashboard, **Click** the **Sandbox** item.

![Select Sandbox](images/STEP4-01-Select_Sandbox.png)

**Next**, **Click** the **Settings** tab.

![Select Settings](images/STEP4-02-Select_Settings.png)

**Next**, **Click** the **Portal** Menu Option.

![Select Portal](images/STEP4-03-Select_Portal.png)

This will display information about the Developer Portal configuration. Notice that the IBM Developer Portal has been selected and there is a URL that has been created. **Click** the **Portal URL** to open the Developer Portal.

![Portal URL](images/STEP4-04-Portal_URL.png)

**Next**, with the Developer Portal open, **Click** the **Create Account** to create a new developer account.

![Developer Portal](images/STEP4-05-Developer_Portal.png)

**Next**, Complete the registration form

> **Note:** You will need to use an email address other than the one provided for you as the adminstrator. The email address you use, you must have access to so that you can confirm the registration.

![Registration](images/STEP4-06-Registration_1.png)

With the Registration Form complete, **Click** the **Create new account** button.

![Registration](images/STEP4-06-Registration_2.png)

A message stating that an email confirmation has been sent is your queue that your registration has been created and is awaiting confirmation.

![Registration](images/STEP4-06-Registration_3.png)

To confirm your registration, go to your email account and click the confirmation link.

![Confirmation Email](images/STEP4-07-Confirmation_Email.png)

The confirmation will take you to a login page once you yoru confirmation has been accepted.  **Click** the **Log in** button.

![Confirmation Login](images/STEP4-08-Confirmation_Login.png)

Once you have logged into the Developer Portal, you will need to create an App that will be used to subscribe to the API.  **Click** the **Apps** link.

![Developer Portal](images/STEP4-09-Portal_Main.png)

**Click** the **Register new application** link.

![Developer Portal](images/STEP4-10-Register_Application_Link.png)

Complete the registration form and then **Click** the **Submit** button.

![Developer Portal](images/STEP4-11-Register_Application.png)

Once the application is registered you will need to make note of the Client ID and the Client Secret. These will be used to authenticate your right to use the API.  **Check** the **Show Client Secret** checkbox to show the Client Secret Code, copy this code to the Mousepad application. Also **Check** the **Show** checkbox for the Client ID to show the Client ID and copy this code to the Mousepad application. (See next to learn how to open the Mousepad application).

![Developer Portal](images/STEP4-12-Registered_Application.png)

You can find the Mousepad application under the Operating System Menu | Accessories Menu

![Developer Portal](images/STEP4-12-Mousepad.png)

**Next** choose an API to associate with this application by **Clicking** either the **API Products** tab at the top of the page or the **available APIs** link at the bottom of the page.

![Developer Portal](images/STEP4-13-Available_APIs.png)

**Next**, with the list of APIs shown, **Click** the **MyNotesAPI**

![Developer Portal](images/STEP4-14-Select_API.png)

**Next**, with the API page open, **Click** the **Subscribe** button.

![Developer Portal](images/STEP4-15-Subscribe_to_API.png)

When the dialod window opens, **Check** the **MyNotesApp** radio button and then **Click** the **Subscribe** button.

![Developer Portal](images/STEP4-15-Subscribe_to_API_MyNotesApp.png)

You will see that a message informing you that you have Successfully subscribed to this plan will indicate that your application is now subscribed.

![Developer Portal](images/STEP4-16-Subscribe_to_API_Success.png)

**Next** you can now test out your API.  **Click** the **MyNotesAPI** link on the left.  This will open a list of API endpoints.

![Developer Portal](images/STEP4-16-Subscribe_to_API_Success.png)

**Next** with the list of API endpoints show, scroll to the **GET /Notes** endpoint.

![Developer Portal](images/STEP4-18-Click_Get_Notes.png)

On the right hand side of the page you will see the defination of the API endpoint.  Scroll until you find the **Client Secret** textbox paste in your Client Secret to copied into Mousepad earlier. 

**Click** the **Call operation** button.

![Developer Portal](images/STEP4-18-Get_Notes.png)

Once the operation completes, scroll a little more and you will see the **Request** that was sent and the **Response** that was returned.

![Developer Portal](images/STEP4-18-Get_Notes_Result.png)

> **Note:** If you get a CORS error, follow the link and accept that the error. Then re-run the operation.

## Step 5 - Create MobileFirst Foundation Adapter

In this step you will create a MobileFirst Adapater to consume the API you just created. Adapters provide mobile security, analytics, and a way to create mobile aware micro-services for your mobile applications. To create a MobileFirst adapter you will use the MobileFirst Command Line Interface.

Start by opening a terminal and navigating to your main project directory. Type the following:

```
cd ~/MyNotes
```

**Next**, create your adapter by typing the following:

```
mfpdev adapter create
```

Enter the following when prompted:

| Question | Answer |
| :--- | :--- |
| Enter adapter name: | MyNotesAdapter |
| Select adapter type: | HTTP |
| Enter group id: | com.ibm.mynotes |

This will create a new folder **MyNotesAdapter**

**Next** Open Visual Studio Code

![Open Visual Studio Code](images/STEP5-01-Open_Visual_Studio_Code.png)

**Next** with Visual Studio Code open, open the folder you just created (~/MyNotes/MyNotesAdapter).

![Open Adapter Folder](images/STEP5-02-Open_Adapter_Folder.png)

![Open Adapter Folder](images/STEP5-02-Open_Adapter_Folder_More.png)

HTTP Adapters have two components. The first is an xml file that describes the properties of the adapter. The second is a Javascript file that contains the code to process the adapter methods.

Open the adapter.xml file found in `src/main/adapter-resources`.

**Next** Modify the connection parameters to match the URL from API Connect. For example: `http://api.eu.apiconnect.ibmcloud.com/ibmobileapi-dev/sb/api/Notes`.

| Component | Description  |
| :--- | :--- |
| http | Protocol |
| api.eu.apiconnect.ibmcloud.com | Domain |
| ibmobileapi-dev | Bluemix Organization & Space |
| sb/api/Notes | API URL Component |

Edit the connection policy to the following:

```
	<protocol>https</protocol>
	<domain>api.us.apiconnect.ibmcloud.com</domain>
	<port>443</port>

```

Remove all the existing procedures and replace with the following:

```
	<procedure name="getNotes"/>
	<procedure name="createNote"/>
	<procedure name="updateNote"/>
	<procedure name="deleteNote"/>
```

Your adapter.xml file should look like the following:

```xml
<mfp:adapter name="MyNotesAdapter"
			 xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
			 xmlns:mfp="http://www.ibm.com/mfp/integration"
			 xmlns:http="http://www.ibm.com/mfp/integration/http">

	<displayName>MyNotesAdapter</displayName>
	<description>MyNotesAdapter</description>
	<connectivity>
		<connectionPolicy xsi:type="http:HTTPConnectionPolicyType">
			<protocol>https</protocol>
			<domain>api.us.apiconnect.ibmcloud.com</domain>
			<port>443</port>
			<connectionTimeoutInMilliseconds>30000</connectionTimeoutInMilliseconds>
			<socketTimeoutInMilliseconds>30000</socketTimeoutInMilliseconds>
			<maxConcurrentConnectionsPerNode>50</maxConcurrentConnectionsPerNode>
		</connectionPolicy>
	</connectivity>

	<!-- Publicly available procedures -->
	<procedure name="getNotes"/>
	<procedure name="createNote"/>
	<procedure name="updateNote"/>
	<procedure name="deleteNote"/>

</mfp:adapter>
```

**Next** edit the MyNotesAdapter-impl.js. Remove all the code and add the methods to support the procedures identified in the adapter.xml

**First** add following variables. Note that you will need to replace your CLIENT ID, CLIENT SECRET, and BASE URL.

```javascript
var CLIENT_ID = '[REPLACE WITH CLIENT ID]';
var CLIENT_SECRET = '[REPLACE CLIENT SECRET]';
var ACCEPT = 'application/json';
var JSON_CONTENT_TYPE = 'application/json';
var URLENCODED_CONTENT_TYPE = 'application/x-www-form-urlencoded';
var JSON = 'json';
var POST = 'post';
var GET = 'get';
var PUT = 'put';
var DELETE = 'delete';
var BASE_URL = '[REPLACE WITH URL]';

var INPUT = {
	method : this.GET,
	returnedContentType : JSON,
	headers: {
		'Accept': ACCEPT,
		'Content-Type': JSON_CONTENT_TYPE,
		'x-ibm-client-id': CLIENT_ID,
		'x-ibm-client-secret' : CLIENT_SECRET
	}
};
```

**Next** add the code to get the list of notes:

```javascript
function getNotes() {
	INPUT.path = BASE_URL;
	INPUT.method = GET;

	return MFP.Server.invokeHttp(INPUT);
}
```

**Next** add the code to create a new note:

```javascript
function createNote(title, content){
	var note =  "title=" + title + "&content=" + content;

	var input = {
		method : PUT,
		path: BASE_URL,
		headers: {
			'Accept' : JSON_CONTENT_TYPE,
			'x-ibm-client-id': CLIENT_ID,
			'x-ibm-client-secret' : CLIENT_SECRET},
		body: {
			content: note,
			contentType: URLENCODED_CONTENT_TYPE
		}
	};

	return MFP.Server.invokeHttp(input);
}
```

**Next** add the code to update an existing note:

```javascript
function updateNote(id, title, content){
	var note =  "title=" + title + "&content=" + content;
	var where = encodeURIComponent('{"_id": "' + id + '"}')

	var input = {
		method : POST,
		path: BASE_URL + '/update?where=' + where,
		headers: {
			'Accept' : JSON_CONTENT_TYPE,
			'x-ibm-client-id': CLIENT_ID,
			'x-ibm-client-secret' : CLIENT_SECRET},
		body: {
			content: note,
			contentType: URLENCODED_CONTENT_TYPE
		}
	};

	return MFP.Server.invokeHttp(input);
}
```

**Finally** add the code to delete an existing note:

```javascript
function deleteNote(id){
	var input = {
		method : DELETE,
		path: BASE_URL + '/' + id,
		headers: {
			'Accept' : JSON_CONTENT_TYPE,
			'x-ibm-client-id': CLIENT_ID,
			'x-ibm-client-secret' : CLIENT_SECRET
		}
	};

	return MFP.Server.invokeHttp(input);
}
```

## Step 6 - Build & Deploy MobileFirst Foundation Adapter

To build your adapter you will use the MobileFirst Command Line Interface. **Start** by opening a terminal and navigating to your MyNotesAdapter directory by typing:

```
cd ~/MyNotes/MyNotesAdapter
```

**Next** Build your adapter by typing the following:

```
mfpdev adapter build
```

**Next** You will need to add the server to the list of servers to deploy to. For this you will use the mfpdev server add command.

```
mfpdev server add
```

| Question | Answer |
| :-- | :-- |
| Enter the name of the new server profile | MyBluemix | 
| Enter the fully qualified URL of this server | [REFER TO TABLE BELOW] | 
| Enter the MobileFirst Server administrator login ID: | admin | 
| Enter the MobileFirst Server administrator password: | admin | 
| Enter the context root of the MobileFirst administration services: | mfpadmin | 
| Enter the MobileFirst Server connection timeout in seconds: 30Make this server the default? | Y | 

| User | URL |
| :-- | :-- |


## Step 7 - Test MobileFirst Foundation Adapter

To test your adapter you will use the MobileFirst Server Console. All adapters maintain a Swagger document that is great for testing your adapter.

**To Start** You will need to start your server console to test your API. To do that open a terminal session, if not already open, and type:

```
mfpdev server console
```

Login if necessary. The username is admin and the password is admin.

**Next** you will need to add a user id for testing purposes. MobileFirst Foundation provides a facility for creating temporary credentials in the form of confidential clients. A client has already been created for you, howver if you are interested in seeing where a confidential client is created, **Click** the **Runtime Settings** menu option on the left hand side of the page. Then **Click** the **Confidential Clients** Tab. You will see that a test client has been create for the scope of * (Wildcard), you would want to remove this client id for production.

**Next** Open the MyNotesAdapter by **Clicking** the **MyNotesAdapter** on the left hand side of the page.

![My Notes Adapter](images/STEP7-05-MyNotesAdapter.png)

**Next** **Click** the **Resources** tab.

![Resource Tab](images/STEP7-06-ResourcesTab.png)

Notice the endpoints listed on the Resources page. These are the endpoints created by the adapter. **Click** the **View Swagger Docs** button.

![Swagger Docs](images/STEP7-07-View_Swagger_Docs.png)

**Click** the **default** link to expand the Swagger Doc and display the endpoints.

![Swagger Default](images/STEP7-08-Swagger_Default_Link.png)

**Click** the **GET /getNotes** link to open the getNotes endpoint.

![Get notes](images/STEP7-09-Get_Notes.png)

By default the endpoints are restricted to authenticated users. If you are not authenticated you will get a 401 error. You can test this out if you would like by **Click** the **Try it out!** button. 

![Try it out](images/STEP7-10-Authenticate_User.png)

Notice the error in the **Response Code**.

![Try it out](images/STEP7-11-401_Response.png)

Now authenticate by **Clicking** the **Authentication** switch on the right side of the page.

![Try it out](images/STEP7-12-Authenticate_User.png)

A dialog will open to select the Oauth Scope.  **Check** the **DEFAULT_SCOPE** and then **Click** the **Authorize** button.

![Try it out](images/STEP7-12-Select_Oauth_Scope.png)

Another dialog will open to authenticate the user. Enter **test** for the User Name and **test** for the Password. Then **Click** the **Log In** button to authenticate the user.
test

![Try it out](images/STEP7-12-Authenticate.png)

Once authenticated you will be brought back to the Swagger page.  **Click** the **Try it out!** button one more time. Once the response comes back, scroll the Response Body and you will see that your call was successful and that there is an array of values.

![Success](images/STEP7-13-Success.png)

The getNotes endpoint does not have any parameters, however the other endpoints do. For instance to create a note you will need to supply a title and some content, for an update you will need to supply an id, title, and content, and to delete you will need to supply an id.

(Optional) To supply parameters enter them as an array of values in the params field for the endpoint. For instance to create a new note provide something like ["My really new note", "This is my really new note content"]

![Parameters](images/STEP7-14-Parameters.png)

**Click** the **Try it out!** button. When the response comes back, scroll the Repsonse Boddy to the end and you will see that a new document has been created.

![Parameters](images/STEP7-15-Success.png)


## Step 8 - Get and Configure Notes Application

A hybrid mobile has been created that consumes records directly from a Cloudant database. This is the same Cloudant database that you directed API Connect to read from in earlier steps. The application source is stored in a git repository. To download the application from github, first change directories to your working directory:

```
cd ~/MyNotes
```

**Next** download the application from GitHub by typing the following:

```
git clone https://github.com/kenatibm/MyNotesApp
```

The previous statement will only download the source. Now you will need to add all the libraries needed to run the app. But first you will need to change directories to the application directory by typing:

```
cd MyNotesApp
```

**Next** install the libraries from npm by typing

```
npm install
```

**Next** add a platform. A platform is a device type such as android, ios, etc. To add a platform type

```
ionic platform add android
```

**Next** add the MobileFirst Foundation plugin by typing

```
ionic plugin add cordova-plugin-mfp
```

> **Note:** this will only install the base plugin for MobileFirst Foundation. If your app will support push notifications or offline storage, live update, or fips encryption you will need to install additional plugins. Click the following for a [list of available MobileFirst Foundation plugins](https://www.npmjs.com/search?q=cordova-plugin-mfp).

## Step 9 - Modify Notes Application

You will use Visual Studio Code to modify the application that was just downloaded to support MobileFirst Foundation. Visual Studio Code supports Javascript as well as frameworks like Ionic 2 and Angular 2, both were used to create the MyNotesApp.  In addition to Javascript support, Visual Studio Code supports Typescript which provides strong typing to Javascript.

**Start** by opening Visual Studio Code if not already open. Then open the folder for the MyNotesApp - File | Open Folder.

![Open MyNotesApp](images/STEP9-01-Open_MyNotesApp.png)

**Next** expand the src directory. The src directory is were all code modification happens within an Angular2/Ionic2 application. When ready to build your application the source code is transpiled from ECMAScript 6 to ECMAScript 5.

![Open src Directory](images/STEP9-02-Expand_SRC_Directory.png)

**Next** open the app.component.ts file under the app directory. The modifications to this component provide the bootstrapping for the MobileFirst libraries.  First add the Renderer library to the @angular/core import.

```javascript
import { Component, Renderer } from '@angular/core';
```

**Next** We do not want the page to show until after the MobileFirst lirary has been bootstrapped. Change the rootPage assignment from 

```javascript
  rootPage = NotesPage;
```

to

```javascript
  rootPage: any;
```

**Next** Add a statement to the constructor to listen for the bootstrapping of the MobileFirst library.

```javascript
    renderer.listenGlobal('document', 'mfpjsloaded', () => {
      console.log("==> MFP API Init Complete");
      this.MFPInit();
    });
```

**Next** Remove the following as it is not need as we do not have a Splash screen for this application

```
   Splashscreen.hide();
```

**Next** add the MFPInit() method after the constructor.

```javascript
  MFPInit(){
    console.log("==> MFP Init Complete.");
    this.rootPage  = NotesPage;
  }
```

The final code should look like below

```javascript
import { Component, Renderer } from '@angular/core';
import { Platform } from 'ionic-angular';
import { StatusBar, Splashscreen } from 'ionic-native';
import { NotesPage } from '../pages/notes/notes';


@Component({
  template: `<ion-nav [root]="rootPage"></ion-nav>`
})
export class MyApp {
  rootPage: any;

  constructor(platform: Platform, renderer: Renderer) {

    renderer.listenGlobal('document', 'mfpjsloaded', () => {
      console.log("==> MFP API Init Complete");
      this.MFPInit();
    });

    platform.ready().then(() => {
      StatusBar.styleDefault();
    });
  }

  MFPInit(){
    console.log("==> MFP Init Complete.");
    this.rootPage  = NotesPage;
  }
}
```

**Next** open the note-provider.ts file under the providers directory. 


**COPY worklight.d.ts to providers**



## Step 10 - Deploy Notes Application to Bluemix

## Step 11 - Test Notes Application




