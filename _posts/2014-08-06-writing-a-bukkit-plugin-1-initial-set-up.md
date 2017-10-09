---
id: 420
title: 'Writing a Bukkit plugin #1 (Initial Set-Up)'
date: 2014-08-06T15:38:09+00:00
author: Duncan Leo
layout: post


categories:
  - Bukkit Plugins
---
Requirements:<figure style="width: 177px" class="wp-caption alignleft">

<img src="http://mtacertification.com/images/core-java.jpg" alt="" width="177" height="125" /><figcaption class="wp-caption-text">Oracle Java</figcaption></figure> 

Oracle Java. Most servers today run Java 7, and it is recommended that you develop your plugins on that version. While you can use older versions of Java, plugins written using the new Java 8 **will not work on Java 7 servers.**     This is the general layout of a Bukkit plugin (the contents of the JAR file) Root &#8211; &#8216;package name&#8217; folder &#8211; &#8216;META-INF&#8217; folder &#8211; plugin.yml <span style="text-decoration: underline;">&#8216;Package name&#8217; folder</span> The package name folder is a folder containing more folder in it, based on your plugin&#8217;s package name. For example, a plugin named com.test.example will have the &#8216;com&#8217; folder, a &#8216;test&#8217; folder in the &#8216;com&#8217; folder and an &#8216;example&#8217; folder within the &#8216;test&#8217; folder. <span style="text-decoration: underline;">META-INF</span> This folder is auto-generated. It may be ignored. <span style="text-decoration: underline;">plugin.yml</span> This file contains data for the Bukkit server to read.   For developing Bukkit plugins, one can use any Integrated Development Environment, but for this example, we will be using **Eclipse Luna.**

Follow the steps below to set up Eclipse, download Bukkit and create your first plugin.

