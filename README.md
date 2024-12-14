<a name="readme-top"></a>

<br />
<div align="center">

  [![Discussions][discussions-shield]][discussions-url]
  [![Contributors][contributors-shield]][contributors-url]
  [![Forks][forks-shield]][forks-url]
  [![MIT + Apache-2.0 License][license-shield]][license-url]

  <h2 align="center">me<sup>3</sup></h2>

  <p align="center">
    A framework for modifying and instrumenting games.
    <br />
    <a href="https://garyttierney.github.io/me3/me3_framework/"><strong>Explore the docs »</strong></a>
    <br />
    <br />
    <a href="https://github.com/garyttierney/me3/discussions/categories/bug-reports">Report Bug</a>
    ·
    <a href="https://github.com/garyttierney/me3/discussions/categories/ideas">Request Feature</a>
  </p>
</div>

- [About The Project](#about-the-project)
  - [Built With](#built-with)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgments](#acknowledgments)

<!-- ABOUT THE PROJECT -->
## About The Project

TODO: write me

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

* [Rust](https://rust-lang.org/)
* Many others...

<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- GETTING STARTED -->
## Getting Started

me3 is a launcher and mod loader for the Dark Souls series of games from FROMSOFTWARE and similar titles.

### Prerequisites

* Cargo
  - Windows: download and run [rustup‑init.exe][rustup-installer] then follow the onscreen instructions.
  - Linux:
    ```bash
    curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
    ```
* Visual Studio C++ Build Tools
  - Windows: download and run [vs_BuildTools.exe][buildtools-installer] then follow the onscreen instructions.
  - Linux: while me3 can be built against mingw64, this generally isn't recommended. Instead acquire the Windows SDK using `xwin`
    ```bash
    cargo install xwin && xwin --accept-license splat --output ~/.xwin
    ```
    And configure Cargo to link with LLD and use the binaries from xwin in `~/.cargo/config.toml`
    ```toml
    [target.x86_64-pc-windows-msvc]
    linker = "lld"
    runner = "wine"
    rustflags = [
    "-Lnative=/home/gtierney/.xwin/crt/lib/x86_64",
    "-Lnative=/home/gtierney/.xwin/sdk/lib/um/x86_64",
    "-Lnative=/home/gtierney/.xwin/sdk/lib/ucrt/x86_64"
    ]
    ```
### Usage

1. Clone the repo
   ```sh
   git clone https://github.com/garyttierney/me3.git
   ```
2. Build the binaries
   ```sh
   cargo build [--release]
   ```
3. Attach the sample host DLL to your game
   ```sh
   TODO: fix these instructions.
   ```
<p align="right">(<a href="#readme-top">back to top</a>)</p>


<!-- CONTRIBUTING -->
## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md)

<!-- LICENSE -->
## License

Distributed under either the Apache Software License 2.0 or MIT License. See LICENSE-APACHE and LICENSE-MIT for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->
## Contact

Project Link: [https://github.com/garyttierney/me3](https://github.com/garyttierney/me3)

Discussions Board: [https://github.com/garyttierney/me3/discussions](https://github.com/garyttierney/me3/discussions)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

* [Mod Engine](https://github.com/katalash/ModEngine/tree/master/DS3ModEngine) - prior art for runtime modification of FROMSOFTWARE games.
* [Mod Organizer 2](https://github.com/ModOrganizer2/modorganizer/) - inspiration for the VFS framework.
* [Elden Ring Reforged](https://www.nexusmods.com/eldenring/mods/541) - provided invaluable feedback on the end-user perspective

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[buildtools-installer]: https://aka.ms/vs/17/release/vs_BuildTools.exe
[discussions-shield]: https://img.shields.io/github/discussions/garyttierney/me3
[discussions-url]: https://github.com/garyttierney/me3/discussions
[contributors-shield]: https://img.shields.io/github/contributors/garyttierney/me3.svg?style=flat
[contributors-url]: https://github.com/garyttierney/me3/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/garyttierney/me3.svg?style=flat
[forks-url]: https://github.com/garyttierney/me3/network/members
[stars-shield]: https://img.shields.io/github/stars/garyttierney/me3.svg?style=flat
[stars-url]: https://github.com/garyttierney/me3/stargazers
[issues-shield]: https://img.shields.io/github/issues/garyttierney/me3.svg?style=flat
[issues-url]: https://github.com/garyttierney/me3/issues
[license-shield]: https://img.shields.io/badge/license-MIT%2FApache--2.0-green?style=flat
[license-url]: https://github.com/garyttierney/me3/blob/master/LICENSE.txt
