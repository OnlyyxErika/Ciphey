Fully automated decryption/decoding/cracking tool using natural language processing & artificial intelligence, along with some common sense.

<hr>

## [Installation Guide](https://github.com/Ciphey/Ciphey/wiki/Installation)

| <p align="center"><a href="https://pypi.org/project/ciphey">🐍 Python                                          | <p align="center"><a href="https://hub.docker.com/r/remnux/ciphey">🐋 Docker (Universal)                       | <p align="center"><a href="https://ports.macports.org/port/ciphey/summary">🍎 MacPorts (macOS)                   | <p align="center"><a href="https://formulae.brew.sh/formula/ciphey">🍺 Homebrew (macOS/Linux)                    |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| <p align="center"><img src="https://github.com/Ciphey/Ciphey/raw/master/Pictures_for_README/python.png" /></p> | <p align="center"><img src="https://github.com/Ciphey/Ciphey/raw/master/Pictures_for_README/docker.png" /></p> | <p align="center"><img src="https://github.com/Ciphey/Ciphey/raw/master/Pictures_for_README/macports.png" /></p> | <p align="center"><img src="https://github.com/Ciphey/Ciphey/raw/master/Pictures_for_README/homebrew.png" /></p> |
| `python3 -m pip install ciphey --upgrade`                                                                      | `docker run -it --rm remnux/ciphey`                                                                            | `sudo port install ciphey`                                                                                       | `brew install ciphey`                                                                                            |

