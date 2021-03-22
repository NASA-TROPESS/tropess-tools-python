# macOS

>  Shell scripts are `bash`

## Setup

Install [XQuartz](https://www.xquartz.org)

Install the Apple Command Line Tools:

```bash
xcode-select --install
```

Install [Homebrew](https://brew.sh/):

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Install required packages:

```bash
brew install wget curl
```

## Anaconda

Install [Anaconda 3](https://docs.conda.io/projects/conda/en/latest/user-guide/install/macos.html). To get the default working environment (recommended), answer `yes` to all questions when asked:

```bash
wget https://repo.anaconda.com/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
chmod +x Miniconda3-latest-MacOSX-x86_64.sh
bash Miniconda3-latest-MacOSX-x86_64.sh
```

>  IMPORTANT: At this point close and re-open your current shell for changes to take effect.

Do not activate the base environment by default (optional):

```bash
conda config --set auto_activate_base false
```

Create a `tropess` Anaconda environment:

```bash
conda create --prefix ~/.conda/envs/tropess
```

Update `.bash_profile` to activate the `tropess` environment  by default when you login into `bash` (optional):

```bash
cat << EOT >> ~/.bash_profile
# Activate the tropess environment by default when you login
conda activate tropess
EOT
```

## Packages

Install the following Anaconda packages:

### Python

```bash
conda install --channel anaconda python pip
```

Test:

```bash
python --version
```

## Anaconda Environments

> Just for your information

To activate:

```bash
conda activate tropess
```

To deactivate:

```bash
conda deactivate
```

If you ever decide to remove it:

```bash
conda env remove --name tropess
```

