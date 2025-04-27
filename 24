#!/usr/bin/env python3

import os
import random
import string
import time

# 生成随机字符串
def generate_random_string(length=100):
    return ''.join(random.choices(string.ascii_letters + string.digits, k=length))

# 显示横幅
def display_banner():
    print("欢迎使用文件生成、编辑、删除脚本！")
    print("此脚本将会在循环中创建、编辑和删除文件。")
    print("-" * 50)

# 创建、编辑、删除文件
def create_edit_delete_file():
    folder_name = "24 7 file"
    os.makedirs(folder_name, exist_ok=True)

    while True:
        try:
            # 生成一个随机文件名
            file_name = os.path.join(folder_name, f"{generate_random_string(8)}.txt")

            # 创建文件并写入内容
            with open(file_name, "w") as file:
                for _ in range(random.randint(10, 100)):
                    file.write(generate_random_string(100) + "\n")
            print(f"Created: {file_name}")

            time.sleep(2)

            # 编辑文件（重写内容）
            with open(file_name, "w") as file:
                for _ in range(random.randint(10, 100)):
                    file.write(generate_random_string(100) + "\n")
            print(f"Edited: {file_name}")

            time.sleep(1)

            # 删除文件
            os.remove(file_name)
            print(f"Deleted: {file_name}")

            time.sleep(1)

        except Exception as e:
            print(f"An error occurred: {e}")
            time.sleep(5)

if __name__ == "__main__":
    # 显示横幅
    display_banner()
    # 执行创建、编辑、删除文件的任务
    create_edit_delete_file()
