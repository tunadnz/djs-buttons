![Image](https://img.shields.io/npm/v/djs-buttons?style=flat-square&color=0091EA)
![Image](https://img.shields.io/npm/dt/djs-buttons.svg?style=flat-square&color=0091EA&maxAge=3600) 

#

# 📥 Yüklemek İçin
```npm
npm i djs-buttons
```

# ❗️ Uyarı
```javascript
//----------------------------Main----------------------------\\

const Discord = require('discord.js');
const client = new Discord.Client();
const { MessageButton, MessageActionRow } = require('djs-buttons');
require('djs-buttons')(client);
// --> Ek Bir İşlem Yapmanıza Gerek Yok Ana Dosyanıza Tanımlamanız Yeterli Olacaktır.

//------------------------------------------------------------\\
```

# ⚙️ Örnek Method Kullanımı
```javascript

//-----------------------Örnek-----------------------\\

const Discord = require('discord.js');
const client = new Discord.Client();
const { MessageButton, MessageActionRow } = require('djs-buttons');

client.on("clickButton", async (button) => {
await button.clicker.fetch();
//await button.defer();
const utilityEmbed = new MessageEmbed().setDescription(`${button.clicker.user.tag}`);

const btn = new MessageButton()
.setEmoji("")
.setID("button_1")
.setStyle("blurple");
.setURL("");
.setDisabled();

const row = new MessageActionRow().addComponent(btn);
await button.channel.send("Selam!", { components: row });
await button.reply.send("Selam!", { components: row });
});

//---------------------------------------------------\\
```

# 💬 İletişim
[Discord](https://discord.gg/rVnKDGcRKR) 
