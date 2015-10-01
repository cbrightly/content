# content
Text content for nautilus (markdown)

## Wiki: How to edit

add any section you want to see on the website in the wiki folder.

Use only underscore in the filename and end it with the language suffix: ```my_file_en.md```

Once ready, add it to the ```wiki.json```:
```javascript
  {
    "title": "My Title", // the title which will appear on the wiki menu - KEEP IT SHORT
    "slug": "my_file", // the filename without the language suffix
    "languages": ["en"], // list of all the available languages - only english for now
    "subtitles": [
      "What is it about ?",
      "How is it useful ?",
      "Hum, what else ?"
    ], // the subtitles are the questions visible on the wiki menu
    "not_live": true // default to false - use only if you want to remove this section from the website
  }
```

### Available Classes:

#### header h1 (#):
The file must start with an h1. This give a large blue underlined title
Please use only one per file!

#### headers h2 (##) , h3 (###):
Use as many as you'd like to separate you sections

#### paragraph p:
Just plain text

IMPORTANT: hashtags for headers must be followed/preceded by a blank space, otherwise the compile won't recognize it:
```## My Awesome Subtitle ##```

## License

Except where otherwise noted, content on this site is licensed under a Creative Commons Attribution 4.0 International license.
See License.md for more infos
