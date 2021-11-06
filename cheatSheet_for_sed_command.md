# Sed Command
Sed Command is a tool used to filter and transform the text.
## Syntax
```
sed [option] {script to execute on the file} [file_name]
```
Before moving into the Commands, we need to understand one thing to better understand the Sed Command

i.e. **Sed Command treats the every line as a row and every word in each line as a column.**

## Following are the different Use Cases of Sed Command

* To search for a pattern and replace every occurence of that pattern with an other string,
```
sed "s/pattern/string_to_replace/g" file_name
```


* To search for a pattern and replace only the Nth occurence of that pattern in each line with an other string,
  * we have to replace the occurence number with "N" beside "g"
```
sed "s/pattern/string_to_replace/Ng" file_name
```


* To search for a pattern in a range of lines(N1 to N2) and replace every occurence of that pattern with an other string,
```
sed "N1,N2 s/pattern/string_to_replace/g" file_name
```


* To search for a pattern in a Nth Line and replace every occurence of that pattern with an other string,
  * we have to replace the Line number with "N" beside "s"
```
sed "Ns/pattern/string_to_replace/g" file_name
```

* To search for a pattern in Nth line and replace only the Mth occurence of that pattern with an other string,
  * Observe N beside s, M beside g
```
sed "Ns/pattern/string_to_replace/Mg" file_name
```

* To search for a pattern2 and replace every occurence of that pattern2 with an other string, if and only if the pattern1 is existed in that line
```
sed "/pattern1/ s/pattern2/string_to_replace/g" file_name
```

* If we want to give multiple expressions like "s/pattern/string_to_replace/g" in the same command, we can use the following syntax,
  * we have to seperate each expression with a semicolon(;)
```
sed "s1/pattern1/string_to_replace_1/g1;s2/pattern2/string_to_replace_2/g2; ................. ;sN/patternN/string_to_replace_N/gN
```

* To print the lines which contain the given pattern,
```
sed -n "/pattern/p" file_name
```

* To delete the lines which contain the given pattern,
```
sed "/pattern/d" file_name
```

* To display certain range(N1 to N2) of lines from the given file,
```
sed -n "N1,N2p" file_name
```

* To display the entire content except the given range(N1 to N2),
```
sed "N1,N2d" file_name
```

* To delete a line number N from the given file,
```
sed Nd file_name
```

* To insert blank line after every non-blank line,
```
sed "G" file_name
```

* To insert multiple blank lines after every non-blank line,
  * we can give as many G's as blank lines we want.
  * we have to seperate each "G" with a semi-colon(;)
```
sed "G(1);G(2);........;G(n)" file_name
```

* All the Commands above don't change the file in-place.If we want to change the file in-place we have to include `-i` flag in the command.
```
sed -i "s/pattern/string_to_replace/g" file_name
```

* Before changing the file, if we want to have a backup of the original file, we have to include `-i.bak` option, it will create a backup file(.bak extension) with your file_name
```
sed -i.bak "s/pattern/string_to_replace/g" file_name
```
