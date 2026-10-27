## Deluge Important #important  
  
  
 2681159 Test sound n clip  
  
  
→ Workflow on mulktiselect lookup edit is not suopported, so on edit condition when multiseledct lookup is added / edited then the workflow will works  
  
→on field event in client script the multiselct lookup fields are not supported ( cannot be configured )  
  
→Client script lookup fields are upported  
  
  
  
→ Client script works on manuall intervention ( the user should manialy do the work in the UI to trigger )→ no workflow etc  
  
On change on page event will also not work for multiselct lookup fields → but for lookup it will work  
  
→when the deluge team has updated login credentials, then the person who triggered the function/ action is the one will be updated ; Example note add, the person who triggered the action will be updated with the note owner , but we cannot change the owneer based on our requirement.  
  
→Updating the pipeline is supported in above v2 version, should use invoke URL  
  
→The line break /n will be enabled by Zoho Deluge team  
  
The send mail deluge task to add attachments , we can just download the attachment and pass it the same under attachments , but there is no need to make use of ZFS  
  
→ and usinh send mail deluge task the from address will be of   
++[systemgenerated@usermail.zohodeluge.com](mailto:systemgenerated@usermail.zohodeluge.com)++ . if they want to change it , then they should contact deluge support team to verify  
  
You can send the template( any template , inventory template) in print preview and use it to download and send it via the attachments in Zoho Send mail ( deluge task or API )  
  
Same for mail merge as well.  
  
fileUrl = "++[https://www.zohoapis.com/crm/v8/settings/inventory_templates/](https://www.zohoapis.com/crm/v8/settings/inventory_templates/)++" + attachment_template_id + "/actions/print_preview?record_id=" + record_id + "&print_type=pdf"; download = invokeurl [ url :fileUrl type :GET connection:"zzz" ]; info download;  
  
  
→If we want to trigger based on multiseelct lookup field , then enable the linking module and then set up a workflow based on linking module creation and get the records from that module.  
  
→We can get the product image using deuge and update the product image using migration.  
  
→ If there is a scope that is not present in CRM, then make use of custom connection and build it. ( API help documet all the details are present )  
  
→We can send email to custom email field and keep the button in list view ( A code function is bookmarked)  
  
→HTML →to have the subform data ( refer the help document )  
  
→In personal settings there is one time zone but in function when tried to use zoho.currentime then it gived different time , then it should be checked witj zoho deluge  
  
→ To triggeer a action via when a attachment is added. Or Any related list adding action, then we can set up a roll up summary field and use it under workflow to trigger the action.  
  
→ To update a related list/ multiselct you can not only use update related list API , but also you can get the related list records and then take the record ID and use it to update the lookup field in the related record , so it would update the related list as well.  
  
→We can have a pop up on list view page and select the records and update the value for those records using client script ( Very imporat to test )  
  
→ On note added , then trigger a workflow . Then we can make use of note ( tarun )  
  
→ CRM implied view error → Check if the module has permission for the user   
  
→ and to get and update the team modules , make use of invoke URL method  
  
→ Using create task method the owner cannot be changed in client script, only using invoke connection method it will work  
  
→ Client script will not work on quick create page   
  
→ Function will also trigger for the records created via email parser  
  
→ For users to download the file upload field we can also make use of Get Files API if that is not supported in Get attacgments API.  
  
  
→File download : get Attachments API -> ZFS -> and then use the id to send the file in emails ( send mail API )  
  
→ There is no need to have ZFS used for deluge ssend mail task ,we can directly get the file and and attache it ,.  
  
→ Includes() syntax is used in client script and contains() is used in deluge .  
  
→ To convert the one file upload field to downloadable URL, then you need to pass that into a workdrve and make it a public, and access that URL and paste it to have the public access.  
  
→Lets say the custom profile user has configured the custom function and associated a workflow . So, when triggered it will be taken as a super admin rather than the person who has done the trigger ( this is by default )  
  
But , if they want the user who triggers the function , then they need to write the code based on API ( update record API ) and enable the login user credentials -> once enabled , and code is updated with API, then the user who triggers will the updated owner and will be listed in the timeline as this person updated the record.  
  
→ External ID ( a new feature in Zoho CRM ) Using it we can update / insert new records and seacrh with this external ID and upsert/ insert  
This is the API  
  
