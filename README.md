
# Description

Minimal Python Docker image. It`s intended use is for [kool.dev]('https://kool.dev'), but you can use it for other use-cases.

# Avaliable Tags

## 3.9

## Environment Variables

| Variable   | Default Value | Description                                                                        |
| ---------- | ------------- | ---------------------------------------------------------------------------------- |
| **ASUSER** | `0`           | Changes the user id that executes the commands                                     |
| **UID**    | `0`           | Changes the user id that executes the commands **(ignored if ASUSER is provided)** |

## Usage

With `docker run`:

```sh
docker run -it --rm kooldev/node:14 node -v
```

With environment variables:

```sh
docker run -it --rm -e ASUSER=500 kooldev/node:14 node -v
```

With `docker-compose.yml`:

```yaml
app:
  image: kooldev/node:14
  environment:
    ASUSER: "${$UID}"
```

## Contributing

### Dependencies

- [fwd](https://github.com/fireworkweb/fwd#fireworkwebfwd)

You should change `fwd-template.json` and `template` folder.

After your changes, just run `fwd template` to compile the template and generate all version folder/files.

## License

The MIT License (MIT). Please see [License File](LICENSE.md) for more information.