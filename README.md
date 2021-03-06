# Using Local History

**Local History** is a feature built into PyCharm that allows you to chronologically view changes to a file or directory, diff changes to files as you're working on them, and revert changes, all without using a version control system.

You can think of Local History as your own personal version control system (VCS) inside of PyCharm. Local History doesn't depend on any external VCS like Subversion, Mercurial, or Git. This means Local History will work with files that aren't being tracked by your VCS and doesn't require commits to a repository.

> Local History will persist until you install a new version of PyCharm or [invalidate PyCharm's caches](https://www.jetbrains.com/help/pycharm/cleaning-system-cache.html). If you need to keep track of the changes you've made, be sure you commit your files and changes to your VCS before updating PyCharm or clearing caches.

You'll find all of the commands for Local History under the main **VCS** menu item.

## Local History of a File or Directory

Local History can show you changes made to a certain file or to a whole directory. Each entry in the Local History dialog box is displayed with its time stamp, action, and an optional label. The Local History for a file includes all changes that affect both the selected file and the whole project. Local History for a directory shows changes to the source code tree in general. You can explore changes, selecting the respective row in the Local History dialog box.

### Viewing Local History for a file or directory:

1. Select a directory or file in the Project tool window, or open a file in the editor.
2. Then, do one of the following:
    * On the main **VCS** menu, or on the context menu of the selection, choose **Local History | Show History**.
    * Press `Alt+Back Quote`, and choose the desired command from the VCS Operations quick list.
    * Use **View | Recent Changes** which shows a summary of recent changes in a single pop-up list. Clicking an entry in this list will show the associated Local History entry.
3. Use the Local History view to compare local versions and accept or revert changes.
    ![Local history view to compare, accept, and/or reject local changes](images/lvcViewHistoryDiff.png)

## Local History of Source Code

You don't always need to see changes for an entire file or directory. In these cases, Local History can show you just the history for a particular fragment of code.

### Viewing Local History of a source code block:

1. In the editor, select the fragment of source code you want to inspect.
2. Then, do one of the following:
    * On the main **VCS** menu, or on the context menu of the selection, choose **Local History | Show History for Selection**.
    * Press `Alt+Back Quote`, and choose the desired command from the VCS Operations quick list.

## Restoring a File from Local History

If you find that you need to completely restore a file back to a previous version, Local History will allow you to do that. Rolling back changes from Local History works same way as in most version control systems.

### Rolling back changes to a file:

1. Open the Local History view through either the **VCS | Local History** menu item or the context menu in the Project explorer.
2. Select the version you want to roll back to.
3. In the context menu for your selected version, choose **Revert**.

## Local History Labels

If you're familiar with Git's `tag` concept, this next feature will feel comfortable to you. Before you undertake a major overhaul of your code, it can be a really good idea to mark the current version as "stable". Local History provides a feature known as **labels** that allow you to mark the current state of your code with a meaningful tag. Then, if you need to, you can roll your code back to a particular label.

Labels don't just apply to a single file or directory, though; they apply to the entire project.

### Adding a label to your project

1. Select a file or directory in the Project tool window, or open a file in the editor.
2. Then, do one of the following:
    * On the main **VCS** menu, or in the context menu of the selection, choose **Local History | Put Label**.
    * Press `Alt+Back Quote` and choose **Put Label** command from the VCS Operations quick list.
5. In the Put Label dialog box, type the label name.

### Reverting a project to a label

If you find yourself needing to revert to a labelled version of your code, the process is identical to reverting to any other version.

1. Open the Local History view through either the **VCS | Local History** menu item or the context menu in the Project explorer.
2. Look for the label you want to roll back to.
3. In the context menu for the label, choose **Revert**.

## Viewing Changes Across Recent Projects

While it's not part of the Local History feature, PyCharm also allows you to view the summary of recent changes to all recent projects, the PyCharm configuration directory, and more. From the Recent Changes pop-up, you can browse through the history of changes, navigate to and inspect a particular change, compare versions, and revert changes if necessary.

### Viewing recent changes

1. From the main menu, choose **View | Recent Changes**, or press `Shift+Alt+C`.
2. In the **Recent Changes** pop-up, select the change you are interested in:
    ![Selecting a recent change](images/recentChanges.png)
3. In the dialog that opens, review the differences and discard changes if necessary.