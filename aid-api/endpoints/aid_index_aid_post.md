# Aid Index POST

## Description
Aid index provides an filterable paginated array of aid items with meta information about the pagination and total records availible.  The filter will be provided as values 

## Swagger Link
https://services.intocareers.net/swagger/aid#/Aid_Index/post_api_v1_aid

## State Scoping

The response is scoped to the state(s) used at JWT creation time with the base intoCareers appended after all state specific aid items.  A states base aid items DO NOT "extend" the base intoCareers keys.  Due to this, providing multiple states with your JWT WILL NOT result in duplicated aid items.


## Example Aid Index POST request

````
{
  "page": 1,
  "limit": 100,
  "aidName": "string",
  "closeDateIDs": {
    "from": 0,
    "to": 12
  },
  "closeDates": [
    [
      "None",
      "January",
      "February",
      "March",
      "April",
      "May",
      "June",
      "July",
      "August",
      "September",
      "October",
      "November",
      "December"
    ]
  ],
  "gpaIDs": {
    "from": 0,
    "to": 3
  },
  "gpa": [
    [
      "None",
      "2.5",
      "3.0",
      "3.5"
    ]
  ],
  "need": true,
  "national": true,
  "clusterIDs": [
    [
      799068
    ]
  ],
  "extendedFilters": {
    "genders": [
      [
        "omit1",
        "men",
        "women"
      ]
    ],
    "raceHeratiges": [
      [
        "omit2",
        "afri",
        "asia",
        "hisp",
        "nativ",
        "race"
      ]
    ],
    "disablities": [
      [
        "omit3",
        "blind",
        "deaf",
        "learn",
        "phys"
      ]
    ],
    "stateResidences": [
      [
        "omit4",
        "OR",
        "AZ"
      ]
    ],
    "ethnicAndNationalHeratiges": [
      [
        "omit5",
        "etkope",
        "etlape",
        "ethspe"
      ]
    ],
    "religiousAffiliations": [
      [
        "omit6",
        "reldpe",
        "reotpe",
        "rejwpe"
      ]
    ],
    "completedEducations": [
      [
        "omit7",
        "hs",
        "post"
      ]
    ],
    "gradePointAverages": [
      [
        "omit8",
        "gpa2",
        "gpa3",
        "gpa4"
      ]
    ],
    "schoolTypes": [
      [
        "omit9",
        "2yr",
        "4yr",
        "trtech"
      ]
    ],
    "studyLoads": [
      [
        "omit10",
        "ftime",
        "ptime"
      ]
    ],
    "entryYears": [
      [
        "omit11",
        "fresh",
        "gr",
        "jr",
        "soph",
        "sr"
      ]
    ],
    "postSecondaryLocations": [
      [
        "omit12",
        "12MT",
        "12OR"
      ]
    ],
    "communityLocations": [
      [
        "omit13",
        100,
        99,
        98,
        97
      ]
    ],
    "programs": [
      [
        "omit14",
        110000,
        160000
      ]
    ],
    "awardTypes": [
      [
        "omit16",
        "loan",
        "other",
        "ren",
        "schol"
      ]
    ],
    "needs": [
      [
        "omit17",
        "need"
      ]
    ],
    "deadlines": [
      [
        "omit18",
        "apr",
        "may",
        "jun",
        "jun-only"
      ]
    ],
    "hobbiesTalentsInterests": [
      [
        "omit19",
        "tawppe",
        "talgpe",
        "taeppe",
        "tasnpe"
      ]
    ],
    "leadership": [
      [
        "omit20",
        "leader"
      ]
    ],
    "militaryBranches": [
      [
        "omit21",
        "af",
        "army",
        "cc",
        "kd",
        "mari",
        "mil",
        "navy"
      ]
    ],
    "employmentVolunteerExperiences": [
      [
        "omit22",
        "emsepe",
        "emjcpe",
        "emsfpe"
      ]
    ],
    "clubsCivicAssociationsUnions": [
      [
        "omit23",
        "ciadut",
        "ciaaut",
        "ciaeut"
      ]
    ],
    "businessAffiliations": [
      [
        "omit24",
        "coodpe",
        "codtpe",
        "coubpe"
      ]
    ]
  },
  "includeFields": [
    [
      "closeDate",
      "closeDateID",
      "gpa",
      "gpaID",
      "need",
      "national"
    ]
  ]
}
````

## Example Aid Index Item

See aid-index-get.md