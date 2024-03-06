# Task 1: Last Hope
Question: flag = RWSC{wifipass}

Hint: Have you ever used Aircrack?

Attachment: [RAWSECWIFI-01.cap](https://cdn.discordapp.com/attachments/524898749911400458/1215070736184639528/RAWSECWIFI-01.cap?ex=65fb69ce&is=65e8f4ce&hm=9362f65b3c1427e1aec4305e5682f04cf2a9d9f152f11f238622b42864846b5c&)

Flag: RWSC{anonymous}

Not gonna lie, I thought this one requiring 4-way handshake checking inside Wireshark, but it was Aircrack the whole time. I figured it out before the hint was revealed and so I decided to crack the wifi password by using a aircrack dictionary attack with "rockyou.txt" word list file. This is the output:

![aircrackoutput](https://media.discordapp.net/attachments/524898749911400458/1215072722586050611/WhatsApp_Image_2024-03-05_at_10.51.16_47538c59.jpg?ex=65fb6ba8&is=65e8f6a8&hm=0a7915fb5dfc1e5da36e851ccbe7208c029f54b63af8d3685b6c43c99c5737c9&=&format=webp&width=590&height=663)
