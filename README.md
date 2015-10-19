n-cube-editor
=============
n-cube-editor is a web-based GUI editor for editing and managing n-cubes.

```
<dependency>
  <groupId>com.cedarsoftware</groupId>
  <artifactId>n-cube</artifactId>
  <version>0.3.0</version>
</dependency>
```
Like **n-cube-editor** and find it useful? Donate some **Bitcoin**: 1MJFgxTVFZZ3EkmdPabsQ5UremUg2HHPe7

#### Licensing
Copyright 2012-2015 Cedar Software, LLC

Licensed under the Apache License, Version 2.0

### Sponsors
![Alt text](https://www.yourkit.com/images/yklogo.png "Yourkit")

YourKit supports open source projects with its full-featured Java Profiler.
YourKit, LLC is the creator of <a href="https://www.yourkit.com/java/profiler/index.jsp">YourKit Java Profiler</a>
and <a href="https://www.yourkit.com/.net/profiler/index.jsp">YourKit .NET Profiler</a>,
innovative and intelligent tools for profiling Java and .NET applications.

![Alt text](https://encrypted-tbn2.gstatic.com/images?q=tbn:ANd9GcS-ZOCfy4ezfTmbGat9NYuyfe-aMwbo3Czx3-kUfKreRKche2f8fg "IntellijIDEA")
___
### Version History
* 0.3.0
 * Update Branch - Before it was operating transactionally, meaning that no cubes were updated if there were any merge conflict.  Now, Update branch makes all possible updates (commits them) and then shows the number of updates, merges, and conflicts.  If there are any conflicts, a merge conflict window will pop-up to allow the conflict to be resolved.
 * Search now only searches locally in memory unless the 'contains' field has content.  This dramatically speeds up search and reduces a lot of database server load.
 * Search now illustrates the selected text in the drop down even when a wildcard ('*') is used.
 * Rule names - now display much nicer and without the 'name:' text.
 * Rule conditions - user can now enter 'url|' or 'cache|' in front of the rule condition to indicate that the expression should be cached (or from a URL).  Both can be used, or either one, or no prefix.
 * Link highlight / substituion - the algorithm that matches the cube names within the cube cells now finds the longer cube names before the shorter cube names. It also handles multiple in a cell.  The alogrithm no longer attempts substitutions in URLs, which was rendering the URL unable to be clicked and followed.
 * Cube HTML is loaded faster using innerHTML instead of JQuery HTML (loads cube HTML twice as fast).
 * Default cell values are now displayed (in light gray) so that you can easily tell when a cell will pickup the n-cube leverl default.
 * The default cell can now be completely set from the 'Details' page (GroovyExpression, String, Template, ... all data types and linked types).
 * The back-button now recognizes when the app, version, status, and branch have not change, and simply selects the desired cube (rather than reload cubes for the changed app, version, etc.).  This makes the normal back-button use-case much faster.
 * 'Loading...' is now displayed when the application is starting.
 * Test tab reformatted to match the rest of the application.
 * Test inputs can now be GroovyExpressions or Groovy Templates (any CommandCell).
 * Application and Versions list now use single bootstrap-select widget so that they use much less vertical screen space, allowing more n-cubes to show.
 * Revision History now has separate options for HTML, JSON, and to open a 'Compare' website.
 * Updated to n-cube 3.3.9
 * Updated to Twitter Bootstrap 3.3.5
 * Updated to JQuery 2.1.4.
 * New logo image.
 * Added favicon.ico
* 0.2.0
 * Updated to use n-cube 3.3.3 (using new search API)
 * Added HTML / JSON / Compare buttons to the Revision History screen
* 0.1.0
 * Initial version

By: John DeRegnaucourt
