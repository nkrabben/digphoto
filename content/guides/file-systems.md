# Notes

A file need a location to be stored and then found. For the 1980s into the 2000s, that location was burrowed in a nested hierarchy folders. The principle extends from storing folders in a file cabinet, except any folder can contain a seemingly infinite number of files and folders. Infinite possibilities can lead to fragmentation and problems.

Software and hardware companies encouraged some behaviors with defaults like `~/Pictures/` and `~/My Documents/` and standards like HFS, but the users had freedom to design their file system how they wanted and to use whatever software they wanted for those files.

If the user has less control of the file system, it's easier to build system integrations. The DCF standard is a prime example. A memory card from one DCF-compliant camera can be used by any other DCF-compliant camera, scanner, or printer. On a mass consumer scale, that interoperability is more valuable than the freedom to name and folder files how one user wants.

Beyond better interoperability possibilities, hiding the file system removes the burden of even thinking about file management. Steve Jobs famously spoke against the use of software like `Finder` and `Explorer` in 2005. ....

When Apple released the iPhone in 2007, it had no app for file management. Photos and videos were not icons that could be moved between folders, but thumbnails in the Camera Roll that could be shared with other applications. All the files were still stored in folders, but those folders have never been directly accessible in stock iOS.

Android has a similar experience, although not as a extreme. It also encourages users to look at media primarily through a media app instead of a file browser, but file browsers are available.

This approach has some advantages.

1. Users don't see file names and don' think about them. Does it matter if a file is called `IMG_0001.JPG` or `Christmas Tree 2013.JPG` if the user can see the thumbnail overlayed by the datestamp extracted from the EXIF data.
2. Users don't see storage devices and don't think about them. If a file is on a phone or in the cloud, all the thumbnails can be available in the app, ready to call the full file.

On a computer, a task might look like this.

1. Find the required file amongst all the files on the computer.
2. Open that file with the software that you want to use
3. Find a place to save a new file amongst all the files on the computer.

Software designers would prefer that users don't think about any files except the ones needed for their task.

iOS goes further
