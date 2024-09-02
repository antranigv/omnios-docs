# OmniOS Handbook

> Currently running on [docs.omnios.illumos.am](https://docs.omnios.illumos.am)

The OmniOS Handbook project aims to provide comprehensive, up-to-date, and easily accessible documentation for the OmniOS Community Edition (OmniOSce).

The goal is to support new users and system administrators by providing clear guidance, tutorials, and reference materials.

## Running

To run the documentation locally, follow these steps:

1. Clone the Repository:  
   ```
   git clone https://github.com/antranigv/omnios-docs.git
   cd omnios-docs
   git submodule update --init --recursive
   ```
2. Install Hugo: If you do not have Hugo installed, follow the instructions on the Hugo website to install it for your platform.
3. Run the Hugo Server:
   ```
   hugo server
   ```
   This command will start a local server. You may navigate to http://localhost:1313.
4. Contribute: If you wish to contribute to the Handbook, please fork the repository, make your changes, and submit a Pull Request (PR) for review.

## Acknowledgements

- The FreeBSD Project's FreeBSD Handbook
- The OmniOS maintainers and developers
- The illumos community
