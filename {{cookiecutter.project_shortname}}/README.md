# {{cookiecutter.project_name}}

{{cookiecutter.description}}

## Install

```shell
pip install {{cookiecutter.project_shortname}}
```

## Development
### Getting Started

1. Create a new python environment:
   ```shell
   python -m venv venv
   . venv/bin/activate
   ```
   _Note: venv\Scripts\activate for windows_

2. Install python dependencies:
   ```shell
   pip install -r requirements.txt
   ```
3. Install npm packages:
   1. Optional: use [nvm](https://github.com/nvm-sh/nvm) to manage node version:
      ```shell
      nvm install
      nvm use
      ```
   2. Install:
      ```shell
      npm install
      ```
4. Build:
   ```shell
   npm run build
   ```

### Component Code

### Publish

1. Clean up build and  dist - removes old and temp tarballs:
```
rm -rf dist build
```


2. Run a new build
```
npm install
npm run build
```

2. Build source distribution.  
```
npm run dist
```

3. Test your tarball by copying it into a new environment and installing it locally, for example:
```
pip install <your-project-name-version>.tar.gz
```

Note:  For local install, use  `pip install -e ./path-to-project`

4. Prepare release on the GitHub UI - For more information see [Managing Releases](https://docs.github.com/en/repositories/releasing-projects-on-github/managing-releases-in-a-repository)
When in doubt, do an alpha release first

5. Publish on PyPI
```
$ twine upload dist/*
```



### Justfile

Alternatively, use the provided [just](https://github.com/casey/just) commands:

1. Create a Python environment from previous step 1 and install:
   ```shell
   just install
   ```
2. Build
   ```shell
   just build
   ```
3. Publish
   ```shell
   just publish
   ```
4. See all commands with `just -l`
