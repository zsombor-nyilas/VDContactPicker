<p align="center" >
<img src="Logo.jpg" alt="VDContactPicker" title="VDContactPicker" width="196">
</p>

# VDContactPicker
A contacts picker component using Apple's Contacts framework.

[![Platform](https://img.shields.io/cocoapods/p/VDContactPicker.svg?style=flat)](http://cocoapods.org/pods/VDContactPicker)
[![Swift 3](https://img.shields.io/badge/Swift-3.0-orange.svg?style=flat)](https://developer.apple.com/swift/)
[![CocoaPods Compatible](https://img.shields.io/cocoapods/v/VDContactPicker.svg?style=flat)](http://cocoadocs.org/docsets/VDContactPicker)
[![CI Status](https://travis-ci.org/vdeep/VDContactPicker.svg?branch=master)](https://travis-ci.org/vdeep/VDContactPicker)
[![License](https://img.shields.io/cocoapods/l/Ouroboros.svg?style=flat)](https://github.com/vdeep/VDContactPicker/blob/master/LICENSE)
[![Twitter: @VishalDeep](https://img.shields.io/badge/contact-@vishal_deep-blue.svg?style=flat)](https://twitter.com/vishal_deep)

This library was originally forked from [JFContactsPicker](https://github.com/jettf/JFContactsPicker)

## Preview
![Single Selection](https://raw.githubusercontent.com/vdeep/VDContactPicker/master/Screenshots/Screen1.png)![Multi Selection](https://raw.githubusercontent.com/vdeep/VDContactPicker/master/Screenshots/Screen2.png)

## Installation

### CocoaPods
VDContactPicker is available on CocoaPods. Just add the following to your project Podfile:

`pod 'VDContactPicker', '~> 1.0'`

### Manual Installation

Just drag and drop the `Source` folder into your project

## Requirements

* iOS9+
* Swift 4.1
* ARC

For manual installation you may need to add these frameworks in your Build Phases:
`ContactsUI.framework` and `Contacts.framework`.

## Features

VDContactPicker provides all common functionality and customization features:

[x] Single selection and multi-selection options.
[x] Search Contacts
[x] Configure the contact data to be shown. (Phone Number, Email, Birthday, or Organization)
[x] Section indexes to easily navigate through the contacts.
[x] Shows initials when image is not available.
[x] Contact object to get the properties of the contacts

If you would like additional support for additional customization features, please [Create a New Issue](https://github.com/vdeep/VDContactPicker/issues/new). 

## Initialization

Initialize the picker by passing the delegate, multiselection option, and the secondary data type to be displayed (Phone Number, Email, Birthday, or Organization). 

```swift
let contactPicker = VDContactPicker(delegate: self, multiSelection:false, subtitleCellType: .email)
let navigationController = UINavigationController(rootViewController: contactPicker)
self.present(navigationController, animated: true, completion: nil)
```
## Delegates

VDContactPicker provides you four delegate methods for responding to the picker's events.

```swift
func contactPicker(_ contactPicker: VDContactsPicker, didContactFetchFailed error : NSError)
func contactPicker(_ contactPicker: VDContactsPicker, didCancel error : NSError)
func contactPicker(_ contactPicker: VDContactsPicker, didSelectContact contact : VDContact)
func contactPicker(_ contactPicker: VDContactsPicker, didSelectMultipleContacts contacts : [VDContact])
```

## Contact Object

The `VDContact` object provides you the properties of a contact. This contains properties like displayName, initials, firstName, lastName, company, birthday, etc.

## License

VDContactPicker is available under the MIT license. See the [LICENSE](https://github.com/vdeep/VDContactPicker/blob/master/LICENSE) file for more info.

## Contributors

[@vdeep](https://github.com/vdeep)

*Original Authors*
[@JettF](https://github.com/JettF)  
[@AnthonyMDev](https://github.com/AnthonyMDev)  
[@ipraba](https://github.com/ipraba)  
[@Sorix](https://github.com/Sorix)

