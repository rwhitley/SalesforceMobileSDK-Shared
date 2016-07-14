#Build Hybrid Sample Apps


To build hybrid apps from the <em>samples</em>
directory of the <a href="https://github.html">SalesforceMobileSDK-Shared</a>
repository, you use forcedroid or forceios and the Cordova command line. You create
a `hybrid_local` or `hybrid_remote` app and then add the web assets—HTML, JavaScript, and CSS
files—and the <em>bootconfig.json</em> file from the Shared repo. 

<hr>

### Note:


The ContactExplorer sample requires the `cordova-plugin-contacts` and `cordova-plugin-statusbar` plug-ins. The other hybrid sample apps do not require
special Cordova plug-ins.
<hr>
To build one of the sample apps: 

1.    Open a command prompt or terminal window.
2.    Clone the shared repo:
<pre><code>git clone https://github.com/forcedotcom/SalesforceMobileSDK-Shared</code></pre>
3.    Use forcedroid or forceios to create an app. For `type`, enter “hybrid_local”.
4.    Change to your new app
directory:<pre><code>cd &lt;app_target_directory&gt;</code></pre>
5.    If you’re building the ContactExplorer sample app, add the required Cordova plug-ins:
<pre><code>cordova plugin add cordova-plugin-contacts
cordova plugin add cordova-plugin-statusbar</code></pre>
6.    To add Android support to a forceios
project:<pre><code>cordova platform add android</code></pre>
7.    (Mac only) To add iOS support to a forcedroid
project:<pre><code>cordova platform add ios</code></pre>
8.    Copy the sample source files to the <em>www</em> folder of your new project
directory. On
Mac:<pre><code>cp -RL &lt;local path to SalesforceMobileSDK-Shared&gt;/samples/&lt;template&gt;/* www/</code></pre>On
Windows:<pre><code>copy &lt;local path to SalesforceMobileSDK-Shared&gt;\samples\&lt;template&gt;\*.* www</code></pre>If
you’re asked, affirm that you want to overwrite existing files.
9.    Do the final Cordova
preparation:<pre><code>cordova prepare</code></pre>
10.    To build and run, open the <em>platforms/&lt;_ios_or_android_&gt;</em>
project in the platform compiler—Android Studio or Xcode.


<hr>

### Note:





*   <a name="" id=""></a> refers to
forcedroid hybrid projects by the platform name ("android"). For example, to run your
project, select "android" as the startup project and then click Run.

*   On Windows, <a name="" id=""></a> sets the
default project encoding to `windows-1252`. This
setting conflicts with the `UTF-8` encoding of the
forcedroid Gradle build files. For best results, change the default project encoding
to
<code>UTF-8</code>.

*   <a name="" id=""></a>


<hr>
