Modular NSMI

IssueObject

**Children**

.children

Children of an IssueObject are more specific subsets of the IssueObject.

A child does not inherit from the parent IssueObject, except for Special Fields Children (and maybe Special Fields).  The parent's metadata, such as legal information, may be incorporated.

**Special Fields Children**

.sfchildren: DADict.using(DADict

.sfchildren['typeofhousing']['publichousing'] is an IssueObject that inherits from the parent IssueObject

This attribute lists the IssueObjects that are special fields children - the same issue in a specific area.  For example, Eviction is an IssueObject, and Eviction in Public Housing is the same issue in the specific area of public housing regulations.

**Special Fields**

.specialfields: DADict.using(SFMETADATA)

.specialfields['typeofhousing'] is a SFMETADATA object with information about the specific field (a description and link to more information about public housing, for example)

Special Fields say when this issue object has a special field that must be true for this to be applicable.

If this special field is marked and the parent is an IssueObject with the same label, which has this IssueObject in its Special Fields Children list, then this IssueObject is a special field child of the other IssueObject, and inherits from it (with modifications as denoted in the ).
If this special field is marked and the parent is an IssueObject with a different label, then this is a child of the IssueObject, not a special field child, but a child that only applies if the special field is appropriate.

**Information**
.code
.description
