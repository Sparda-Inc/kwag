kwag = "kivy wallet gui" RPC wrapper
This is initial experimental kivy based version of duckNote GUI. KWAG needs working ./ducknoted and ./simplewallet with open RPC ports. 

Possible use cases:

1. Running local  ./ducknoted and ./simplewallet and interacting with them by JSON-RPC via kwag GUI.
2. Running remote ./ducknoted and ./simplewallet and interacting with them by JSON-RPC via kwag GUI remotely via any OS/device. 

Dependencies:
kivy >1.8

<code>
sudo add-apt-repository ppa:kivy-team/kivy;sudo apt-get update;sudo apt-get install kivy
</code>

To run kwag:

1. Run ducknoted with <code>--rpc-bind-port=42081</code>
2. Run simplewallet you want to use with KWAG with <code>--rpc-bind-port=42082</code>
3. Unzip KWAG to your "ducknote" folder or any folder where ducknoted, simplewallet and probably your wallet files are located.
4. Run kivywallet.py with <code>python kivywallet.py</code> command. Make sure you got both ducknoted and simplewallet syncronized. 
5. Use at your own risk, there is NO WARRANTY, software is experimental. 

Under development.

NOTE:
KWAG is kivy based, and can be loaded on any OS/device. 
E.G. follow python-android instructions and try to run it on your android device. You can control remote wallet via GUI application.

1. https://github.com/kivy 
2. https://github.com/kivy/buildozer
3. http://kivy.org/docs/guide/android.html
4. http://kivy.org/docs/guide/packaging-android.html


