---
layout: post
title: "How to submit patches to ArrowOS Gerrit"
description: "This guide helps you on how to start contributing to the project"
thumb_image: "https://avatars3.githubusercontent.com/u/40351870?s=200&v=4"
tags: [arrowos, android, gerrit]
---

Published July 28, 2018 by **Bauuuuu, Kuber Sharma**<br>
Last updated on: **13th September,2018**

##### STEP 1:
  - Sign up on our gerrit [review.arrowos.net](https://review.arrowos.net) using either a google account or github account and set a **USERNAME** in profile section.<br>
<br>
**Note:** Username once set cannot be changed. If signed up via github, the username by default will be set to your github username.

##### STEP 2:
  - Open your local terminal and generate a ssh key by running the following command. Refer this [guide](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) for more info on how to generate ssh keys.
{% highlight bash %}
ssh-keygen
{% endhighlight %}
  - Now add the contents of your ssh public key(~/.ssh/id_rsa.pub) to your gerrit account in the SSH Public Keys section.
{% highlight bash %}
#This command will print out all the contents of your public key file
cat ~/.ssh/id_rsa.pub
{% endhighlight %}
  - Once done adding the ssh key to your gerrit account you may run the following command to check the connection with gerrit.
{% highlight bash %}
ssh -p 29418 USERNAME@review.arrowos.net
{% endhighlight %}

If everything went well you'll be greeted with a welcome message that the connection has been established. If you receive any error saying "**permission denied(public key)**", that means your SSH keys aren't entered correctly, try repeating STEP 2 again.<br>
In this case it is better to start things from scratch by removing your old ssh keys with the following command.
{% highlight bash %}
rm -rf ~/.ssh
{% endhighlight %}

Once you have verified your SSH keys and a successful connection with gerrit, you're ready to submit patches.

##### Below is an example showing how to submit a commit to **android_vendor_arrow** repo on ArrowOS gerrit:
This example commit shows you how to add a device to official list.

From the root of your source:
{% highlight bash %}
cd vendor/arrow/
{% endhighlight %}

Now make your changes, i.e. here we edit the **arrow.devices** file to add the device codename and build type.<br>
Once you have finished doing the changes
{% highlight bash %}
git add .
git commit -m "vendor: added xyz device to official"
{% endhighlight %}
This will generate a commit with the changes you have made.

##### Now to push the changes:
{% highlight bash %}
git push ssh://USERNAME@review.arrowos.net:29418/ArrowOS/android_vendor_arrow HEAD:refs/for/arrow-8.x
{% endhighlight %}
Here **android_vendor_arrow** is the repository name and arrow-8.x is the branch, change them accordingly to the repo and branch you're trying to push to.<br>

If you receive a message saying missing change id in the commit then read the error message carefully and do the exact step shown in the hint of the error message and push again.

With that your commit should be visible on ArrowOS gerrit for review.<br>
If you still have issues please contact anyone from the ArrowOS team.<br>
<br>
Last but not the least, it is important that port **29418** on your network should be open else you will receive an error saying "no route to host".
Some universities, institutions effectively block this port and in such cases you should push the patches form some other network where its allowed.

<center><img src="https://media.giphy.com/media/3o7qE1YN7aBOFPRw8E/giphy.gif"></center>
