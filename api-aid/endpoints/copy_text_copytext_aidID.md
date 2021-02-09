# Copy Text

## Description
Copy Text is information provided about the aid item meant to be displayed on the page with as a description for the aid item.

## Swagger Link
https://services.intocareers.net/swagger/aid#/Copy_Text/get_api_v1_aid_copytext__aidID_

## State Scoping

The response is scoped to the state(s) used at JWT creation time.  Because the aid id is provided, only aid items that are scoped to the state in the JWT will be returned.  Requesting an aid item from another state will return an empty response.

## Example Copy Text Element

```javascript
    sectionData:
        descriptors:
        - key: "DefaultEditHeight"
            value: "3"
        - key: "PE"
            value: "1"
        - key: "NA"
            value: "1"
        - key: "ST"
            value: "1"
        - key: "ViewTopic"
            value: "1"
        label: "1 - $1,000 scholarship; renewable."
        key: "AIAward"
        sequenceKey: 1
    topicID: 2
    topicKey: "AIAward"
    topicLabel: "Award:"
```

------------
#### sectionData
Description:  This object contains the copy text of this topic intended to display for the aid item.
Properties:
````
Descriptors =  // Meta information about how to display this copy text.
[
DefaultEditHeight, //
PE, //
NA, //
ST, //
ViewTopic, // should this aid item be displayed?
];
label = any; //
key = any; //
sequenceKey = number; // 
````
------------
#### topicID:
Description: Unique keys the represent the copy text element "type".
------------
#### topicKey:
Description: Unique keys the represent the copy text element "type".
Values:
````
AIDeadline - Copy Text element is a description of the deadline for this aid item.
AIDescription - Copy Text element is a full description of the aid item in a user friendly format.
AIOpenTo - Copy Text element is a description of the type of students that may apply.
AIProcedureExamples - Copy Text element is a description of instructions to follow to apply.
AISelectionCriteria - Copy Text element is a description of the criteria (need, academic, ect.) applicants must meet.
AIToStudy - Copy Text element is a description of the field of study.
AIWhereAt - Copy Text element is a description of the type of institution.
````
#### topicLabel:
Description: The string value label copy text of this topic intended to display as a label for the sectionData label for the aid item.
