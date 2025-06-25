
# aiobale

**aiobale** is an asynchronous Python framework for building bots on the [Bale Messenger](https://bale.ai), heavily inspired by [aiogram](https://github.com/aiogram/aiogram). It allows developers to write fast and modern bots using Python's `asyncio` features with a clean and intuitive API.

## 🔧 Features

- Fully asynchronous and based on `asyncio`
- Familiar API similar to `aiogram`
- Easy to use and extend
- Designed specifically for the Bale bot API
- Fast and lightweight

## 📦 Installation

```bash
pip install aiobale
````

> Note: This package is under development. Use it with caution in production.

## 🚀 Quick Start

```python
import asyncio
from aiobale import Bot, Dispatcher
from aiobale.types import Message
from aiobale.filters import Command

API_TOKEN = "YOUR_BALE_BOT_TOKEN"

bot = Bot(token=API_TOKEN)
dp = Dispatcher()

@dp.message(Command("start"))
async def start_handler(message: Message):
    await message.reply("سلام! من یک ربات بله هستم :)")

async def main():
    await dp.start_polling(bot)

if __name__ == "__main__":
    asyncio.run(main())
```

## 📚 Documentation

Since **aiobale** is based on the structure and philosophy of [aiogram](https://docs.aiogram.dev), you can refer to the [aiogram documentation](https://docs.aiogram.dev) as a guide for working with aiobale.

> ⚠ Note: While most concepts and patterns are similar, some endpoint names and platform-specific behaviors may differ.

## 🤝 Contributing

Contributions are welcome! If you’ve found a bug or have a feature request, feel free to open an issue or submit a pull request.

## ⚠️ Disclaimer

This project is not affiliated with the official Bale team. Use at your own risk. API compatibility is based on unofficial documentation and reverse engineering.

## 📜 License

This project is licensed under the MIT License.

