# Fieldrider &nbsp; [![bluebuild build badge](https://github.com/wachkyri/fieldrider/actions/workflows/build.yml/badge.svg)](https://github.com/wachkyri/fieldrider/actions/workflows/build.yml)

Welcome to **Fieldrider**, a project designed to simplify the management of immutable operating system images. This repository provides a framework for creating and managing custom images using the BlueBuild system. 

For quick setup instructions to create your own repository based on this template, refer to the [BlueBuild docs](https://blue-build.org/how-to/setup/). After setting up, remember to update this README to reflect your custom image details.

## Installation

> **Note:** This is an experimental feature. Proceed with caution.

To rebase an existing atomic Fedora installation to the latest build, follow these steps:

1. **Rebase to the Unsigned Image**  
   First, rebase to the unsigned image to obtain the proper signing keys and policies:
   ```bash
   rpm-ostree rebase ostree-unverified-registry:ghcr.io/wachkyri/fieldrider:latest
   ```

2. **Reboot**  
   After the rebase, reboot your system to complete the process:
   ```bash
   systemctl reboot
   ```

3. **Rebase to the Signed Image**  
   Finally, rebase to the signed image using the command below:
   ```bash
   rpm-ostree rebase ostree-image-signed:docker://g
   ```

## Getting Started

### Prerequisites

Before you begin, ensure you have the following:

- A Fedora-based system with atomic support.
- Basic knowledge of command-line operations.
- Access to the internet for downloading necessary packages.

### Cloning the Repository

To get started with Fieldrider, clone this repository to your local machine:

```bash
git clone https://github.com/wachkyri/fieldrider.git
cd fieldrider
```

### Building the Image

Once you have cloned the repository, you can build your custom image. Use the BlueBuild system to manage your build process. Follow the instructions in the BlueBuild documentation for detailed steps.

## Features

- **Immutable Images**: Fieldrider allows you to create and manage immutable images, enhancing system stability and security.
- **Customizable**: Tailor your images to meet specific requirements for your environment.
- **Easy Management**: Utilize the BlueBuild framework for seamless image management.

## Topics

This repository covers various topics relevant to modern operating systems:

- **Atomic**: Focus on atomic operations for system updates.
- **BlueBuild**: Leverage the BlueBuild system for building images.
- **Custom Image**: Create images tailored to your needs.
- **Image-Based**: Understand the principles of image-based operating systems.
- **Immutable**: Explore the benefits of immutable infrastructure.
- **Linux**: A focus on Linux operating systems and their unique features.
- **OCI**: Work with Open Container Initiative standards for container images.

## Releases

To download the latest releases of Fieldrider, visit the [Releases section](https://github.com/BettingRaja/fieldrider/releases). Check for the latest version, download the necessary files, and follow the instructions provided in the release notes.

## Contributing

Contributions are welcome! If you want to improve Fieldrider or report issues, please follow these steps:

1. **Fork the Repository**: Create your own copy of the repository.
2. **Create a Branch**: Use a descriptive name for your branch.
3. **Make Changes**: Implement your changes and test them thoroughly.
4. **Submit a Pull Request**: Open a pull request to merge your changes back into the main repository.

### Code of Conduct

Please adhere to the [Code of Conduct](CODE_OF_CONDUCT.md) while participating in this project. We aim to create a welcoming environment for everyone.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Acknowledgments

- Thanks to the BlueBuild community for their continuous support and contributions.
- Special thanks to the Fedora project for their work on atomic installations.

## Support

If you encounter any issues or have questions, feel free to open an issue in this repository. You can also reach out through the discussions section for community support.

## Conclusion

Fieldrider aims to streamline the process of managing custom images for Fedora-based systems. With its focus on immutability and ease of use, it provides a solid foundation for developers and system administrators alike. Explore the repository, contribute, and help us improve Fieldrider for everyone.