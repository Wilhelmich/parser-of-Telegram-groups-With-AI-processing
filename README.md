# parser-of-Telegram-groups-With-AI-processing

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

python3 mainBot.py



The script is designed to automate the process of fetching, processing, and forwarding messages within the Telegram platform using the Telethon library and OpenAI's API.

Functionality:

1. **Initialization**: The script initializes by setting up the OpenAI API key and configuring the Telethon Telegram client.
2. **Fetching Messages**: Every hour, the script fetches the last 100 messages from a specified Telegram group (`YOUR_GROUP_LINK`).
3. **Message Processing with OpenAI**: It then concatenates these messages and sends them to OpenAI's API. The goal is to summarize and reformat the content based on a given prompt: "Concisely rewrite the main points, start each new point on a new line, and provide an objective opinion at the end".
4. **Forwarding the Processed Message**: Once processed, the script sends the resulting content to another specified Telegram group (`GROUP_ID`).
5. **Error Handling**: The script has mechanisms to handle potential errors. For instance, if the bot isn't part of the group or if the group is private, the script will provide a feedback message.
6. **Repetitive Execution**: The entire process (fetch, process, forward) runs indefinitely every 60 minutes.

In essence, this script acts as a bridge between a Telegram group and OpenAI, summarizing and reformatting group messages on an hourly basis.


