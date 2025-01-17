<img src="https://cdn4.iconfinder.com/data/icons/social-media-and-logos-12/32/Logo_telegram_Airplane_Air_plane_paper_airplane-33-256.png" align="right" width="131" />

# TGSessionsConverter

![PyPI](https://img.shields.io/pypi/v/TGSessionsConverter)
![PyPI - License](https://img.shields.io/pypi/l/TGSessionsConverter)

This module is small util for easy converting Telegram sessions to various formats (Telethon, Pyrogram, Tdata)
<hr/>

## Installation

```
$ git clone https://github.com/frymex/TGConvertor
$ cd TGConvertor & python setup.py install
```

## Quickstart

```python

from pathlib import Path
from TGConvertor import SessionManager

API_ID = 123
API_HASH = "Your API HASH"


def main():
    session = SessionManager.from_tdata_folder(Path("TDATA/tdata"))
    string_session = session.to_pyrogram_string()
    print(string_session)


if __name__ == "__main__":
    main()
```

### How it works

> An authorization session consists of an authorization key and some additional data required to connect. The module
> simply extracts this data and creates an instance of TelegramSession based on it, the methods of which are convenient to
> use to convert to the format you need.

