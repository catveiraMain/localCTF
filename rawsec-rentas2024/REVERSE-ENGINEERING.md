# Task 1: Resign Letter

Question: One of our staff have provided a resign letter to the human resource. But our antivirus detected it as malware. It seems there are password embedded inside it. Can you take a look?

Attachment: [Resign-letter-template.rar](https://cdn.discordapp.com/attachments/524898749911400458/1215074639542493245/Resign_letter_template.rar?ex=65fb6d71&is=65e8f871&hm=95d44a7a5b972217013ca98bcd6fb5b96574f56b28851799f6a6f41c9d3288ca&)

Flag: RWSC{p@ss123}

At first I was the one who did this challenge, but then my friend decided to look into it because I was doing something else and used the same method as mine. In which we are using [Oletools](https://github.com/decalage2/oletools) to investigate the content of the macros and by performing the "olevba" on the file, this is the result:
![olevbaoutput](https://media.discordapp.net/attachments/524898749911400458/1215075577992708187/WhatsApp_Image_2024-03-05_at_19.18.28_19a8a34f.jpg?ex=65fb6e50&is=65e8f950&hm=40ac61f7bf6de5a5d3b7071da65338b2849e8266fc2ba3161536744fe0a0ba3f&=&format=webp&width=1072&height=663)

Inside the file, it contains a Shell command that execute and download a file from Github which is "lenovo.exe". My friend look into it by downloading it, and performed "string" command on the file:
![stringsoutput](https://media.discordapp.net/attachments/524898749911400458/1215075987398594570/WhatsApp_Image_2024-03-05_at_19.21.07_d16e8364.jpg?ex=65fb6eb2&is=65e8f9b2&hm=9c7438a1221cca4bd0a051f480d15b754c33769b237afcfd0e413ad8e957458b&=&format=webp&width=732&height=70)
![stringsoutput-2](https://media.discordapp.net/attachments/524898749911400458/1215076192223498331/WhatsApp_Image_2024-03-05_at_19.21.39_b5689bc3.jpg?ex=65fb6ee3&is=65e8f9e3&hm=dbaacfc14e4b00036d8de57b26fb6a95098c821caba2ae69fb938e3bb704b304&=&format=webp&width=738&height=28)

So there are some weird string that he knows it needs to be decoded and he brings it to base64 decoder:
![base64decoder](https://media.discordapp.net/attachments/524898749911400458/1215076831678435378/WhatsApp_Image_2024-03-05_at_18.38.16_fc1b5cc2.jpg?ex=65fb6f7b&is=65e8fa7b&hm=1abf270866d60a3d6f43129112f86535417985ae8e45c0b7a9709b04afc32876&=&format=webp&width=968&height=663)
