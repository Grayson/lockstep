# What is lockstep?

`lockstep` is a small, Python-based, command line utility that keeps files synchronized.  It does this by allowing the user to define a master file and some targets.  When `lockstep` runs, it compares the files and determines if there have been any changes.  If the master file is different than any of the targets, then it will replace the target location with a copy of the master file.


# Why was lockstep created?

Have you ever wanted some file backed up?  Not like the entire drive, but one particular project.  You're working on, say, your TPS report and you'd like the exact same file backed up to a networked folder for the company as well as your USB drive so you can take it home.  `lockstep` can do that.

`lockstep` lets you work on a master file while copying the file to other locations.


# How do I use lockstep

At the moment, `lockstep` is merely the command line tool.  There may be other components added in the future.  In any case, you can utilize `lockstep` by adding it somewhere in your `$PATH` and making sure that it is executable (`chmod +x lockstep`).  You can then simply run `lockstep` to copy the master files to their targets.

You can add masters and targets using the `lockstep` utility itself.  Simply use the `-t`, `--target`, `-s`, `--source` flags to add file associations.

	./lockstep -s /path/to/masterfile -t /path/to/targetfile

or

	./lockstep --source /path/to/masterfile --target /path/to/targetfile

At the moment, `lockstep` requires full paths to the files, although it does handle expansion of `~`.

If you'd like to associate one master file with multiple targets, simply repeat the request with a new target.

	./lockstep --source /path/to/masterfile --target /path/to/targetfile
	./lockstep --source /path/to/masterfile --target /path/to/anothertargetfile

In the above example, the masterfile will now be copied to targetfile and anothertargetfile whenever `lockstep` is run.


# Future plans for lockstep

* Remove file associates, both in part and in whole
* Add simple globbing and handle relative paths
* Handle folders, perhaps by recursion
* Add application/System Prefs pane to management
* Create launchdaemon


# License information

Assume a public domain license, although I'd appreciate that if anyone improves the code that they fork the project and submit the improvements back for the public good.

And if someone that isn't me finds a market for it and gets rich selling a user-friendly version to grandparents, I'll congratulate you and call you an asshole.  You'll also owe me a beer.


# Contact

[Grayson Hansard](mailto:support@fromconcentratesoftware.com)  
[From Concentrate Software](http://www.fromconcentratesoftware.com/)  
[@Grayson](http://twitter.com/Grayson)
