# Button JSON Format

## Description
The button JSON format defines the properties and behavior of a button element within the UI. Buttons are interactive components used for triggering actions or navigating within the app.

## JSON Structure
The button JSON object consists of the following key elements:
- `identifier`: A unique identifier for the button, used for referencing and handling its actions.
- `type`: Specifies the type of UI element, which is "button."
- `properties`: Contains properties specific to the button, such as the displayed title, style, and enabled state.
- `action`: Defines the action to be performed when the button is interacted with, such as navigation or triggering an event.

## Properties
- `title`: The text displayed on the button, indicating its purpose or action.
- `style`: Indicates the visual style or appearance of the button, ensuring consistency with the app's design theme.
- `isEnabled`: Specifies whether the button is enabled or disabled. Disabled buttons may be grayed out and non-interactive.
  
## Action
The `action` object within the button JSON defines the behavior triggered by the button interaction:
- `type`: Specifies the type of action, which can be "navigation," "api," or other custom actions.
- `apiIdentifier`: Identifies the API endpoint or service associated with the button action.
- `details`: Contains additional details specific to the action, such as URL, method, headers, and request body for API calls.
- `requiredInputValues`: Specifies any input values required for the action, such as data from other UI elements.

## Example Usage
Below is an example of the button JSON format in use:
```json
{
    "identifier": "login_button",
    "type": "button",
    "properties": {
        "title": "Log in",
        "style": "theme1.button.primary",
        "isEnabled": false
    },
    "action": {
        "type": "api",
        "apiIdentifier": "authentication",
        "details": {
            "url": "submitDataiOS",
            "method": "POST",
            "headers": {
                "contentType": "application/json"
            },
            "body": {
                "identifier": "login",
                "data": {
                    "username": "username_text_field",
                    "password": "password_text_field"
                }
            }
        },
        "requiredInputValues": [
            "username_text_field",
            "password_text_field"
        ]
    }
}
