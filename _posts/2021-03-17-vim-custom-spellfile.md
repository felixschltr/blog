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
```
In:
	:setlocal spell spelllang=en
```

Wanting to specify any other language in this way throws an error:
```
In:
	:setlocal spell spelllang=de
Out:
	Warning: Cannot find word list "fr.utf-8.spl" or "fr.ascii.spl"
```

Vims spellcheck offers the option to create spellfiles from dictionaries which are used by other word-processing software, such as LibreOffice (see `:help spell-mkspell`). To be able to do so, you first need to download such a dictionary, e.g. from the [LibreOffice Extensions site](https://extensions.libreoffice.org/).

These dictionaries typically come as `.oxt`-files but they can be extracted after being renamed to `.zip`-files. The two files that are crucial to construct the spellfile are the `.dic`-file and the `.aff`-file that must be located somewhere in the directories created when extracting the `.oxt`-file. 

To create the spellfile from the extracted `.dic` and `.aff`-file, you call the following command **from within vim**:
```
	:mkspell {outname} {inname} 
```
(see `:help mkspell` for more details)

## More concrete example

Let's imagine you have downloaded an `.oxt`-file for some dictionary you would like to use in vim. Let's imagine this file is now stored in your `~/Downloads/` directory.
After having extracted this file as `.zip`,you want to check the name of the `.dic` and `.aff`-files. They should be the same for valid dictionary files, i.e. `<dict_name>.dic` and `<dict_name>.aff`.
Next, you open up vim and call the following:
```
	:mkspell {outname} ~/Downloads/PATH_TO_EXTRACTED_FILES/<dict_name>
```
Where `{outname}` is typically chosen as the lowercase abbreviation for the language of the dictionary, i.e. `fr` for French.

