# Grep & Regex Lab

## Task

In this lab, we will make use of `grep` and regex to conduct pattern searches within a text files.

## Instructions

### Creating the Text File

Let's create two text files to run `grep` and regex commands on. Use any text editor to create a text file named `regex-lab-1.txt` and `regex-lab-2.txt` and save them somewhere under your home (~) directory. Alternatively, you can use the following code to create the text files:

```bash
$ echo "This is a sample snippet of text to place within your new lab file. Make sure this file is saved in an easy-to-access directory." > regex-lab-1.txt
```

```bash
$ echo "Our second file. This one has less text in it." > regex-lab-2.txt
```

### Using Grep with Basic Patterns

Now that we have our text file set up, search for the word "lab" within your new file:

```bash
$ grep "lab" regex-lab-1.txt
```

Search for the word "file" next:

```bash
$ grep "file" regex-lab-1.txt
```

Let's test what kind of results we get once we start adding options to grep:

```bash
$ grep -i "this" regex-lab-1.txt
```

Note any differences between the latter and the former output? The `-i` option returns all case-insensitive matches to the search term.

Sometimes, we want to know which files contain a word but do not want to spend time looking through an entire directory. For this, use the `-l` option.

```bash
$ grep -l "place" regex-lab-1.txt regex-lab-2.txt
```

If a file is too large, we have a grep option that will print the line number along with the output. Give it a try by using the `-n` option:

```bash
$ grep -n "directory" regex-lab-1.txt
```

### Using Regex Metacharacters

Regular expression metacharacters specify different search patterns for us. For example, run the following command to search for lines that contain "sample", "baker" or "saved":

```bash
$ grep "sample\|baker\|saved" regex-lab-1.txt
```
The results should show you how multiple words can be searched for within a file.

Finally, let's ask the terminal to find any lines that have the word "make" as the first word regardless of case.

```bash
$ grep -i "^make" regex-lab-1.txt
```
As you can see, we are able to combine grep options and regex metacharacters to manipulate the output we need.

## Submission

Take a screenshot of the terminal with the output visible; upload the screenshot as the submission for this assignment.