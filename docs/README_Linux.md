This repo holds a stock vagrant implementation for use in devlopment.

In the rollup, I have:

**CentOS Linux 6.5**<br>
Puppet Master with **Puppet Enterprise 2015.3**<br>
Puppet Agents 1-3, all customized to the following three environments:<br>
- development<br>
- testing<br>
- production<br>

**REQUIRED:**

You must have Vagrant Installed for your platform:
	
	https://vagrantup.com

Also, this is designed to run over Virtualbox.  Virtualbox can be obtained from the official site here:
	
	https://www.virtualbox.org/

To use this module with your current Vagrant and Virtualbox Installation, you have to install two vagrant plugins:

	- vagrant-hosts<br>
	- vagrant-pe_build<br>

To install the required plugins, on your local system simply run:

	vagrant plugin install vagrant-hosts<br>
	vagrant plugin install vagrant-pe_build<br>

to prepare Vagrant to use the included Vagrantfile.

**NOTES:**

With the default installaiton of PE 2015.3 r10k now comes installed by default along with the new Code Sync and Code Manager features which utilize r10k and MCollective under the covers. 

Linux testing is now complete.  After a professional services engagement recently, I had a 
number of students need to use the instance who were all Linux users, and they were able to
"fire test" for me.  Issues, if any, should be opened on the project in the GitHub page.


	TODO:
	- VMWare Fusion Support
		If anyone nows how to get the Vagrantfile to determine
    	the right virtualization technology and just "do the 
    	right thing" all in one Vagrantfile, that's the  "silver bullet"
    	I'm looking for.
    	
	- Sometimes the vagrant package will not download the Puppet 
		Enterprise properly depending on platform.  Needs resolution.

---

**CREDITS:**

I initially discovered the impetus for this project by being pointed to it by a Puppet Labs Employee, Tom Linkin.  He showed me a package he had entitled vagrant-pelab that did something similar to what I'm doing here.  As near as I can determine, that project is hosted here:

	https://bitbucket.org/picklesau/pelab-vagrant
	
In addition, FInch from Puppet Labs has also been immensely helpful in that he has created the Vagrant Plugins that makes pelab-vagrant work.  They are:

	[vagrant-pe_build](https://github.com/oscar-stack/vagrant-pe_build) - Builds Puppet Enterprise
	[vagrant-hosts](https://github.com/oscar-stack/vagrant-hosts)    - Incorproates "sensible" DNS into the VMs
	

	  
	
