## Description
This conversion script is designed to convert vicuna datasets to a more alpaca-like format.
To be used with the trainer found here: https://github.com/oobabooga/text-generation-webui/wiki/Using-LoRAs#training-a-lora
This was designed to conform to SOME of the format from the conv_vicuna_v1_1 format from the FastChat Github repo (https://github.com/lm-sys/FastChat/blob/main/fastchat/conversation.py) while working within the format of Ooba's Trainer. Some liberties were taken on this format adaptation...

## Note about versions
3 Different versions. Not sure which is best.
* Version A - My original Script - least like Vicuna
* Version B - Somewhere in the middle - Adds `<s>` and `<\s>` but keeps New Lines (`\n`) between Responses
* Version C - As Close to Vicuna 1.1 format as I can - Adds `<s>` and `<\s>` with only a space (` `) between Responses

**Make sure whatever version you pick matches the vicuna-format JSON**

## How to use Script
1. Convert vicuna json to alpaca format with `python vicuna_to_alpacan_format_A.py --input <path_to_vicuna_dataset>`
2. Copy the datasets folder to `text-generation-webui/training/datasets`
3. Copy the formats folder to `text-generation-webui/training/formats`

Still Totally Untested WIP
