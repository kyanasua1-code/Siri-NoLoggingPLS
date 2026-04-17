Configuration profile disabling server-side logging of Siri requests for your Mac, iPhone and iPad

## Installation steps:
1) Open the `Prevent server-side logging of Siri commands.mobileconfig` file from this repository and switch to the Raw view to download the profile ([direct link](https://github.com/jankais3r/Siri-NoLoggingPLS/raw/master/Prevent%20server-side%20logging%20of%20Siri%20commands.mobileconfig))
2) Finish the profile installation in Settings
![Profile installation](https://github.com/jankais3r/Siri-NoLoggingPLS/raw/master/installation.png)
3) There is no step 3. Your Siri requests are no longer logged.
4) If you feel like there should be an easier way to achieve this, let Apple know using their [Feedback form](https://www.apple.com/feedback/).

### Alternatively, you can create your own profile using Apple's Configurator
![Profile creation](https://github.com/jankais3r/Siri-NoLoggingPLS/raw/master/{
  "title": "Siri System Settings (com.apple.systempreferences)",
  "description": "Use this section to disable the Siri & Apple Intelligence panel in System Settings.",
    "links": [
    {
      "rel": "Siri-Specific Source",
      "href": "https://gist.github.com/jonesiscoding/270dffd9676b212ae741b9571afc9751"
    },
    {
      "rel": "Original Source",
      "href": "https://github.com/Jamf-Custom-Profile-Schemas/ProfileManifestsMirror/blob/main/manifests/ManifestsApple/com.apple.systempreferences.json"
    }
  ],
  "properties": {
    "DisabledSystemSettings": {
      "type": "array",
      "items": {
        "type": "string",
        "enum": [
          "com.apple.Siri-Settings.extension"
        ],
        "options": {
          "enum_titles": [
            "Siri"
          ]
        }
      },
      "description": "The list of disabled System Settings extensions. All other items will be enabled. When DisabledSystemSettings is specified. Note that a given System Settings extension may supply more than one section in System Settings; disabling such an extension will disable all sections it supplies.",
      "property_order": 5
    }
  }
}
