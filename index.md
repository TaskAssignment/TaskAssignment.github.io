---
layout: default
---

# How to use TaskAssignment

This is the user manual fot the task assignment system.
If you are looking for the developer's documentation, you should check [this place](https://github.com/TaskAssignment/software-expertise/wiki) or the [API docs](https://taskassignment.github.io/api/).

![export](/images/go-to-home-page.gif "Home Page")

## Manage Data

The first thing to do when using the system is to populate the database. If you are not the first user, it's possible it is already populated. You can check that by exporting the data.

### Export Data
In this page you can see the options of files you can generate and export. When a file has been generated already, the timestamp will be above the `Generate` button, but you can regenerate it if you want/need. Pressing `Download` will give you a zip file with the contents explained in the section you want.

![export](/images/go-to-export.gif "Export Page")

### Import Data
Here you can populate the database, with data from several sources. By picking the source,
you will see your options. Just press populate and wait for the loading icon to desappear.

![import](/images/go-to-import.gif "Import Page")

![import](/images/select-source.gif "Select import source")

## Visualize similarity

After you have the database populated, you can check the similarity between bugs and developers.
To do that, you can look for the name of the project you want to analyze. The search bar will appear once you hover the mouse over the magnifying glass icon.

When you press the magnifying glass, the projects with the searched name will appear, separated by their source, GitHub and Bugzilla, as of right now. Select the desired project and the bugs will appear on the left side of your screen.

![import](/images/search-project.gif "Search project")
