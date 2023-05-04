# SYNOPSIS
> **ima** [ -x | --retries-per-sites **NUM** ] [ -q | --more-lines ] [ -k | --no-color ] [ -m | --image-count **NUM** ] [ -a | --auto-name ] [ -p | --no-progress-bar ] [ -r | --retries **NUM** ] [ -l | --image-link **OUTPUT_FORMAT** ] [ -h | --help ] [ -t | --timeout ] [ -w | --overwrite ] [ --version ] [ -n **NUM** ] [ -v | --verbose ] [ -e | --engine **ENGINE** ] [ -i | --ignore-domains **DOMAIN** ] [ -d | --dest-dir **DEST_DIR** ] [ -u | --number-sites **NUM** ] [ -o | --min-score **SCORE** ] [ -s | --search-only ] **QUERY** [..QUERY]

> Mandatory arguments to long options are mandatory for short options too.
> **-u --number-sites** NUM
>> The number of websites to visit from the search results.
> **-d --dest-dir** DEST_DIR
>> Specify the destination directory were downloaded files will be stored, default to the current working directory of the executing program.
> **-s --search-only**
>> Query search engine and output search results only. This option is in conflict with the `-l\' option.
> **-o --min-score** SCORE
>> Define mininum score for images. This option should not be used with the `-s\' option.
> **-e --engine** ENGINE
>> Comma separated list of search engines to use, possible search engines are duckduckgo, google, and yahoo. Engine defaults to "duckduckgo". If more than one search engine is specified, cycle through when connection fails too much.
> **-v --verbose**
>> Print status messages to the standard output.
> **-n** NUM
>> Print NUM results obtained from the `-s\' or `-i\' option or download NUM images when neither of these options were specified.
> **--version**
>> Print program version and exit.
> **-i --ignore-domains** DOMAIN
>> A comma separated list of domains to ignore on search results.
> **-h --help**
>> Print this help text and exit.
> **-r --retries** NUM
>> Number of retries before giving up if any connection fails.
> **-l --image-link** OUTPUT_FORMAT
>> Output image links instead of downloading them. You can use the following specifiers to format output: `{s}\' represents the score of the given image, `{d}\' its description, `{l}\' its url, `{e}\' its file extension and `{w}\' the url from which the image link was extracted e.g: we can for example format our output as such --> "image {l} has score {s}".
> **-p --no-progress-bar**
>> Disable download progress bar.
> **-t --timeout**
>> Set connection timeout.
> **-w --overwrite**
>> Overwrite existing files, This option is in conflict with the `-a\' option.
> **-q --more-lines**
>> Wipe out download progress after download has finished
> **-x --retries-per-sites** NUM
>> Number of retries per sites if any connection fails.
> **-a --auto-name**
>> Auto generate a new file name if a file name already exist in filesystem.
> **-m --image-count** NUM
>> Set NUM as maximum number of image links to be extracted from a website.
> **-k --no-color**
>> Disable ANSI colors

# AUTHORS
> tcheukueppo <tcheukueppo@tutanota.com>

# BUGS

Presumably. Report them or discuss them at:

> https://github.com/tcheukueppo/ima/issues

# COPYRIGHT

> License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>.

