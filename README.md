# PickerTextField

UITextField with ability to pick dates as well as to provide drop-down selection

# Installation

Simply include PickerTextField.swift inside your project and use it:

1. Go to your storyboard and change class of your UITextField to PickerTextField
2. Connect your IBOutlet
3. Go to your code:

```
@IBOutlet weak var textField: PickerTextField!
```
Inside your viewDidLoad method for example, you can configure it:

```
textField.pickerDelegate = self
textField.mode = Mode.date
```

or

```
textField.pickerDelegate = self
textField.mode = Mode.picker
textField.options = ["First", "Second", "Third"]
```

In picker mode, we have delegate method:

```
func pickerTextField(_ textField: PickerTextField, didSelectOption option: String)
```

Which will give us a feedback when user did actually select something.
