# 一、Configure the working environment
## 1、Download Source
<pre><code>$  sudo apt­-get install build-­essential 
$  sudo apt­-get install libgl1­-mesa­-dev 
$  sudo apt­-get install libglu1­-mesa­-dev
$  sudo apt­-get install freeglut3­-dev</code></pre>
## 2、Install the package "glib2.0"
<pre><code>$  sudo apt-get install libglib2.0-dev
</code></pre>
## 3、Cmake to generate make file
<pre><code>$  cd Velodyne_viewer
$  mkdir test
$  cd test
$  cmake -DCMAKE_INSTALL_PREFIX=`pwd`/../ ..
$  make
$  make install</code></pre>
### While I CMake the file "CMakeLists.txt" a problem  
*"cmake aborts with an error message stating it cannot find GLUT Xi   
LIBRARY and GLUT Xmu LIBRARY"*  
### We could solve with  
<pre><code>$  sudo apt-get install libxmu-dev libxi-dev</code></pre>
## 3、Carry out simulation work
### run the project, located at ./Velodyne_viewer/build/bin
<pre><code>$  cd Velodyne_viewer/build/bin
$  sudo chmod u+x run.sh
$  ./run.sh</code></pre>
### When running ./run.sh，a problem with "Pemission denied"  
### we could solve with
![](http://a1.qpic.cn/psb?/V10xhQuy3m7suY/Q.RGPa5MVLn1CGtb9A7MW4OT9aQ*0I4rxicrKvvxZQ8!/b/dGgBAAAAAAAA&bo=0QHTAQAAAAADByA!&rf=viewer_4)
# 二、Do the simulation
## 1、run the project in /Velodyne_viewer/bin
<pre><code>$  cd ..
$  cd bin
$  sudo chmod u+x run.sh
$  ./run.sh</code></pre>  
## 2、Go to the folder “pcap” and run the python script with the result  
![](http://a1.qpic.cn/psb?/V10xhQuy3m7suY/nxfjGEzwU*K9*3EJhvcHxUMQZKk12CEzFMzNFDsgd0Q!/b/dFYBAAAAAAAA&bo=4gFWAQAAAAADB5Y!&rf=viewer_4)  
## 3、Implement the recvPacket() function in velodyneDriver.cpp  
### Mapping Cartesian and Polar Coordinates
![](http://a2.qpic.cn/psb?/V10xhQuy3m7suY/.XxfhppKbtoSkAVa2IvSRRJFJg4M*WnNPBh2ziQXHCA!/b/dGkBAAAAAAAA&ek=1&kp=1&pt=0&bo=iAM3AgAAAAARF54!&tm=1492156800&sce=60-1-1&rf=viewer_4)  
### Restart the cmake operation  
<pre><code>$  cd Velodyne_viewer
$  mkdir test
$  cd test
$  cmake -DCMAKE_INSTALL_PREFIX=`pwd`/../ ..
$  make
$  make install</code></pre>
### repeat “Go to the folder “pcap” and run the python script with the result” and Get the result graph  
![](http://a2.qpic.cn/psb?/V10xhQuy3m7suY/6H*fg1g3jpxCSN5653yFKLA6uKIqzyJrUW4TS*bKvkI!/b/dGkBAAAAAAAA&ek=1&kp=1&pt=0&bo=IANzAgAAAAADF2A!&tm=1492156800&sce=60-1-1&rf=viewer_4)
  
