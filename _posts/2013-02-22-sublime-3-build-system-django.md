---
layout: post
title: Sublime 3 build system for Django
---

I'm a longtime user of Sublime Text. If you've never tried it I really advise you to give it a look, it's really worth it.
The beta version of Sublime 3 has been out for a few weeks now and I'm using it in parallel with the stable version 2 to test the new features.
While those new features are interesting by themselves trying a new version is also the moment where I dig in the documentation to understand the features I have not used yet in the previous versions.
And one of those features is the build systems.

In Sublime I mostly code in Python so I've never been attracted to this build concept ... how wrong I've been !
You can type a script in a file in Sublime and just by hitting Ctrl+B have your script run in a python interpreter and the result displayed inside your editor. What a time saver.

No more going back and forth between Sublime and that pesky windows command prompt (yes, I use windows at work ...) to test my code.

But there was still a problem : I do a lot of django coding and the default python build system does know how to import my django models. After a few more digging in the docs I came up with the following solution :

```python
{
    "working_dir": "c:/path/to/your/django/project",
    "path": "c:/path/to/your/python/binary;c:/path/to/site-packages",
    "env": {
         "DJANGO_SETTINGS_MODULE": "your.settings.module",
     },
    "cmd": ["python", "manage.py", "shell", "<", "$file"],
    "file_regex": "^[ ]*File \"(...*?)\", line ([0-9]*)",
    "selector": "source.python",
    "shell": true
}
```

Et voilà !
