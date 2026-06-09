# Team Roster

> Our team at a glance. Each person's profile links to their full page with tasks and activity.

## Members

```dataview
TABLE WITHOUT ID
  link(file.path, regexreplace(file.folder, "team/", "")) AS "Name",
  Role
FROM "team"
WHERE file.name = "profile" AND Role != null
SORT Joined ASC
```

## Quick Links

```dataview
LIST WITHOUT ID "**" + file.folder + "** — [[" + file.path + "|Profile]] · [[" + regexreplace(file.path, "profile", "tasks") + "|Tasks]] · [[" + regexreplace(file.path, "profile", "activity/activity") + "|Activity]]"
FROM "team"
WHERE file.name = "profile" AND Role != null
SORT Joined ASC
```

---

> Add your picture and a fun fact in your `profile.md`!
> New here? Copy `team/_new_user/` and follow the README, or ask claude to fill it.
