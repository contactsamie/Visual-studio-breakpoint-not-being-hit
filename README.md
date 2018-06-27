# Visual-studio-breakpoint-not-being-hit


I struggled forever trying to fix this. Finally this is what did it for me.

Select Debug->Options->Debugging->General

Tick Enable .NET Framework source stepping.

(This may be all you need to do but if you are like me, you also have to do the ones stated below. The below solution will also fix errors where your project is loading old assemblies/.pdb files despite rebuilding and cleaning.)

Select Tools -> Options -> Projects and Solutions -> Build and Run,

Untick the checkbox of "Only Build startup projects and dependencies on Run",

Select Always Build from the "On Run, when project are out of date" dropdown.


https://stackoverflow.com/questions/21582022/visual-studio-breakpoints-not-being-hit
