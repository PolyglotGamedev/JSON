# JSON
JSON language definition files

Export from 1.0.0 master sheet September 2015

# FILE NAME STRUCTURE
Every JSON file has the following file name structure:

Polyglot-$version_$language[_$anotherLanguage].json

- POLYGLOT is the name of the project
- VERSION is the version string (3 digits, no point or comma), e.g. "100"
- LANGUAGE is the ISO-639-1 language code (lower case) and the regional code (upper case), e.g. "enUS"

Version has a "-" (minus) in front, and all languages are separated by "_" (underscores) for easy string explosion.

# INTERNAL JSON STRUCTURE
Every JSON language file has the following structure:

<pre>{
    "resources": {
        "polyglot": {
            "LANG": $langstring,
            "DIRECTION": $direction,
            "VERSION": $version,
            "DATE": $date
        },
        "data": [
            {
                "n": $idString,
                "s": $translation
            },
            ...
        ]
    }
}</pre>

Explanation:
- "resources" root element
- "polyglot" info tag & attributes: $langstring (e.g. "German"), $direction ("ltr"/"rtl"), $version (e.g. "100"), $date (e.g. "2015-09-26")
- "data" block with subsections containing "n": $idString and "s": $translation pairs from the Polyglot database
