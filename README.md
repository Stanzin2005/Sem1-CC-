
<h1><b>Making an account on AWS</b></h1>
1.Go to ["https://aws.amazon.com/resources/create-account"] and follow the instructions

<h1><b>Starting an EC2 instance</b></h1>
1. On the AWS dashboard, search for EC2 and click EC2<br><br>

2.Click Launch Instance<br>
<br>

<br><br>
3.Type your server name and choose the OS you desire (We are choosing Ubuntu for this tutorial)<br><br>

4.In the "Key Pair" section click on "Create new key pair"<br><br>

<br>
5. Name your key pair and click on .ppk and then create new key (The key pair will get downloaded)<br><br>

6. In the network section click on "Allow HTTP traffic from the internet"<br><br>
<img src="https://github.com/user-attachments/assets/568ba0ce-8acc-4621-8f46-933f36f28af5"height="350"><br><br>
7. Finally click on "Launch Instance"<br><br>
<h1><b>Installing PuTTY</b></h1>
Go to ["https://support.bondtech.se/Guide/How%20to%20install%20PuTTY%20in%20Windows/35.html"] and follow the instructions
<h1><b>Setting up PuTTY and the instance</b></h1>
1.Go on the <b>Instance</b> dashboard, you'll notice that the instance is running and below a public IP address is visible, Copy it<br><br>
If you open the IP address in your browser you'll notice nothing loads because no server is installed on your Instance as of yet. <br><br>
2.Now Open PuTTY, You'll notice a space titled "Host Name", Paste the IP address you copied<br><br>
3.On the left column, Click <b>"SSH"</b>, then click <b>"Auth"</b>, and click on <b>"Credentials"</b><br><br>
4. Click <b>"Browse"</b> and select the key pair you downloaded and click <b>"Open"</b><br><br>
5. Click accept and in the username type <b>"ubuntu"</b><br> and press <b>ENTER</b><br><br>
<h1><b>Using the command line interface</b></h1>
1. In the command line run the following linux commands in the following order
     sudo su
     apt update
It'll update the dependecies
<br><br>
2. We need to install <b>apache2</b> HTTP server, for that run the following command
    apt install apache2
It'll starting install the <b>apache2</b> server on your VM.<br><br>
3. If you go into your browser and search the IP you got earlier now you'll see this<br><br>
4. Now back on the PuTTY command line, run these commands
       /var/wwww/html/
       rm index.html
       vi index.html
5.Now you'll be in the edit window, Press <b>I</b> <br><br>
5. Now you can edit the file, for this tutorial let us simply type "hi" using HTML format<br><br>
6.Next to save the file, FIrst press <b>Ctrl+C</b> ( This will bring you out of the edit mode), then type <b>:wq</b> to exit the window<br><br>
7. Now on the browser, the "hi" is displayed<br><br>
Using this method you can connect it to your github too<br><br>
<h1><b>Closing the Running Instance</b></h1>
It is always recommended to close the running instance <br><br>
1.On the Instances dashboard, right click on the running instance and click on <b>"Terminate Running instance"</b>
<br><br>

