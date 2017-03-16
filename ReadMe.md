# Attempt to set a breakpoint on a D project using monodevelop

Well, integration is really uncool and it's not fun. At least I managed to get a breakpoint working

![](./breakpoint-in-mono-with-dlang.png)

This works, but handling external libraries with `dub` seems to be a mess.

What I did:

1. Install dlang
2. Install Monodevelop
3. Create an empty dlang project
4. Run `dub init` in the folder that contains the `dproj` project file
5. Open project in monodevelop (if you installed dlang from script, open monodevelop with command line where you activated dlang so it can see `dmd` and `dub` commands)
6. Right click on your project, `Add existing folder`, select `source`
7. Run with debug (have your breakpoint ready). 

This worked for me, but it was a pain to figure this out. To have your dependencies loaded, you can double click the project (Project options), go to `Includes` and then manually add **every single dependecie's `source` folder**.

Don't enjoy.
