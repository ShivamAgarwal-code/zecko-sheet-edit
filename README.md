
# Zecko Website Category Assigner

A Simple JavaScript program which finds out the framework of E-commerce websites and assigns them framework categories respectively in a separate column of a pre-existing Google Sheet, using Express and Google Sheets API in Google Cloud Platform


## Local Setup

Clone the project

```bash
git clone https://github.com/ShivamAgarwal-code/zecko-sheet-edit.git
```

Go to the root project directory

```bash
cd zecko-sheet-edit
```


## Installation

For intializing new npm project :

```bash
npm init
```
Next install the following dependencies
## Dependencies

#### nodemon (Dev Dependency)

```bash
npm install -D nodemon --global
```

#### express, ejs, googleapis node-fetch@2

```bash
npm install express ejs googleapis node-fetch@2
```


## Editing Necessary Variables and Code Sections

In **index.js** modify the following variables according to your spreadsheetID which can be found in the spreadsheet URL just before **/edit**

For Example, in this case :
https://docs.google.com/spreadsheets/d/1q95051Ie7ZeWSXEi5O_LNR1wI5jIynuXHri0eGDGlTc/edit

Spreadsheet ID is **1q95051Ie7ZeWSXEi5O_LNR1wI5jIynuXHri0eGDGlTc**

```javascript
const spreadsheetID = "1q95051xxxxxxxxxxxxxxIynuXHri0eGDG1Tc";
```

Next setup Sheets API by creating a new project in Google Cloud Console, enabling the Google Sheets API and creating a new credential key under it. Place the credential key in the root folder and rename it to **credentials.json**
## Usage

The app by default listens on port 1337, but you can modify it with your own message using this line :

```javascript
app.listen(1337,(req,res) => console.log("Running Server Zecko"));
```

To run the program, type in terminal :
```
nodemon index.js
```

Then open your browser on the listening port (by default 1337) by going to :
```
http://localhost:1337
```

On successful request, you should see the Raw Data of the first column containing the websites, and if you check the original sheet, the categories would be updated as well.


## Screenshots

Setup Google Cloud Credentials :
![Cloud](https://github.com/ShivamAgarwal-code/zecko-sheet-edit/blob/main/WhatsApp%20Image%202022-07-28%20at%2010.11.24%20PM.jpeg)

Code :
![Code](https://github.com/ShivamAgarwal-code/zecko-sheet-edit/blob/main/WhatsApp%20Image%202022-07-28%20at%2010.12.04%20PM.jpeg)

Sheet Before Run :
![Before](https://github.com/ShivamAgarwal-code/zecko-sheet-edit/blob/main/WhatsApp%20Image%202022-07-28%20at%2010.18.59%20PM.jpeg)

Sheet After Run :
![After](https://github.com/ShivamAgarwal-code/zecko-sheet-edit/blob/main/WhatsApp%20Image%202022-07-28%20at%2010.35.40%20PM.jpeg)
