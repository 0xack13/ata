# ata

Ask the Terminal Anything (ATA): OpenAI GPT in the terminal.

At the time of writing, you can use `text-davinci-003`, which is similar to ChatGPT and gives less verbose answers.

[![asciicast](https://asciinema.org/a/557270.svg)](https://asciinema.org/a/557270)

## Productivity benefits

- The terminal starts more quickly and requires **less resources** than a browser.
- A terminal can be set to **run in the background and show/hide with one keypress**. To do this, use iTerm2 (Mac), Guake (Ubuntu), or scratchpad (i3), or the quake mode for Windows Terminal.
- The **keyboard shortcuts** allow for quick interaction with the query. For example, press `CTRL + c` to cancel the stream, `CTRL + ↑` to get the previous query again, and `CTRL + w` to remove the last word.
- The prompts are **reproducible** because each prompt is sent as a stand-alone prompt without history. Tweaking the prompt can be done by pressing `CTRL + ↑` and making changes.

## Usage

Download the binary for your system from [Releases](https://github.com/rikhuijzer/ata/releases).

Request an API key via <https://beta.openai.com/account/api-keys>.
Next, set the API key, the model that you want to use, and the maximum amount of tokens that the server can respond with in `ata.toml`:

```toml
api_key = "<YOUR SECRET API KEY>"
model = "text-davinci-003"
max_tokens = 500
temperature = 0
```

and run:

```sh
$ ata --config=ata.toml
```

Or, change the current directory to the one where `ata.toml` is located and run

```sh
$ ata
```

For more information, see:

```sh
$ ata --help
```

## FAQ

**How much will I have to pay for the API?**

Using OpenAI's API is quite cheap, I have been using this terminal application heavily for a few weeks now and my costs are about $0.15 per day ($4.50 per month).
The first $18.00 for free, so you can use it for about 120 days (4 months) before having to pay.
