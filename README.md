# Material Chip View

Material Chip view. Can be used as tags for categories, contacts or creating text clouds.

[![Android Arsenal](https://github.com/robertlevonyan/materialChipView/blob/master/Images/aa.png)](https://android-arsenal.com/details/1/5396)

## Setup

#### Gradle:

Add following line of code to your module(app) level gradle file

```java
    compile 'com.robertlevonyan.view:MaterialChipView:1.0.1'
```

#### Maven:

```xml
  <dependency>
    <groupId>com.robertlevonyan.view</groupId>
    <artifactId>MaterialChipView</artifactId>
    <version>1.0.1</version>
    <type>pom</type>
  </dependency>
```

## Usage

```xml
  <com.robertlevonyan.views.chip.Chip
    android:id="@+id/chip"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    app:mcv_chipText="@string/customTitle" />
```
![alt text](https://github.com/robertlevonyan/materialChipView/blob/master/Images/sample.png)

### Cutomizing Chip

```xml
    app:mcv_closable="true"
```
![alt text](https://github.com/robertlevonyan/materialChipView/blob/master/Images/closable.png)

```xml
    app:mcv_selectable="true"
```
![alt text](https://github.com/robertlevonyan/materialChipView/blob/master/Images/selectable.png)

```xml
    app:mcv_hasIcon="true"
    app:mcv_chipIcon="@drawable/customIcon"
```
![alt text](https://github.com/robertlevonyan/materialChipView/blob/master/Images/hasIcon.png)

```xml
    app:mcv_hasIcon="true"
    app:mcv_chipIcon="@drawable/customIcon"
    app:mcv_closable="true"
```
![alt text](https://github.com/robertlevonyan/materialChipView/blob/master/Images/hasIconClosable.png)

```xml
    app:mcv_backgroundColor="@color/customChipBackgroundColor"
    app:mcv_closeColor="@color/customCloseIconColor"
    app:mcv_selectedBackgroundColor="@color/customSelectedChipColor"
    app:mcv_textColor="@color/customTitleColor"
```

|![alt text](https://github.com/robertlevonyan/materialChipView/blob/master/Images/custom1.png)|![alt text](https://github.com/robertlevonyan/materialChipView/blob/master/Images/custom2.png)|
|----------------------------------------------------------------------------------------------|-----------|

### Attributes

|Custom Atributes             |Description                                 |
|-----------------------------|--------------------------------------------|
|`app:mcv_chipText`               |Text label of Chip                          |
|`app:mcv_textColor`              |Custom color for text label                 |
|`app:mcv_backgroundColor`        |Custom background color                     |
|`app:mcv_selectedBackgroundColor`|Custom background color when selected       |
|`app:mcv_hasIcon`                |Chip with icon                              |
|`app:mcv_chipIcon`               |Icon resource for Chip                      |
|`app:mcv_closable`               |Chip with close button                      |
|`app:mcv_closeColor`             |Custom color for close button               |
|`app:mcv_selectable`             |Chip with selection button                  |
|`app:mcv_selectedTextColor`      |Custom color for label when selected        |
|`app:mcv_selectedCloseColor`     |Custom color for close button when selected |

### Setting Listeners

```java
    Chip chip = (Chip) findViewById(R.id.chip);
```
Chip click listener
```java
    chip.setOnChipClickListener(new OnChipClickListener() {
            @Override
            public void onChipClick(View v) {
                //Your action here...
            }
        });

```

On Close button click listener
```java
        chip.setOnCloseClickListener(new OnCloseClickListener() {
            @Override
            public void onCloseClick(View v) {
                //Your action here...
            }
        });

```

On Icon click listener
```java
        chip.setOnIconClickListener(new OnIconClickListener() {
            @Override
            public void onIconClick(View v) {
                //Your action here...
            }
        });

```

On Select button click listener
```java
        chip.setOnSelectClickListener(new OnSelectClickListener() {
            @Override
            public void onSelectClick(View v, boolean selected) {
                //Your action here...
            }
        });
```
### Customizing Chip from Java

```java
        chip.setChipText(); // Set Chip label
        chip.setTextColor(); // Set Chip label color
        chip.changeBackgroundColor(); //Set custom background color
        chip.changeSelectedBackgroundColor(); //Set custom background color when selected
        chip.setHasIcon(); //Set chip has icon
        chip.setChipIcon(); //Set Icon Drawable for Chip
        chip.setClosable(); //Set Chip has close button
        chip.setCloseColor(); //Set custom color for close button
        chip.setSelectable(); //Set Chip has selection button
        chip.setClicked(); // Set Chip as clicked
        chip.setSelectedTextColor(); //Set custom color for label when selected
        chip.setSelectedCloseColor(); //Set custom color for close button when selected
```

## Versions

#### 1.0.1

Recreation issues are fixed

### 1.0.0

First version of library

## Licence

```
    Material Chip View©
    Copyright 2017 Robert Levonyan
    Url: https://github.com/robertlevonyan/materialChipView

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
```
