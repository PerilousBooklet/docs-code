# Bash

TODO: toc

https://devhints.io/bash
https://www.redhat.com/en/blog/arguments-options-bash-scripts

https://stackoverflow.com/questions/8880603/loop-through-an-array-of-strings-in-bash
https://superuser.com/questions/1533900/difference-between-and-or-and-in-bash

## Loops

### C++-like for loop

```sh
for ((i = 1; i < 11; i++))
do
  echo "Iteration number $i"
done
```

## Files

## Folders

To create multiple directories with one command:

```sh
mkdir -vp dir1/{1,2} dir2/{2,3/{dir3,dir4}}
```

To create numbered directories:

```sh
mkdir -v ch{1..12}
```

Check that a folder already exists: 

```sh
if [ -d ./java ]; then
  echo "Folder java exists!"
fi
```

Check that a folder doesn't already exist: 

```sh
if [ ! -d ./java ]; then
  echo "Folder java doesn't exist yet!"
fi
```

## Strings

### Insert a multi-line string into a text file

To overwrite:

```sh
cat << EOL > example.txt
This is line one.
This is line two.
This is line three.
EOL
```

To append:

```sh
cat << EOL >> example.txt
This is line one.
This is line two.
This is line three.
EOL
```

### sed

TODO: sed

### awk

TODO: awk

## JSON

TODO: jq
