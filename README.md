# xpanel-desktop-custom-dpi
Set a Custom DPI For the XPANEL Desktop App


<h2>Set a Custom DPI for ULX Mouse - Speedx77</h2>
<img src="https://github.com/user-attachments/assets/92985d6b-4624-4ca3-b81c-1da6b8e3d9f7" alt="xpanel desktop app with changed dpi">
<h4>For Setting a Custom DPI via the webpage, please refer to: <a href="https://github.com/red0x0002/xpanel-custom-dpi">red0x0002's guide</a></h4>
<p>BIG SHOUTOUT to red0x0002 for creating the guide for the webpage, this guide will cover how to change the DPI options for the desktop application (this guide is for windows)</p>
<p><strong>This is not an official FINALMOUSE guide, I am not responsible if anything may happen to your mouse.</strong></p>

<hr/>
<h3>Download and Extract XPANEL</h3>

<ol>
  <li>Desktop App https://xpanel.finalmouse.com/desktop</li>
  <li>Create a folder/directory and place the xpanel desktop app in that folder</li>
    <img src="https://github.com/user-attachments/assets/8ad2d665-0a19-423f-b96a-f234943c2c61" alt="new folder">
  <li>Extract Files to that folder (or a new folder)</li>
    <img src="https://github.com/user-attachments/assets/61a6bc37-4d56-4ba5-949e-091395913be6" alt="extract xpanel files">
    <p>You should see all of the dev files for xpanel in one folder</p>
  <li>Delete original XPANEL download (delete xpanel-desktop.1.0.4.exe file, it is not needed)</li>
</ol>

<hr/>

<h3>Download npx</h3>

<p>In order to edit the code for the dpi we will need npx to unpack the app.asar file and repack it after making our changes</p>

<ol>
  <li>Download NodeJs (npm)
    <p>From this website download NodeJs (NodeJS comes with npm which we'll need to download npx) </p>
    <p>https://nodejs.org/en/download/package-manager/current</p>
    <p>You can follow this video guide if needed: https://www.youtube.com/watch?v=wbQPGgQqKf4</p>
  </li>
  <li>With NodeJS and npm downloaded open a cmd terminal or powershell</li>
  <li>Check the version of NodeJS and npm by excuting the following commands:
    <p>'node -v' and 'npm -v'</p>
    <img src="https://github.com/user-attachments/assets/55cea83e-da53-4bb4-a941-15a9ff948b88" alt="nodejs and npm commands">
  </li>
  <li>Install npx by typing in the following command: 'npm install -g npx'</li>
  <li>Once installed check the version of npx with the following command: 'npx -v'
    <img src="https://github.com/user-attachments/assets/82024276-b2b9-4328-82dc-5eeaeca178e6" alt="npx command">
  </li>
</ol>

<hr/>

<h3>Unpack app.asar and change DPI</h3>
<ol>
  <li>Finally with npx installed, within the xpanel folder with the files you extracted navigate to 'resources' folder</li>
  <li>Open a powershell window here via right click + shift or navigate to this folder in the cmd terminal
    <img src="https://github.com/user-attachments/assets/9502b70e-b60a-4321-bcf0-e8e6b7eddbdf" alt="open powershell window">
  </li>
  <li>Excute the following command to unpack the app.asar file: 'npx asar extract app.asar unpack' the last word 'unpack' will be the name of the folder with the contents of app.asar
    <img src="https://github.com/user-attachments/assets/dfc8a20b-8d9e-492b-9e90-d722b8131c2d" alt="unpack app.asar command">
    <p>Navigate into the unpack folder to this destination: 'unpack\xpanel\dist\_next\static\chunks\app\dpi'</p>
    <p>Open the javascript file 'page-29d5febe915cbaff' in any text editor of your choice ex. notepade, VsCode, sublime, etc. </p>
    <p>If you open the javascript file in vscode or atom, be sure to formate the code to make this easier</p>
    <p>CTRL+F to search for '6400'</p>
    <img src="https://github.com/user-attachments/assets/d65cb785-284e-4b50-acf2-9fb2116326c5" alt="search for dpis">
  </li>
  <li>Within the ["400","800","1600","3200","6400"] change one of the numbers within the qoutation marks "" to your desired dpi for example: "["400","800","1600","1200","6400"]" I changed 3200 to be 1200 (good dpi for 27inch 1440p monitors when browsing)
  </li>
  <li>After making your changes save the file as a .js file (javascript file)</li>
</ol>

<hr/>

<h3>Repack app.asar</h3>
<ol>
  <li>After setting your DPI navigate back to the resources folder</li>
  <li>Move the original app.asar file somewhere out of this directory or delete the file entirely</li>
  <li>Open a powershell window here via right click + shift or navigate to this folder in the cmd terminal
      <img src="https://github.com/user-attachments/assets/9502b70e-b60a-4321-bcf0-e8e6b7eddbdf" alt="open powershell window">
  </li>
  <li>Excute the following command to pack the unpack folder into a new app.asar file with your made changes: 'npx asar pack unpack app.asar'
      <img src="https://github.com/user-attachments/assets/bba512f1-a14d-4bfb-8f9d-457cb884eb73" alt="pack unpack to rebuild app.asar">
  </li>
  
  <hr />
  <h3>Open xpanel-desktop.exe</h3>
  <li>Return to the folder where you originally extracted all the files and open xpanel-desktop.exe</li>
  <li>On the DPI page your new DPI should be there now! Enjoy :)</li>
  <img src="https://github.com/user-attachments/assets/95c7bf41-1341-4bd1-9ef8-57e757f90a83" alt="Finsihed DPI!">
</ol>










