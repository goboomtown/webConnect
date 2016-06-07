# Boomtown webConnect (v1)

## Overview
A JavaScript SDK that allows Connect partners to integrate issue creation, notification, and chat in a single button.

#Getting Started
1. Clone this Repository
2. Include webConnect.js in the head of your page
3. Include webConnect snippet in your page
4. Set your partnerToken and PartnerTeam, and set your desired parameters

## Provider Token Generation
1. Log onto the Admin Portal (https://admin.goboomtown.com)
2. Click "Providers" in the left menu
3. Find your provider in the list
4. Double-click your provider to show the "Edit Provider" window
5. Click "API Settings,"" near the button of the configuration panel
6. Select Sandbox or Live, depending on the state of development
7. Click "Re-Generate"
8. Copy the access token

## Partner Team Id
1. Log onto the Admin Portal (https://admin.goboomtown.com)
2. Click "Providers" in the left menu
3. Find your provider in the list
4. Double-click your provider to show the "Edit Provider" window
5. Click on the "Teams" tab
6. Find your team in the list
7. Double-Click your team to show the "Edit Team" window
8. Find your team id near the bottom of the "Provider Info" panel
9. Copy the team id

## Private Label Template Settings
1. Log onto the Admin Portal (https://admin.goboomtown.com)
2. Click "Providers" in the left menu
3. Find your provider in the list
4. Double-click your provider to show the "Edit Provider" window
5. Click on the "Teams" tab
6. Find your team in the list
7. Double-Click your team to show the "Edit Team" window
8. Select "yes" for Private Label near the middle of the "Additional Settings" panel
9. Set Brand Color1 to change the main background color
10. Set Brand Color2 to change the main accent color
11. Set Text Color to set the color of page text
12. Set Link Color to set the color of page links

## Private Label Logo Settings
1. Log onto the Admin Portal (https://admin.goboomtown.com)
2. Click "Providers" in the left menu
3. Find your provider in the list
4. Double-click your provider to show the "Edit Provider" window
5. Click on the "Teams" tab
6. Find your team in the list
7. Double-Click your team to show the "Edit Team" window
8. Select your logo size in the "File Type" select; Brand Logo (125x20), Brand Logo (250x40), or Brand Logo (500x60) in t
9. Click on "Select File" button and select your local file
10. Click on "Upload File" button to upload and save your file

## Usage
### Include webConnect.js
```
<script type="application/javascript" src="https://http://webconnect.goboomtown.com/assets/webConnect.js"></script>
```
### Include Code Snippet
```
    <script type="application/javascript">
        /**
         * Loads an instance of webConnect into element `el`.
         *
         * @param {String|Element} el An element, elementId or query string (e.g. #web-connect, #mySupportDiv, div.webConnect, etc.)
         * @param {String} [options.width=640px] iFrame width
         * @param {String} [options.height=480px] iFrame height
         * @param {String} options.partnerToken API public key/token for the Partner Team. Required.
         * @param {String} options.partnerTeam Partner Team ID from which private label settings, support email/phone/website are derived, and members are created/authenticated and linked to. Required.
         * @param {String} [options.supportEmail] Whether or not to offer the 'Email Support' choice on the help screen. Optional, default to true.
         * @param {String} [options.supportPhone] Whether or not to offer the 'Phone Support' choice on the help screen. Optional, default to true.
         * @param {String} [options.supportWebsite] Whether or not to offer the 'Web Support' choice on the help screen. Optional, default to true.
         * @param {String} [options.routeTo] 'default', 'boomtown', 'provider'. Controls whether to force route new issues created to Boomtown, to the Partner Team, or to not specify and thus allow the default behavior on the back-end.
         */
        window.onload = function() {
            WebConnect.load('#web-connect', {
                partnerToken: '1234567890ABCDEFGHIJ',
                partnerTeam: 'ABC-123',
                width: '440px',
                height: '640px',
                supportEmail: 'true',
                supportPhone: 'true',
                supportWebsite: 'true',
                routeTo: 'boomtown'
            });
        };
    </script>
```
### Add Id to Html Element
```
<div id="web-connect"></div>
```
