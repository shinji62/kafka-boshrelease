# Hybris - bosh java package

### Description
This project is used for java packages in BOSH releases.

### How to use
1. Add this repository to your bosh release project packages folder:

   ```bash
   $> cd ~/bosh-release-x
   $~/bosh-release-x> git submodule add https://github.wdf.sap.corp/idefix/bosh-package-java packages/java
   ```
2. Checkout the version you need by looking at the available tags:

   ```bash
   $~/bosh-release-x> git submodule update --init --recursive
   $~/bosh-release-x> cd packages/java
   $~/bosh-release-x/packages/java> git checkout <tagname>
   $~/bosh-release-x/packages/java> cd ..
   $~/bosh-release-x>
   ```
3. Download the java tar file matching the tag you selected (see table below for the *url* and *output filename*).

   ```bash
   $~/bosh-release-x> cd tmp
   $~/bosh-release-x/tmp> wget <url> -O <output filename>
   ```
4. Add the downloaded file to your project blobs

   ```bash
   $~/bosh-release-x> bosh add blob tmp/<output filename> java
   ```
5. Adapt your bosh release dependencies, scripts, etc..., to match this new package
6. Finally test and do a final release

### Files
The files can be downloaded from the following locations:

| OS | Type | Version | Download URL | Output Filname |
| -------- | -------- | -------- | ------------ | -------- |
| lucid | JRE | 1.7.0_55 | https://download.run.pivotal.io/openjdk/lucid/x86_64/openjdk-1.7.0_55.tar.gz | openjdk-jre-lucid-1.7.0_55.tar.gz |
| trusty | JDK | 1.7.0_65 | https://download.run.pivotal.io/openjdk-jdk/trusty/x86_64/openjdk-1.7.0_65.tar.gz | openjdk-jdk-trusty-1.7.0_65.tar.gz |
| trusty | JRE | 1.7.0_65 | https://download.run.pivotal.io/openjdk/trusty/x86_64/openjdk-1.7.0_65.tar.gz | openjdk-jre-trusty-1.7.0_65.tar.gz |
| trusty | JDK | 1.8.0_25 | https://download.run.pivotal.io/openjdk-jdk/trusty/x86_64/openjdk-1.8.0_25.tar.gz | openjdk-jdk-trusty-1.8.0_25.tar.gz |
| trusty | JRE | 1.8.0_25 | https://download.run.pivotal.io/openjdk/trusty/x86_64/openjdk-1.8.0_25.tar.gz | openjdk-jre-trusty-1.8.0_25.tar.gz |
| trusty | JDK | 1.8.0_40 | https://download.run.pivotal.io/openjdk-jdk/trusty/x86_64/openjdk-1.8.0_40.tar.gz | openjdk-jdk-trusty-1.8.0_40.tar.gz |
| trusty | JRE | 1.8.0_40 | https://download.run.pivotal.io/openjdk/trusty/x86_64/openjdk-1.8.0_40.tar.gz | openjdk-jre-trusty-1.8.0_40.tar.gz |
| trusty | JDK | 1.8.0_45 | https://download.run.pivotal.io/openjdk-jdk/trusty/x86_64/openjdk-1.8.0_45.tar.gz | openjdk-jdk-trusty-1.8.0_45.tar.gz |
| trusty | JRE | 1.8.0_45 | https://download.run.pivotal.io/openjdk/trusty/x86_64/openjdk-1.8.0_45.tar.gz | openjdk-jre-trusty-1.8.0_45.tar.gz |
