This is a sample project to revisit antlr based apps using a proper maven build rather than relying on vscode to do the right thing.  Nothing to see here.  Move along.  Okay just one thing to see.

Initially the project pom had included the `pluginManagement` tag around the plugins.  This tag was part of the original maven project generation with `maven-archetype-simple`.  It was also part of the project generated with `maven-archetype-quickstart`.  Turns out the `pluginManagement` tag configures plugins for project builds that inherit from the current project.  This is not what I wanted.  I wanted the plugins to be configured for the current project.  So I removed the `pluginManagement` tag and the plugins were configured for the current project.  In my case, I wanted the antlr plugin to actually do something in this project as I have no projects that inherit from this project.