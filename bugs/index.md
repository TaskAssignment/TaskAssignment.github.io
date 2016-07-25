---
layout: default
---

# Bugs

Bugs can come from GitHub or Bugzilla, as of now.
Those are considered subprofiles and reference a [`Bug`](/api/Bug.html)
that will contain the basic information for a bug analized in this system.

For now, a [`Bug`](/api/Bug.html) must be created just before the creation of a
specific profile. The specific profile must, then, reference the general [`Bug`](/api/Bug.html).

Because this is not an issue tracker, and we fetch bugs from other places, **[`Bug`](/api/Bug.html) id must be the
a 2 letter acronym representing the origin plus the specific id.** Example:
A Bug from GitHub has an `id` equals to 123. If I fetch this bug to the system database,
I'll have a [`GitHubIssue`](/api/GitHubIssue.html) with id 123 that will reference a [`Bug`](/api/Bug.html) with id 'GH123'.
A Bug from Bugzilla with the same id, would reference a [`Bug`](/api/Bug.html) with
id 'BZ123'.

This ensures that bugs from different sources with the same id will have different ids on our database.
It's also an easy way to check the source of a bug. And, because an id is already unique inside a system,
like a GitHub id, we can safely refer to them when any other information on the bug is needed.
