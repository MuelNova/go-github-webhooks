<div align="center">

# Go-GitHub-Webhooks

_✨ Webhooks Builder Written in Golang. ✨_	
<p>
<a href="./LICENSE">
    <img src="https://img.shields.io/github/license/MuelNova/go-github-webhooks.svg" alt="license">
</a>
<a href="https://go.dev">
	<img src="https://img.shields.io/github/go-mod/go-version/MuelNova/go-github-webhooks?filename=src%2Fgo.mod&style=for-the-badge&logo=go&logoColor=white" alt="golang">
</a>
</p>

<p>
<img alt="GitHub last commit" src="https://img.shields.io/github/last-commit/MuelNova/go-github-webhooks?logo=github&style=for-the-badge">
</p>
</div>



## Installation

```sh
git clone https://github.com/MuelNova/go-github-webhooks.git
cd go-github-webhooks/src
go build
```

### Run as service

```sh
mkdir ~/.config/systemd/user -p
cp go-github-webhooks.example ~/.config/systemd/user/go-github-webhooks.service
```

Edit `~/.config/systemd/user/go-github-webhooks.service` to the config you want.

```sh
systemctl --user daemon-reload
systemctl --user start go-github-webhooks
```



## Configuration

```sh
cp .env.example .env
```

| Item          | Description                                       | Default Value | Type     |
| ------------- | ------------------------------------------------- | ------------- | -------- |
| GITHUB_SECRET | Webhook secret, see [below](#below)               | -             | Must     |
| PORT          | Listening port                                    | 4567          | Optional |
| EXTRA_COMMAND | Command to be executed when receiving PUSH event. | -             | Optional |
