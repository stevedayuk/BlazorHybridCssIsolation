# Blazor Hybrid Css Isolation
Repro of Blazor Hybrid CSS Isolation issue in .NET MAUI for .NET 6.0 when deploying on Windows 10 abd the assembly name of the project has been changed.

# CssIsolation.Working
This project was added using File -> New Project -> .NET MAUI Blazor App and has not been modified. CSS isolation works in this project as expected.

# CssIsolation.NotWorking
This project was added using File -> New Project -> .NET MAUI Blazor App too. However, the AssemblyName has had '.NotWorking' appended to it (making it CssIsolation.NotWorking.NotWorking) and the CSS 'link' element has been updated in wwwroot/index.html to suit.

When running the project, the compiled CSS isolation file is loaded by the running app but the CSS isolation attributes appended to the elements on the page differ from the attribute in the compiled CSS file, meaning that CSS isolation doesn't work.
