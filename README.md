# Follina-lab

this lab is from Blue Team Labs Online (BTLO)

steps by steps:
this is the lab that we will try to solve it (i aready solve some of the qoution)
`imae of the lab`

let downlaod the file of this lab that contain the chalenge
notice: i will solve this lab in isolated envirment becase it malwear

firstthings we will do is to unzip the file uing cmmand `unzip`

we will `sample.doc`
lets start with sloving qoutions 

Question 1) What is the SHA1 hash value of the sample? (Format: SHA1Hash) 
answer is 06727ffda60359236a8029e0b3e8a0fd11c23313
`get the hash of the file`

Question 2) According to VirusTotal, what is the full filetype of the provided sample?

let open VirusTotal and past in it the hash of the file 
answer: Office Open XML Document
`filetype virustotal`

Question 3) Extract the URL that is used within the sample and submit it?

firstfall i thing that the answer is in viruestotal becase i open the file and i found it empty so i didnt find anything in virueTotal 
so i start to thing maybe there is hidden text and the filetype said that its *open xml document*
so i use `strings` cmmand to see what is the hidden text
`strings to open the file`

from that i see that there is files insied that file and i decaver that it is zip file by seeing *PK* at the end of the file and it mean that its zip file
let chnage the extension of the file to zip and unzip it with `unzip`
`change file extension`

lets search in these files and look for that url 
Answer:https://www.xmlformats.com/office/word/2022/wordprocessingDrawing/RDF842l.html!
`get URL file`

Question 4) What is the name of the XML file that is storing the extracted URL? (Format: file.name.ext)
Answer:document.xml.rels

Question 5) The extracted URL accesses a HTML file that triggers the vulnerability to execute a malicious payload. According to the HTML processing functions, any files with fewer than <Number> bytes would not invoke the payload. Submit the <Number> (Format: Number of Bytes) 

to get the answer of this Question and all other Question in the bottom we need to search for this type of vulnblity and we will get the answer *but* what i will do is to proform that vulnblity in my lap at `(my lab link)` and see it effects and see what logs it create
