1. Go to[ https://www.eclipse.org/](https://www.eclipse.org/ "Eclipse")<figure id="attachment_435" style="width: 234px" class="wp-caption alignnone">

[<img class="wp-image-435" src="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_homepage-620x681.png" alt="Screenshot of the Eclipse.org homepage" width="234" height="257" srcset="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_homepage-620x681.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_homepage-940x1033.png 940w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_homepage.png 1366w" sizes="(max-width: 234px) 100vw, 234px" />](/thinking-minecraft/wp-content/uploads/2014/08/eclipse_homepage.png)<figcaption class="wp-caption-text">Screenshot of the Eclipse.org homepage</figcaption></figure> 

2. Click on &#8216;Download&#8217;, and choose your OS.<figure id="attachment_437" style="width: 232px" class="wp-caption alignnone">

[<img class="wp-image-437" src="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_download-620x1194.png" alt="Screenshot of the Eclipse.org download page (for Linux)" width="232" height="446" srcset="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_download-620x1194.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_download-940x1810.png 940w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_download.png 1366w" sizes="(max-width: 232px) 100vw, 232px" />](/thinking-minecraft/wp-content/uploads/2014/08/eclipse_download.png)<figcaption class="wp-caption-text">Screenshot of the Eclipse.org download page (for Linux)</figcaption></figure> 

3. After downloading the file, install it, depending on your OS. (i.e. install (Windows), copy to Applications folder (Mac) and extract to somewhere (Linux)). Launch the program.<figure id="attachment_439" style="width: 229px" class="wp-caption alignnone">

[<img class="wp-image-439" src="/thinking-minecraft/wp-content/uploads/2014/08/blank_eclipse-620x336.png" alt="Screenshot of Eclipse" width="229" height="124" srcset="/thinking-minecraft/wp-content/uploads/2014/08/blank_eclipse-620x336.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/blank_eclipse-940x509.png 940w, /thinking-minecraft/wp-content/uploads/2014/08/blank_eclipse.png 1366w" sizes="(max-width: 229px) 100vw, 229px" />](/thinking-minecraft/wp-content/uploads/2014/08/blank_eclipse.png)<figcaption class="wp-caption-text">Screenshot of Eclipse</figcaption></figure> 

4. Open the menu **File > New > Java Project.**<figure id="attachment_440" style="width: 121px" class="wp-caption alignnone">

[<img class="wp-image-440" src="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_newproject.png" alt="New Java Project window in Eclipse" width="121" height="146" />](/thinking-minecraft/wp-content/uploads/2014/08/eclipse_newproject.png)<figcaption class="wp-caption-text">New Java Project window in Eclipse</figcaption></figure> 

5. Give it a name, and click &#8216;Create&#8217;.<figure id="attachment_441" style="width: 249px" class="wp-caption alignnone">

[<img class="wp-image-441" src="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_newlycreatedproject-620x336.png" alt="Screenshot of a newly created project" width="249" height="135" srcset="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_newlycreatedproject-620x336.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_newlycreatedproject-940x509.png 940w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_newlycreatedproject.png 1366w" sizes="(max-width: 249px) 100vw, 249px" />](/thinking-minecraft/wp-content/uploads/2014/08/eclipse_newlycreatedproject.png)<figcaption class="wp-caption-text">Screenshot of a newly created project</figcaption></figure> 

6. Download a Bukkit JAR file. **Take Note: ****We&#8217;re looking for a Bukkit JAR file, NOT a CraftBukkit one.** Download link: [https://dl.bukkit.org/downloads/craftbukkit/list/dev/](https://dl.bukkit.org/downloads/craftbukkit/list/dev/ "Bukkit DEV builds")<figure id="attachment_442" style="width: 250px" class="wp-caption alignnone">

[<img class="wp-image-442" src="/thinking-minecraft/wp-content/uploads/2014/08/craftbukkit_download-620x536.png" alt="CraftBukkit download page" width="250" height="216" srcset="/thinking-minecraft/wp-content/uploads/2014/08/craftbukkit_download-620x536.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/craftbukkit_download-940x813.png 940w, /thinking-minecraft/wp-content/uploads/2014/08/craftbukkit_download.png 1366w" sizes="(max-width: 250px) 100vw, 250px" />](/thinking-minecraft/wp-content/uploads/2014/08/craftbukkit_download.png)<figcaption class="wp-caption-text">CraftBukkit download page</figcaption></figure> 

After selecting your desired build, scroll down and click on the link in **&#8216;Upstream Artifacts&#8217;.**   7. Download the file, place it somewhere that you can remember.<figure id="attachment_443" style="width: 253px" class="wp-caption alignnone">

[<img class="wp-image-443" src="/thinking-minecraft/wp-content/uploads/2014/08/bukkit_download-620x500.png" alt="bukkit_download" width="253" height="204" srcset="/thinking-minecraft/wp-content/uploads/2014/08/bukkit_download-620x500.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/bukkit_download-940x759.png 940w, /thinking-minecraft/wp-content/uploads/2014/08/bukkit_download.png 1366w" sizes="(max-width: 253px) 100vw, 253px" />](/thinking-minecraft/wp-content/uploads/2014/08/bukkit_download.png)<figcaption class="wp-caption-text">Bukkit download page</figcaption></figure> 

8. Right-click your project name in Eclipse and click &#8216;Properties&#8217;. Navigate to **Java Build Path** and to the **Libraries **tab.<figure id="attachment_446" style="width: 246px" class="wp-caption alignnone">

[<img class="wp-image-446" src="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_libraries-620x473.png" alt="Screenshot of Eclipse's Libraries window" width="246" height="188" srcset="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_libraries-620x473.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_libraries.png 811w" sizes="(max-width: 246px) 100vw, 246px" />](/thinking-minecraft/wp-content/uploads/2014/08/eclipse_libraries.png)<figcaption class="wp-caption-text">Screenshot of Eclipse&#8217;s Libraries window</figcaption></figure> 

9. Click &#8216;**Add External JARs**&#8216; and add the Bukkit JAR file downloaded in Step 7.<figure id="attachment_447" style="width: 246px" class="wp-caption alignnone">

[<img class="wp-image-447" src="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_addedlibraryJAR-620x473.png" alt="Screenshot of the Bukkit JAR added." width="246" height="188" srcset="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_addedlibraryJAR-620x473.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_addedlibraryJAR.png 811w" sizes="(max-width: 246px) 100vw, 246px" />](/thinking-minecraft/wp-content/uploads/2014/08/eclipse_addedlibraryJAR.png)<figcaption class="wp-caption-text">Screenshot of the Bukkit JAR added.</figcaption></figure> 

10. Expand the selection (Click on &#8216;+&#8217;), double click on &#8216;Javadoc location&#8217; and type &#8216;http://jd.bukkit.org/dev/apidocs&#8217; into the &#8216;Javadoc location path&#8217;. Click &#8216;OK&#8217; and return to the Eclipse window.<figure id="attachment_448" style="width: 251px" class="wp-caption alignnone">

[<img class="wp-image-448" src="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_javadoc_location-620x418.png" alt="Screenshot of the Javadoc window" width="251" height="169" srcset="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_javadoc_location-620x418.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_javadoc_location.png 663w" sizes="(max-width: 251px) 100vw, 251px" />](/thinking-minecraft/wp-content/uploads/2014/08/eclipse_javadoc_location.png)<figcaption class="wp-caption-text">Screenshot of the Javadoc window</figcaption></figure> 

11. Right click on the &#8216;src&#8217; folder and click **New > Java package** Name it as you would wish. Refer [here](http://docs.oracle.com/javase/tutorial/java/package/namingpkgs.html "Oracle Java Documentation") on package naming conventions.<figure id="attachment_451" style="width: 249px" class="wp-caption alignnone">

[<img class="wp-image-451" src="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_newpackage.png" alt="Screenshot of New Package window" width="249" height="203" />](/thinking-minecraft/wp-content/uploads/2014/08/eclipse_newpackage.png)<figcaption class="wp-caption-text">Screenshot of New Package window</figcaption></figure> 

12. After clicking &#8216;Finish&#8217;, you would get the package under the &#8216;src&#8217; folder.<figure id="attachment_452" style="width: 245px" class="wp-caption alignnone">

[<img class="wp-image-452" src="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_addedpackage-620x336.png" alt="Eclipse after adding your package" width="245" height="133" srcset="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_addedpackage-620x336.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_addedpackage-940x509.png 940w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_addedpackage.png 1366w" sizes="(max-width: 245px) 100vw, 245px" />](/thinking-minecraft/wp-content/uploads/2014/08/eclipse_addedpackage.png)<figcaption class="wp-caption-text">Eclipse after adding your package</figcaption></figure> 

13. Right click the package name and select **New > Class.**Name it as you wish.<figure id="attachment_454" style="width: 241px" class="wp-caption alignnone">

[<img class="wp-image-454" src="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_newclass-620x712.png" alt="Eclipse New Class window" width="241" height="277" srcset="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_newclass-620x712.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_newclass.png 645w" sizes="(max-width: 241px) 100vw, 241px" />](/thinking-minecraft/wp-content/uploads/2014/08/eclipse_newclass.png)<figcaption class="wp-caption-text">Eclipse New Class window</figcaption></figure> 

14. At the `public class Main` line, add &#8216;`extends JavaPlugin implements Listener`&#8216;. In this example, I named my class &#8216;Main&#8217;. Change it accordingly for your setup.<figure id="attachment_456" style="width: 244px" class="wp-caption alignnone">

[<img class="wp-image-456" src="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_initialcode-620x336.png" alt="The code after adding 'extends JavaPlugin implements Listener'" width="244" height="132" srcset="/thinking-minecraft/wp-content/uploads/2014/08/eclipse_initialcode-620x336.png 620w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_initialcode-940x509.png 940w, /thinking-minecraft/wp-content/uploads/2014/08/eclipse_initialcode.png 1366w" sizes="(max-width: 244px) 100vw, 244px" />](/thinking-minecraft/wp-content/uploads/2014/08/eclipse_initialcode.png)<figcaption class="wp-caption-text">The code after adding &#8216;extends JavaPlugin implements Listener&#8217;</figcaption></figure> 

15. Eclipse will underline &#8216;JavaPlugin&#8217; and &#8216;Listener&#8217; because they are external classes that need to be imported. Eclipse is able to do auto-importing by a key combination:

`Ctrl+Shift+O` (for Windows & Linux)

`Cmd+Shift+O` (for Mac OS X)

The tutorial will continue on Part #2.

_References:_
  
_Java logo: http://mtacertification.com/images/core-java.jpg_