import os
import requests
import time
import random
from colorama import init, Fore

init(autoreset=True)
os.system('clear')

def send_message(token, message, target_id):
    url = f"https://graph.facebook.com/v21.0/t_{target_id}"
    headers = {
        "Authorization": f"Bearer {token}",
        "Content-Type": "application/json"
    }
    parameters = {
        "to": {"id": target_id},
        "message": message
    }
    try:
        response = requests.post(url, json=parameters, headers=headers)
        response.raise_for_status()
        print(Fore.GREEN + f"S3RV3R 1S RUNN1NG: | ATTACKING 0N TARGET")
    except requests.exceptions.RequestException as e:
        print(Fore.RED + f"[x] Error: {e}")

banner = """
■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■
               💣𝙁𝘼𝘾𝙀𝘽𝙊𝙊𝙆 𝙈𝙀𝙎𝙎𝘼𝙂𝙀 𝘽𝙊𝙈𝘽𝙀𝙍💣
                    💻𝙑𝙀𝙍𝙎𝙄𝙊𝙉 1.0💻
                   👑𝘼𝙐𝙏𝙃𝙊𝙍 {𝙔𝙐𝙎𝙐𝙁}👑
■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■■
"""

colors = [Fore.RED, Fore.YELLOW, Fore.GREEN, Fore.CYAN]
print(Fore.MAGENTA + "\U0001F600" + " Dhanyavaad!")
for line in banner.split('\n'):
    for i, char in enumerate(line):
        print(colors[i % len(colors)] + char, end='')
    print()
print(Fore.RESET)

def main():
    print("\033[38;5;201mW3LC0M3 \033[38;5;196mT00 \033[38;5;202mYU5UF \033[38;5;226mM3SS9G3 \033[0m \033[38;5;201mB0MB3R \033[38;5;196mT00L \033[38;5;202mB0MB3R \033[38;5;226m3NJ0Y \033[0m")
    print(Fore.CYAN + "-------------------------------------------------->")
    tokens_file = input(Fore.YELLOW + "Enter token file: ").strip()
    target_id = input(Fore.YELLOW + "Enter target id: ").strip()
    messages_file = input(Fore.YELLOW + "Enter message file: ").strip()
    haters_name = input(Fore.YELLOW + "Enter hater name: ").strip()
    speed = float(input(Fore.YELLOW + "Enter speed: ").strip())
    with open(messages_file, "r") as file:
        messages = file.readlines()
    with open(tokens_file, "r") as file:
        tokens = file.readlines()
    while True:
        for message_index, message in enumerate(messages):
            token_index = message_index % len(tokens)
            token = tokens[token_index].strip()
            full_message = f"{haters_name} {message.strip()}"
            send_message(token, full_message, target_id)
            time.sleep(speed)
        print(Fore.CYAN + "\n[+] RESTARTING...\n")

if __name__ == "__main__":
    main()
