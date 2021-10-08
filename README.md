# eslamp - Eww, Stop Looking At My Privates!
or P**n, you degenerate.<br>
<br>
<br>
Simple script that encrypts files, randomizes their names, and logs them for user reference or management.<br>
No more third-parties. Preserve your privacy, your own way.<br><br>
This was for my personal use, but decided to upload it for others to try as well.

Powered by [7za](https://www.7-zip.org).

## What does it do?
Using 7za, it compresses (optional) your files into an archive, encrypting it (aes-256) with your password, generates a random string to place on newly created archive, and stores that archive's reference name on a text file for your convenience.

## Potential use
* Discourages employers or organization admins from snooping your files.
* Private file-sharing.
* Prevent hackers from accessing your files in case of server breaches. (as long as you use a strong password!)
* Preserving your privacy.
* Depends on your use case, but might be a good alternative to boxcryptor, cryptomator, axcrypt, or aescrypt.

## Setting parameters (DO THIS FIRST)
Open `eslamp.bat` in your text editor of choice (i'll be using [Notepad++](https://notepad-plus-plus.org)).
![2021-08-25_4-40-40](https://user-images.githubusercontent.com/65538621/130700590-fda140ee-98f3-4641-807c-193ac4883032.png)

Use a password generator, like this one: https://passwordsgenerator.net<br>
Make sure you DON'T include symbols, because it may affect batch processing. (some symbols are allowed, but it's better to be safe)

## Encrypting your files
This is what it'll look like on launch.<br>
![2021-08-25_4-40-40](https://user-images.githubusercontent.com/65538621/130687253-6a794ef3-256a-4423-9ba2-396f0d355cf8.png)
<br>Enter the folder or path that contain your confidential files or file.<br>
![2021-08-25_4-46-39](https://user-images.githubusercontent.com/65538621/130687862-09c61c89-64c4-4372-ae69-a3f309905801.png)
<br>Enter a reference name. This is for tracking your files. Cuz names will be randomized.<br>
![2021-08-25_4-40-40](https://user-images.githubusercontent.com/65538621/130688405-4f7afef1-4192-4761-8928-92fe05a8e8e7.png)
<br>Once encryption is done, you have the choice to randomize your archive name or not.<br>
![2021-08-25_4-40-40](https://user-images.githubusercontent.com/65538621/130689220-12ccee62-686b-43ec-a9f1-5f3eee89894e.png)
<br>A file named `filelog.txt` will be created that contain your reference file names. You can then proceed to keep that log or remove it. The more you encrypt files, the more logs will be stored in that text file. Think of it as a database.<br>
![2021-08-25_4-40-40](https://user-images.githubusercontent.com/65538621/130691638-1d92d1d1-a6a9-4e2a-b010-a06fbb4768c0.png)

## Decrypting your files
Enter `dec` on launch.<br>
![2021-08-25_4-40-40](https://user-images.githubusercontent.com/65538621/130694683-fe48ab3a-edb1-456a-b054-fee3fe3ce526.png)
<br>Then Enter again (don't type anything on second prompt), until you reach Decryption mode.<br>
![2021-08-25_4-40-40](https://user-images.githubusercontent.com/65538621/130694990-83f8a9ab-7ec4-469c-90dc-ca356b881006.png)
<br>Make sure the file you're trying to decrypt is in the same path or directory as `eslamp.bat`.<br>
![2021-08-25_4-40-40](https://user-images.githubusercontent.com/65538621/130695379-ae0efa90-0026-4fc2-b769-da6d57848d57.png)

## Managing your files
Just use `CTRL`+`F` to find your files.
![2021-08-25 06 10 06 drive google com c4cf7359b68b](https://user-images.githubusercontent.com/65538621/130696764-d2cc4b15-f9fa-4deb-8db6-7c527b8af056.png)
![2021-08-25_4-40-40](https://user-images.githubusercontent.com/65538621/130697369-e1015637-73a5-4f88-a7b7-d3f7bad13bbd.png)

## Decrypting files as end-user
You have an encrypted file, and you want to share that encrypted file to someone. That's where `key.bat` comes in.<br>

Before anything else, make sure you edit the parameters in `key.bat` as well.<br>
The password in `key.bat` MUST be the same as `eslamp.bat`.

Send that encrypted file to someone, then SEPARATELY send `key.bat` in a secure channel (`key.bat` is an EXPOSED password).<br>
You can send them alongside, but it's on your own risk. Try https://wormhole.app

Instruct the end-user to have `key.bat` and the encrypted file in the same directory or folder, then run it.

Oh btw, it auto-deletes. With a surprise at the end ;) Make sure you make copies.

## Known bugs
* Won't delete first log. Solution for now: remove it urself lol. I need to study more powershell.

## Planned features
* Better UI
* Filelog querying
* Bug fixes
* Universal compatibility (bash)

## License
[WTFPL](https://github.com/sabakuran/eslamp/blob/main/LICENSE)<br>
I don't care whatever you do with it. Improve it, steal it, sell it, claim it, up to you. It's messy code anyways.
