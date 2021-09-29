# wine-32-64-env

this scripts will allow us to seperate 32-bit and 64-bit installation

<h2> USAGE </h2>

<h3> NOTE:</h3> {arch} is either 32 or 64

<hr>

<code>wine-{arch} [path of exe program]</code>
<p>exececute an exe program</p>
<p>this scipt will run an exe program with {arch}-bit environment
if the default path was not yet created, it will create a new one
default path: /home/unknown-user/.wine{arch} for user unknown-user</p>
<hr>
<code>wine-{arch} -t [winetricks program]</code>
<p>install a program included in winetricks
for example, when installing .NET 4.5, this is the same as executing:</p>

 <code>"winetricks dotnet45" </code>

<p>but the usage with this script should be:</p>

<code> "wine-{arch} -t dotnet45" </code>

<p> this is to ensure that you're executing winetricks on the correct directory (/home/unknown-user/.wine32)</p>

<h5> NOTE: you could also execute "<code>wine-{arch} -t</code>" for GUI mode </h5>
<hr>
<code> wine-{arch} -c </code>
<p>execute winecfg on correct directory (/home/unknown-user/.wine{arch})</p>
<hr>
<code> wine-64 -r </code>
<h5>NOTE: this will delete the installation path /home/unknown-user/.wine{arch}. and install a fresh installation of windows environment</h5>

<h5> NOTE: you could display this help page on terminal by executing</h5> <code>wine{arch} -h</code>

<hr>

<h2> INSTALLATION</h2>
<p> (skip 1-3 if you already do so)
<p> 1.) make sure that you added the x86 architecture by executing:

2.) <code>sudo dpkg --add-architecture i386</code>
then update your packages by executing <code> sudo apt update</code>

<p> 3.) install wine and winetricks</p>

<code> sudo apt install wine wine32 wine64 wine-stable winetricks</code>

4.) Download the repo in zip <a href="https://codeload.github.com/magbulogtong81/wine-32-64-env/zip/refs/heads/main">here</a> or fire up terminal and execute <code> git clone https://https://github.com/magbulogtong81/wine-32-64-env</code>

5.)<code>cd wine-32-64-env</code>

<p>6.)make the scripts executable</p>
<code> chmod +x wine-32 wine-64</code>

<p>7.) move the script file to be able to execute it system-wide
  <code>sudo mv wine-32 wine-64 /usr/local/bin</code>
  <p>8.) execute <code>wine-32</code>to get a 32-bit installation or   <code>wine-64</code> for 64-bit</p>
