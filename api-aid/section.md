# SECTIONS

Synopsis: ````Aid Item````s will have one or more sections for each of the unique topics.  These sections contain meta information about the ````Aid Item```` used for display and/or filtering purposes.

Sections are a generic container for information related to a given ````Aid Item````.  This can include ````Sort Type```` sections or ````Copy Text```` sections.  Section types are used to differentiate between these 2 types of sections.  Sections are further identified with topics.  Each section element has a topic specific data that identifies the "bucket" for which the section item is a member.

### Sort Type
````Sort Type```` sections are the sections used as the basis for filtering the aid items into "sectional buckets".  This means that any filter options provided within a section are treat as a union filter with other filter options in the same topic.  However, filter options act as a intersection filter with filter options outside of the same topic.

### Copy Text
````Copy Text```` sections are the sections used as the basis for displaying an aid item.

### Topics

Topics represent the logical boundaries for the section elements.  Topics allow section elements to create an association between ````Aid Item````s and "buckets" such as gender, heratige, finacial need, ect.  There are 22 unique topics for ````Sort Type```` sections and 10 unique topics for ````Copy Text```` sections.