# EventB-Modelling-with-OpenSMT2

Setup and Experimentation Guide
System and Software Requirements
Before initiating the setup, ensure your system meets the following specifications:
1. VMware Version: 12.2.5 (this is version I used, but any version from and above can be used)
2. CPU: 4 cores
3. Memory: 8192 MB
4. Storage: 20 GB minimum

Required Tools and Software
The following tools and software are installed within the VMware environment:
1. Eclipse: An integrated development environment used for programming. For installation details, visit Eclipse Downloads (https://www.eclipse.org/downloads/).
2. Rodin Platform: A toolset for modelling and verifying systems using the Event-B formal method. Download from the Rodin Platform website (https://www.event-b.org/install.html).
3. OpenSMT2: An SMT solver for verifying properties of models expressed in SMT-LIB format. Information and download instructions can be found at OpenSMT GitHub repository (https://github.com/usi-verification-and-security/opensmt).

Setup Instructions
1. download the VMware image from here: https://mega.nz/folder/0ediGJrS#PhWWH5sCcq52CnVeMa_8yA
2. the image contains all the required tools and case study source code
   
Alternatively if the image does not work in your environment you may follow the guide below:
VMware Environment Setup:
1. Install VMware Workstation 12.2.5 on your host machine.
2. Create a new virtual machine with the specified CPU, memory, and storage settings.
Operating System and Software Installation:
1. Install your preferred Linux distribution on the virtual machine.
2. Install Eclipse, Rodin Platform, and OpenSMT2 within the virtual machine. Use the links provided above for download and installation guidance.

Accessing and Running the Rodin Platform
1. Start your virtual machine and open a terminal window.
2.  Use the cd command to navigate to the Downloads folder where the Rodin folder is located. Example: cd ~/Downloads/rodin
3.  Execute the Rodin platform by running the command: ./rodin 



Working with the Event-B Model
1. Accessing the Model:
Once the Rodin Platform is open, locate the "vuln_smart_router" folder under the "EventB explorer" section on the left-hand side.
2. Verifying the Model:
In the Rodin Platform, navigate to "Proof Obligations" and double-click on alloc_buff/inv3/INV to focus on the specific proof obligation related to the smart router model's integer vulnerability.

Proof Obligation Details:
1. Label: alloc_buff/inv3/INV
2. Goal: Ensure that size + fnum ≤ maxint to avoid buffer overflow vulnerabilities.
3. Hypotheses: buff ≤ maxint, indicating the buffer's size constraint.

Verification with OpenSMT2:
1. Selecting SMT Solver:
For the verification step, choose OpenSMT2 from the available SMT solvers. 


Running the Verification:
1. Execute the verification process to assess the proof obligation. The system should automatically use OpenSMT2 to verify the absence or presence of the specified vulnerability.

Documentation and Further Resources
For more detailed information on using the Rodin Platform and modelling with Event-B, refer to the Rodin User’s Handbook (https://wiki.event-b.org/index.php/Category:User_documentation).


