***Puppet Development Environment***

This project contains a Puppet Enterprise Testing
Environment to be used in testing code for Puppet.

It contains a Puppet Master with 3 Agent nodes, each
existing in their own environment, whether "development", "testing", or "production".

R10k is rudimentally installed and configured with a very basic control repo.  This control repo is generic and contains no reference to any custom modules, you will need to supply these for yourself.

Recommendation: Clone this repo and the destination control repo to your own Git repository, and modify the included Puppetfile to suit your own needs.

Read the docs/README_{platform}.md file that is appropriate to your platform for details regarding your OS.