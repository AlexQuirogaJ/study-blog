# Study blog

Blog created with the hugo framework and the Stack theme.

- Link: https://study-blog.netlify.app/

## Requirements and installation guidelines for Debian Linux Distributions:
- Hugo Extended ≥ 0.87.0:

    1. Install brew ([page](https://brew.sh/))
        Run:
        ```bash
        ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
        ```
        Add this line to `~/.bashrc`:
        ```bash
        eval "$(/home/linuxbrew/.linuxbrew/bin/brew shellenv)"
        ```
    2. Run the `brew` Command to Install `hugo`
        ```bash
        brew install hugo
        ```
    3. Verify with:
        ```bash
        hugo version
        ```

- Go version >= 1.12:

  1. Download Go installer [here](https://go.dev/dl/)
  2. Remove any previous Go installation, then extract the downloaded archive:
      ```bash
      sudo su
      rm -rf /usr/local/go && tar -C /usr/local -xzf go1.18.3.linux-amd64.tar.gz
      ```
  3. Add `/usr/local/go/bin` to the PATH environment variable. Add this line to `~/.bashrc`:
      ```bash
      export PATH=$PATH:/usr/local/go/bin
      ```
  4. Verify installation with:
      ```bash
      go version
      ```

- Git:
  1. Install git:
      ```bash
      sudo apt update && sudo apt install git
      ```
  2. Verify installation with:
      ```bash
      git --version
      ```

## How to create a new site using Stack Theme

Open a terminal in desired folder and run:

```bash
hugo new site stack
cd stack
hugo mod init github.com/me/my-new-blog
hugo mod get github.com/CaiJimmy/hugo-theme-stack/v3
rm config.toml
touch config.yaml
```

For more information about how to install and use this theme you should visit [Stack Theme documentation](https://docs.stack.jimmycai.com/). Once you have created your blog they recommend to  use[exampleSite configuration](https://github.com/CaiJimmy/hugo-theme-stack/blob/master/exampleSite/config.yaml) as reference.

## Development

- To start the Hugo Server run:
    ```bash
    hugo server
    ```
- To build static pages (output will be in `./public/` directory) run:
    ```bash
    hugo
    ```

## Deploy
This project is hosted with [Netlify](https://www.netlify.com/), which is connected to this GitHub repository.

## References:
- Hugo Docs: https://gohugo.io/documentation/
- Stack Theme: https://github.com/CaiJimmy/hugo-theme-stack
