# VAQR
Before an event starts, we use the [VAQR web application](https://vietabroader-qr.appspot.com) to generate QR codes and send them out to attendees. The list of attendees need to be kept in a Google sheet.
 
On the day of the event, we use this application to connect to that sheet and check attendees in as they give us their QR code.
## Table of content
- [Installation](#installation)
- [Instruction](#instruction)
    - [Generate QR Code](#generate-qr-code)
    - [Scan QR Code](#scan-qr-code)
   
## Installation
1. Install [Java Runtime Environment](https://java.com/en/download/).
2. Go to [Releases page](https://github.com/vietabroader/VAQR/releases) to get the latest version of VAQR for either macOS or Windows.

## Instruction
### Generate QR Code
- Open the app then click on **Go to QR Generator** to go to the web application, or enter [vietabroader-qr.appspot.com](https://vietabroader-qr.appspot.com) directly into your web browser.
- Click **Connect to Google Drive** and use the Google account that will be used to hold the generated QR code images to sign in.
- Copy folder ID into the **Google Drive folder ID** text field as instructed on the page. Be sure to share this folder to the attendees so that they can access their codes.
- In the attendees sheet, there should be a column holding their emails. Copy this column to the **Email List** text field then click **Generate**.

After a while, the application will generate and upload the corresponding QR code images, then return the list of Google drive links

<img src = "https://user-images.githubusercontent.com/18899970/27971357-09bb7dc2-6318-11e7-8999-4f91a6e057a9.png" width = "600"/>

### Scan QR Code
- Sign in your Google Account by clicking the **Sign In** button.
- Copy your Google Sheet ID into Spreadsheet ID

*Spreadsheet ID is the random looking text in the middle of the spreadsheet URL*
    <img src = "https://user-images.githubusercontent.com/18899970/27970654-43c24cba-6315-11e7-91ed-945db7bc16a7.png"/>

- Specify related information of sheet that you are working on into the Workspace section. 

*For example, let's say you have a list of attendees on a sheet as below. You generate the QR code from each person's email and you want to mark a person's presence in the Checked-in column. In this case, your list goes from row **4** to row **7**. The **Key column** is **B** and the **Output column** is **D**.*

<img width="542" src="https://user-images.githubusercontent.com/6244849/28052399-cddefe14-65bf-11e7-9666-07bfdc7189c4.png">

<img width="444" src="https://user-images.githubusercontent.com/6244849/28052466-4082d058-65c0-11e7-9e93-e9839c1d6242.png">


- Click **Refresh**. Note that all the changes afterward won't be automatically updated so you need to click the **Refresh** button again should you make any change on the sheet.
    
- Click **Start Webcam** to open webcam and scan QR code from attendees.
- After a QR code being scanned, if the email can be found in the list a mark will appear in the **Output column**. Otherwise, a message will appear saying that it cannot find the person in the list.
