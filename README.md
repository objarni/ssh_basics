SSH basics
==========

All you need to know about SSH to use GitHub/GitLab for ssh authentication

First, generate a crypto keypair. Hit enter 3 times to accept all defaults.

    $ ssh-keygen

Then, copy the the public part of the generated keypair to clipboard:

    $ cd ~
    $ cd .ssh
    $ cat id_rsa.pub   # .pub is for public; the 'id_rsa' file is the private part of the keypair!
    (long string of data shown)

Copy the string of data. Login to GitHub/GitLab and look for SSH keys under your account settings.

Paste the string and save! You are now authenticated - no need for a password anymore! Also, it's generally more secure then a short password, as long as the access to your id_rsa file is secure, which it is if your user account has a good password.

A note on ssh-agent
-------------------

This whole magic is based on having the 'ssh agent' service running in the background. You may need to run it, especially on Windows, just type

    $ ssh-agent
    
