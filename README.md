[![Docs][docs-shield]][docs-url]
[![NPM][npm-shield]][npm-url]
[![CI][ci-shield]][ci-url]
[![Issues][issues-shield]][issues-url]
[![MIT License][license-shield]][license-url]
[![Coverage][coverage-shield]][coverage-url]
<!-- OTHER BADGES -->
<!-- [![Contributors][contributors-shield]][contributors-url] -->
<!-- [![Forks][forks-shield]][forks-url] -->
<!-- [![Stargazers][stars-shield]][stars-url] -->

<!-- ANNOUNCEMENT -->

> **📢 Version 4.x introduces several breaking changes. [Please refer to the documentation for more details.](https://chiru-labs.github.io/ERC721A/#/migration)**

_We highly recommend reading the migration guide_, **especially** _the part on [`supportsInterface`](https://chiru-labs.github.io/ERC721A/#/migration?id=supportsinterface) if you are using with OpenZeppelin extensions_ (e.g. ERC2981).

<!-- ABOUT THE PROJECT -->

## About The Project

The goal of ERC721A is to provide a fully compliant implementation of IERC721 with significant gas savings for minting multiple NFTs in a single transaction. This project and implementation will be updated regularly and will continue to stay up to date with best practices.

The [Azuki](https://twitter.com/AzukiOfficial) team created ERC721A for its sale on 1/12/22. There was significant demand for 8700 tokens made available to the public, and all were minted within minutes. The network BASEFEE remained low despite huge demand, resulting in low gas costs for minters, while minimizing network disruption for the wider ecosystem as well.

![Gas Savings](https://pbs.twimg.com/media/FIdILKpVQAEQ_5U?format=jpg&name=medium)

For more information on how ERC721A works under the hood, please visit our [blog](https://www.azuki.com/erc721a). To find other projects that are using ERC721A, please visit [erc721a.org](https://www.erc721a.org) and our [curated projects list](https://github.com/chiru-labs/ERC721A/blob/main/projects.md).


<!-- Installation -->

## Installation

```sh

npm install --save-dev erc721a

```

<!-- USAGE EXAMPLES -->

## Usage

Once installed, you can use the contracts in the library by importing them:

```solidity
pragma solidity ^0.8.4;

import "erc721a/contracts/ERC721A.sol";

contract Azuki is ERC721A {
    constructor() ERC721A("Azuki", "AZUKI") {}

    function mint(uint256 quantity) external payable {
        // `_mint`'s second argument now takes in a `quantity`, not a `tokenId`.
        _mint(msg.sender, quantity);
    }
}

```

<!-- ROADMAP -->

## Roadmap

- [ ] Improve general repo and code quality (workflows, comments, etc.)
- [ ] Add more documentation on benefits of using ERC721A
- [ ] Maintain full test coverage

See the [open issues](https://github.com/chiru-labs/ERC721A/issues) for a full list of proposed features (and known issues).

<!-- CONTRIBUTING -->

## Contributing

Contributions are what make the open source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.

If you have a suggestion that would make this better, please fork the repo and create a pull request. You can also simply open an issue with the tag "enhancement".

Don't forget to give the project a star! Thanks again!

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

<!-- ROADMAP -->

### Running tests locally

1. `npm install`
2. `npm run test`


