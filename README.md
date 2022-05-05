# Borrit - Google Sheets

This package allows you to use Google Sheet as a database for [Borrit](https://github.com/rthery/borrit)

## Installation
Use the package manager in Unity to install this package from its git url `https://github.com/rthery/borrit-gsheet.git`  

Because Unity packages don't support git dependency, you will need to install [Borrit](`https://github.com/rthery/borrit`) `2.1.0` (or later) package manually.

### Google Sheets (Google API)
This method can be interesting if you want all your users to be authenticated with their Google account.
It's very cumbersome to set up for all your devs though.

#### Project Setup
1. Go to Google Drive and create a Spreadsheet with at least one sheet sheet in it with the name of your project
   ([Application.productName](https://docs.unity3d.com/ScriptReference/Application-productName.html))
1. Share as Editor with Google accounts who will use Borrit  
1. Follow the instructions [here](https://developers.google.com/sheets/api/guides/authorizing) to create
   an application that will allow you to access Google Sheets  
1. Download the OAuth 2.0 credentials JSON file you'll obtained through Google Cloud Console  
1. Place this file somewhere in your project, a good place would be in `ProjectSettings\Packages\io.github.borrit`
   beside the other settings of Borrit, if your repository is not public  
1. In Unity, Open Borrit settings, Edit > Project Settings > Borrit  
1. Select 'Google Sheets' Database  
1. Select the credentials.json file in the Credentials field  
1. Input the [spreadsheet id](https://developers.google.com/sheets/api/guides/concepts#spreadsheet_id)  

#### User Setup
Once the project is setup and credentials.json available somewhere 
1. Open Borrit settings, Edit > Project Settings > Borrit  
1. Select a username if it's empty  
1. Make sure Credentials file is present, otherwise select it  
1. Create your authentication token  
1. Connect and you are ready to use Borrit  