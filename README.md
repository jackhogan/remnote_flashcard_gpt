# remnote_flashcard_gpt
Automatically generate a RemNote flashcard from highlighted text in any app using OpenAI's GPT-3.

## Setup

1. **Dependencies**: Make sure you have Python 3.x and the OpenAI Python client installed. Install the latter with pip: `pip install openai`.

2. **Clone**: Clone this repository to your local machine. 

3. **API Key**: Sign up at OpenAI and get your API key. Store this in `.env`.

## Usage

1. **Automator**: Open Automator App on Mac and import the `.workflow` file included in the repo.

2. **Python script**: Make sure the Python script in Automator points to the python script `flashcard.py` in this repo. Modify the path to your python version if necessary.

3. **Selected text**: Once Automator Service is saved, you should be able to see it in the right-click menu under `Services` when you select any text in any application.

## How It Works

The Automator Service uses AppleScript to fetch the selected text, which is then passed to a Python script. The Python script uses the OpenAI API to generate a suggested flashcard question/answer pair. The response is then passed back to AppleScript, which inputs the flashcard into Remnote using system events.

All the Python logic, including calling the OpenAI API and parsing the response, is in `flashcard.py`.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)
