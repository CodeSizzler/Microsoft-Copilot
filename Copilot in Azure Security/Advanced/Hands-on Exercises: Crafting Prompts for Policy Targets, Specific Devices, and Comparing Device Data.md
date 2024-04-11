# Hands-on Exercises: Crafting Prompts for Policy Targets, Specific Devices, and Comparing Device Data
In this document, you will learn how to craft prompts for different policy targets, such as users, groups, or devices. You will also learn how to specify devices by their attributes, such as model, OS, or location. Finally, you will learn how to compare device data using operators, such as equal, greater than, or contains.
## Exercise 1: Crafting Prompts for Policy Targets
A policy target is the entity that you want to apply a policy to. You can target users, groups, or devices. To craft a prompt for a policy target, you need to use the following syntax:
`target [entity type] [entity name]`
For example, if you want to target a user named Alice, you can write:
`target user Alice`
If you want to target a group named Marketing, you can write:
`target group Marketing`
If you want to target a device named Laptop-01, you can write:
`target device Laptop-01`
### Task
Write a prompt for each of the following policy targets:
- A user named Bob
- A group named Sales
- A device named Tablet-02
### Solution
- `target user Bob`
- `target group Sales`
- `target device Tablet-02`
## Exercise 2: Specifying Devices by Attributes
Sometimes, you may want to target devices by their attributes, such as model, OS, or location. To do this, you need to use the following syntax:
`target device [attribute name] [operator] [attribute value]`
For example, if you want to target devices that have the model iPhone 12, you can write:
`target device model = iPhone 12`
If you want to target devices that have the OS Android 11, you can write:
`target device OS = Android 11`
If you want to target devices that are located in New York, you can write:
`target device location = New York`
### Task
Write a prompt for each of the following device attributes:
- Devices that have the model Samsung Galaxy S21
- Devices that have the OS Windows 10
- Devices that are located in London
### Solution
- `target device model = Samsung Galaxy S21`
- `target device OS = Windows 10`
- `target device location = London`
## Exercise 3: Comparing Device Data
Sometimes, you may want to compare device data using operators, such as equal, greater than, or contains. To do this, you need to use the following syntax:
`target device [data name] [operator] [data value]`
For example, if you want to target devices that have the battery level less than 20%, you can write:
`target device battery < 20`
If you want to target devices that have the screen size greater than 6 inches, you can write:
`target device screen > 6`
If you want to target devices that have the app name containing Facebook, you can write:
`target device app contains Facebook`
### Task
Write a prompt for each of the following device data comparisons:
- Devices that have the storage space less than 10 GB
- Devices that have the camera resolution greater than 12 MP
- Devices that have the wifi name containing Starbucks
### Solution
- `target device storage < 10`
- `target device camera > 12`
- `target device wifi contains Starbucks`

