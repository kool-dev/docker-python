
# Description

Minimal Python Docker image. It`s intended use is for [kool.dev]('https://kool.dev'), but you can use it for other use-cases.

# Avaliable Tags

## 3.9.7

## Environment Variables

| Variable   | Default Value | Description                                                                        |
| ---------- | ------------- | ---------------------------------------------------------------------------------- |
| **ASUSER** | `0`           | Changes the user id that executes the commands                                     |
| **UID**    | `0`           | Changes the user id that executes the commands **(ignored if ASUSER is provided)** |

## Usage

With `docker run`:

```sh
docker run -it --rm python:3.9.7
```

With environment variables:

```sh
docker run -it --rm -e ASUSER=500 python:3.9.7 
```

With `docker-compose.yml`:

```yaml
app:
  image: python:3.9.7
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