This is a wrapper for a cryptonote currency command line wallet. It was tested using bitmonerod.exe and the accompanying simplewallet.exe. Although the program has only been tested on Windows 7, I believe it should run on linux as well.

It is still quite a buggy program, but I don't think there should be anyway to lose your coins. 

The general idea is that you unzip/clone the repository to the folder which contains the daemon and wallet program (and possibly your wallet file). Then run kivywallet.py to start the program. You can also initial with two arguments, which will be interpreted as your wallet file name and password, for instance: kivywallet.py mywallet.bin mysecretpassword.

After starting the program, if you don't already have the bitmonderod daemon running, press the button at the top left to start it. If you passed your wallet and password as arguments, then the Wallet name and Wallet password fields should already be filled in, otherwise enter a wallet name and password. If the wallet doesn't exist in the local directory, it will be created when the simplewallet daemon is launched.

Next, press the button at the upper right to launch the simplewallet daemon. You should see your address displayed after this step, and another window should launch the simplewallet daemon. If you're creating a new address it can take a few seconds to get the daemon window launched.

Now you can press the Refresh balance button. It will just say "Out of sync" until both the bitmonerod and simplewallet daemons are fully synced. After everything is up to date, you should see your wallet balance displayed after pressing refresh balance.

The transactions portion at the bottom half of the screen seems to work OK. Just keep in mind that you cannot attach a payment ID to a transaction using the JSON RPC, so please heed the warning and DO NOT try and send funds to a coin exchange.

There are several things you can do to crash the program. For example, if you push the Transfer funds button when all of the input fields are empty, the program will simply close. This was more an exercise for myself to learn some Kivy, but I thought I would share it, since as far as I know there still aren't any GUIs for cryptonote wallets. Hope you enjoy, and would be glad to hear any comments or suggestions.

The only dependency required besides python is the requests library and Kivy itself (I used v1.8).
