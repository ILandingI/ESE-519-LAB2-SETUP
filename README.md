# ESE-519-LAB2-SETUP Guide
```   
 Muyuan sheng
Tested on: Legion Y9000 (i7), windows 11    
```  
## WSL Setup
Download Ubuntu Microsoft Store.After enter a username and set a password,you'll see.

<img width="725" alt="Screenshot 2022-10-14 210407" src="https://user-images.githubusercontent.com/96441697/195964891-5e7b6d30-fdbc-42bc-be53-63555dcb5e6d.png">

## Installation of the SDK on RP2040
Now we clone the SDK repositories into the directory that we created.



``` 
$ cd ~/    
$ mkdir pico  
$ cd pico  
$ git clone -b master https://github.com/raspberrypi/pico-sdk.git   
$ cd pico-sdk   
$ git submodule update --init   
$ cd ..   
$ git clone -b master https://github.com/raspberrypi/pico-examples.git   
```
  
<img width="724" alt="Screenshot 2022-10-14 223556" src="https://user-images.githubusercontent.com/96441697/195965108-ed91ba73-95bf-47a2-afb6-62346d00ddff.png">

Also follow the instructions to install toolchains for the SDK:

<img width="725" alt="Screenshot 2022-10-14 232006" src="https://user-images.githubusercontent.com/96441697/195966738-1565c622-2e3d-429d-a3cd-70af5c1cd25a.png">

## Build Examples using SDK
Now we can use the example to test the SDK
```
cd pico/pico-example
mkdir build
cd build  
cmake ..  
cd hello_world/usb  
make -j4  
``` 
After this,by searching "uf2" , we can find a ``` .uf2```  file in the directory.Connect the RP2040 in USB mode, you should press the boot button and  press reset button. Also copy it to the RP2040.  
<img width="374" alt="Screenshot 2022-10-14 234145" src="https://user-images.githubusercontent.com/96441697/195967389-2ba8803d-a769-4d6a-bdb3-0672868ea841.png"> 


## Installing Putty  
Set the putty.    

<img width="338" alt="Screenshot 2022-10-14 234540" src="https://user-images.githubusercontent.com/96441697/195967445-386e3ca1-14ab-4863-bf9e-bd08fd7bd6c0.png">

Then we can check the "Hello World!"    

![Screenshot 2022-10-14 225735](https://user-images.githubusercontent.com/96441697/195967541-ccfbc1a5-e881-4114-bebd-a2ccbfe78fbd.png)

