// ==UserScript==
// @name         Taskimp HTML
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  try to take over the world!
// @author       You
// @match        https://trimpstest56.netlify.app/
// @icon         https://www.google.com/s2/favicons?domain=netlify.app
// @grant        none
// ==/UserScript==

(function() {
    'use strict';

    // Your code here...
//This needs to be in your object.  Also any references to Taskimp should probably by Taskimp
var Taskimp = { displayed: false,};
function Thides(){
    var divies = document.getElementById("TOptions").children;
    for (var i=0;i<divies.length;i++){
        divies[i].style.display = "none";
    }
    return;
}
function TEnable() {
	var menuElem = document.getElementById("TEnable");
    if (menuElem.classList.contains("btn-danger")) {
        menuElem.classList.add("btn-success");
        menuElem.classList.remove("btn-danger");
        menuElem.innerHTML = "Taskimp Enabled";
        return;
    } else {
        menuElem.classList.add("btn-danger");
        menuElem.classList.remove("btn-success");
        menuElem.innerHTML = "Taskimp Disabled";
        //disabled
        return;
    }
}
function TUniverse() {
	var menuElem = document.getElementById("TUniverse");
    if (menuElem.classList.contains("btn-primary")) {
        menuElem.classList.add("btn-info");
        menuElem.classList.remove("btn-primary");
        menuElem.innerHTML = "Helium Universe";
        return;
    } else {
        menuElem.classList.add("btn-primary");
        menuElem.classList.remove("btn-info");
        menuElem.innerHTML = "Radon Universe";
        return;
    }
}
function TPretty() {
    Thides();
    document.getElementById("PrettyOptions").style.display = "block";
    return;
}
function THelpers() {
    Thides();
    document.getElementById("THelpme").style.display = "block";
    return;
}
function TSaves() {
    Thides();
    document.getElementById("SaveOptions").style.display = "block";
    return;
}

//The buttons across the bottom are table cells.
//This creates a table cell next to the "Settings" menu option
var leTable = document.getElementById("settingsText").parentElement ; // "Settings" <td>
var myElement = document.createElement("TD");
    myElement.appendChild(document.createTextNode("Taskimp")); //Name on the button
    myElement.classList.add("btn");
    myElement.style.color = "GoldenRod";
    myElement.style.backgroundColor = "Purple";
    myElement.onclick = toggleTaskimpMenu;
    myElement.id = "TaskimpBtn";
    leTable.insertAdjacentElement("afterend", myElement);

//This creates a hidden area for populating all of the items you want in your pop-up window
leTable = document.getElementById("settingsTable") ;
    myElement = document.createElement("DIV");
    myElement.style.display = "none";
    myElement.id = "TaskimpOptions";

// We interrupt our definition of the Div element to explain the following
// This will contain all of the HTML for getting/setting the Taskimp options.
// Design will probably take a while.....
    myElement.innerHTML = `<!--  First Column  -->
    <div style='margin: 10px; flex-flow: column'>Taskimp Option Menu
         <span id="TEnable" class='btn btn-success fightBtn' style='margin: 5px;'>Taskimp Enabled</span>
         <span id="TUniverse" class='btn btn-info fightBtn' style='margin: 5px;'>Helium Universe</span>
         <span id="TPretty" class='btn btn-warning fightBtn' style='margin: 5px;'>Display Updates</span>
         <span id="THelpers" class='btn btn-warning fightBtn' style='margin: 5px;'>Game Helpers</span>
         <span id="THeirlooms" class='btn btn-warning fightBtn' style='margin: 5px;'>Heirlooms</span>
         <span id="TSaves" class='btn btn-warning fightBtn' style='margin: 5px;'>Save Options</span>
    </div>
    <!-- Second Column  -->
    <div id = "TOptions" style='flex-basis:70%; flex-flow: row; margin:10px;'>
         <div id="PrettyOptions" style="display: none;">
              <div><span class='btn btn-success' style='width: 80px; margin: 2px;'>Enabled</span> Show zone in browser tab (zone2BTab)</div>
              <div><span class='btn btn-danger' style='width: 80px; margin: 2px;'>Disabled</span> Show zone in messages when starting the zone(nextZone2Spam)</div>
              <div><span class='btn btn-danger' style='width: 80px; margin: 2px;'>Disabled</span> Bionic Wonderland map start time to messages (nextBW2Spam Still a work in Progress)</div>
              <div><span class='btn btn-danger' style='width: 80px; margin: 2px;'>Disabled</span> Add icons to map/world to identify various types of imps.  (Adds not replace)</div>
         </div>
         <ul id = "THelpme" style="display: none;">
              <li>When using Map at Zone and you get stuck in the map chamber, buy map and put you in it when you can afford it.</li>
              <li>Empowerment transfer rate, upgrade, and convert (choose Poison, Wind or Ice)</li>
              <li>Autoequip - toggle on / off at zones specified.</li>
              <li>Player employment (what resource you will help with and when.</li>
         </ul>
         <ul id="SaveOptions" style="display: none;">
              <li>Load/Save/Export/Import Taskimp settings.</li>
              <li>Game save/load as (so you can have multiple saves available)</li>
              <li>Game settings save/load/export/import (so you can save your trimp settings without affecting the game)</li>
         </ul>
    </div>
`;

// Ok, add the options.
leTable.insertAdjacentElement("afterend", myElement);
document.getElementById("TEnable").onclick = TEnable;
document.getElementById("TUniverse").onclick = TUniverse;
document.getElementById("TPretty").onclick = TPretty;
document.getElementById("THelpers").onclick = THelpers;
document.getElementById("TSaves").onclick = TSaves;

function toggleTaskimpMenu(){
	game.options.displayed = true;
    toggleSettingsMenu();
	Taskimp.displayed = !Taskimp.displayed;
	var menuElem = document.getElementById("TaskimpOptions");
    if (Taskimp.displayed) {
        menuElem.style = "display: flex; flex-flow: row nowrap; align-items: stretch;";
        return;
    }
    menuElem.style.display = "none";
    return;
}

})();
