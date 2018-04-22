# Install the latest version of Bibliograph

With the scripts in this directory, you can easily download, install and test
the latest version of Bibliograph (including alpha and beta versions). Your
currently running instance will not be touched. Instead, the new version will
be installed in a separate directory, and a copy of all data will be imported
into the new instance. This will allow you to extensively test the new version 
before going into production with it, and even after that, the old version is kept
fully functional until deleted. 

In order to install the new version, please proceed as follows:

1. Configuration (`app.conf.toml`) 
  - If this is the first install: 
    ```
    cp app.conf.toml.dist app.conf.toml
    cp install.sh.dist install.sh && chmod +x ./install.sh
    ```
    Adapt both `app.conf.toml` and `install.sh` with the parameters that
    match your local installation
  - If you are updating the installation, check the release notes to se if you 
    have to modify `app.conf.toml` (usually not needed)
  - To edit the file, I recommend to install/activate a plugin for editing
    ".toml" file in your editor (i.e. for Sublime Text, [this one](https://packagecontrol.io/packages/TOML)). 
    This will allow to validate your changes and prevent errors. 
  - Please do not change the placeholders ("{{...}}") which are dynamically
    replaced by the install script
2. Run ./install.sh in this directory
3. Open a browser window at the URL that is displayed at the end of a successful
   installation. On a Mac, you can hold the "Command" Key and double-click on the
   URL. 
  