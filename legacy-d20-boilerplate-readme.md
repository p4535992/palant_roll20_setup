Description

Roll20 userscript boilerplate.
Bypass Content Security Policy and gain access to d20 object.

Why?

For a while now, I've been wanting to tinker with a Roll20 userscript. I soon realized there were a couple of obstacles to overcome for this project.

###1.) The Content Security Policy is very restrictive.
Simple enough, we can eval our code within the unsafeWindow.

###2.) The main object, d20, is not accessible outside of scope.
To gain access, we have to wait until d20ext is created and override the setting of the environment property to development.

###3.) Setting the environment to Development triggers a series of changes that impede gameplay.
As soon as the d20 object is exposed, we set everything back to production and cleanly back out.

TA-DA!

After solving all three issues, we now have our code running on Roll20 with the d20 object exposed and it's all nice and clean :)
