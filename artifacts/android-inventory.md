---
layout: default
title: "Artifact 1: Android Inventory"
---

{% include nav.md page="/android-inventory" %}

## Artifact 1: Android Inventory

## Competency: Software Engineering and Design

### Repo Links

- Original Code: <a href="https://github.com/areif-dev/CS360-android-app/tree/original-cs360-code" target="_blank">https://github.com/areif-dev/CS360-android-app/tree/original-cs360-code</a>
- Enhanced Code: <a href="https://github.com/areif-dev/CS360-android-app/tree/enhancements" target="_blank">https://github.com/areif-dev/CS360-android-app/tree/enhancements</a>

### Description

The first artifact in my portfolio is an Android app for managing inventory. I built it as a final project for CS 360 during my Junior year of university. This app started as an introduction to SQLite and Android development in general, but it has actually served me well when taking stock of my fridge and pantry for making shopping lists and generally being aware of what I have available.

|                Add Product Screen                |             Scan Product Screen             |                     Inventory Screen                     |
| :----------------------------------------------: | :-----------------------------------------: | :------------------------------------------------------: |
| ![add_product_screen](/assets/imgs/add_item.jpg) | ![scanner_screen](/assets/imgs/scanner.jpg) | ![inventory_screen](/assets/imgs/inventory_listings.jpg) |

### Enhancements Performed

1. Remove unnecessary user accounts and login screen because all information is stored locally
2. Add Google Zebra Crossing library for reading barcodes
3. Create new Activity for opening camera and automatically scan US or EU style UPCs
4. Identify products by UPC using free, public data from [upcitemdb.com](https://upcitemdb.com)
5. Automatically update quantity on hand for a product whenever its UPC is scanned
6. Improve dark theme support by using default adaptive Android font colors
7. Document previously undocumented functions and classes

### Skills Demonstrated

1. Proficiency in Java, Gradle, and the Android SDK
2. Ability to leverage hardware of embedded devices to improve user experience
3. Proficiency in designing mobile user interfaces
4. Proficiency in SQLite and relational databases in general
5. Ability to leverage 3rd party REST APIs for data aggregation

### Justification

I included this application in my portfolio because it showcases my knowledge in technologies such as relational databases, Java, Android, emulation, and build systems such as Gradle. Additionally, the new barcode scanning activity showcases my ability to use the hardware of a device to create a better experience for users while the inclusion of a form to manually enter products demonstrates my ability to create more inclusive interfaces for devices with hardware limitations.

### Objectives

The primary objective of this artifact is to demonstrate my ability to use well-founded and innovative techniques, skills, and tools in computing practices for the purpose of implementing computer solutions that deliver value and accomplish industry-specific goals. I believe I have achieved this by engineering a product to help people easily keep track of the things around them. My inventory management application provides value because it can be used by small businesses for the purpose of taking inventory to reorder a product section or to update the inventory in a POS. It could also be used in a household to help keep a pantry stocked.

Another objective that I sought to fulfill with this artifact was to design, develop, and deliver professional-quality written communications that are coherent, technically sound, and appropriately adapted to specific audiences and contexts. This narrative outlining the enhancements I have made to the inventory management app serves that purpose. In this narrative, I have written coherently about the skills and technical knowledge I learned while developing an Android app. I have also adapted the piece for any potential employers who need to quickly understand what the inventory management application shows about my skills and knowledge as they relate to the field of software engineering.

### Reflection

The primary lesson I learned while modifying the Inventory application was how to use the Google Zebra Crossing (zxing) Android library. This is an open source project for recognizing and reading 1D and 2D barcodes. I was able to use this library to process data from a device’s camera and return any UPC-A or UPC-E codes that the camera saw.

This process also gave me a better grasp on managing dependencies in Java. Both the zxing library and dm7.barcodescanner libraries are external and had to be included in the project by modifying the app/build.gradle file. Before making these modifications, I had never worked with Gradle for managing dependencies.

Another useful technology I learned when enhancing the inventory management app was making HTTP requests with Java. I was able to search UPCs on a free to use REST API with the HttpsURLConnection class from javax.net.ssl. This API returns all sorts of useful information about products, but I currently only use it to get a brief description of the product to add to the database.
