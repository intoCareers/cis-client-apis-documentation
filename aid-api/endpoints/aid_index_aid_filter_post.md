# Aid Filter POST

## Description
Aid filter provides an array of aid items ids filtered from sections attributes.  This filter is faster compared to the filtered index request, but does not provide data about the aid items.

## Swagger Link
http://localhost:3000/swagger/aid#/Aid_Index/post_api_v1_aid_filter

## State Scoping

The response is scoped to the state(s) used at JWT creation time extended with the base intoCareers aid items.  A states base aid items DO NOT "extend" the base intoCareers keys.  Due to this, providing multiple states with your JWT WILL NOT result in duplicated aid items.


## Example Aid Index POST request

````
{
  "genders": [
    "omit1",
    "men",
    "women"
  ],
  "raceHeratiges": [
    "omit2",
    "afri",
    "asia",
    "hisp",
    "nativ",
    "race"
  ],
  "disablities": [
    "omit3",
    "blind",
    "deaf",
    "learn",
    "phys"
  ],
  "stateResidences": [
    "omit4",
    "OR",
    "AZ"
  ],
  "ethnicAndNationalHeratiges": [
    "omit5",
    "etkope",
    "etlape",
    "ethspe"
  ],
  "religiousAffiliations": [
    "omit6",
    "reldpe",
    "reotpe",
    "rejwpe"
  ],
  "completedEducations": [
    "omit7",
    "hs",
    "post"
  ],
  "gradePointAverages": [
    "omit8",
    "gpa2",
    "gpa3",
    "gpa4"
  ],
  "schoolTypes": [
    "omit9",
    "2yr",
    "4yr",
    "trtech"
  ],
  "studyLoads": [
    "omit10",
    "ftime",
    "ptime"
  ],
  "entryYears": [
    "omit11",
    "fresh",
    "gr",
    "jr",
    "soph",
    "sr"
  ],
  "postSecondaryLocations": [
    "omit12",
    "12MT",
    "12OR"
  ],
  "communityLocations": [
    "omit13",
    100,
    99,
    98,
    97
  ],
  "programs": [
    "omit14",
    110000,
    160000
  ],
  "awardTypes": [
    "omit16",
    "loan",
    "other",
    "ren",
    "schol"
  ],
  "needs": [
    "omit17",
    "need"
  ],
  "deadlines": [
    "omit18",
    "apr",
    "may",
    "jun",
    "jun-only"
  ],
  "hobbiesTalentsInterests": [
    "omit19",
    "tawppe",
    "talgpe",
    "taeppe",
    "tasnpe"
  ],
  "leadership": [
    "omit20",
    "leader"
  ],
  "militaryBranches": [
    "omit21",
    "af",
    "army",
    "cc",
    "kd",
    "mari",
    "mil",
    "navy"
  ],
  "employmentVolunteerExperiences": [
    "omit22",
    "emsepe",
    "emjcpe",
    "emsfpe"
  ],
  "clubsCivicAssociationsUnions": [
    "omit23",
    "ciadut",
    "ciaaut",
    "ciaeut"
  ],
  "businessAffiliations": [
    "omit24",
    "coodpe",
    "codtpe",
    "coubpe"
  ]
}
````

## Example Aid Index Item

See aid-index-get.md

## NOTES

Providing an empty object will return items that have a full set of not specified sections.