# dumpsys

There is a handy command-line tool called <code>dumpsys</code>. It allows us to dump the state of system services.

The very interesting thing we can do is dump activities from Activity Manager and look for the running ones.
This is the thing that is missing from the IDE we use, because what we can use in Android Studio is the Layout Inspector, so we can dump a state of a single activity and look at individual views inside of it. 
But if we have multiple activities - for example, if we are getting introduced to a new code base and we get into some activity - there are certain methods to know what activity we are in, but this is one of the handiest ones. 

We have a currently running activity on top here. 
If out app has multiple activities that are somewhere in the stack, this is the way to find out where we are.

<img width="600" src="https://user-images.githubusercontent.com/70295997/222946930-b3828924-16f2-4531-9efd-44d756d49ca0.png">

We can also dump the status of <code>jobscheduler</code> and may therefore find out, for example, that Calendar uses two jobs. 
One of the jobs periodically queries the content provider and the other one queries the notifications provider.

<img width="600" src="https://user-images.githubusercontent.com/70295997/222946953-d829f28a-cbb4-418b-840b-68c7c5975891.png">

If we are debugging an app which uses some jobs, we can force our jobs to be executed using the  <code>-f</code> flag,

<img width="600" src="https://user-images.githubusercontent.com/70295997/222947060-663b43c1-fa7c-4b02-bfc6-69515d917890.png">
