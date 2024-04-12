## JDK-Updater

JDKUpdater works from MacOS 14 onwards.

JDKUpdater is a little tool, written in Swift, that should help you to keep track
of updates related to builds of OpenJDK and GraalVM.

Be aware that it takes some time to find all installed JVM's at startup, after the
initial scan, it will be repeated automatically every 3 hours.

It scans the ~/Library/Java folder for installed builds of OpenJDK and GraalVM and
should be able to detect the following distributions:

- AdoptOpenJDK
- AdoptOpenJDK J9
- Bisheng
- Corretto
- Dragonwell
- Gluon GraalVM
- GraalVM community
- GraalVM
- Homebrew build of OpenJDK
- JebBrains
- Kona
- Liberica
- Liberica NIK
- Mandrel
- Microsoft
- OJDKBuild
- OpenLogic
- Oracle OpenJDK
- Oracle JDK
- RedHat
- SAP Machine
- Semeru
- Semeru certified
- Temurin
- Trava
- Zulu
- Prime


![JDKUpdater](https://github.com/HanSolo/JDK-Updater/raw/main/screenshots/JDKUpdater.png)


The application is a stand alone application and will show you the latest early access and
general availability builds that it found for each distribution.

In addition it will identify jbang, sdkman, homebrew and nix managed builds of OpenJDK.
It will also offer you the downloads of the available files that it found (tar.gz, zip, pkg, dmg) for
download. To enable the scanning for one of these package managers you have to enable them in the
menubar icon menu.

![MenubarIconMenu](https://github.com/HanSolo/JDK-Updater/raw/main/screenshots/JDKUpdater_MenuBar.png)

There are indicators for the JVM type (JDK / JRE) and the architecture of the installed JVM (x64/ARM).

The Download button in the toolbar will enable you to download a specific distribution of your choice.
In the Download view you can select the distribution (e.g. Zulu, JetBrains etc.), the available major 
versions (e.g. 17, 18, 19, 20, 21 etc.) for this distribution, the available updates (e.g. 17.0.8, 17.0.9, 17.0.10 etc.) 
and finally the packages you can download (e.g. dmg, pkg, tar.gz or zip).

![DownloadView](https://github.com/HanSolo/JDK-Updater/raw/main/screenshots/JDKUpdater_Download.png)

In the Toolbar you will find a button named "Projects" which will open an OpenJDK Project explorer where
you can search for existing OpenJDK projects. If you click on a project, it will be opened in your default
browser.

![ProjectExplorer](https://github.com/HanSolo/JDK-Updater/raw/main/screenshots/JDKUpdater_ProjectExplorer.png)

There is also a button called "JEPs" in the toolbar which will open a JEP explorer where you can search for
existing JEP's (JDK Enhancement Proposals) and open them in your default browser by clicking on a JEP.
If you click on the info icon on the left side of each JEP, it will show you the summary of this JEP in the
lower part of the window.

![JEPExplorer](https://github.com/HanSolo/JDK-Updater/raw/main/screenshots/JDKUpdater_JEPExplorer.png)

It will download the file to your Downloads folder and from there you can install it as you would normaly do.
In case it finds a distribution that is managed by sdkman, you will see an install button.
Once you click that button, it will open a terminal window and it will copy the command sdk install java x.y.z-DISTRO
to the clipboard. Meaning to say you can simply press ⌘ + v and it will paste it into the terminal so that you can
execute the installation by sdkman by pressing enter.

In case it finds a distribution that is managed by jbang, pressing the install button will download and install the
selected JDK in the correct folder on your drive and no further action is needed.

The distribution that is set as default JVM in MacOS will be highlighted by a bold italics font. This doesn't mean that
you cannot set a different JAVA_HOME variable in .bash_profile or .zshrhc. The default JVM is the one that you get when you
execute /usr/libexec/java_home.
MacOS will choose a JVM from the folder /Library/Java/JavaVirtualMachines and in addition the JVM Info.plist file needs
to be in the folder /JVM_NAME/Contents/Info.plist to be correctly detected by libexec. 

When clicking on the name of the distribution, a context menu will open with two entries. You can either open the
download page of the selected distribution in your default browser or open the installation path of the distribution 
in a terminal window.

There are also 2 widgets (small and medium) available that show the next upcoming release and how long it will take
to the next release and to the next update of the OpenJDK project.

![WidgetSmall](https://github.com/HanSolo/JDK-Updater/raw/main/screenshots/JDKUpdater_Widget_Small.png)

![WidgetMedium](https://github.com/HanSolo/JDK-Updater/raw/main/screenshots/JDKUpdater_Widget_Medium.png)
