# Bash

TODO: toc

https://devhints.io/bash
https://www.redhat.com/en/blog/arguments-options-bash-scripts

https://stackoverflow.com/questions/8880603/loop-through-an-array-of-strings-in-bash
https://superuser.com/questions/1533900/difference-between-and-or-and-in-bash

## Logging

### How to color the logs

You can use ANSI escape codes to add color to specific parts of your output in the terminal.

#### Example: Coloring `[INFO]` in Green

```bash
echo -e "\e[32m[INFO]\e[0m: generated TOC for $i"
```

#### Breakdown:

- `\e[32m` — sets the text color to green.
- `[INFO]` — the part that gets colored.
- `\e[0m` — resets the color back to default so the rest of the line isn't affected.
- `-e` — enables interpretation of escape sequences in `echo`.

#### Other Color Codes You Can Use:
  
| Color      | Code  |
|------------|-------|
| Black      | `\e[30m` |
| Red        | `\e[31m` |
| Green      | `\e[32m` |
| Yellow     | `\e[33m` |
| Blue       | `\e[34m` |
| Magenta    | `\e[35m` |
| Cyan       | `\e[36m` |
| White      | `\e[37m` |

You can also make it **bold** by adding `\e[1m` before the color code:

```bash
echo -e "\e[1;32m[INFO]\e[0m: generated TOC for $i"
```

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
