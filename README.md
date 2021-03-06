# DPTimePicker

![alt tag](https://github.com/dariopellegrini/DPTimePicker/blob/master/DPTimePicker1.gif)
![alt tag](https://github.com/dariopellegrini/DPTimePicker/blob/master/DPTimePicker1.png)

Custom fullscreen time picker with scrollviews and animations written in Swift.

## Example

To run the example project, clone or download the repo and run DPTimePicker.xcodeproj. Time picker's classes are in DPTimePicker subfolder.

## Requirements
iOS 9.0+

## Installation

Simply drag DPTimePicker subfolder into your project (to do: port on Cocoapods).

## Usage

Use this code to add the time picker to your view controller:

```swift
let timePicker: DPTimePicker = DPTimePicker.timePicker()
timePicker.insertInView(view)

/*
Customization goes here
*/

timePicker.show(nil)
```
For further details check the example project

## Customization

Customization must be made before calling ``show`` method.
Here are possible customizations:

```swift
/*
Close and Confirm buttons customizations
*/
timePicker.closeButton.titleLabel?.textColor = UIColor.black
timePicker.closeButton.setTitle("X", for: .normal)
timePicker.okButton.titleLabel?.textColor = UIColor.red
timePicker.okButton.setTitle("OK", for: .normal)

timePicker.backgroundColor = UIColor.red // background color
timePicker.numbersColor = UIColor.blue // time picker's numbers color
timePicker.linesColor = UIColor.brown // central lines color
timePicker.pointsColor = UIColor.cyan // central points color
timePicker.topGradientColor = UIColor.blue // bottom gradient view color
timePicker.bottomGradientColor = UIColor.green // top gradient view color
timePicker.fadeAnimation = true // is fade animation enabled (default true)
timePicker.springAnimations = true // are spring animations enabled (default true)
timePicker.fadeAnimation = true // is initial scroll animation enabled
timePicker.areLinesHidden = false // are central lines hidden (default false)
timePicker.arePointsHidden = false // are centra points hidden (default false)
timePicker.initialHour = "15" // set initial hour (default "00")
timePicker.initialMinute = "12" // set initial minute (default "00")
```

## Delegate
It's possible to catch close and confirm action of the time picker using its delegate.
```swift

timePicker.delegate = self

func timePickerDidConfirm(_ hour: String, minute: String, timePicker: DPTimePicker) {
    print("Confirm")
}

func timePickerDidClose(_ timePicker: DPTimePicker) {
    print("Cancel")
}

```

## Author

Dario Pellegrini, pellegrini.dario.1303@gmail.com

## Credits

Gradient view are built with: [EZGradientView](https://github.com/shashankpali/EZYGradientView)
