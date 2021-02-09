# Aid Filter

Description: The aid filter uses a concept of sectional buckets.  This means that any Sort Type filter options sections are treated unioned with other filter options in the same topic.  However, filter options act as a intersection filter with filter options outside of the same topic.

## Eligibility Filter Contridictions
Do to the nature of this sectional bucket filtering, it is easy to create a contridiction.  I.e. if a user filters for both men and women, then by definition the user would not be eligible for all of the aid items returned.  The user would only be eligible for those those that match their gender.  However, if a male user searches for men and not specified they would be eligible for all aid items returned.

### Single Topic Single Bucket
Filter for aid items that are for men.  This will return only aid items specified for men.

### Single Topic Single Bucket - Not Specified
Filter for aid items that are for not specified for gender.  This will return only items that are not specified.  No aid items marked as for men or for women will be returned.

### Single Topic Multiple Filter Options
Filter for aid items that are for women and men.  This will return a union of aid items specified for women and men, but will not return not specified aid items.

### Single Topic Single Bucket - Not Specified
Filter for aid items that are for women, men, and are not specified for gender.  This will return all aid items.

### Multiple Topics Single Bucket
Filter for aid items that are for women and people of african heratige.  This will return an intersection of the two.  So only aid items that are both for women and people of african heratige will be returned.

### Multiple Topics Multiple Buckets
Filter for aid items that are for men and women and people of african heratige.  This will return an intersection of aid items flagged with african heratige and the union of aid items flagged men and specified aid items women.  This would not include the not specified aid items.