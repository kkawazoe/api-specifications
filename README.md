# api-specifications

## Required

* Docker
* VS Code
  * Extensions: [Dev Containers](vscode:extension/ms-vscode-remote.remote-containers)

## Folder Structure

<pre>
./
├── docs/
│  └── open_api/
│     ├── dist/
│     │  └── sample_api.html
│     └── src/
│        └── sample_api.yaml
└── README.md
</pre>

## [Redocly CLI Commands](https://redocly.com/docs/cli/commands/#redocly-cli-commands)

### Lint

```sh
redocly lint docs/open_api/src/sample_api.yaml
```

### Preview Docs

```sh
redocly preview-docs docs/open_api/src/sample_api.yaml
```

### Generate HTML file

```sh
redocly build-docs docs/open_api/src/sample_api.yaml --output=docs/open_api/dist/sample_api.html
```

## Trouble Shooting

### Error on git connection

ex. git pull origin main

```sh
git pull origin source
# fatal: unable to access 'https://github.com/<<remote-url>>/': server certificate verification failed. CAfile: none CRLfile: none
```

Execute the following commands
※Dev container, so once this way around

```sh
git config --local http.sslverify false
```
