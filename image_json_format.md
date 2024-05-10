# Image JSON Format

## Description
The image JSON format defines the properties and style of an image element within the UI. Images are visual components used to enhance the user interface by displaying graphics, icons, or illustrations.

## JSON Structure
The image JSON object consists of the following key elements:
- `type`: Specifies the type of UI element, which is "image."
- `identifier`: A unique identifier for the image, used for referencing and styling.
- `properties`: Contains properties specific to the image, such as the visual style or appearance.

## Properties
- `style`: Indicates the visual style or appearance of the image, ensuring consistency with the app's design theme.

## Example Usage
Below is an example of the image JSON format in use:
```json
{
    "type": "image",
    "identifier": "warning_icon",
    "properties": {
        "style": "theme1.image.warning"
    }
}
