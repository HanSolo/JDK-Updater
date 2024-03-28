## JDK-Updater

JDK Updater is a little tool, written in Swift, that should help you to keep track
of updates related to builds of OpenJDK and GraalVM.
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


![JDK Updater](https://i.ibb.co/WvzQM9Z/JDKUpdater.png)


The application is a stand alone application and will show you the latest early access and
general availability builds that it found for each distribution.

In addition it will scan ~/.jbang/cache/jdks and ~/.sdkman/candidates/java for installed builds of OpenJDK.
It will also offer you the downloads of the available files that it found (tar.gz, zip, pkg, dmg) for
download. 

There are indicators for the JVM type (JDK / JRE) and the architecture of the installed JVM (x64/ARM).

It will download the file to your Downloads folder and from there you can install it as you would normaly do.
In case it finds a distribution that is managed by sdkman, you will see an install button.
Once you click that button, it will open a terminal window and it will copy the command sdk install java x.y.z-DISTRO
to the clipboard. Meaning to say you can simply press ⌘ + v and it will paste it into the terminal so that you can
execute the installation by sdkman by pressing enter.

In case it finds a distribution that is managed by jbang, pressing the install button will download and install the
selected JDK in the correct folder on your drive and no further action is needed.

When clicking on the name of the distribution, a context menu will open with two entries. You can either open the
download page of the selected distribution in your default browser or open the installation path of the distribution 
in a terminal window.

