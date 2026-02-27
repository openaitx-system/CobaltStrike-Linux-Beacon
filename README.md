
<div align="right">
  <details>
    <summary >🌐 Language</summary>
    <div>
      <div align="center">
        <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=en">English</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=zh-CN">简体中文</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=zh-TW">繁體中文</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=ja">日本語</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=ko">한국어</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=hi">हिन्दी</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=th">ไทย</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=fr">Français</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=de">Deutsch</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=es">Español</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=it">Italiano</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=ru">Русский</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=pt">Português</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=nl">Nederlands</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=pl">Polski</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=ar">العربية</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=fa">فارسی</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=tr">Türkçe</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=vi">Tiếng Việt</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=id">Bahasa Indonesia</a>
        | <a href="https://openaitx.github.io/view.html?user=EricEsquivel&project=CobaltStrike-Linux-Beacon&lang=as">অসমীয়া</
      </div>
    </div>
  </details>
</div>

# Cobalt Strike Linux Beacon

A proof-of-concept custom Linux Beacon written in C that communicates with the Cobalt Strike teamserver using the HTTP/S protocol.

The goal of this project isn't to be a fully featured implant, nor is it limited to just Linux. It is to show that it is possible to make custom implants for Cobalt Strike for any platform. The only requirement is communicating with the teamserver correctly.

With custom implants you can define custom behavior, add new features, support different platforms and file types, apply obfuscation at compile time, and more. The possibilities are endless.

Hopefully one day Cobalt Strike will officially support developing custom Beacons by adding more documentation and quality of life features.


## Features
- HTTP/S listener support (default C2 profile)
- Contains some built-in commands: `sleep`, `cd`, `pwd`, `shell`, `ls`, `exit`, `upload`, `download`
- Linux BOF execution using TrustedSec's ELFLoader. Supports both TrustedSec & Outflank BOFs
- SOCKS proxy

## Demo
Generating payloads with the Aggressor Script
![Linux Beacon Payload Generation](demo/generate_payloads.gif)

Running commands & BOFs in the Linux Beacon
![Linux Beacon Commands Demo](demo/commands.gif)

## Setup
You can view the setup steps in the [SETUP](SETUP.md) file.

## Special Thanks
Thank you to [Kyle Avery](https://x.com/kyleavery) for your help with integrating BOF execution and testing out the implant.

## Future goals
* Add support for custom C2 profiles
* Add TCP listener + connect functionality
* Continue fixing bugs

## Resources
- Cobalt Strike (wow!)
- [TrustedSec's ELFLoader & BOFs](https://github.com/trustedsec/ELFLoader)
- [Outflank's BOFs](https://github.com/outflanknl/nix_bof_template)
- [PaloAltoNetworks Unit42](https://unit42.paloaltonetworks.com/cobalt-strike-metadata-encryption-decryption/)
- [SANS ISC](https://isc.sans.edu/diary/27968)
- [cs-decrypt-metadata-py](https://blog.didierstevens.com/2021/10/22/new-tool-cs-decrypt-metadata-py/)
- [SentinelOne CobaltStrikeParser](https://github.com/Sentinel-One/CobaltStrikeParser)