| Linux                                                                                                                   | Mac OS                                                                                                                     | Windows                                                                                                                   |
| ----------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------- |
| ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/ciphey/ciphey/Python%20application?label=Linux) | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/ciphey/ciphey/Python%20application?label=Mac%20OS) | ![GitHub Workflow Status](https://img.shields.io/github/workflow/status/ciphey/ciphey/Python%20application?label=Windows) |

<hr>

# 🤔 What is this?

Input encrypted text, get the decrypted text back.

> "What type of encryption?"

That's the point. You don't know, you just know it's possibly encrypted. Ciphey will figure it out for you.

Ciphey can solve most things in 3 seconds or less.

<p align="center" href="https://asciinema.org/a/336257">
  <img src="https://github.com/Ciphey/Ciphey/raw/master/Pictures_for_README/index.gif" alt="Ciphey demo">
</p>

Ciphey aims to be a tool to automate a lot of decryptions & decodings such as multiple base encodings, classical ciphers, hashes or more advanced cryptography.

If you don't know much about cryptography, or you want to quickly check the ciphertext before working on it yourself, Ciphey is for you.

**The technical part.** Ciphey uses a custom built artificial intelligence module (_AuSearch_) with a _Cipher Detection Interface_ to approximate what something is encrypted with. And then a custom-built, customisable natural language processing _Language Checker Interface_, which can detect when the given text becomes plaintext.

No neural networks or bloated AI here. We only use what is fast and minimal.

And that's just the tip of the iceberg. For the full technical explanation, check out our [documentation](https://github.com/Ciphey/Ciphey/wiki).

# ✨ Features

- **50+ encryptions/encodings supported** such as binary, Morse code and Base64. Classical ciphers like the Caesar cipher, Affine cipher and the Vigenere cipher. Along with modern encryption like repeating-key XOR and more. **[For the full list, click here](https://github.com/Ciphey/Ciphey/wiki/Supported-Ciphers)**
- **Custom Built Artificial Intelligence with Augmented Search (AuSearch) for answering the question "what encryption was used?"** Resulting in decryptions taking less than 3 seconds.
- **Custom built natural language processing module** Ciphey can determine whether something is plaintext or not. Whether that plaintext is JSON, a CTF flag, or English, Ciphey can get it in a couple of milliseconds.
- **Multi Language Support** at present, only German & English (with AU, UK, CAN, USA variants).
- **Supports encryptions and hashes** Which the alternatives such as CyberChef Magic do not.
- **[C++ core](https://github.com/Ciphey/CipheyCore)** Blazingly fast.

# 🔭 Ciphey vs CyberChef

## 🔁 Base64 Encoded 42 times

<table>
  <tr>
  <th>Name</th>
    <th>⚡ Ciphey ⚡ </th>
    <th>🐢 CyberChef 🐢</th>
  </tr>
  <tr>
  <th>Gif</th>
    <td><img src="https://github.com/Ciphey/Ciphey/raw/master/Pictures_for_README/ciphey_gooder_cyberchef.gif" alt="The guy she tells you not to worry about"></td>
    <td><img src="https://github.com/Ciphey/Ciphey/raw/master/Pictures_for_README/not_dying.gif" alt="You"></td>
  </tr>
  <tr>
  <th>Time</th>
    <td>2 seconds</td>
    <td>6 seconds</td>
  </tr>
    <tr>
  <th>Setup</th>
    <td><ul><li>Run ciphey on the file</li></ul></td>
    <td><ul><li>Set the regex param to "{"</li><li>You need to know how many times to recurse</li><li>You need to know it's Base64 all the way down</li><li>You need to load CyberChef (it's a bloated JS app)</li><li>Know enough about CyberChef to create this pipeline</li><li>Invert the match</li></ul></td>
  </tr>
</table>

<sub><b>Note</b> The gifs may load at different times, so one may appear significantly faster than another.</sub><br>
<sub><b>A note on magic </b>CyberChef's most similar feature to Ciphey is Magic. Magic fails instantly on this input and crashes. The only way we could force CyberChef to compete was to manually define it.</sub>

We also tested CyberChef and Ciphey with a **6gb file**. Ciphey cracked it in **5 minutes and 54 seconds**. CyberChef crashed before it even started.

## 📊 Ciphey vs Katana vs CyberChef Magic

| **Name**                                   | ⚡ Ciphey ⚡ | 🗡️ Katana 🗡️ | 🐢 CyberChef Magic 🐢 |
| ------------------------------------------ | ------------ | ------------ | --------------------- |
| Advanced Language Checker                  | ✅           | ❌           | ✅                    |
| Supports Encryptions                       | ✅           | ✅           | ❌                    |
| Releases named after Dystopian themes 🌃   | ✅           | ❌           | ❌                    |
| Supports hashes                            | ✅           | ✅           | ❌                    |
| Easy to set up                             | ✅           | ❌           | ✅                    |
| Can guess what something is encrypted with | ✅           | ❌           | ❌                    |
| Created for hackers by hackers             | ✅           | ✅           | ❌                    |

# 🎬 Getting Started

## ‼️ Important Links (Docs, Installation guide, Discord Support)

| Installation Guide                                                          | Documentation                                             | Discord                                     | Docker Image (from REMnux)                                                                          |
| --------------------------------------------------------------------------- | --------------------------------------------------------- | ------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| 📖 [Installation Guide](https://github.com/Ciphey/Ciphey/wiki/Installation) | 📚 [Documentation](https://github.com/Ciphey/Ciphey/wiki) | 🦜 [Discord](https://discord.gg/zYTM3rZM4T) | 🐋 [Docker Documentation](https://docs.remnux.org/run-tools-in-containers/remnux-containers#ciphey) |

## 🏃‍♀️Running Ciphey

There are 3 ways to run Ciphey.

1. File Input `ciphey -f encrypted.txt`
2. Unqualified input `ciphey -- "Encrypted input"`
3. Normal way `ciphey -t "Encrypted input"`

![Gif showing 3 ways to run Ciphey](https://github.com/Ciphey/Ciphey/raw/master/Pictures_for_README/3ways.gif)

To get rid of the progress bars, probability table, and all the noise use the quiet mode.

`ciphey -t "encrypted text here" -q`

For a full list of arguments, run `ciphey --help`.

### ⚗️ Importing Ciphey

You can import Ciphey\'s main and use it in your own programs and code. `from Ciphey.__main__ import main`

---

## Contributors

Thanks to everyone who contributed to Ciphey. This project follows the all-contributors specification, to recognize all contributions to the project.

<!-- ALL-CONTRIBUTORS-BADGE:START -->

[![All Contributors](https://img.shields.io/badge/all_contributors-1-orange.svg?style=flat-square)](#contributors-)

<!-- ALL-CONTRIBUTORS-BADGE:END -->

<!-- ALL-CONTRIBUTORS-LIST:START -->
<!-- prettier-ignore-start -->
<table>
  <tr>  
    <td align="center"><a href="https://github.com/TechieGbemi"><img src="https://github.com/TechieGbemi.png" width="100px;" alt="TechieGbemi"/><br /><sub><b>TechieGbemi</b></sub></a><br /><a href="#contributors-code" title="Code">Python Programmer</a></td>
  </tr>
</table>
<!-- ALL-CONTRIBUTORS-LIST:END -->
