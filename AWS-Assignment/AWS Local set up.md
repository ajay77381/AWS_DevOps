### The Software Development Kit Manager

### create the directory in d rive by the name *dev*

ls -la /mnt/d/dev/

ln -sf /mnt/d/dev/
ls -la
cd dev

git clone https://github.com/ajay77381/java_tdd_maven.git

cd java_tdd_maven/

## Local Java version manager set up-

java -vervsion

``` 
Sudo apt  update
```
```
sudo apt install zip unzip
``
 ``
curl -s "https://get.sdkman.io" | bash
``
Follow the on-screen instructions to wrap up the installation. Afterward, open a new terminal or run the following in the same shell-
 source "$HOME/.sdkman/bin/sdkman-init.sh"


Lastly, run the following snippet to confirm the installation's success:
$ sdk version
```

You should see output containing the latest script and native versions:

SDKMAN!
script: 5.18.2
native: 0.4.6


sdk list java



Now install the required version of java from the given list-

sdk install java 8.0.412-amzn

java -version


