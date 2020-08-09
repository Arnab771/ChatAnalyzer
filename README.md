![logo](https://github.com/lev-kusanagi/ChatAnalyzer/blob/master/img/logo/logotype1.png?raw=true)

A JavaScript application to analyze WhatsApp chat history locally in your browser.

## Usage

* Clone the repository `git clone https://github.com/Arnab771/ChatAnalyzer.git`or download the repository
* Open `index.html` in the root folder.
* Follow instructions on the web page.

Alternatively you can use the official [hosted version](https://chatanalyzer.moritzwolf.com) of this code.

## What happens to my chat data?

**No chat data is transferred to any remote server, all analysis is performed locally on your device**

The application works completly offline once the page has loaded. You can turn off your internet before loading your data file if you are particularly concerned. You can also take a look at the source code and give it an audit.

### Add your language identifier for audio/video/pictures

Please see the header of `main.js`. There you can add your identifiers.

### How the data is parsed & how you can build on that

The chat data is parsed via regex and splitted into it's parts. There are two variables that hold the data.

*`structArray`:*
Formatted line data in the form of a struct with the keys: name date time message

- `name`: "Name Surname"
- `date`: "YYYY-MM-DD"
- `time`: "HH:MM:SS"
- `message`: text

each key represents an array, the index represents the line number
e.g. structArray.date[0] is the date of the first line

*`userStruct`:*

Array of structs with the keys:

- `name`: "Name Surname"
- `date`: "YYYY-MM-DD"
- `time`: "HH:MM:SS"
- `message`: text

For every person there is one struct, same format as above, the `index` represents messageNumber of `name`.
