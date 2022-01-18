## EMO

## Description
This challenge under forensics requires multiple tools to identify the flag.

## Hints

<details> 
  <summary>1: Stuck at obfuscated Macro. </summary>
   A: You can run the sample in a VM to get the second stage payload as a new powershell process under Wmiprvse with the encoded commandline. You can also debug the macro in VBEdit to understand it's flow and identify the replace statement where you should break at. You can also dump the encoded payload with strings and then deobfuscate with the correct contents of replace.
</details>

<details> 
  <summary>2: Stuck at decoding Powershell -Encod. </summary>
   A: Base64 decoding it with utf-8 gives garbled text. However, the command runs without any issues. So I bypassed the hunt for the correct encoding by using powershell script block logs.
</details>

<details> 
  <summary>3: Stuck at deobfuscating Powershell</summary>
   A: PSdecode to make it humand readable.
</details>

<details> 
  <summary>4: URLs seem down</summary>
   A: URLs are used for another purpose. Analyze the decoded powershell to understand it's flow and how it's creating the possible dropped files. Start messing with the code and running it to get the file to be written.
</details>

<details> 
  <summary>5: URLs seem down</summary>
   A: Analyze the decoded powershell to understand it's flow and how it's creating the possible dropped files. Start messing with the code and running it to get the file to be written.
</details>

<details> 
  <summary>6: Where's the Flag?</summary>
   A: Analyze the decoded powershell again to identify the encoding the author uses and then reverse it to get the flag.
</details>