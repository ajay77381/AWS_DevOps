What is A Active directory ?

Active directory is a data base of your user , group ,services, resource and all these all are know as object in Active directory and collection of object know as Active directory.
Active directory domain services provide centralize authentication service for microsoft network. 

## What is A Active directory benefits ?

- Hierarchical organization structure

  ![image](https://github.com/user-attachments/assets/d1e71ed5-cfb3-4289-a7b3-ff71d4fad1a2)

- Multi master authentication & multimaster replication (The ability to access and modify ADDS from multiple point of administation )
- A single point of access to network resources
- Ability to create trust relationship with external network runing various version of Active directory even unix.

- Note- Forest is the bigest container in Active directory in which we can keep other container

## There are 06 types of Trust in Active Directory –

- Parent-child Trust.
- Tree-Root Trust.
- Forest Trust.
- Shortcut Trust.
- Realm Trust.
- External Trust.

## Parent-child Trust

Parent-child trust is implicitly established. It is a two-way transitive trust. Parent-child trust is automatically generated when a child domain is added to a parent domain. When a new child domain is added, the trust path flows upward through the domain hierarchy.


## Tree-Root Trust

Tree-root trust is also a two-way transitive trust similar to parent-child trust. When a new domain tree is created within a forest, a tree-root trust is automatically created between the new domain tree and all exiting tree domains.


## Forest Trust

Forest trust are transitive trust, and they can either one-way or two-way trust. It is explicitly transitive (between two forest) created trust between two forest root domains. Forest trust are manually created, one-way transitive or two-way transitive trust that allows you to provide access to the resource between multiple forest. It required DNS resolution to be established between forests.

Forest trust cannot be extended to other forests, for example, if Forest1.com trusts Forest2.com, and another forest Forest3.com trust is created between Forest2.com and Forest3.com, Forest1.com does not have an implied trust. If a trust is required, one must be manually created.


## Shortcut Trust

Shortcut trust are manually created one-way, transitive trusts. They can only exist within a forest. They are created to optimize the authentication process shortening the trust path. These trusts are created when one domain needs to trust another domain by bypassing the hierarchy of trusts such as parent-child trust and Tree-root trusts.


## External Trust

An External trust is a one-way non-transitive trust. These trusts are manually established. An external trust is established with an external domain outside the forest of the trusting domain.


## Realm Trust

These kinds of trust between a domain or a forest with another domain and a forest that is not based on Windows Active Directory. A Realm Trust can be established to provide resource access and cross-platform inter-operability between an AD DS Domain and non-windows Kerberos v5 Realm.


## Active Directory componenet -

As we know active directory is a collection of user, gourp , services and resources and all know as object and active directory is installed in our network on a server and this server called a active directory domain controlled.

