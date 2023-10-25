# XcodeTemplates
## Useful paths

- `/Applications/Xcode.app/Contents/Developer/Platforms/iPhoneOS.platform/Developer/Library/Xcode/Templates/Project Templates/iOS/Application` - Xcode templates **(#1)**
- `~/Library/Developer/Xcode/Templates/` – custom user templates **(#2)**

## Main steps to create a custom template
1. Create a folder with the template's name in the **(#2)** folder. For example, *UIKit App.xctemplate*
1. Copy there the most similar *TemplateInfo.plist* file from **(#1)** or create a new one
1. Fill *TemplateInfo.plist* file parameters
1. (Optional) Add template project files if needed. For example, some *.swift* files

### TemplateInfo.plist parameters
- **SortOrder** – the order in the Xcode custom section with user templates
- **Description** – text description, possibly not used
- **Concrete** – **YES**, if we want to see a template in Xcode. **NO** if we're going to use a template just as an Ancestor for other templates
- **Kind** – for project templates we should use the **Xcode.Xcode3.ProjectTemplateUnitKind** value
- **Identifier** – a unique identifier
- **NameOfInitialFileForEditor** – a name of a file that will be opened after a project creating
- **Ancestors** – existing templates we want to inherit properties from
- **Image** – an icon in the Xcode custom section with user templates. It is OK to copy from an existing template
- **Nodes** – an array of items to create in a project
- **Definitions** – a dictionary with keys from **Nodes** elements. A value for every key is a dictionary with file parameters like *Path* and *SortOrder*. Without it, the file will be created empty
- **Options** – UI template parameters if needed. For example, if we should include Unit tests
- **Targets** – just a copy of the **Cocoa Touch App Base.xctemplate** value because I don't need it as an Ancestor template. Possibly, not required in other cases

## This Repository Templates
- **UIKit App** – a UIKit application without a storyboard interface
