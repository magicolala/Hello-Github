Gitflow

Gitflow est une ressource vous simplifiant la mise en place d'un workflow très connu par Vincent Driessen (nvie). Vous aurez de cette manière accès à des outils comme git feature simplifiant les taches répétitives comme créer une branch depuis develop et checkout dedans.

GIT COMMIT

NAME

git-commit - Record changes to the repository
SYNOPSIS

git commit [-a | --interactive | --patch] [-s] [-v] [-u<mode>] [--amend]
	   [--dry-run] [(-c | -C | --fixup | --squash) <commit>]
	   [-F <file> | -m <msg>] [--reset-author] [--allow-empty]
	   [--allow-empty-message] [--no-verify] [-e] [--author=<author>]
	   [--date=<date>] [--cleanup=<mode>] [--[no-]status]
	   [-i | -o] [-S[<keyid>]] [--] [<file>…​]

DESCRIPTION

Stores the current contents of the index in a new commit along with a log message from the user describing the changes.

The content to be added can be specified in several ways:

    by using git add to incrementally "add" changes to the index before using the commit command (Note: even modified files must be "added");

    by using git rm to remove files from the working tree and the index, again before using the commit command;

    by listing files as arguments to the commit command, in which case the commit will ignore changes staged in the index, and instead record the current content of the listed files (which must already be known to Git);

    by using the -a switch with the commit command to automatically "add" changes from all known files (i.e. all files that are already listed in the index) and to automatically "rm" files in the index that have been removed from the working tree, and then perform the actual commit;

    by using the --interactive or --patch switches with the commit command to decide one by one which files or hunks should be part of the commit, before finalizing the operation. See the “Interactive Mode” section of git-add[1] to learn how to operate these modes.

The --dry-run option can be used to obtain a summary of what is included by any of the above for the next commit by giving the same set of parameters (options and paths).

If you make a commit and then find a mistake immediately after that, you can recover from it with git reset.
