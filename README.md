# LightBulb
LightBulb is an open source python framework for auditing web applications firewalls.

## Synopsis

The framework consists of two main algorithms:

* **GOFA**: An active learning algorithm that infers symbolic representations of automata in the standard membership/equivalence query model.
 
    Active learning algorithms permits the analysis of filter and sanitizer programs remotely, i.e. given only the ability to query the targeted program and observe the output.

* **SFADiff**: A black-box differential testing algorithm based on Symbolic Finite Automata (SFA) learning

    Finding differences between programs with similar functionality is an important security problem as such differences can be used for fingerprinting or creating evasion attacks against security software like Web Application Firewalls (WAFs) which are designed to detect malicious inputs to web applications.

## Motivation

Web Applications Firewalls (WAFs) are fundamental building blocks of modern application security. For example, the PCI standard for organizations handling credit card transactions dictates that any application facing the internet should be either protected by a WAF or successfully pass a code review process. Nevertheless, despite their popularity and importance, auditing web application firewalls remains a challenging and complex task. Finding attacks that bypass the firewall usually requires expert domain knowledge for a specific vulnerability class. Thus, penetration testers not armed with this knowledge are left with publicly available lists of attack strings, like the XSS Cheat Sheet, which are usually insufficient for thoroughly evaluating the security of a WAF product.


## Commands Usage

Main interface commands:
 
 Command       | Description                           
 ------------- | ------------------------------------- 
 core          | Shows available core modules 
 utils         | Shows available query handlers 
 info  \<module\>  | Prints module information             
 library       | Enters library                       
 modules       | Shows available application modules  
 use \<module\>    | Enters module  
 start \<moduleA\> \<moduleB\>    | Initiate algorithm
 help          | Prints help                           
 complete      | Prints bash completion command        

Module commands:
 
 Command       | Description                           
 ------------- | ------------------------------------- 
 back          | Go back to main menu         
 info          | Prints  current module information             
 library       | Enters library                       
 options       | Shows available options
 define \<option\>  \<value\>   | Set an option value
 start         | Initiate algoritm   
 complete      | Prints bash completion command    

Library commands:

 Command       | Description                           
 ------------- | ------------------------------------- 
 back          | Go back to main menu     
 info \<folder\\module\>  | Prints requested module information (folder must be located in lightbulb/data/)
 cat \<folder\\module\>  | Prints requested module  (folder must be located in lightbulb/data/)
 modules  \<folder\>     | Shows available library modules in the requested folder (folder must be located in lightbulb/data/)
 search  \<keywords\>    | Searches available library modules using comma separated keywords
 complete      | Prints bash completion command    

## Installation

In order to use the application without complete package installation:

```bash
make
pip install -r requirements.txt
```

In order to perform complete package installation You can also install it from pip repository:

```bash
pip install lightbulb-framework
lightbulb
```


## Contributors

* George Argyros
* Ioannis Stais

## License

A short snippet describing the license (MIT, Apache, etc.)