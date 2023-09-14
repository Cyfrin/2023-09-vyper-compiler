# Vyper 0.3.10rc3 Compiler - Competition Details

<img src="https://raw.githubusercontent.com/vyperlang/vyper/master/logo/vyper-logo-transparent.svg?sanitize=true" alt="" width="300">

# Contest Details
- Total Prize Pool: $150,000(+) USDC
  - HM: 95%
  - L: 5%
- Starts: September 14, 2023 
- Ends: November 4th, 2023
- nSLOC: ~14,644

The donation address for prizes is:
- `eth:0x18996AdDe10E9AC12e47e5D6a0F486793fad2c15` (vyper-contest.eth)
- Any EVM Chain: `0xf71d2231bc1309db6419F82afD8157ea858ADd8C`

# Vyper Compiler Walkthrough

- [READ HERE](https://hackmd.io/@pcaversaccio/how-vyper-compiles-into-bytecode)

# About the Contest

## In Scope:
- Everything in ./vyper (~15,000 nSLOC)
- Vyper Commit Hash:
  - `3b310d5` 
  - Aka the [0.3.10rc3](https://github.com/vyperlang/vyper/releases/tag/v0.3.10rc3)
    - _All the code for this commit is also located in this repo_


## Out of scope:
- Anything outside `./vyper` folder
- Any issue in the repo labeled "bug" is a known bug, and any issue merged or closed from past versions of vyper is a known bug, and does not qualify. 
- EVM version related bugs. For example, the following finding would not qualify: 
```
Vyper 0.3.9 defaults to shanghai which adds the PUSH0 opcode and which is not yet supported on many chains like Optimism. This can lead to dangerous creation and runtime failures.
```

## Known Issues

You can see the list of [known issues here.](https://github.com/Cyfrin/2023-09-vyper-compiler/issues/1)

## Judging

Due to the sensitivity of the contest, judging for this contest will be private, and conducted by the Cyfrin team, VSA (Vyper Security Alliance), and the contest will likely involve additional external participants. 

## Scoring:
For this contest, we are looking exclusively for Highs & Mediums. There will be no Informational / QA prize pool. 
- H/M - 95%
- L - 5%
  
You can check the total prize pool here: [0x18996AdDe10E9AC12e47e5D6a0F486793fad2c15](https://etherscan.io/address/0x18996AdDe10E9AC12e47e5D6a0F486793fad2c15)

## Severity Rating

We will use the matrix in the CodeHawks documentation to decide severity, but here are some examples.

## Severity Rating Examples 

### High 
- High Impact: Reentrancy locks are in the wrong storage slot
- High Likelihood: Always 

### Medium
- High Impact: Compiler puts reentrancy lock at the wrong spot 
- Low Likelihood: Only when the contract address starts with 0x0000, your codebase is exactly 4,567 lines long, and has a very specific function name. 

### Low
- Low Impact: An extra `INVALID` Opcode is added at the end of metadata
- Low Likelihood: If the first text in the codebase is "snek snek snek snek is king" 

## Invited Hawk

This is our first contest that will include a paid "Invited Hawk". We are excited to welcome [obront.eth](https://twitter.com/zachobront) to this contest! He will be paid an additional flat fee from outside the prize pool. 

## Additional context:
- The codegen and optimizer sections are critical because it creates/modifies the output EVM code, so if you're looking for Highs, that's likely where you'll find them.
- It's likely that if the compiler produces EVM opcodes/bytecode that is not correct, it could be considered a H/M even if it's not apparent. So please submit your lows. 

We will be working closely with the Vyper Security Alliance on submissions. 

# Sponsors 


<br/>
<table>
  <tr>
    <th align="center">Lido</th>
    <th align="center">Yearn</th>
    <th align="center">Curve</th>
  </tr>
  <tr>
  <td align="center">
      <a href="https://lido.fi/">
        <img src="https://raw.githubusercontent.com/Cyfrin/2023-09-vyper-compiler/main/images/lido.png" alt="" width="300">
      </a>
    </td>
    <td align="center">
      <a href="https://yearn.fi/">
        <img src="https://raw.githubusercontent.com/cyfrin/2023-09-vyper-compiler/main/images/yearn-logo.png" alt="" width="300">
      </a>
    </td>
    <td align="center">
      <a href="https://curve.fi/">
      <img src="https://raw.githubusercontent.com/Cyfrin/2023-09-vyper-compiler/main/images/curve.png" alt="" width="300">
    </a>
    </td>
  </tr>
  <tr>
    <th align="center">Cyfrin</th>
    <th align="center">UnoRe</th>
  </tr>
  <tr>
    <td align="center">
      <a href="https://cyfrin.io/">
      <img src="https://raw.githubusercontent.com/cyfrin/2023-09-vyper-compiler/main/images/cyfrin.png" alt="" width="300">
    </a>
    </td>
    <td>
      <a href="https://unore.io/">
      <img src="https://raw.githubusercontent.com/cyfrin/2023-09-vyper-compiler/main/images/unore.png" alt="" width="300">
    </a>
    </td>
  </tr>
</table>
<br/>

--------------------------------------------------------

**Vyper compiler security audit competition starts 14th September with $150k worth of bounties.** [See the competition on CodeHawks](https://www.codehawks.com/contests/cll5rujmw0001js08menkj7hc) and find [more details in this blog post](https://mirror.xyz/0xBA41A04A14aeaEec79e2D694B21ba5Ab610982f1/WTZ3l3MLhTz9P4avq6JqipN5d4HJNiUY-d8zT0pfmXg).

<img src="https://raw.githubusercontent.com/vyperlang/vyper/master/logo/vyper-logo-transparent.svg?sanitize=true" alt="" width="110">

[![Build Status](https://github.com/vyperlang/vyper/workflows/Test/badge.svg)](https://github.com/vyperlang/vyper/actions/workflows/test.yml)
[![Documentation Status](https://readthedocs.org/projects/vyper/badge/?version=latest)](http://vyper.readthedocs.io/en/latest/?badge=latest "ReadTheDocs")
[![Discord](https://img.shields.io/discord/969926564286459934.svg?label=%23vyper)](https://discord.gg/6tw7PTM7C2)

[![PyPI](https://badge.fury.io/py/vyper.svg)](https://pypi.org/project/vyper "PyPI")
[![Docker](https://img.shields.io/docker/cloud/build/vyperlang/vyper)](https://hub.docker.com/r/vyperlang/vyper "DockerHub")

[![Coverage Status](https://codecov.io/gh/vyperlang/vyper/branch/master/graph/badge.svg)](https://codecov.io/gh/vyperlang/vyper "Codecov")
[![Language grade: Python](https://github.com/vyperlang/vyper/workflows/CodeQL/badge.svg)](https://github.com/vyperlang/vyper/actions/workflows/codeql.yml)

# Getting Started
See [Installing Vyper](http://vyper.readthedocs.io/en/latest/installing-vyper.html) to install vyper.
See [Tools and Resources](https://github.com/vyperlang/vyper/wiki/Vyper-tools-and-resources) for an additional list of framework and tools with vyper support.
See [Documentation](http://vyper.readthedocs.io/en/latest/index.html) for the documentation and overall design goals of the Vyper language.

See [Learn.Vyperlang.org](https://learn.vyperlang.org/) for **learning Vyper by building a Pokémon game**.
See [try.vyperlang.org](https://try.vyperlang.org/) to use Vyper in a hosted jupyter environment!

**Note: Vyper is beta software, use with care**

# Installation
See the [Vyper documentation](https://vyper.readthedocs.io/en/latest/installing-vyper.html)
for build instructions.

# Compiling a contract
To compile a contract, use:
```bash
vyper your_file_name.vy
```
***generate bytecode***

    vyper -f bytecode file-name.vy > file-name.bin

***generate abi***

    vyper -f abi file-name.vy > file-name.abi

There is also an [online compiler](https://vyper.online/) available you can use to experiment with
the language and compile to ``bytecode`` and/or ``IR``.

**Note: While the vyper version of the online compiler is updated on a regular basis it might
be a bit behind the latest version found in the master branch of this repository.**

## Testing (using pytest)

(Complete [installation steps](https://vyper.readthedocs.io/en/latest/installing-vyper.html) first.)

```bash
make dev-init
python setup.py test
```

# Contributing
* See Issues tab, and feel free to submit your own issues
* Add PRs if you discover a solution to an existing issue
* For further discussions and questions, post in [Discussions](https://github.com/vyperlang/vyper/discussions) or talk to us on [Discord](https://discord.gg/6tw7PTM7C2)
* For more information, see [Contributing](http://vyper.readthedocs.io/en/latest/contributing.html)
