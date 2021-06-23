

<!-- ABOUT THE PROJECT -->
# Interac Landing Zone Deployment on Azure Stack Hub

<!-- [![Product Name Screen Shot][product-screenshot]](https://example.com) -->

## Summary 

Deploy Landing Zone foundational resources to the Azure Stack Hub environment.

## Folder Structure

The repo contains nested files in several folders. 

#### `DATA` Folder
* Contains the input *.csv files for this package. Each module receives its input parameters from these files and creates a map object to deploy resources based on the number of map elements. 

#### `LZ_MODULES` Folder
* Contains the invidual Azure Stack Hub components for the Landing Zone. This includes Resource Groups, NSG, NSG Rules, Virtual Networks, Virtual Network Peering, Subnets, Key Vault, RBAC Policies and Storage Account.

#### LZ_MODULES Sub Folders
* These are the Azure Stack Hub components which are called individually by the "main.tf" file in the root directory. These components can be used individually to deploy singular resoures, but the recommended method is to deploy everyting through the "main.tf" file. 

### Technologies

Majority of the repo is written in the HashiCorp Configuration Language (HCI) but it also contains a few Azure Resource Manager (ARM) templates to deploy reources not supported by the HashiCorp provider.  

* [HCL](https://www.terraform.io/docs/language/syntax/configuration.html)
* [ARM Templates](https://docs.microsoft.com/en-us/azure/azure-resource-manager/templates/overview)

<!-- GETTING STARTED -->
## Getting Started

The script requires Terraform to be installed or referenced locally. 

### Prerequisites

This 

* npm
  ```sh
  npm install npm@latest -g
  ```

### Installation

* [Terraform Download](https://www.terraform.io/downloads.html)
* [Terraform Installation](https://learn.hashicorp.com/tutorials/terraform/install-cli?in=terraform/azure-get-started)


#### Windows

1. Download the Terraform binary for Windows from the above link:
2. Move the binary to a local folder ex. **C:/tools/terraform/**
3. Set **C:/tools/terraform/** in your **Environment Variables**. 
4. Validate your installation by running the following commands and verifying that the Terraform version you installed is displaying. 
```sh 
C:\Users\user> terraform -v
```

#### Linux

1. Download the Terraform binary for Linux from the above link:
* [Terraform](https://www.terraform.io/downloads.html)
2. List out the locations in your **PATH**.
```sh 
$ echo $PATH
```
3. Assuming you have downloaded to the "downloads" folder, move the binary to **/usr/local/bin**. 
```sh 
$ mv ~/Downloads/terraform /usr/local/bin/
```
4. Set your **PATH** variable: 
```sh 
$ export PATH=$PATH:/usr/local/bin/
```
5. Validate your installation by running the following commands and verifying that the Terraform version you installed is displaying. 
```sh 
$ terraform -v
```



1. Get a free API Key at [https://example.com](https://example.com)
2. Clone the repo
   ```sh
   git clone https://github.com/your_username_/Project-Name.git
   ```
3. Install NPM packages
   ```sh
   npm install
   ```
4. Enter your API in `config.js`
   ```JS
   const API_KEY = 'ENTER YOUR API';
   ```



<!-- USAGE EXAMPLES -->
## Usage

Use this space to show useful examples of how a project can be used. Additional screenshots, code examples and demos work well in this space. You may also link to more resources.

_For more examples, please refer to the [Documentation](https://example.com)_



<!-- ROADMAP -->
## Roadmap

See the [open issues](https://github.com/othneildrew/Best-README-Template/issues) for a list of proposed features (and known issues).



<!-- CONTRIBUTING -->
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request



<!-- LICENSE -->
## License

Distributed under the MIT License. See `LICENSE` for more information.



<!-- CONTACT -->
## Contact

Your Name - [@your_twitter](https://twitter.com/your_username) - email@example.com

Project Link: [https://github.com/your_username/repo_name](https://github.com/your_username/repo_name)



<!-- ACKNOWLEDGEMENTS -->
## Acknowledgements
* [GitHub Emoji Cheat Sheet](https://www.webpagefx.com/tools/emoji-cheat-sheet)
* [Img Shields](https://shields.io)
* [Choose an Open Source License](https://choosealicense.com)
* [GitHub Pages](https://pages.github.com)
* [Animate.css](https://daneden.github.io/animate.css)
* [Loaders.css](https://connoratherton.com/loaders)
* [Slick Carousel](https://kenwheeler.github.io/slick)
* [Smooth Scroll](https://github.com/cferdinandi/smooth-scroll)
* [Sticky Kit](http://leafo.net/sticky-kit)
* [JVectorMap](http://jvectormap.com)
* [Font Awesome](https://fontawesome.com)





<!-- MARKDOWN LINKS & IMAGES -->
<!-- https://www.markdownguide.org/basic-syntax/#reference-style-links -->
[contributors-shield]: https://img.shields.io/github/contributors/othneildrew/Best-README-Template.svg?style=for-the-badge
[contributors-url]: https://github.com/othneildrew/Best-README-Template/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/othneildrew/Best-README-Template.svg?style=for-the-badge
[forks-url]: https://github.com/othneildrew/Best-README-Template/network/members
[stars-shield]: https://img.shields.io/github/stars/othneildrew/Best-README-Template.svg?style=for-the-badge
[stars-url]: https://github.com/othneildrew/Best-README-Template/stargazers
[issues-shield]: https://img.shields.io/github/issues/othneildrew/Best-README-Template.svg?style=for-the-badge
[issues-url]: https://github.com/othneildrew/Best-README-Template/issues
[license-shield]: https://img.shields.io/github/license/othneildrew/Best-README-Template.svg?style=for-the-badge
[license-url]: https://github.com/othneildrew/Best-README-Template/blob/master/LICENSE.txt
[linkedin-shield]: https://img.shields.io/badge/-LinkedIn-black.svg?style=for-the-badge&logo=linkedin&colorB=555
[linkedin-url]: https://linkedin.com/in/othneildrew
[product-screenshot]: images/screenshot.png
