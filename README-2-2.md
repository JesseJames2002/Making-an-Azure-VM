<p align="center">Creating a VM
  </a>
</p>
<br>
Using: Microsoft Azure
and remote desktop

# 🚀 Getting Started

Navigate to the Azure Portal and sign in (create an account and start a subscription if needed).

Click the menu button (**&#8801;**) in the top left to reveal the side panel. Then, click ```Create a resource```.


Under the **Virtual machine** section, click ```Create```.


# ⚙️ Settings Configuration
> [!NOTE]
> The configuration options below should be adjusted accordingly based on use case. For example, for a Windows 10 Pro VM that shuts down automatically and runs osTicket, the following settings would be used.

### Basics Tab
> **Subscription**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select the subscription to be used by the VM.

> **Resource Group**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Click ```Create new``` and enter ```osTicket-RG```, then click ```OK```.

> **Virtual machine name**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enter ```osTicket-VM```.

> **Region**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Enter preferred region to host the VM.

> **Availability options**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select ```No infrastructure redundancy required```.

> **Security type**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select ```Standard```.

> **Image**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Search for and select ```Windows 10 Pro, version 22H2 - x64```.

> **VM Architecture**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select ```x64```.

> **Size**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select ```Standard_B2ms - 2 vcpus, 8 GiB memory```.

> **Username & Password**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Set up a secure username and password.

> **Licensing**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tick the &#9989;```I confirm I have an eligible Windows 10/11 license with multi-tenant hosting rights``` checkbox.


### Networking Tab
> **Select inbound ports**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Select ```RDP (3389)```, ```HTTP (80)```, and ```HTTPS (443)```.


### Management Tab
> **Auto-shutdown**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Tick the &#9989;```Enable auto-shutdown``` checkbox and configure the settings as desired.


<br> Click the ```Review + Create``` button at the bottom of the page. Verify that validation has passed. Lastly, click ```Create```.

# 🖥️ Accessing the Virtual Machine Remotely
On the Azure Portal homepage, navigate to the **Azure services** section and click ```Virtual machines```. Click on the virtual machine name in question. Then, click the &#9654;```Start``` button on the toolbar.

On Windows:

Press ```Win+R```, type in ```mstsc``` and  then click ```OK``` to open the Remote Desktop Connection window.


In the **Computer:** field, enter the public IPv4 address of the virtual machine.


Enter the username and password that was set up earlier during the creation of the Azure virtual machine.


If there is an error validating the remote computer's certificate, this can be dismisssed by pressing ```Yes```.


Connect to the virtual machine and wait for the login process to complete.


On Mac, download [Microsoft Remote Desktop](https://apps.apple.com/us/app/microsoft-remote-desktop/id1295203466?mt=12) to connect to the virtual machine.

On Linux, use Remmina or a similar client in substitution of Microsoft Remote Desktop.

# ❌ Deleting the Virtual Machine
Under the **Virtual machines** section of Azure, tick the checkbox next to the virtual machine you want to delete. Then, click the &#128465;```Delete``` button in the toolbar on the top right off the webpage.


A side panel will open up on the right of the webpage. You must tick the &#9989;```Apply force delete for selected virtual machines and Virtual machine scale sets``` checkbox. Then, type ```delete``` into the text field. Lastly, click the red ```Delete``` button.
