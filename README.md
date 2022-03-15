# Kaveh
Kaveh is a simple website generator, it aims to generate static html files from markdown files, no databases and bloat-web, just texts.

## Dependencies
Kaveh requires a markdown parser in your `$PATH`, to install it:
```bash
pacman -S discount
```

## Installation
```bash
git clone https://github.com/MahdyMirzade/gip.git
cp Kaveh/Kaveh /usr/bin
Kaveh -v
```
> You may need to run some of these commands with root permissions. (sudo)

## Usage
| Method | Description |
| --- | --- |
| **-i**    | The source directory, where to read markdowns and copy other assets from.     |
| **-o**    | The output directory, where to generate html files and copy other files to.   |
| **-t**    | The template directory, where the `header.html` and `footer.html` is.         |

### Example of usage
Example of `build.sh` and scripting:
```bash
Kaveh -i /var/doc/mahdym.ir -o /var/www/mahdym.ir
```
> Then just run the `build.sh` file, whenever you've updated the `/var/doc/mahdym.ir`'s files.

### Example of output
I've made an example so you can understand what's going on, take a look at the `./src/index.md`, then open the `./out/index.html` in your browser.

## How to edit pre-existing files?
1. Clone this repository and enter it.
2. Edit the files in `src` directory.
3. Write your other documents with `.md` in the end, like: `index.md`.
4. Go back to your parent directory, and generate your website into `./out` using: ```Kaveh -i ./src -o ./out```
