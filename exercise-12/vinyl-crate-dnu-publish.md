# Publish Vinyl Crate Using DNU

The publish command in `dnu` will package the application for deployment.

When an ASP.NET Core application is published, it is entirely self-contained; meaning it includes all necessary dependencies, including framework references.

If you run `dnu publish` in your `VinylCrate.Web` directory, in your `bin` folder, you will now see an `output` folder. If you open the `output` folder, you will see three main components:

* approot
* logs
* wwwroot

The `approot` contains all of the server-side source code. This is a change from ASP.NET 4, as there are no binaries included. With the new compiler, the application is built and rendered on-demand.

The `wwwroot` is exactly what it is in the project during development; it contains all of the static files for the application. The files in the `wwwroot` are the only files that will be accessible by the browser.

The `logs` folder is simply the default location where logs will be written.

If you open the `approot` folder, you will see a `cmd` file in the root named "web" which was created for you.

Running this will run the application.

You can take this `output` directory, place it wherever you need, and run this command to start the site.

And that's it. Really.