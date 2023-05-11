**Lab Report 3**

* Option 1: -r (Recursive Search)

This option allows grep to search for a pattern recursively within directories and their subdirectories. It is useful when you want to search for a specific pattern across multiple files in a directory tree.

Example 1: Searching for a pattern within files in a directory
```
$ grep -r "keyword" ./technical
```
This command searches for the pattern "keyword" within all files in the ./technical directory and its subdirectories.

Example 2: Searching for a pattern within filenames
```
$ grep -r -l "pattern" ./technical
```
This command searches for the pattern "pattern" within the filenames of all files in the ./technical directory and its subdirectories. The -l option lists only the filenames that match the pattern.

Source: Linuxize - How to Use the Grep Command on Linux

* Option 2: -i (Case-insensitive Search)

This option tells grep to perform a case-insensitive search, ignoring the distinction between uppercase and lowercase letters. It is useful when you want to search for a pattern without being case-sensitive.

Example 1: Case-insensitive search within files
```
$ grep -i "pattern" ./technical/file.txt
```
This command searches for the pattern "pattern" within the file file.txt in the ./technical directory, ignoring case sensitivity.

Example 2: Case-insensitive search within filenames
```
$ grep -i -l "keyword" ./technical
```
This command searches for the pattern "keyword" within filenames in the ./technical directory, ignoring case sensitivity. The -l option lists only the filenames that match the pattern.

Source: GNU Grep manual

* Option 3: -v (Invert Match)

This option allows grep to display lines that do not match the specified pattern. It is useful when you want to exclude lines containing a particular pattern.

Example 1: Invert match within files
```
$ grep -v "pattern" ./technical/file.txt
```
This command displays all lines within the file file.txt in the ./technical directory that do not contain the pattern "pattern".

Example 2: Invert match within filenames
```
$ grep -v -l "keyword" ./technical
```
This command lists the filenames in the ./technical directory that do not contain the pattern "keyword". The -l option is used to only display filenames.

Source: The Linux Documentation Project - Grep

* Option 4: -A (After Context)

This option displays lines after the match. It is useful when you want to see the context or surrounding lines of a matched pattern.

Example 1: Display lines after the match within files
```
$ grep -A 2 "pattern" ./technical/file.txt
```
This command displays the line containing the pattern "pattern" within the file file.txt in the ./technical directory, as well as the two lines that follow it.

Example 2: Display lines after the match within filenames
```
$ grep -A 3 "keyword" ./technical
```
This command searches for the pattern "keyword" within all files in the ./technical directory and its subdirectories. It displays the matching line as well as the three lines that follow it. This can be helpful to get a better understanding of the context surrounding the matched pattern.**