++[https://www.zoho.com/crm/developer/docs/api/v8/upsert-records-ext.html](https://www.zoho.com/crm/developer/docs/api/v8/upsert-records-ext.html)++  
  
  
We do have upsert records API as well . To check based on unique values. if there is a record , then it will update that if not it will create a new one.  
  
Using CPQ we can associate multiple products ( Product configuration )  
  
Using CPQ we can set discounts based on percentage for multiple products and also use the list price for that as well.  
  
  
-> We also can delete the attachments by bulk   
  
There is a code in my test account based on COQL which deletes the attachments one by one .  
  
-> toLong will convert any string number into decimal number .   
  
ax=“0023”  
ax.toLong()=23;  
numStr = if(num < 10,"00" + num.toString(),if(num < 100,"0" + num.toString(),num.toString()));  
T  
  
-> On create add the products in quoted items , the client script will not check if the product is active or not, it just adds it in client script where as in normal from UI , it will not  
  
  
-> We can update the Zoho projects related list in deal/ contact module, using the below code in Wiki  
  
->Client script we cannot trigger on standard button action , only via custom button action  
  
-> In Zoho projects there will be no any custom fields Like in CRM , as we need to get the customers fields via API itselff using Zoho projects end  
  
-> To move Zoho CRM attachment of a record to Zoho Books /. Any product-> We need to use download attachment API and download ( this is our part ) and another part will be done from Zoho Books.  -> Using widgets we can popup any thing in the screen  
  
->\n is used as a line break in notes and multiline field  “an \n dhsj”  
  
->There is function trigger action after the record is approved  
  
-> We cannot carry over tags using convert lead option  
  
-> Custom function will work when record is created via portals  
  
-> Yes CS supports for Portal Users too. But if in CS, if they are searching for other module data using connection or calling CF in it, it doesn't support for portal users.  
  
-> We can restrict some of the fields to enter from clone page using client script clone page load by setting the values null  
  
->And we cannot update the owner of the notes that is being created via function  
  
-> Don’t forgot there is a client script for clone page as well  
  
-> To disable the add row in quotes subform , we can ask them to make use of set read only for the entire row once clicked on add row -> and then make a error message ( workaround )  Code:  kindly go to setup -> developer hub -> client script -> new script -> enter name -> Create/Edit/Detail page -> select Quotes module and layout -> Subform event -> on row add -> save -> paste the code.  
  
ZDK.Page.getSubform('Quoted_Items').getRow(index).setReadOnly(true);  
ZDK.Client.showMessage('Adding rows is not allowed in the subform', {  
	type: 'error'  
});  
  
  
The formulae field will not automatically update if we update the record using integration tasks, it will update if we use v8 API  
  
TRigger parametes will not work on update if we are updating the same value , so, we need to update the value to some dummy and then update it  
  
-> In client script the get buttons API method will not work for the custom buttons, should use getlabel and disable the button .  ->The New address fields can be get and updated using v8 API. And note that we cannot update the new address fields in create page using client script , rather they can do this in detail page , by using API v8 .  
  
->Image upload fields cannot be fetched using v2 integration task. It can be get by invoke Url method and also . We can get file upload field using integration tasks  
  
-> We cannot hide subform , but by hiding the subform fields we can hide the subform  
  
->The update related records method will not work for custom modules  
  
->We cannot set mandatory field via client script on detail page  
  
-> ZDK error in client script comes if field API names are of wrong  
  
4/3/2026  
  
-> ZDK error in send email client script is caused if the from address is of not valid one. So add the from address as a org email and include the parameters and try  
  
->The Approval process works if on edit and create or edit if those those fields that are edited is listed as a criteria of the approval process  
  
->The flow is workflow -> Approval process  
  
->we cannot set the formula fields as a when condition in workflow , rather we can get the formula fields via fields of lookup and then use ut in the condition within the workflow.  ->To add any mathematical to the date field->first convert it into toDateTime() format and then try adding  
  
Sample: record.get("Date_of_Allocation").toDateTime("  
").addMinutes(330).toString("yyyy-MM-dd'T'HH:mm:ss+05:30")  -> In validation rule, the record id will not be available in create page validation, but on the detail page, it will be available   
  
11/3/2026  
  
-> pls use the below URL. It will automatically refresh the token when the access token is expired. Otherwise you will need to revoke and reconnect the connection everytime  
   
Authorize URL: [https://accounts.zoho.in/oauth/v2/auth?access_type=offline&prompt=consent](https://accounts.zoho.in/oauth/v2/auth?access_type=offline&prompt=consent)  
  For custom connection, you need to use server based connection.   
   
go to: [https://api-console.zoho.in/](https://api-console.zoho.in/) and select - >Server based connection  
   
Homepage URL: anyURL  
   
Authorized Redirect URIs: [https://deluge.zoho.in/delugeauth/callback](https://deluge.zoho.in/delugeauth/callback)  
  
Access token URL:[https://accounts.zoho.in/oauth/v2/token](https://accounts.zoho.in/oauth/v2/token)  Refresh token URL : [https://accounts.zoho.in/oauth/v2/token](https://accounts.zoho.in/oauth/v2/token)  
  
-> Important to generate Grant token using server based application in API Console page.  Please goto API console page and then click on Add client and choose server based application   
  
And then give the details as:  Client Name: As any name  
  
HomePage URL: [https://www.google.com/](https://www.google.com/)  
  
Authorised Redirect URL: [https://www.google.com/main](https://www.google.com/main) ( This should be the cx application redirect URL as per their wish )  Click on create - > and then you will be able to see the client ID and client secret , Copy the client ID and client secret. Will that work everytime if the value of the Country and Testing Type is different?  
   
For example, each products have different values of Country and Testing Type. So when this value is selected. The product should be auto assigned to the Products lookup in Deal.  
 And then paste it in the below URL;  
  
Authorization request URL:  
"[https://accounts.zoho.com/oauth/v2/auth?scope=ZohoCRM.users.ALL&client_id={client_id}&response_type=code&access_type=offline&redirect_uri={redirect_uri}](https://accounts.zoho.com/oauth/v2/auth?scope=ZohoCRM.users.ALL&client_id=%7Bclient_id%7D&response_type=code&access_type=offline&redirect_uri=%7Bredirect_uri%7D)”  Here in the above URL give client ID as the client ID from the Zoho API console page and redirect_url is the Authorised redirect URL from the Zoho API console page.  And copy the above link with all the replaced values and paste it in the browser url and click on enter , once clicked then it will ask for the CRM account to choose and once clicked and selected on accept then it will be opened a page . In that page within the URL, you will be able to see the code =" value” and it the grant token that is generated.  Use it to get access and refresh toke  -> And for data backup API we can get the URL’s and download it from the other tab  
  
->And API consume , the credits will be consumed if the Zoho CRM API call is made from our end or 3 rd party end  
  
->File upload field can be set as a mandatory in create and edit page , but not on detail page   
  
->Image upload field cannot be get via client script ( need to use connections in client script )  
  
->Invoke URl in functions limit is 5 Mb and response needs to be fetched with in 40 sec.  -> And the 5 mb is the Download file mb. As download attachments we can download upto 5 mb .  
  
1. The maximum content length of the response that can be returned by an invokeUrl task is **5 MB.**  
  ->When passing payload as a post request , the payload should not exceed  In Body - 95000 lines (as JSON object).  [https://www.zoho.com/crm/developer/docs/functions/serverless-functions.html](https://www.zoho.com/crm/developer/docs/functions/serverless-functions.html)  ->we can trigger the function via external webhook, right ? Through creating a standalone function and enabling REST API 's for it  
  
->When a field is set to read only in client script and when the same record is cloned the read only field will not get updated  
  
->To make subform fields mandatory on the blue print transition , we can set up a client script on before transition and check if the subform,is present or not with the data.  
  
->Disabling custom button via client script will also work for mobile Zoho CRM as well.  
  
->We can call standalone function within any other function in CRM:  -> Connection time out error : Check with deluge team   
  
->we cannot hide aggregate fields on create page using client script,   -> We cannot hide aggregate fields within any page ( Detail, create , edit ) using client script.    
  
->beforeTransition ( transition ) Interceptor  
This event occurs before the transition states of a Blueprint, as per the process flow designed in the blueprint. Add the return false statement at the end of the script, to prevent the blueprint transition  
  
  
12/03.2026  Widget: To run the already widget goto terminal and enter cd - my test widget and then click on zet run.  -> It will initialise the widget and run-> now copy this Url and paste it in the web browser: [https://127.0.0.1:5000/app/widget.html](https://127.0.0.1:5000/app/widget.html)  -> and click on advanced and allow -> and try the widget in CRM.  -> and to edit the code , please edit in visual studio by opening the file and the widget code and do the changes and save the code - and then try opening the widget in browser or crm to see the changes.  -> Important codes in widget:->  
  
<script src="https://live.zwidgets.com/js-sdk/1.0.5/ZohoEmbededAppSDK.min.js"></script>  This is the most important line in the HTML file. It loads the **Zoho Embedded App SDK. S**tandard web pages cannot legally reach into a CRM and grab private data. This script acts as a secure "bridge" between your custom HTML file and Zoho CRM's database, giving you access to the ZOHO. commands used later in the script  ZOHO.embeddedApp.on("PageLoad", function(data) { const recordId = data.EntityId[0]; const module = data.Entity; -> This code extracts the record ID and the module name.  ZOHO.CRM.API.getRecord({ Entity: module, RecordID: recordId }) .then(function(response) { ... }-> this is used to get the record data using the above method  
  
var config = { Entity: module, APIData: { "id": recordId, "Company": "Zylker", "Last_Name": "Peterson" }, Trigger: ["workflow"] }; ZOHO.CRM.API.updateRecord(config) -> and this is for updating the record  
  
ZOHO.embeddedApp.init();-> To start the widget ( Starter motor )  Important Points in widget:  **It MUST be HTTPS:** Zoho CRM loads inside a secure environment. If your external URL starts with http:// instead of https://, Google Chrome and Zoho will completely block the widget from loading to protect the user's data.   
**It must point to the exact file:** Do not just link to the folder (e.g., https://mywebsite.com/widget-folder/). You must include the actual file name at the end of the URL (e.g., .../widget.html or .../index.html).   
**It must be publicly accessible:** The URL cannot be hidden behind a login screen on your website. Zoho CRM needs to be able to reach the HTML and JavaScript files directly.  
  
Troubleshooting:  The Cross-Origin Resource Sharing (CORS) policy error - when trying to make thrid party API call:   
1. If the authorization is not secure.   
2. If their website SSL certificate is not secure.   
3. If their website is blocking the request.  
  
 And to call 3 rd party URL , ask the user to make use of HTTPS method:  helplink: https://www.zohocrm.dev/explore/widgets/v1.5/ZOHO_CRM_HTTP#post  Widget Codes that I tested:   ->ZOHO.embeddedApp.on("PageLoad", function (data) {  
                var recordId = data.EntityId ? data.EntityId[0] : null;  
                console.log("Record ID from PageLoad:", recordId);  
                currentrecordid=recordId;  The above codes only runs on pageload it is initially used to keep at the initial of the widget. So, once the widget loads then it takes the current record ID and the module name.  -> In Widget ( Java script ) in order to make a variable value global , we need to declare in this way : currentrecordid=“”; using var and const it is used only within the function but not outside the function.    console.log("currentrecordid",currentrecordid);  
  
  
   
->When a field is updated through API , the validation rule will not get applied . So, even the field is under validation rule, the update will be done without checking using API  
  
->The static subform will not getter via integration task and v2 API ’s . They need to make use of v6 and above API  
  
->Get related records using COQL: Best method  query = "select id, Deal_Name, Closing_Date from Deals where Contact_Name.id = " + contactId + " order by Closing_Date asc";  
  
->Custom button Disable : var exportBtn = ZDK.Page.getButtons().find(b => b.getLabel() == "Export to PDF").disable();;  -> When developer Hub permission is removed, the client script and functions tab will not be shown , but the client script will trigger.  
  
->Remember this formulae:   
  
If(IsEmpty(${Test1.Phone}),'',If(Len(${Test1.Phone})>2,Concat('********',Substring(${Test1.Phone},Len(${Test1.Phone})-1,Len(${Test1.Phone}))),${Test1.Phone}))  
  
-> formulae to know the difference between created time and the Now():    DateBetween(${Deals.Created Time},Now(),'days')  The above will only work if the {Deals.Created Time} field is edited but will not update automatically.  So, to resolve this problem, use the below way.  (Datecomp(Now(), ${Deals.Created Time}))/1440  
  
Datecomp(Now(), ${Deals.Created Time}))/1440/365.25-> this if for age calculation  
  
And enable the auto refresh .  
  
-> If conditions formula looping: So, if deal product and deal project duration in days should satisfy then, you can use the below:  If(${Deals.Product} == 'SOC_cybersoc', If(${Deals.Project duration in days} > 0, (${Deals.Amount} / ${Deals.Project duration in days}) * 30, 0), 0)  To mask the phone field  
  
16/03/2026  
  
-> Validation function on a field will not work when the same field is set under blueprint , as the field will not validate when the record is under b;ueprint  
  
->Size() is used for list data type   
  
-> length() is used for strings and number data type format  
  
-> toNumber() to convert string to number  
  
-> we cannot make mandatory in detail page , but we can have a validation within field , like if the length!=0 then return false.  
  
-> and to check the length of a number in client script: convert the field value into toString() and use .length to get the length  
  
var val = valstring.toString();  
  
console.log("vallength", val.length);  
  
17/03/2026  
  
  
-> The below method is used to refresh the page when a specific field is updated in detail page on before update  
  
ZDK.Client.navigateTo('record_detail', { module: 'Leads', record_id: $Page.record_id }); -> This will work , but the change done on the specific field will not change , because before it changes it loads the page .  As a best workaround -> Create a another script on same field -> On before update and use $Client.refresh(); and make sure it is after the 1 st script -> so , the 1 st script updates and the page refreshes and value changes.  
  
-> But do not use the above code on the action of detail page on load , as it keeps on reccuring without no stop because it loads the detail page every time.  
  
In order to stop on load , we need to update a check box on first load and have it under condition:  Sample code:   var box = ZDK.Page.getField("Checkbox_sharma").getValue();  
  
console.log("box", box);  
  
var restrictedStages = ["Closed Won"];  
  
if (stageField != null && restrictedStages.includes(stageField) && box==false)   
{  
    console.log("true");  
      
    var docusignBtn = ZDK.Page.getButtons().find(b => b.getLabel() == "Send with Zoho Sign").disable();  
  
    var lead = ZDK.Apps.CRM.Deals.fetchById($Page.record_id);  
lead.Checkbox_sharma = true;  
    var response = ZDK.Apps.CRM.Leads.updateById(lead, $Page.record_id);  
  
    ZDK.Client.navigateTo('record_detail', {  
    module: 'Deals',  
    record_id: $Page.record_id  
  
    });  
  
  
->We can mask the fields in list page   
  
-> Workflow: If a record is not touched or not modified for 3 hour, then need to change the owner : For this. You can set up a workflow on date / time field on last activity time / created time and set 3 hours after -> and under scheduled action 3 hours   
  
-> We can get the field values even under blueprint transition using client script. Zdk.getfield(“dada”)’  
  
-> We cannot make blueprints fields as a mandatory using client script   
  
-> Previous value ( Execution info ) -> It gives the previous field value before it is updated . And the Main use is it gives the fields that are being updated  
  
17/03/2026  -> Time Zones in deluge:  
  
Important note: the Zoho.currenttime() function gives timezone based on the DC they have initially logged in into Zoho CRM. So, this cannot be changed by any settings in CRM. In order to change they need to reach out Zoho CRM deluge team and change it permanently from their end , so that will reflect in their CRM.  IN DC -  IST  
 US DC - PST,  
 EU DC - GMT,  
 AU DC - AST,   
SA DC - KSA  
  
 -> When a record is created in Zoho CRM it takes personal setting timezone and update the created time. But if your company time zone is US and your personal settings time zone is India, then the time will be shown in Indian time in UI of the record, the same way goes for other personal settings time zone as well.  
  
->info zoho.currenttime.toString("yyyy-MM-dd'T'HH:mm:ssXXX"); This will automatically add the time zone based on their local computer   
  
-> To update another timezone date time format into a specific date time field in Zoho CRM, you need to use the below code format.  reminderTime = zoho.currenttime.addMinutes(2);  
	formattedTime = reminderTime.toString("yyyy-MM-dd'T'HH:mm:ss", "Europe/Berlin");  
  
* Asia/Calcutta  
zoho.currenttime.toString(“yyyy-MM-dd'T'HH:mm:ss", "Asia/Calcutta")  
  And here the "Europe/Berlin" can be taken from the below help doc:  [https://www.zoho.com/deluge/help/limitations/time-zones.html](https://www.zoho.com/deluge/help/limitations/time-zones.html)  
  
-> For client script date format: If we are trying to update a date field in a module via client script , if a admin has one date time format and the non admin has another date time format in personal settings and if we update the field using admin date / time format then it will work only in admin but not in non admins , need to use another format for non admins based on their date time format.  
  
Sample code:  
  
  var today = new Date();  
      
    var day = ("0" + today.getDate()).slice(-2);  
    var month = ("0" + (today.getMonth() + 1)).slice(-2);  
    var year = today.getFullYear();  
  
    var formattedDate = day + "/" + month + "/" + year;  
  
    ZDK.Page.getField("Date_of_Visit").setValue(formattedDate);  
  
  
-> if we delete a button , then the function associated with that button will not get deleted .   
  
-> Calling a function via client , you can not only call a standalone function from client script but also you can call any automated functions as well.   
  
Sample code:  
  
parameters = {mp:$Page.record_id};  
log("Parameters:", parameters);  
  
    var response = ZDK.Apps.CRM.Functions.execute("convertlead_1", parameters);  
log("Response:", response);  
  
  
-> but using CRM functions we can call only standalone function:  
  
18/03/2026  
  
-> Set mandatory / set field visibility will not work on blueprint transition pop up using Client script  
  
->Using before blueprint transition we can validate the fields inside the records via client script by returning false  
  
18/03/2026  
  
->Buttons :  
  
When a button is created in Canvas by selecting it from Elements and dragging and configuring it within the Canvas layout, it cannot be disabled.  
  
However, if the button is created via **Customization → Modules and Fields → Create Button → Define Action → Client Script**, and under Position you select **Detail (Canvas)** and add the client script code there, the behavior changes.  
Once this is done, open the Canvas Detail View, search for the previously created button, and drag it into the layout. In this case, the disable functionality will work as expected.  
  
-> Buttons that are created by elements in canvas we can associate an element ID to the button , and using that we element ID we can make the button set visibility / freeze ( where if we click on button no action will be performed ) using (UI Element) feature within client script.  
  
Sample : ZDK.UI.getElementByID('Button').setVisibility(false);  
 To Disable a button in Cavas page . We can also make use of normal method as well :  ZDK.Page.getButtons().find(a => a.getApiName() === "Create Contact in Software").disable();  If the above does not work, then use the below method  
  
ZDK.Page.getButtonByID('Replaceid').disable();  
  
  
-> Also, we can get the custom button ID in the URL, when we create a custom button , we will get the button ID from the URL of the page and copy and use it to disable and do any thing :  sample: ZDK.Page.getButtonByID(‘xxxx’).disable();  
  
  
->  It is possible to disable the convert and send mail button in invoice using client script.  var exportBtn = ZDK.Page.getButtons().find(b => b.getLabel() == "Convert").disable();  
var exportBtn = ZDK.Page.getButtons().find(b => b.getLabel() == "Send Email").disable();  
  
19/03/2026  
 Emails since between Contacts and Deals.  -> there is a contact and 5 deals associated to it. So, if a email is sent to a contact then the email will not sync to the deal. ( but under condition of ** Deal Prediction Mechanism )**  
  
-> but , if we send an email from deal for the same contact, then the email will be shown in deal and be synced in contact as well.  
  
-> And if the deal received the response , then the same response will be shown in deal and contact as well.  -> and if the email is sent from the thread of contact that is received from the deal, then the sent email will be shown under contact as well as deal, because the CRM will sync the emails based on threads.  -> if they still want to link a specific email to a deal , then they can and the replies will be synced across contact and deal accordingly.   ->**Deal Prediction Mechanism: **  
In a deal record, the association with a contact can happen in two ways: through the lookup field (*Contact Name*) and through *Contact Roles* (related list). When a contact is added via the lookup field, it is automatically reflected in the Contact Roles related list as well.  
Using the deal prediction mechanism, this linking is handled automatically. For example, when a contact receives an email, the system checks the deals associated with that contact. If there is only one deal linked to the contact, and the contact is marked as the *primary contact* (rather than just being in Contact Roles), and the deal is in *Closed Won* or any open stage (but not *Closed Lost*), then the contact’s emails will be synced to that deal.   
If there are multiple deals associated with the contact, and they are either in *Closed Won* or open stages, the emails will be synced to the **most recently modified deal**.  And also we can manually link the contact to a specific deal in emails .  Help doc.  https://help.zoho.com/portal/en/kb/crm/connect-with-customers/email/user-functions/articles/email-association-with-deal#Auto-link_Emails_by_Deal_Prediction_Mechanism  
  
  
Fields of lookup:  -> We can make fields of lookup field as read only and it will get updated without any issue via fields of lookup feature  
  
-> Fields of lookup is edited , then edit action under the workflow will not trigger it even though fields of lookup is updated.  
  
-> If they have mistakenly changed the owner or any field and there are around of more records , then they can ask for the data backup for SME team and import the data    
  
-> Using convert records API, if we do not want to update existing records when converting , then we can remove the unique field in email of contacts , so duplicates will be created  
  
20/03/2026  
  
Date / Time Formats in Deluge:  ->20-Mar-2026 14:58:27-> in response if we get this , then it is in Date time Object format  
  
->When we get a Datetime field from the get record , it would be in this format: (2026-04-15T00:00:00+02:00 ) as a string format.  
  
-> Requirement : To get the Date time field and update date into one field and time into another field:  follow_up=as.get("Date_time_test_for_kotte");  
	  
	ab=follow_up.toDateTime("yyyy-MM-dd'T'HH:mm:ss");  
	  
	follow_up_date = ab.toString("yyyy-MM-dd'T'HH:mm:ss");  
info follow_up_date;  
parts = follow_up_date.toString().toList("T");  
info parts;  
follow_up_time = parts.get(1); // "17:00:00+05:30"  
info follow_up_time;  
follow_up=parts.get(0);  
info follow_up;  
  
So, the follow up comes in toString format ,so we can directly use toList("T") and segregate the date and time field. Actually this code works:  parts = follow_up.toList("T");  
info parts;  
follow_up_time = parts.get(1); // "17:00:00+05:30"  
info follow_up_time;  
follow_up=parts.get(0);  
info follow_up;  Another way to do that   
follow_up = record.get("Follow_up_Date_1");  
info follow_up;  
Time = follow_up.replaceFirst("T", " ").getTime();  
info Time;  
Dt = follow_up.getPrefix("T");  
info Dt;  
  
  
-> In cases module , when we try to send email , it will be sent from related to contact email , as it is the default functionality. A method is using function we can update the related to field as desired and send an email ( harshen ,method Manas )  
  
-> We can also get the attachments using COQL API :  Here is the example:   todayStr = zoho.currentdate.toString("yyyy-MM-dd");  
queryStr = "select id, Deal_Name, Stage, Closing_Date, Account_Name.id, Owner.id, Owner.first_name, Owner.last_name from Deals where ((Closing_Date < '" + todayStr + "') and (Stage not in ('Closed Won', 'Closed Lost')))";  
  
  
-> in client script using create page , we can get the multiselect lookup field values after selected , but those will be appeared only 2 record names but not more than 2 record names even though sleeted  
  
  
24/03/2026:  
Kisok:  ->Current record : In kiosk besides the bar at left side, the current record is used to get the current record when the kiosk is set on detail page , it gives the record details like name , email and every thing which works only in record detail page.  
  
->Requirement: Lets say I am in deal record and I want to show all the accounts that has the same deal within the deal record .  So, I create a kiosk and under current record I choose deals ->  
  
And click on screen -> get records via Kisok -> and by default the get records from will be of “parent Module “ -> and under choose module -> Accounts -> under condition choose -> Account name is field Account name ( Current record ) and save   So, this will display all the Deals that are being linked to an Account.  
  
  
->New address fields in Client script : The client script will not work for new address fields , even on cell change will also not work for those new address fields.  
  
-> If condition in formulas: If(${Deals.Revenue Recognition}=='One-Time', ${Deals.Amount}, ${Deals.Amount} / (13 - Month(${Deals.Closing Date})))  
  
-> We can also create a hyper link in notes, where it will redirect to specific page.  Here is the code for that;  	targetUrl = "https://crm.zoho.in/crm/abcdefg/tab/Calls/517970000022069001";  
noteContent = "Related Call Link: <a href='" + targetUrl + "' target='_blank'>Click here to open Call in this tab</a>";  
noteMap = Map();  
noteMap.put("Parent_Id", "517970000022444089"); // The ID of the record where the note   
noteMap.put("Note_Title", "Call Quick Link");  
noteMap.put("$se_module","Accounts");  
noteMap.put("Note_Content", noteContent);  
  
notecreate = zoho.crm.createRecord("Notes",noteMap);    
target='_blank’-> this will take you to the another tab which clicked on hyper link .  target=‘_self’-> This will take you to the same page when clicked on hyper link  
  
  
-> Using var input = ZDK.Client.getInput()  method we can show as number of fields within the pop up and take the values from that pop up and use it in the record.  File upload / download / upload into attachments;  
  
-> You wish to download a file and attach to attachments of a record , then we can just download the file and use attach file integration task or, you can use the below method.  photo = invokeUrl  
[  
	url: "https://pbs.twimg.com/text.txt"  
	type: GET  
];  
photo.setParamName("file");  
response = invokeurl  
[  
	url: "https://www.zohoapis.com/crm/v8/Leads/1000000231009/Attachments"  
	type: POST  
	files: text file  
	connection:"crm_oauth_connection"  
];  
  
There is no need to have ZFS needed for this.  -> if you wish to download and upload the file in another file upload or image upload field , then you need to download the file and pass it to ZFS and get its iD and use its id to upload into file upload/ image upload field.  fileVariable = invokeurl  
[  
	url: "https://file-examples-com.github.io/uploads/2017/10/file-sample_150kB.pdf"  
	type: GET  
];  
fileVariable.setParamName("file");  
response = invokeurl  
[  
	url :"https://www.zohoapis.com/crm/v8/files"  
	type :POST  
	files: fileVariable  
	connection:"crm_oauth_connection"  
];  
info response;  
  
  
-> Using upload attachments API we can also upload the links ( any help links ) into attachments , I mean not only files but also the links can be uploaded into attachments.  
  
One case is : I need the call recordings to be uploaded into their respective contacts , so we can get the call recording and upload it into attachments as a link, so once they click on the link then you can listen to call recording, but the call recording needs to be of public.  
  
Example :    
Module="Contacts";  
recid=517970000022474001;  
existing=10;  
VR="https://www.zoho.com/deluge/help/crm/attach-file.html";  
  
api_url = "https://www.zohoapis.in/crm/v8/" + Module + "/" + recid + "/Attachments?attachmentUrl=" + zoho.encryption.urlEncode(VR);  
  
attachResp = invokeurl  
[  
    url : api_url  
    type : POST  
    connection: "hellokar"   
];  
  
info attachResp;  
  
  
Layout rule ( important ) -> In order to hide the fields based on other values we can also use layout rules.  if a field has value -> then hide the second field : for this , we can set up a layout rule that if a (field A is empty then show field B) Reverse physiology  
  
-> In a client script on the Detail Page (on before update), predefined fields return the updated value correctly. However, for lookup fields, only the record name is returned, not the record ID  
  
  
-> Error : {"code":"INVALID_DATA","details":{"expected_data_type":"jsonobject"},"message":"body","status":"error"}  
  
The invoke API / invoke url always accepts the only JSON ( JavaScript Object Notation ) format.  
 So , the data needs to be in this specific format in order to accept:    
{  
  "data": [  
    {  
      "NoteCreated": "2026-03-24...",  
      "NoteCreatedBy1": "Thrintheesa...",  
      "Recent_Note": "Related Call Link..."  
    }  
  ]  
}  
  So, I can construct this in the below one in one go : {"data":[AccMap]} and AccMap consists of map . But this give me the error .  So, I need to use {"data":[AccMap]} +” “  
  
As this will work, or else you can use .toString() at the end .  
  
-> We can do set visibility for formulae field as well  
  
->When using send mail API: the error ;  {"code":"INVALID_DATA","details":{},"message":"the related id given seems to be invalid","status":"error"  
 This means the template ID is invalid or the template ID and the module specified in the API are different  
  
27/03/2026  
  
To automatically generate access token using my Zoho CRM Deluge code. (Very important )    refresh_token = "1000.e3b968fc901d58bd59ca2db94f620eb2.e33d33413e44da2c1d568a96aa798800";  
        client_id = "1000.NDDYDLQK94XSOS89020EH35A367ULF";  
        client_secret = "c0bc42c79353e2e900cb2fbba5755b34e6c3679931";  
  
        token_url = "https://accounts.zoho.in/oauth/v2/token" +  
                    "?refresh_token=" + refresh_token +  
                    "&client_id=" + client_id +  
                    "&client_secret=" + client_secret +  
                    "&grant_type=refresh_token";  
  
        token_response = invokeurl  
        [  
            url : token_url  
            type : POST  
        ];  
		  
		info token_response;  
  
        access_token = token_response.get("access_token");  
		  
		info access_token;  
  
  
7/04/2026  
  
-> The rollup summary fields cannot be brought using getrecordbyID method , as we need to make use of invoke url method to get the roll up summary fields  
  
-> The rollup summary fields cannot be included in the formulae fields.  
  
  
	as=invokeurl  
    [  
    	url: "https://www.zohoapis.in/crm/v8/Deals/"+recId  
    	type: GET  
    	connection:"hellokar"  
    ];  
	  
	info as;  
	  
	recordData=as.get("data").get(0);  
  
-> In postman we generally generate an access token using grant token and then using access token we will get the records that are needed for you.  So, while getting the records there will be Authorization and Headers .  To directly pass the access token we can set the Authorization as “ Bearer token” and paste the access token directly there.  If you want old method , then they can set the Authorization as “No Auth” and set the Headers and include “Authorization” and set it to Zoho-oauthtoken {{Access token}}. As this will do the work.  
  
-> The new feature Radio Button will work on to get the value using getrecordbyID and updaterecordbyID method as well.   
  
8/04/2026  
  
-> Using fetchbyid method in client script we will not able to get the custom field data within the record . So, for the same page record they can use the $Page.record; or for another record they can make use of the connection and get the data of the custom field.  
  
var parameters = {}; var headers = {}; var response = ZDK.Apps.CRM.Connections.invoke("cscript", "https://www.zohoapis.com/crm/v2/Leads", "GET", 1, parameters, headers);  
  
Var ab=Response.data.details;  
Var abc=ab.  
  
  
-> Validation function: Using validation function we cannot get subform details and some other fields .  I mean : entityMap = crmAPIRequest.toMap().get("record");  The above will not get the subform details and some field values as well.  
  
So, for this as a workaround , using client script on change of field , we can get the values and update it into outside subform fields ( custom fields ) and get the custom field data from the entityMap and use it to validate .  Or , if it is in detail page , we can use connection or getrecordbyID method and get the subform details and validate it . The record id will be within the logs of entityMap.  ->Approval Process:  We cannot ( we have sample code but not the official documentation)  approve a record using function as there is no API for that . But using client script we do have a feature to approve a record   [https://www.zohocrm.dev/explore/client-script/webapi/Modules#approveRecord](https://www.zohocrm.dev/explore/client-script/webapi/Modules#approveRecord)  Sample code: v2:  
  
response4 = invokeurl   
[  
    url: "https://www.zohoapis.in/crm/v6/Leads/" + lead_id + "/actions/approvals?action=approve&comments=thisisacomment"  
    type: POST   
    connection: "hellokar"  
];  
  
info response4;  
  
Sample code ; v8.  AccMap = Map();  
AccMap.put("status", "approve");   
AccMap.put("comments", "thisisacomment");  
  
payloadMap = Map();  
payloadMap.put("approvals", {AccMap});  
  
response10 = invokeurl   
[  
    url: "https://www.zohoapis.in/crm/v8/Leads/" + lead_id + "/actions/approvals"   
    type: POST  
    parameters: payloadMap.toString()  
    connection: "hellokar"  
];  
  
info response10;   
When retrieving a record that is in an approval process using the v8 API, the response includes an $approval payload with various flags:  
  
* delegate: true – Indicates that the user can delegate the approval to another user.  
* takeover: false – Indicates that the user cannot take over the approval process.  
* approve: true – Indicates that the user has permission to approve the record.  
* reject: true – Indicates that the user has permission to reject the record.  
* recall: false – Indicates that the user cannot recall the approval request (used to revoke a delegated approval before it is acted upon).  
* resubmit: false – Indicates that the user cannot resubmit the record for approval (typically available after rejection).  
All these flags in the payload represent whether the user has permission to perform the respective actions on the record.  
  
  
10/04/26  
  
-> Client script on inventory subform within sales order ( Code 2 client script )  For updating discount or any other values within the subform in inventory modules especially in create page.  ZDK.Page.getSubform('CFSubform').getValues();-> This is used to get the subform values.  And get the details and update it within the same variable and use set value.  ZDK.Page.getSubform('CFSubform').setValues([{ 'Name': 'Zylker', 'Age': '20', ... }, { ... }, ... ]);  
  
  
-> Custom function written to push the data from Google sheets to Zoho CRM . ( Code 1 function )  Google Sheets API”s : help doc.  [https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/get](https://developers.google.com/workspace/sheets/api/reference/rest/v4/spreadsheets.values/get)  
  
  
-> Search records API and Get records Count API.  These both are different ,  Get record count supports: ->we can get the count based on CVID, email, phone , word and criteria .  Here for criteria ;  In order to check between 2 date fields , we need to have date time values in toString() formats , then only we can do relation in criteria for search.  
  
Sample:  currentDate = zoho.currenttime;  
	info currentDate;  
todayStart = currentDate.toString("yyyy-MM-dd'T'HH:mm:ss+05:30");  
  
info todayStart;  
  
criteria = "(Created_Time:less_than:" + todayStart + ")";  
  
info "criteria"+criteria;  
  
encodedCriteria = zoho.encryption.urlEncode(criteria);  
  
response = invokeurl  
[  
    url :"https://www.zohoapis.in/crm/v8/Leads/actions/count?criteria=" + encodedCriteria  
    type :GET  
    connection:"hellokar"  
];  
  
info response;  
  
Test for Alex  We use zoho.encryption.urlEncode because when we send an API request, special characters may be interpreted incorrectly by the receiving server. To ensure the data is sent and received without corruption, we encode the URL so that special characters are converted into formats like %20, allowing them to be transmitted safely.  
  
For example, in the above code, todayStart contains +5:30. The + character may be converted into a space during the API request, and the receiving server will also interpret it as a space. As a result, the search API may return an “invalid datetime” or “expected datetime” error.  
To resolve this, we encode the search criteria before sending the request, which ensures the data is interpreted correctly and returns the expected result.  
  
  
13/04/2026  
  
-> Zoho CRM to Zoho books custom fields Data sync .  The code is in the functions Tab in my Zoho CRM Account . Name of the function :   

| ZohoCRMtoZohobookscustomfieldskrishna |
| ------------------------------------- |
  
  
Zoho CRM API invoke URL:  headers : It is used to store the access token in order to get the request/ data .  The sample would be of :   
  
headerMap = Map();   
headerMap.put("Authorization", "Zoho-oauthtoken 1000.xxxxxxxxxxxx");   
headerMap.put("Content-Type", "application/json");  
  
	response = invokeurl  
[  
    url :"https://www.zohoapis.com/crm/v6/Leads"  
    type :POST  
    parameters :finalPayload.toString()  // The data being sent  
    headers :headerMap                   // The security and formatting instructions  
];  Headers is simply formatting the data into a structured format so the receiving application knows which data to be received   
  
  
And the content type is : Telling the payload format I am sending you , so that you can decode it when wanted.  Hey, look at the payload (the parameters) I am sending you. Here is the format you should use to decode it.   Different types of Content types:  "application/json”-> {"First_Name": "John"}  
  
application/x-www-form-urlencoded->  This is the default format used by standard HTML websites when you fill out a form and hit "Submit".  
It structures the data into a single, continuous string. It uses an equals sign (=) to connect a key to its value, and an ampersand (&) to separate different pairs. Spaces are usually converted to a + or %20  
  The server sees and example : First_Name=Jane&Last_Name=Doe&Company=Zoho  
  
  
text/plain->This format has zero structural rules->   If the parameters format is different but in the header it is written as a different format, then an error will be shown.  
  
  
Get emails API:  Get Emails of a Record API -> it gives all the email details within for a record.  View Email API -> It just gives one single Email Details , where the attachemenst also can be getting from this response.  Download Email Attachments-> this will allow to download the attachment of an email .  Sample code : Updated in the functions.  
  
View Email API  response would be different in both v2 and v9 API’s  
  
14/04/2026  
  
Client scripts work based on individual user permissions. This means that when a script is triggered, it executes using the access rights of the user who initiated it.   
For example, if I use a client script to fetch a record that I do not have access to, but an admin does, the record will not be retrieved. This is because I do not have the necessary permissions to access that record.  
  
This happens because ZDK operates using the credentials of the user who triggers the script, not with elevated or admin-level access  If they still want to access, then they can make use of connections and use the admin credentials and get the record details.  
  
  
  
15/04/2026  
  
Fields of lookup complex:  So, I want the fields of lookup field to be shown in another fields of lookup.  Let’s say there is a lookup field in module A , and for that lookup there is a fields of lookup field. So, there is a lookup field on module A in module B field , so I want the module A fields of lookup field to be shown under module B custom field , when module A record is selected .  So, for this you can create a formula field in module A and insert the fields of lookup field in it and store it. And then in module A lookup field in module B, add the fields of lookup and get the formula field and map it to the new custom field , so it will be shown.  And also using fields of lookup we can also map the lookup fields as well. And for that lookup we cannot set fields of lookup because it is also a fields of lookup . So, we cannot have fields of lookup on a lookup field that is also a fields of lookup.  
  
  
**Fields of Lookup – Explanation**  
If you want to display values from a lookup field in another module, you can achieve this using “Fields of Lookup.”  
For example, consider:  
* Module A has a lookup field, and that lookup contains certain fields (Fields of Lookup).  
* Module B has a lookup field that references Module A.  
Now, if you want to display values from Module A’s lookup-related fields inside Module B:  
You can create a **formula field in Module A** that captures the required Fields of Lookup values and stores them.  
Then, in Module B:  
* Use the lookup field that points to Module A  
* Add **Fields of Lookup**  
* Select the formula field you created in Module A  
* Map it to a custom field in Module B  
This way, whenever a record from Module A is selected in Module B, the corresponding values will be displayed automatically.  
Additionally, Fields of Lookup can also be used to map lookup fields themselves. However, you cannot apply Fields of Lookup on a field that is already a Fields of Lookup. In other words, nested Fields of Lookup are not supported.  
  
  
  
->Zoho campaigns :  
  
Requirement: User needs to automate the Zoho campaigns . So, they want to send campaigns on every day at 9 am.  So, we can use schedule functions , but we cannot trigger the Zoho campaign emails from CRM. Rather then can make use of send email .  And we can update the email campaign for a specific lead using update related records API.  dataMap = Map(); // Sets the status in the Campaign related list. Adjust if they use a different status. dataMap.put("Member_Status", "Planned"); zoho.crm.updateRelatedRecord("Campaigns", campaignID.toLong(), "Leads", leadID.toLong(), dataMap);  
  
  
It just associated the campaign to the lead but not send an email . If they want to send automatically , then they need to manually do that.    
-> Calling a function from 3 rd party or postman  
  
A function can be called and get executed from 3 rd party end such as postman. For this , 2 ways  -> API method : Try going to that function and then click on 3 dots besides the function and enable REST API for that. Once enabled copy the API url and paste it within the postman ( just paste the URL with the get request ) so the function executes and gives the response.   If there is input that you need to put , then add them under parameters those key and its value .  -> OAuth2 method: For this you need to enable OAuth2 and copy its url and paste it in the request within postman. Once done, you need to pass the access token under authorisation and as bearer token -> access token and under parameters auth_type->oauth  
  
And pass the inputs as a parameters if needed .  
  
  
  
To get the current record in widget , we can make use of the below code.       ZOHO.embeddedApp.on("PageLoad", function(data) {  
            console.log("Record Data received:", data);  
            const recordId = data.EntityId[0];  
            const module = data.Entity;  
  
  
Not possible no workarounds;  -> Update by ID method:   Zoho CRM client script is not supported to update the custom lookup fields in a module using update by ID method.  var lead = ZDK.Apps.CRM.Leads.fetchById("423383000005261048");   
lead.customlokup = “123344443223443;   
var response = ZDK.Apps.CRM.Leads.updateById(lead, "423383000005261048");  
  
  
-> Update variable By ID method will not work.  var variable = ZDK.Apps.CRM.Settings.fetchVariablesById("423383000000015966"); variable.name = "tax_rate"; var response = ZDK.Apps.CRM.Settings.updateVariablesById(variable, "423383000000015966");  
  
  
 17/04/2026  
  
->Convert lead integration task will not work if the current owner of the lead is an inactive user . And to assign to some other active user , cx needs to add “assign_to” param.  	mp=map();  
	  
	mp.put("assign_to","517970000005425001");  
	  
	convert = zoho.crm.convertLead(id,mp);    
-> Scheduled functions : Very important : To run the function for 1 lakh records or any more records , we need make use of COQL or you can make use of custom view to fetch the records in it and do the scheduled actions.  Lets say I need to update 10,000 records , so using integration task  get records I can get 200 records at a time , so what we can do is using pagination we can fetch 1000 records and do the process and update a specific check box field within the record .  So, Once done, you need to create a custom view on this check box field and then use the custom view in get records. SO, the updated check box field will out of the custom view and not updated check box field will be present , so running the function every day we can update as many records.  Sample code:  void schedule.salesorderupdate()  
{  
list = {1,2,3,4,5};  
for each  ele in list  
{  
	// Updating Timesheet Recs here  
	// CHANGE CVID TO 'Past 2 weeks' CVID  
	sales_orders_resp = zoho.crm.getRecords("Sales_Orders",ele,500,{"cvid":6525552000002129278},"crm");  
	//info sales_orders_resp;.  
	for each  rec in sales_orders_resp  
	{  
		// 		info rec;  
		rec_id = rec.get("id");  
		mp = Map();  
		mp.put("Sales_Order_Checked",true);  
		update_SO_rec = zoho.crm.updateRecord("Sales_Orders",rec_id,mp);  
		//	info update_SO_rec;  
		prod_recs = rec.get("Product_Details");  
		if(prod_recs.size() > 0)  
		{  
			for each  prod in prod_recs  
			{  
				//	info prod;  
				id = prod.get("product").get("id");  
				//	info id;  
				prodrec = zoho.crm.getRecordById("Products",id);  
				SOA = prodrec.get("Sales_Order_Attached");  
				if(!SOA)  
				{  
					mp = Map();  
					mp.put("Sales_Order_Attached",true);  
					update_prod_rec = zoho.crm.updateRecord("Products",id,mp);  
					//		info update_prod_rec;  
				}  
			}  
		}  
	}  
}  
// return "";  
}  
  
  
  
-> In a record there will be related list named “ Connected Records” -> So, when we connect a record using it , it will be added within the related list and If you wish to retrieve the record details , then you need to make use of getrelatedrecords(“connected”,”Leads”,[22343322333](tel:22343322333));  And the connected is the related list API name , there will be many related list names as “ connected_to__s” , but it is not there will some name within that connected_to lists.  And use that related list name to fetch the record.  So, once a record is attached as a connected record , then in that connected record there will be a normal field that links to the connected record.  And in order to fetch it , we can get the make use of get records API v9 version.  Sample:  asss=invokeurl  
[  
	url: "https://www.zohoapis.in/crm/v9/leads/517970000023381152"  
	type: GET  
	connection:"hellokar"  
];  
  
info asss;  And the field name will be of “connected__To_s”  
  
  20/04/2026  
  
->Subform update via integration task vs API.  integration task: lets say that you want to update a subform using integration task, so , when we do that using integration task , it over rides the subform and insert new subform in the place of existing subform.  I mean it removes the existing subform and replaces it with the new subform data that we are updating.  So, to avoid this , we can get the subform and update within the same subform such as subform.put(“and”,”ddss”);  Example:  as = zoho.crm.getRecordById("Deals",517970000023523280);  
accid = ifnull(as.get("Account_Name"),"");  
info accid;  
if(accid != "")  
{  
	account = ifnull(zoho.crm.getRecordById("Accounts",accid.get("id")).get("Discount_Deal"),"");  
	if(account != "")  
	{  
		subform = as.get("Test_of_subform");  
		for each  rec in subform  
		{  
			if(rec.get("Product_lookup").get("name") != "Nitish product ABC")  
			{  
				rec.put("Discount",account);  
			}  
			else  
			{  
				continue;  
			}  
		}  
	}  
}  
info subform;  
update = zoho.crm.updateRecord("Deals",517970000023523280,{"Test_of_subform":subform});  
info update;  
  
  
API method: using API method , if we use subform.put(“abc”,”def”); then it will add as a new row but not replace . Say if there is a 2 rows , then by putting a row it will not replace by add a new row , so it will be total of 3 rows, so to just update we need to use the subform Id and add it .   
21/04/2026  
  
-> We cannot refresh the page after the blueprint transition is completed because, in the client script, there is no action available after the mandatory form is submitted. Actions are only supported before the mandatory form loads, not after it is submitted  
  
->Java script new method.  console.clear();  
  
var userProfile = $Crm.user.profile.name;  
var restrictedProfiles = ["Sales Reps", "Team Lead"];   
  
if (restrictedProfiles.indexOf(userProfile) !== -1) {  
    console.log("info", restrictedProfiles.indexOf(userProfile));  
    ZDK.Page.getField('Account_Name').setReadOnly(true);  
}   So, the above code checks if userprofile name is listed under restrictedProfiles list and if found then it gives the index of the found name , the index starts with 0 . And if there is no found then it returns = -1.   -> Get Field ID’s using function.  So, in order to get the field ID’s we need to make use of meta Data field API names.  Leads = invokeapi  
 [  
 service: ZohoCRM  
 path: "crm/v8/settings/fields?module=Leads"  
 type: GET  
 ];  
 fields = Leads.get("fields");  
 for each field in fields  
 {  
 if(field.get("api_name")== "Lead_Status")  
 {  
 info field.get("id");  
 }  
 }  
  
  
The above method gets the field ID directly based on the API name .  Another method , use the get meta field API to get the fields and the response would be of more which shows error as info messages stopped as the size tried to exceeded 500000 characters. So for this , need to send an email as the response as then search for the field ID.  
 	as=invokeurl  
    [  
    	url: "https://www.zohoapis.in/crm/v8/settings/fields?module=Leads"  
    	type: GET  
    	connection:"hellokar"  
    ];  
	  
	info as;  
	  
	sendmail  
    [  
    	from: zoho.loginuserid  
    	to: "thrinethragigo@gmail.com"  
    	subject: "Hello message"  
    	message: as  
    ]  
  
Blueprint: We can update records that are in blue print using updaterecordAPI or integration task.    
-> upsert records API : ( need to understand )  -> Client Script FetchbyID method vs ZRC get method:  FetchbyID method: Using this method it gives the _ before the API names so for some it will not work.  ZRC method: It will not provide are give the response via _ as directly the API name will be provided .  And the important method Nitesh method( Joel for loop ) method.  console.clear();  
const contactsAPI = [  
  "Locations",  
  "Number_of_Providers"  
];  
const dealsAPI = [  
  "Locations",  
  "Number_of_Providers"  
];  
var conid = ZDK.Page.getField("Contact_Name").getValue();  
if (conid)  
{  
     var method =await zrc.get('/crm/v8/Contacts/' + conid.id)  
  
  console.log('method', method);  
  
    var contact = method.data.data[0];  
  
    console.log("contact", contact);  
    {  
        contactsAPI.forEach(field => {  
            ZDK.Page.getField(dealsAPI[contactsAPI.indexOf(field)]).setValue(contact[field]);  
        });  
    }  
}  Here the contact[field] method will also give the value of the contact with its API name.  
  
  
13/04/2026  
  
-> Workflow Date/ time :  Let’s say I want to send email to the owner if the deal stage is not changed for more than 14 days . For this , setup a workflow on deal specific field edit and then choose stage is modified to any value -> and under instant actions -> update the dat/time field to execution time.  And then create an another workflow on Date/ time field ->and under define execution date ( custom 14 business days after ) and under instant action-anything you wanted.  -> boolean Table:  And :  t-t‎ = = T  
T-f‎ = =F  
F-t‎ = =F  
F-f‎ = =F  
  
Or:  t-t‎ = t  
T-f‎ = t  
F-t‎ = t  
F-f‎ = F  
  
  
-> When can now also restrict the stages change when we set the Stage field as readonly using client script . Previously we can restrict the stages but the pipeline that comes we cannot restrict, but now we can edit it as well.  ->Download and Upload file sample code Syntax;  	response = invokeurl  
[  
	url: "https://www.zohoapis.in/crm/v8/Leads/"+id+"/photo"  
	type: GET  
	connection:"hellokar"  
];  
info response;  
  
  
response.setparamname("file");  response1 = invokeurl  
[  
	url: "https://www.zohoapis.in/crm/v8/Test1/"+id+"/photo?restrict_triggers=workflow"  
	type: POST  
	files: response  
	connection:"hellokar"  
];  
info response1;  
  
  
response.setparamname("file"); -> this is only used when using upload file API ( such as upload to ZFS or any ) , because the upload file expected the param as file.  So, once the file is download and needs to send any where then we need to make use of setparamname("file") and then use it in upload file API’s.  
  
  
V8/ v2 in Inventory module Subform changes:  
  
V8-> Put  Product_Name  
  
List_Price  
  
Quantity  
  
discount  Quoted_Items  
  
V2-> Put  
  
product  list_price  
  
quantity  
  
discount  
  
Product_Details   -> Also, note that a 204 response may occur if the payload sent in the CRM request does not contain any data  
  
-> We can create task and associate a function after blueprint transition.  
  
-> We can also Create signals in Zoho CRM via functions . The sample code is below:  recordId=517970000023377538;  
	  
signalMap = Map();  
  
signalMap.put("signal_namespace", "srikarsingal_srikar");  
  
signalMap.put("id", recordId);   
  
signalMap.put("subject", "Owner Reassignment");  
signalMap.put("message", "The record owner was successfully updated via custom function.");  
  
  
signalResponse = zoho.crm.raiseSignal(signalMap);  
info signalResponse;   For signal_namespace you need to create a new custom signal under signals and use its name space in the above code.  Make sure the record iD is of Lead or contact that is present in the CRM.   24/04/2026  
  
->3 rd party API which is public to get the exchange rates.   rateResp = invokeurl  
            [  
                url :"https://open.er-api.com/v6/latest/" + depositCurrency  
                type :GET  
            ];  
              
            if(rateResp.get("rates") != null && rateResp.get("rates").get("EUR") != null)  
            {  
                rate = rateResp.get("rates").get("EUR").toDecimal();  
                eurValue = depositAmount * rate;  
            }  
  
  
-> using Multiline rich text rich text field we can do all the HTML supported . A sample code to get make the Double quote text in red colour.  originalText=as.get("Test_multiline");  
	  
	formattedText = originalText.replaceAll("\"([^\"]+)\"","<span style='color:red'>\"$1\"</span>");  
	  
	info formattedText;  
  
27/04/2026  
  
->  When we remove the Developer  permissions from profile ( Zoho CRM API Access) then they cannot access anything in developer Hub section ( but can access Data Model and Catalyst solutions )  And also they can access the zoho API console page and can generate client ID and client secret . But once generated and if tried getting the access token from that client ID and client secret we can get the access ID as well . But if we use the access token to get the details of the record , we cannot get the details of the record as it shows the error as:    "code": "NO_PERMISSION",  
    "details": {  
        "permissions": [  
            "Crm_Implied_Api_Access"  
        ]  
    },  
    "message": "permission denied",  
    "status": "error"  
  
  
-> Meetings record.  When we get a record via Events , we will be able to get all the information related to check in, check out , status of Check in . Time/ date of check in , but we cannot update those fields via API , update method .The only way we can update those will be of updating the check in from Zoho CRM mobile APP. Within meetings record .  
  
-> Detail page client script: We cannot make a field mandatory in detail page , but we can restrict the field from saving if certain conditions are not met.  -> If cx is making use of Postman and getting the records using Sandbox credentials , then they need to make use of sandbox request URL , or else they will get the error as : Invalid request.  Refer this link:  [https://help.zoho.com/portal/en/community/topic/kaizen-120-a-guide-to-api-calls-in-zoho-crm-sandboxes?utm_source=zsbot](https://help.zoho.com/portal/en/community/topic/kaizen-120-a-guide-to-api-calls-in-zoho-crm-sandboxes?utm_source=zsbot)  
  
  
-> If formulae does not work then check with SME  
  
-> toDatetime(“yyyy-MM-dd'T'HH:mm:ssXXX”) will convert it into Date time object and it is used for relational operations . In order to store the Datetime field in a record , we need to use toString(“yyyy-MM-dd'T'HH:mm:ssXXX”) and store it.  
  
  
-> Srikar ->mp  
  
-> Validation function: Lets say we need to setup a validation on create page on save event. So, we can write a validation function on the specific field and under entityMap.get(“xxxx”); -> you can enter the custom field that you need to set the validation on.  So, even in create page it works.   
  
Send the Quote / or any sales orders records In PDF format.  // 	fileUrl = "https://www.zohoapis.com/crm/v8/settings/inventory_templates/" + attachment_template_id + "/actions/print_preview?record_id=" + record_id + "&print_type=pdf";  
// download = invokeurl  
// [  
// 	url :fileUrl  
// 	type :GET  
// 	connection:"zzz"  
// ];  
// info download;  
  
The above code just downloads the file as a Pdf and we can send it using send mail deluge task.  sendmail  
[  
from:zoho.adminuserid  
to:"xxxxx"  
subject:"Subject of the email"  
message:"Your message"  
content type:HTML  
attachments :file:resp  
]  
  
  
28/04/2026  
  
-> If a API is made as public then it will work in all DC’s  
  
->Delay code syntax:  delaySeconds=10;  
currentTime= now;  
futureTime= currentTime.addSeconds(delaySeconds);  
loopCount=100000;  
counter = "".leftPad(loopCount).replaceAll(" ",",").toList().subList(0,loopCount);  
info "Current Time:"+currentTime;  
info "Future Time:"+futureTime;  
for each d in counter  
{  
	if(now.getSeconds()==futureTime.getSeconds()){  
		info "Timer Stopped At:"+now;  
		break;  
	}  
}  
info "This will execute after 10 seconds"  
  
  
-> Invoke URL limit:  The invoke Url response time should be within 40 sec, if not the error will be thrown as timeout error . And the complete function needs to be completed within 5 min . I mean if there are many invoke url used in a function, then the complete function needs to be completed within 5 min, if not error will be thrown  
  
Ask them to reach out to the 3 rd party end to check why it is taking too long in order to respond and state them that 40 sec is the rsponse time limit in Zoho and optimise the url based on that or hem to split the task into two parts so that the response can be received within 40 seconds.  
  
  
  
And for scheduled function , the limit will be of 15 min , but for automated function it is 5 min.  
  
->Upset records API:   
If the duplicate check fields list is given nothing:  Then it takes into account the system defined unique fields and then the user defined fields. So, if a lead enters with the same email addresss that is already present then the same record will be updated.  If the duplicate check fields list is given the user defined field first:  In this case , it ignores the system defined fields and use user unique fields , if the user unique field has same value within any record , then the specific record will be updated , if don’t then it will create new record.  Go through the help doc:  [https://www.zoho.com/crm/developer/docs/api/v8/upsert-records.html](https://www.zoho.com/crm/developer/docs/api/v8/upsert-records.html)  
  
->Zoho CRM Connections  case 1: Error: inactive user cannot access the api","status":"error"  This is because the API connection name used in the code was created by a user who was inactive now , so since the user is inactive the above error appears . Resolution: try asking any active user to revoke the connection and reauthorise again.  case 2: When a record is created via integration task, the owner will be automatically taken as super admin for the specific record that is created . So, if they want it to have the owner of specific user , then ask the user to create a connection for Zoho CRM and use the connection name in create record API , so the connection owner will be the record owner for the specific record.  Case 3: I want the user who triggered the function via button : In this case , ask the super admin to Crete a connection and enable the credentials of login user ID for the specific connection from Deluge team , and the other users needs to revoke and reauthorise the same connection . Once done , the user who triggered the function via button will be added as the record owner.  case 4: For workflow : If there is a workflow and a function to create a record is associated to it . And the create record is done via API and enabled the credentials of login user id . And the owner of the created record , will be the person who has triggered the workflow by field update .  
  
-> Unexpected token found -> Error is due to if the code is copied and pasted in the chat box and later cx tried the same code in the deluge  
  
  
6/05/2026  
  
-> base 64 encode  
  
-> java script some thing  
  
->Restore recycle bin sample code:  payload = {  
    "filters": {  
        "group_operator": "AND",  
        "group": [  
            {  
                "field": { "api_name": "module" },  
                "comparator": "equal",  
                "value": "Tasks"  
            },  
            {  
                "field": { "api_name": "deleted_time" },  
                "comparator": "greater_than",  
                "value": "2026-03-31T23:59:59+05:30"  
            }  
        ]  
    }  
};  
  
  
response = invokeurl  
[  
    url: "https://www.zohoapis.in/crm/v8/settings/recycle_bin/actions/restore"  
    type: POST  
    parameters: payload.toString()  
    connection: "emails"   
];  
  
info response;  
  
-> We can change the currency field using update records method  
  
->Update multiline , owner and also take input code using client script.  var field = ZDK.Page.getField('Email');  
var billingstate = field.getValue();  
  
console.log("State ", billingstate);  
  
if (billingstate && billingstate.valueOf) {  
  
    var response = ZDK.Client.getInput(  
        [  
            {  
                type: "text",  
                label: "Reason for changing"  
            }  
        ],  
        "Billing State Changed",  
        "Submit",  
        "Cancel"  
    );  
  
    console.log("Res ", response);  
  
    if (response && response.length > 0) {  
        ZDK.Page.getField('Multi').setValue(response[0]);  
    }  
}  
  
// var ab = $Crm.user.id;  
// var abb = $Crm.user.full_name;  
var ab = "517970000022073703";  
var abb = "Nethra Reddy";  
var bb = ZDK.Page.getField('Owner').setValue({  
id: ab,  
name: abb  
});  
console.log("bb", bb);  
  
  
14/05/2026  
  
-> For Multiselect pick list field , description field and date field we can just get the values and update it into another fields, as like get and put  
  
update=zoho.crm.updaterecord("ab”,123,{“multiple”:rec.get(“multiple)}); As there is no need of conversion and ding some thing just get and put into another field  
  
-> Sample code to run a standalone function from an Automation function.  info data;  
HEADERS_MAP = Map();  
HEADERS_MAP.put("Content-Type","application/json");  
payload = {"text":data};  
  
send = invokeurl  
[  
	url :"https://sandbox.zohoapis.com/crm/v7/functions/receivetextmessage/actions/execute?auth_type=apikey&zapikey=1003.c4d979e3eb05f9f6dc0f92f702467e3f.e62229354b6a55a4220d612043fefc9d"  
	type :POST  
	headers: HEADERS_MAP  
	content-type :"application/json"  
	parameters:payload.toString()  
];  
info send;  In the above Url needs to be taken from Standalone function REST API URL ( OAUTH2 )  
  
And make sure the Standalone function argument mapping is of “**crmAPIRequest” with Date type as “MAP” and get the body from itto get the request parameters.  Refer the below link.  [https://www.zoho.com/crm/developer/docs/functions/request-response.html](https://www.zoho.com/crm/developer/docs/functions/request-response.html)**  
  
-> We can update Multiline rich text field via client script and embedded the redirect URL ;  Use the below sample code with href.  var field_obj = ZDK.Page.getField('rich_text');  
  
field_obj.setValue('<a href="https://www.freecodecamp.org/news/" target="_blank">Visit freeCodeCamp</a>');  
  
-> Contains important:   
  
vertical=Adobe_DR; be_verticals = {"Adobe_DR","Adobe_MDP","Adobe_TechData","RPI","Autodesk_Adoption","Autodesk_MDP","Autodesk_SIP","Autodesk_TechData","CRI","GPI","TFP","PPI","Bentley_MDP","Chaos_ARK_Incentive","Nemetschek_MDP","SketchUp_ARK_Incentive","SketchUp_Hope_Incentive","Unity_MDP","Others"};  be_verticals.contains(vertical)-> This will give false.  So, we need to convert it into toString() and then do it. Vertical.toString();  
  
-> Zoho forms dynamically show the CRM Data   
  
When creating a form click and drag the webhook option in the left side and then give the search records Url :[https://www.zohoapis.in/crm/v8/Leads/search](https://www.zohoapis.in/crm/v8/Leads/search)  only give upto search the ?criteria will be parameters so we can define it under parameters.  And authorization type -> Choose connection -> and select the connection ->and under url paramerts enter email.  So, the  question mark and after things all are parameters .    
14/05/2026  
  
-> We can update the record using integration task using connection as well.  	id=517970000024203179;  
	  
	WD_Map=map();  
	WD_Map.put("Last_Name","ancc");  
	  
	upd = zoho.crm.updateRecord("Leads", id, WD_Map,map(),"hellokar");  
	info upd;  The above is the sample.  -> Does Zoho Supports only Oauth 2.0 for making APi requests ?  Yes, for making external standard REST API calls to Zoho CRM (and almost all modern Zoho applications), **OAuth 2.0 is the only supported authentication method.**  
  
## 1. External Applications (Strictly OAuth 2.0)  
If you are making requests from an external server, a custom web app, Postman, or a third-party platform (like Zapier or Make), you must use the standard OAuth 2.0 protocol.  
* This involves registering an application in the Zoho API Console (api-console.zoho.com) to generate a client_id and client_secret.  
* You must manage the authorization code, generate an access_token, and continually use a refresh_token to generate new access tokens when they expire (typically every hour).  
  
## 2. Internal Zoho Automation (Connections - Abstracted OAuth)  
If you are writing code *inside* the Zoho ecosystem (like a Deluge Custom Function in CRM, or a Zoho Creator script), you **do not** write standard OAuth 2.0 code.  
* Instead, you use **Zoho Connection **  
## Front-End Zoho Widgets (JS SDK Session Auth)  
If you are building a custom UI Widget that is hosted *inside* Zoho CRM (using zet pack), you also do not use OAuth 2.0 directly.  
* Widgets use the **Zoho Embedded App JS SDK**.  
* When a user opens the widget, the SDK automatically authenticates the API requests (ZOHO.CRM.API.getRecord()) using the logged-in user's active browser session cookies.  
  
  
Zoho Projects and Zoho CRM:  -> Needs to associate a project to one of the contact in Zoho CRM.  	acctid = 517970000022433111;  
	projid=449157000000070004;  
	mp = Map();  
mp.put("name","Claude connected");  
contdet = Map();  
contdet.put("id",acctid);  
contdet.put("Email","feedback@kotakbank.in");  
mp.put("Contacts",contdet.toList());  
datalist = List();  
datalist.add(mp);  
datamp = Map();  
datamp.put("data",datalist);  
resp = invokeurl  
[  
	url :"https://www.zohoapis.in/crm/v8/Contacts/" + acctid + "/Zoho_Projects/" + projid  
	type :POST  
	parameters:datamp.toString()  
	connection:"nethrareddy"  
];  
info resp;  Observe tolist() as using it there is no need to make and use datalist = List(); -> as the toList() will automatically change without writing the code.  
  
For the above . It is mandatory to give the email and also the right contact email needs to be provided , if not they will getting the error : { code: 'INVALID DATA' , details: {...} , message: 'The given crmuserId and email does not match with the account' , status: 'error' }  If the project or contact ID is wrong then it will show the error as “Error occurred internally”  And if the error says record updated with unadded client , then the contact might not be added as a client in Zoho prokjects end, so they need to check in zoho projects if the client users has specific contact ( the real reason is in projects application they don’t have enough client users as they need to purchase the extra  
  
18/05/2026  
  
->API credits consume : We cannot get the exact source of which application or which function triggered . But all we can state is that if the function is triggered by client script / update task ( Zoho CRM )  and the module those actions has been happened. So, if cx says more API is consumed ask them to click on Table view so you can know which module / task does the API consumed.  
  
  
-> Widget Hosting in Zoho method:  
  
This is the correct format it should be in the files:   
📁 (Root of ZIP)  
 ├── 📁 app  
 │    ├── 📄 widget.html  
 │    └── 📄 css, js, etc.  
 └── 📄 plugin-manifest.json  
  
  
![- Screen Reces: 31 6 27,53 PU](Attachments/777E4363-0A13-4D49-B748-7C87E65E5EAD.png)  
  
  
 The index page would be : /app/widget.html  
  
To create this from scratch  -> On your computer, create a new folder called WidgetTest.  
  
Inside WidgetTest, create a file named plugin-manifest.json and paste this code into it: ( to create a file under new folder WidgetTest -> go to terminal and “cd WidgetTest” -> and type touch filename.txt ( (replace "filename.txt" with whatever you want to name your file, including the extension)  
  
  
{  
  "service": "CRM",  
  "pluginName": "MyTestWidget",  
  "version": "1.0",  
  "modules": ["Leads", "Contacts"]  
}  
  
->Still inside WidgetTest, create a new folder named app  
  
->Inside the app folder, create a file named widget.html and paste this basic HTML:  <!DOCTYPE html>  
<html>  
<head><title>Test Widget</title></head>  
<body>  
  <h2>Hello World! The widget loaded successfully.</h2>  
</body>  
</html>  Now, the crucial step:  Open the WidgetTest folder.  
Select both the app folder and the plugin-manifest.json file.  
Right-click them and select **Compress 2 items**.  
Rename the resulting file to test_widget.zip  
  
Once created the zip file . Now, select the hosting as “Zoho” and then upload your zip file and set the index as” Set the **Index Page** to: /app/widget.html”  
  
19/05/2026  
  
-> update the latest sent and received email from all the contacts and update into the account field.  
  
By using getrelatedlist integration task, we cannot get the received emails Data, so need to make use of get emails API to get all the emails .( received and sent data )  Written the code ( check functions -> latestemailsentreceived  
  
-> Update the fiscal year based on the date/ time field .  Written the code ( Check function -> Fiscalyearcalculation  
  
-> Client script key and values codes logic.  console.log("value", value);  
  
var ab = {  
  
    "Confidential Paper Waste (On Site)": "Confidential_Paper",  
    "Animal Waste": "Animal_Waste",  
    "Pharmaceutical Waste": "Pharmaceutical_Waste",  
    "Confidential Paper Waste": "Confidential_Paper_Waste",  
    "Sharps (Orange Hazardous)": "Sharps_Orange_Hazardous",  
    "Sharps (Yello Hazardous)": "Sharps_Yello_Hazardous",  
    "Hazardous Clinical Waste (Orange Bags)": "Hazardous_Clinical_Waste_Orange_Bags",  
    "Paper and Card": "Paper_and_Card",  
    "Mixed Recycling": "Mixed_Recycling",  
    "General Waste": "General_Waste",  
    "Metal, Plastic and Cartons": "Metal_Plastic_and_Cartons",  
    "Food": "Food",  
    "Glass": "Glass",  
    "Offensive Clinical Waste (Yellow Tiger Bags)": "Offensive_Clinical_Waste_Yellow_Tiger_Bags",  
    "Washroom Services": "Washroom_Services",  
    "Number of Containers": "Number_of_Containers",  
    "Collection Frequency": "Collection_Frequency"  
  
};  
  
  
for (var key in ab)  
{  
    console.log(ab[key]);  
    ZDK.Page.getField(ab[key]).setVisibility(false);  
}  
  
for (var i = 0; i < value.length; i++)  
{  
    if (value[i] in ab)  
    {  
        console.log("value", value[i]);  
        ZDK.Page.getField(ab[value[i]]).setVisibility(true);  
    }  
}  
  
  
-> Zoho books custom field Update :   
If cx would like to update a custom field within the subform of Zoho books estimates/ quotes then he can update it using the below code:  Zohobookscustomfieldinsubformupdate -> in functions in my test account .  Note that , we cannot update the subform amount field in the Zoho books, rather what we can do is update the rate field with the desired value , so the rate * quantity will be automatically updated in the amount field . We can update the rate field.  
  
  
->Widget inline image and base 64 Queries:  Cx is currently working on a Zoho CRM Widget where they are trying to fetch and display inline images from emails using the following API:  
  
++[https://crm.zoho.eu/crm/email/v2/Contacts/{recordId}/Emails/inline_images](https://crm.zoho.eu/crm/email/v2/Contacts/%7BrecordId%7D/Emails/inline_images)++  
  
**Issue:**  
The API response received in the widget is a binary string (PNG data) instead of a usable image or base64.  
When attempting to convert this response to Base64 on the frontend, the data becomes corrupted and does not render as an image.  
The same functionality works correctly when implemented using Zoho CRM Deluge, but not within the widget.  
  
**Requirement:**  
Cx need to display inline images within email content inside the Zoho CRM widget.  
  
**Questions:**  
1. Is there a supported way to retrieve inline images as Base64 or Blob in Zoho CRM widgets?  
2. Does ZOHO.CRM.CONNECTION.invoke support binary-safe responses?  
3. What is the recommended approach to render inline email images inside a widget?  
  
  
Answers for this;  **Question 1: ** Yes, you can call a standalone function from the widget to download the inline image and convert the data into Base64 format. The converted Base64 data can then be used within the widget. A sample code snippet is attached for reference.   
**Question 2: ** Unfortunately, no. The response from **ZOHO.CRM.CONNECTION.invoke** returns binary data and does not support binary-safe handling.   
**Question 3: ** The recommended approach is to create a standalone function that retrieves the inline image and converts it into Base64 format. This function can then be invoked from the widget to obtain the image data in a usable Base64 format.  
  
++[https://www.zoho.com/deluge/help/encryption-tasks/base-64-encode.html](https://www.zoho.com/deluge/help/encryption-tasks/base-64-encode.html)++  
  
Please do refer the sample codes attached.  
  Ticket No: [https://crmplus.zoho.in/zohocorppace/index.do/cxapp/agent/zohocorp/crm-deluge/requests/details/205219033673150120](https://crmplus.zoho.in/zohocorppace/index.do/cxapp/agent/zohocorp/crm-deluge/requests/details/205219033673150120)  Ticket no: #157880045   -> Widget connections:  We can call 3rd party URL’s from the widget code itself , but the issue is it is not encouraged to do that , since the widget is live web browser where it can lead to data corruption . So, the best way to call a 3 rd party API is create a custom connection in Zoho CRM and use the connection name in the widget code using the below sample:  This way , the connection is secure and data is passed safely.  [https://www.zohocrm.dev/explore/widgets/v1.5/ZOHO_CRM_CONNECTION#invoke](https://www.zohocrm.dev/explore/widgets/v1.5/ZOHO_CRM_CONNECTION#invoke)  
  
-> Auto Number code:  So if there is a code that takes the previous values from the previous record and auto update the number , then it will not work for bulk import . So, we need to write a schedule function that runs for every 2 hours and update the auto number field . Or make use of default auto number field  
  
  
20/05/2026  
  
-> File upload field:  Using zdk.page.getfield(“file_upload”) will not work and give undefined response even if the file is uploaded because this is not supported as of now . So, to sort it we need to use fetchbyid method and get the fileupload field.    
-> addhour(-1) in deluge minuses the hour. And subhour(-1) gives some other values , so it is not recommended to use that , rather use the addhour() and add the minus values.  -> add a product automatically in create page Sample code ( will also work for custom fields as well in inventory modules )  console.log("value", value);  
  
var productid = value.id;  
var productnam = value.name;  
  
var productdet = ZDK.Apps.CRM.Products.fetchById(productid);  
var ab1=productdet.Parent_Product;  
var ab2=productdet.Unit_Price;  
  
var ab = ZDK.Page.getSubform('Purchase_Items').getRow(0).setValues({ "Product_Name": { "id": productid, "name": productnam }, "Parent_Product_1": ab1,"List_Price":ab2 });  
console.log("ab", ab);  
  
  
-> Search records API   Make sure the connection that is used needs to be of : zohocrm.securesearch and Zohocrm.module.ALL  
  
Because , if we don’t provide the connection with the scopes , then there will be no error but the response will be empty which tells there is no matching record , but it is false, there are records but since the connection has different scopes it shows the null   27/05/2026  
  
->Authorization Zoho OAuth token { Access token} The Access token should be used under Auth   
  
->Client script Event -> On before mandatory form event save .  we can also show a message after clicking on save button in blueprint transition pop up after method.  console.log("form",form);  
  
if (form.Amount && form.Advance_Payment)  
{  
    ZDK.Client.showMessage('The Payment link has been sent to the Customer successfully.', {  
	type: 'success'  
});  
}   
Amount and Advance_Payment are the fields within the blueprint pop .  
  
->Client script behaviour:  In some accounts on change event on subform will not work for number field if the value in the field is being removed and then clicked on beside cell.  
  
And also if some field value within same subform is changed based on the change on another subform field within the same row then the script also runs since there is change in the subform cell change even without manually changing the field.  ->Delete records invoke connector method:  deleteRecordMap = map();  
deleteRecordMap.put("module", "Leads");  
deleteRecordMap.put("id","3388926000000286025");  
deleteResp = zoho.crm.invokeConnector("crm.delete", deleteRecordMap);  
info deleteResp;  
  
  
-> Widget pop up when a specific field value gets changed.  [https://www.zohocrm.dev/explore/client-script/clientapi/Client?features=CSCRIPT_SUBFORM_EVENTS#openPopup](https://www.zohocrm.dev/explore/client-script/clientapi/Client?features=CSCRIPT_SUBFORM_EVENTS#openPopup)  using the above method and showing the widget pop up on specific field event change  
  
//Umair Code .......................................................  
ZDK.Client.openPopup({  
	api_name: ‘xxx’,  
	type: ‘widget',  
	header: 'Sample Widget',  
	animation_type: 4,  
	height: '450px',  
	width: '450px',  
	left: '10px'  
});  
  
Under xxxx you need to replace with the API name of the widget ( I mean widget API name not the button API name )  ->And in the create page and edit page  we are unable to fetch the custom buttons names/ API names/ Label/ Anything . Because custom buttons enable/ disable via client script will not work on edit/ create page   
  
->Zoho CRM action to Create Zoho books Task.  Sample client script code:  if (value == "PO Placed") {  
  
    var parameters = {  
        "title": "further action required - OEM PO Place",  
        "Assign_to":"skg"  
    };  
    var headers = {};  
    var response = ZDK.Apps.CRM.Connections.invoke("taskcreationondealstagepoplaced", "https://www.zohoapis.in/books/v3/tasks?organization_id=60064498120", "POST", 2, parameters, headers);  
    log(response);   
}  
  
  
-> Get Input method client script is being added in Github  
  
->When the user is creating records via Zoho forms . And using a file download and upload function, the files might not be added at that instant , so ask them to add a delay scheduled function after 2 min so the process executes without any issue  
  
-> And also to download the already uploaded file in file upload field , we no need to again pass it to ZFS file upload , as we can just download the file using get files API .  [https://www.zoho.com/crm/developer/docs/api/v8/get-files.html](https://www.zoho.com/crm/developer/docs/api/v8/get-files.html)  Sample code:   		getFile = invokeurl  
		[  
			url :urlStatic + "/crm/v8/files?id=" + getimpotRec.get(0).get("File_to_Imported").get(0).get("file_Id")  
			type :GET  
			connection:"crm1"  
		];  
		info getFile;  
 Here the getimpotRec.get(0).get("File_to_Imported").get(0).get("file_Id") is the file Id of the already uploaded file.  
  
Note that the same will not work for attachments , but for file upload and image upload it will work  
  
-> If there is function failure when the workflow is executed and when manually done the function works fine then we need to get the details and check with SME ( Rajesh )  Team , **For logs tickets get the below all details. In many tickets some things were missing.**   
  
ZUID , ZGID , user DC ,   
Time of executions   
Issue details   
Details you have checked  
Custom functions/ CS code mandatory   
Recording, screenshot if any needed  
  
->Zoho CRM Search records API.  In search records API , we can get the result but when we use equal operator it behaves as contains operator . So, suggest to make use of COQL API  
  
And also in search records integration task ,   rsSessionStrand = zoho.crm.searchRecords("Session_EN_AR_Mapping","(Text_Identifier:equals:Strand) and (Text_in_English:equals:Reading)")  
  
The 1 st equals behaves as equal operator only but for the 2 nd equals it behaves as contains . If there is only 1 equals operator then it work fine, for 2nd equals it works as contains operator. So if they want to make use of more than 1 equal then ask them to use COQL get records API.   -> Add attachment URL sample code.  leadId=517970000024542010;  
	  
	headermap = Map();  
  
headermap.put("Content-Type", "multipart/form-data; boundary=----WebKitFormBoundarYWxkTrZu0gW");  
  
update = invokeurl  
  
[  
  
 url: "https://www.zohoapis.in/crm/v2/Leads/"+ leadId+"/Attachments?attachmentUrl=https://www.zohocorp.com"  
  
 type: POST  
  
headers: headermap  
  
connection : "hellokar"  
  
];  
  
info update;  
  
-> Download attachments vs download file upload vs download image upload.  attachments:  
  
In order to download the attachments we no need to pass them into ZFS. We just need to get the attachments and in the response we will be getting "$file_id" field and this field is the ZFS unique ID for the file uploaded in attachments.  And then using the above file_id we just need to download the file using get files API.  [https://www.zoho.com/crm/developer/docs/api/v8/get-files.html](https://www.zoho.com/crm/developer/docs/api/v8/get-files.html)  
  
Get files API using the above link.  Sample coded:  response = invokeurl  
[  
	url: "https://www.zohoapis.in/crm/v8/Leads/517970000024542010/Attachments?fields=id,$file_id"  
	type: GET  
	connection:"hellokar"  
];  
info response;  
  
asd=zoho.crm.getRelatedRecords("Attachments", "Leads",517970000024542010);  
  
info asd;  
  
for each rec in asd  
{  
	if(rec.get("$file_id")!=null)  
	{  
		  
		response = invokeurl  
[  
	url: "https://www.zohoapis.in/crm/v8/files?id="+rec.get("$file_id")  
	type: GET  
	connection:"sendfileszfs"  
];  
info response;  
		  
	}  
  
  
File upload:   
  
Same for file upload as well , in order to download get the file ID from the field and use the get files API to download it.  Sample:  	as=zoho.crm.getRecordById("Leads",517970000024542010);  
	  
	bds=as.get("File_Upload_1");  
	  
	abc=bds.get(0).get("file_Id");  
	  
	info abc;  
	  
	  
	response = invokeurl  
[  
	url: "https://www.zohoapis.in/crm/v8/files?id="+abc  
	type: GET  
	connection:"sendfileszfs"  
];  
info response;  
  
Image upload:  
  
Same for image upload as well . As the image upload will not be able to get in v2 so need to make use of v8 and need to make use of “File_Id__s” for image upload.  
  
  
Sample:  as=invokeurl  
    [  
    	url: "https://www.zohoapis.in/crm/v8/Leads/517970000024542010"  
    	type: GET  
    	connection:"hellokar"  
    ];  
	  
	info as;  
	  
	abc=as.get("data").get(0).get("Image_Upload_2").get(0).get("File_Id__s");  
	  
	response = invokeurl  
[  
	url: "https://www.zohoapis.in/crm/v8/files?id="+abc  
	type: GET  
	connection:"sendfileszfs"  
];  
info response;  
  
1/06/2026  
  
->Validation on task due date sample code>  
  
entityMap = crmAPIRequest.toMap().get("record");  
// entityMap=zoho.crm.getRecordById("Tasks", 517970000020502244);  
info entityMap;  
Due = entityMap.get("Due_Date").toDate();  
info Due;  
time = zoho.currenttime.toString("HH").toLong();  
info time;  
today = zoho.currentdate;  
info today;  
response = Map();  
if(Due == today && time > 16)  
{  
	response.put('status','error');  
	response.put('message','You cannot select task due date');  
}  
else  
{  
	response.put('status','success');  
}  
return response;  
}  
  
  
-> Data time important:  We need to input the toString() one when we insert the date time into Zoho CRM. And if that does not work then Make use of toDateTime() and then convert to toString() and update the field .  Sample code.  try { // If it is a formatted string from Books dt = getDateTime.toDateTime("dd.MM.yyyy hh:mm a"); DateFormattedValue = dt.toString("yyyy-MM-dd'T'HH:mm:ss"); }  
  
  
-> Send webhook in merge and store API.  [https://www.zoho.com/deluge/help/writer/merge-and-store-v2.html](https://www.zoho.com/deluge/help/writer/merge-and-store-v2.html)  The above is the sample code help doc , as it will take the fields and merge the writer document fields that are merged in writer and use it to send for signature, and from the response of the code you   
  
  
