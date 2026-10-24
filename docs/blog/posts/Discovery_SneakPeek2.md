--- 
date: 2026-10-24
categories: 
  - General 
  - Discovery 
--- 
 
 
# What's Next for "Discovery": Improved answer file features 
 
Unattended. For the better. For the rest of us. 
 
<!-- more --> 
 
One of the best ways to customize the behavior of a Windows image is through the use of unattended answer files. These allow you to automate user account creation, set computer names, run scripts, and so much more. For DISMTools 0.9 "Discovery", some improvements are planned that will help you do more.

## User Accounts

In the current implementation of user account creation, you can create up to 5 user accounts. While most people will either create 1 or 2 users or have them in a domain, someone may wish to create more than 5 local users.

As such, the *Discovery* implementation will allow you to specify unlimited user accounts. Here is how user accounts are planned to be presented in *Discovery*:

<p align="center">
    <img src="https://codingwonders.github.io/pictures/DiscoveryUserPanel.svg">
</p>

As shown in the aforementioned mockup, you begin with 1 user account, and you add up from there. You can delete any slot by clicking the Delete button of the desired account slot.

*Discovery* is planned to improve reusability of items. In the new implementation, you will be able to export user account slots, as well as autologon settings, to a XML file. Then, you can either reuse them in another answer file, or share them to someone else to begin with that set of accounts.

## Domain Join

Integration with Active Directory Domain Services started with DISMTools 0.7 and, over the course of over a year, has been improved. *Discovery* is set to bring the next set of improvements to domain join features.

*Discovery* aims to bring compatibility with server environments in which a forest contains multiple domains. The Lightweight Directory Access Protocol (LDAP) lets us query information about the [Configuration Directory Partition](https://ldapwiki.com/wiki/Wiki.jsp?page=Configuration%20Directory%20Partition) (a naming context) of a domain from which we can grab information such as LDAP paths, domain controller NetBIOS names, and more; effectively allowing us to create a domain tree, from top-level root domains to available child domains. When picking any domain, it will try to pull users and organizational units, and map those accordingly, like it has done since the 0.7 Series.

This eliminates the need to rely on the Active Directory object picker and offers a more cohesive experience to the system administrator.

## Starter Scripts

Some improvements are planned for Starter Scripts in *Discovery* as well. A new *Author* field will allow you to put your name on the script. The Starter Script Editor will also see snippet support so you can write complex blocks with far less keystrokes, as well as a snippet editor.

## Discovery is now closer

The stable release of DISMTools 0.8.2 comes out in a week. After that comes the time to **discover what's next**. Stay tuned for more Sneak Peeks, as there are more things I would like to show!