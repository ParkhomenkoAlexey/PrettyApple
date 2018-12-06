# PrettyApple
Working with the constraints in TableView type app. Pay attention only in auto layout and constraints.

## What I have done

![FinishedApp](https://github.com/ParkhomenkoAlexey/Images/blob/master/PrettyAppleGIF.gif)

## Constraints 

![FinishedApp](https://github.com/ParkhomenkoAlexey/Images/blob/master/PrettyApple.png)

## Code configuration
Sometimes the information your cell contains can be very large or too small. 
Therefore, the orange area should be placed under the size of the content.

This is done in code using these two lines:
``` 
// Make the row height dynamic
tableView.estimatedRowHeight = tableView.rowHeight
tableView.rowHeight = UITableViewAutomaticDimension
```

Result:

![FinishedApp](https://github.com/ParkhomenkoAlexey/Images/blob/master/PrettyApple2.png)

## Keyboard removing
At the second VC you can interact with textField that means to use the keyboard. 
The method that removes the keyboard when you press the button "return" :

```
class YourClassName: UITextFieldDelegate {
func textFieldShouldReturn(_ textField: UITextField) -> Bool {
        // dismiss the keyboard
        textField.resignFirstResponder()
        return true
    }
}
```
