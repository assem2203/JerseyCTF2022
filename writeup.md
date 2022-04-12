JerseyCTF2022
===========

[assem] JerseyCTF 2022 Writeup
----------------------------
This is the writeup of Team(assem) competition JerseyCTF 2022.    
(with. https://github.com/Accio3014)

______________

# [crypto]
### #1 salad
Roman generals really knew how to make salad!   
   atkw{plddp_jrcru_uivjjzex}  
flag hint : Look up some common types of ciphers.
```
 score: 50
 flag : jctf{yummy_salad_dressing}
 solve: Decode to Caesar’s Code.(ROT-9)
```

 ### #2 new-algorithm
On the first day of the job, a new cryptography intern is insisting to upper management that he developed a new encryption algorithm for the company to use for sensitive emails and should get a raise. This seems too good to be true... are you able to prove the intern wrong by decrypting it?
   Here's an example of an encrypted email message using the intern's algorithm: amN0Znt0UllfQUVTX0lOc1QzQGR9    
flag hint : What are some differences between encryption, encoding, and hashing?
 ```
score: 75
 flag : jctf{tRY_AES_INsT3@d}
 solve: Decode to base64.
```

______________

# [Forensics]
 ### #2 speedy-at-midi
Your partner-in-crime gets a hold of a MIDI file, riff.mid, which intelligence officials claim to contain confidential information. He has tried opening it in VLC Media Player, but it sounds just like the piano riff in riff.mp3. Can you find the right tool to extract the hidden data?  
flag hint : You wouldn't have the audacity to try using a MIDI editor, would you?
```
 score: 150
 flag : jctf{kicking_it_since_1983}
 solve: riff.mid and riff.mp3 file have the same signature.
        Open the riff.mid file in the GarageBand.
```

 ### #3 data-backup
The backup of our data was somehow corrupted. Recover the data and be rewarded with a flag.    
flag hint : Try a tool a surgeon might use.
 ```
 score: 250
 flag : jctf{fun_w17h_m461c_by735}
 solve: $ file data-backup
        $ binwalk –e data-backup
        $ ls –al
        The flag.pdf file is extracted
```

______________

# [web]
### #2 speedy-at-midi
Seigward has been storing his secrets on his website https://jerseyctf.co for decades. Hasn't failed him yet.  
flag hint : Where can you find a website's code?
```
 score: 100
 flag : jctf{1M_s0_1M_5o_Dyn4Mit3_092478}
 solve: Open website. Push F12 and you find flag in "login.js“.
              Decode the string in the “login.js” file to base64.
```


