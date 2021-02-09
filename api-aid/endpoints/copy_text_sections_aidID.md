# Sections

## Description
Sections returns aid section elements that represent the filterable topic value for a specific aid item.  Sections are a generic container that has one and only one topic key.

## Swagger Link
https://services.intocareers.net/swagger/aid#/Copy_Text/get_api_v1_aid_sections__aidID_

## State Scoping

The response is scoped to the state(s) used at JWT creation time.  Because the aid id is provided, only sections for aid items that are scoped to the state in the JWT will be returned.  Requesting an aid item from another state will return an empty response.

## Example Aid Section Element

```javascript
  sourceStateAbbr: "IC"
  sectionData:
    label: "Women"
    key: "women"
    sequenceKey: 20
  topicID: 1
  topicKey: "Sex"
  topicLabel: "Gender"
```
------------
#### sectionData
Description:  This object contains the meta and display information of this aid item section element.
Properties:
````
Descriptors =  // Not used
label = any; // Copy Text to display
key = any; //
sequenceKey = number; // 
````
------------
#### topicID:
Description: Unique keys that represent the section element "type".
------------
#### topicKey:
Description: Unique keys that represent the section element "type".  The will be at least one element for each of the 23 topics, but there may be mutliple
elements per topic.  These topicKeys match the keys given by the keys endpoint. (see keys.md)  A topicKey of omit(1-23) for a section represents the Not Specified "Bucket".  When a section has an omit(1-23) topic, then there should not be another section with the same topic.
Values:
````
Sex - Gender topic
Race - Race topic
Disabilities - Disablities topic
StRes - Applicant State residenency topic
EthnNatBkgrd - Ethnic background topic
RelAffil - Religious affliation topic
EdCompleted - Current education completed topic
RankGpa - GPA minimum topic
SchType - School type topic (i.e. 2yr, 4yr, tech school)
FullPartTime - Full or Part time study load topic
EntryYear - Expectd entry year into college (i.e. freshman, sophmore, junior, ect.)
SchLoc - Location of the post secondary school topic
LocalAreas - Applicant Residency State specific regions (i.e. county x resident, eastern region, ect.)
Progs - Programs of study required for aid item topic
AwardType - Finacial payback responsibility topic. (i.e. scholarship, loan, grant, ect.)
Need - Applicant finacial need considered topic
Deadline - The timeline segments.  This generally includes a numerically sequencial series of months starting with an opening month and ending in a final month.
HobTalInts - 
Leadership - 
Military - 
Empl - 
Civc - 
Corp - 
````
#### topicLabel:
Description: The string value label copy text of this topic intended to display as a label for the sectionData label for the aid item.
