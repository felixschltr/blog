---
layout: post
title:  "Creating custom spellfiles for vim"
date:   2021-03-17 18:54:02 +0200
categories: vim text-editor spell 
---
### Creating custom dictionaries

![vim_logo ><](/blog/assets/images/vim_logo.png)

By default, vim seems to only contain an English dictionary and all other dictionaries must be downloaded and created by hand.

When working on a document, spellchecking for English can be activated using:
```vim
:setlocal spell spelllang=en
```

Wanting to specify any other language in this way throws an error:
```vim
[In:]
:setlocal spell spelllang=de
[Out:]
Warning: Cannot find word list "fr.utf-8.spl" or "fr.ascii.spl"
```

Vims spellcheck offers the option to create spellfiles from dictionaries which are used by other word-processing software, such as LibreOffice (see `:help spell-mkspell`).
To be able to do so, you first need to download such a dictionary, e.g. from the [LibreOffice Extensions site](https://extensions.libreoffice.org/){:target="_blank"}.

These dictionaries typically come as `.oxt`-files but they can be extracted after being renamed to `.zip`-files. The two files that are crucial to construct the
spellfile are the `.dic`-file and the `.aff`-file that must be located somewhere in the directories created when extracting the `.oxt`-file. 

To create the spellfile from the extracted `.dic` and `.aff`-file, you call the following command **from within vim**:
```vim
:mkspell {outname} {inname} 
```
(see `:help mkspell` for more details)

## More concrete example
1. Imagine you have downloaded [this dictionary for German](https://extensions.libreoffice.org/en/extensions/show/german-de-de-frami-dictionaries){:target="_blank"} and
the corresponding `.oxt`-file is now stored on your `~/Downloads/` directory.
2. You rename the downloaded `oxt`-file to `.zip` and extract it to `~/Downloads/german_dict`.
3. Next, you navigate to that directory and check that both a `.dic` and a `.aff`-file are contained in it and that they both have the same name, i.e.
`dict_name.dic` and `dict_name.aff`.
(In this example the names would be `de_DE_frami.dic` and `de_DE_frami.aff`)
4. You start vim and call the following:
```vim
:mkspell de ~/Downloads/german_dict/dict_name
```
In this case `de` corresponds to `{outname}` and `~/Downloads/german_dict/dict_name` corresponds to `{inname}`.
If everything works out well you will observe vim processing the dictionary files and eventually, it will produce a file called `{outname}.utf-8.spl` which
is now located in the `~/Downloads/germ_dict` directory.
5. Finally, you need to add this newly created file to the directory from which vim can access it:
```bash
$ mv ~/Downloads/german_dict/de.utf-8.spl ~/.vim/spell/
```
**That's it**. Now you can enable spellchecking for German in vim by calling:
```vim
:setlocal spell spelllang=de
```
**Note**: This general procedure works for any language, given that the necessary `.dic` and `.aff`-files are available.
