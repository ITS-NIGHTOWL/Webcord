[![npm version](https://badge.fury.io/js/webcord.svg)](https://www.npmjs.com/package/webcord)
[![npm](https://img.shields.io/npm/dm/Webcord)](https://www.npmjs.com/package/webcord)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat)](https://github.com/ITS-NIGHTOWL/Webcord/issues)
[![Discord Shield](https://discord.com/api/guilds/687072684819087533/widget.png?style=shield)](https://discord.gg/R9N24NW)
--------------------------------------------------------------------------------------------		
# Webcord		
Webcord is an easy to use, Discord compliant webhook module for Node.js, featuring a simplistic design inspired by [Discord.js](https://discord.js.org/#/) message embeds.<br>
It ships with Typescript support by default (no need to create those pesky typings), and requires zero dependencies!

## Installation		

Using npm:

```shell
npm install webcord		
 ```		

## Examples

The code below features every method built into Webcord. Think of it as the documentation.
Highlighting over the code in [Visual Studio Code](https://code.visualstudio.com/) also shows what the methods do.
### Posting to a Webhook
 ```js		
const webcord = require("webcord")

new webcord({
    url: "https://discordapp.com/api/webhooks/712433174063349761/-YgMVHCyQlfxval8rwJYO79CuJjrIj1jwAqePLluBgfQseU0FFH1GhEeiJf8bxnmfWOQ", // Discord webhook url
    name: "Webcord v2.0.0", // Webhook display name
    avatar: "https://cdn.clipart.email/401241ecd4daff63d501b958f75a734b_discord-logo-icon-293532-free-icons-library_250-250.png" // Webhook display avatar
}) // Configures the webhook
.setTitle("Add titles like this") // Sets an embed title
.setDescription("Set some descriptions") // Sets an embed description
.addField('Add single fields:', "like me!", false) // Adds an embed field (max 25 fields)
.addFields({
    name: "Hate repeating yourself?",
    value: "set mutliple fields with the `.addFields()`!",
    inline: false
},
{
    name: "I'm another field",
    value: "Set with the `addFields()` method!",
    inline: false
}) // Adds multiple fields at once (max 25 fields)
.setAuthor({
    name: "Easily set an author field",
    icon: "https://discord.com/assets/2c21aeda16de354ba5334551a883b481.png",
    url: "https://www.npmjs.com/package/webcord"
}) // Sets an embed author
.setFooter({
    text: "I'm a footer",
    icon: "https://discord.com/assets/e05ead6e6ebc08df9291738d0aa6986d.png"
}) // Sets an embed footer
.setURL("https://www.npmjs.com/package/webcord") // Adds a URL to the embeds title
.setImage("https://discord.com/assets/fc0b01fe10a0b8c602fb0106d8189d9b.png") // Sets the image of the embed
.setTimestamp() // Sets the timestamp of the embed
.setThumbnail("https://discord.com/assets/f72fbed55baa5642d5a0348bab7d7226.png")
.setColor("#7289DA") // Sets an embed color
.inc() // Creates another embed
.setTitle("This title is a part of the new embed!") // Creates a title on the new embed
.send("This is an optional plain text message").then((res) => {
    console.log(res) //Logs all request information to the console
}) 
/*
 Every webcord message must use the .send() method at the end to fire the POST request.
 It also supports a promise which returns request information after the POST request is sent out.
*/
 ```
The above code outputs this:

<img src='https://media.discordapp.net/attachments/712436922290536448/712448785648844850/preview.png'>		

# Contributing		
Webcord Contributors can be found [here](https://github.com/ITS-NIGHTOWL/Webcord/graphs/contributors)!		
Want to contribute? Follow the [Contributing Guide](https://github.com/ITS-NIGHTOWL/Webcord/blob/master/CONTRIBUTING.md)!		
