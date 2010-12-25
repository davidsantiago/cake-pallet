cake-pallet
===========
cake-pallet is a plugin to invoke pallet tasks using cake. Pallet is used as
a library, so Pallet tasks are written as Clojure code you can keep in your
project. By using cake to launch pallet, you can invoke your Pallet scripts
without having to start a repl or write custom scripts. 

Obtaining
---------
In your project file, add 

	[cake-pallet "0.3.0-SNAPSHOT"] 

to your :dev-dependencies, and add 

	:tasks [cake-pallet.tasks] 

to your project (Keep in mind, your deployment tasks will presumably require
pallet, so you should also add a dependency for that). Then run

	cake deps

To make sure it works and get a list of the other tasks available, run

	cake pallet help

Tips
----
If you'd like to make sure your pallet scripts are excluded from any jars you
build, you can put them in a subdirectory of your project called "dev". They
will automatically be added to the classpath while you are developing, but
won't get built into artifacts.

News
----
New to 0.3.0 - Now passes the project file to pallet. Also supports cake's
ignored arguments, so you can pass arguments straight to pallet without
cake processing.

License
-------
Eclipse Public License

Credits
-------
Based on code from pallet-lein by Hugo Duncan.
