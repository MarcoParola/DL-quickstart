# Configuration
Hydra configuration streamlines large-scale project management by offering flexible, hierarchical structures for defining and overriding settings. Its integration with various tools and support for parameter sweeps ensures reproducibility and facilitates efficient experimentation and optimization processes.

## Example
conf/config.yaml
```sh
db:
  driver: mysql
  user: omry
  pass: secret
```

my_app.py
```sh
import hydra

@hydra.main(version_base=None, config_path="path/to/the/configuration/folder", config_name="configuration_file")
def my_app(cfg) -> None:
    print(cfg.db.driver)
    print(cfg.db.user)
    print(cfg.db.pass)

if __name__ == "__main__":
    my_app()
```
Note:
- you can not use more than one configuration into a python file
- you should omit the .yaml extension
- 
```sh
$ python my_app.py db.user=root db.pass=1234
```
```sh
db:
  driver: mysql
  user: root
  pass: 1234
```

## Official giude:
[https://hydra.cc/docs/intro/](https://hydra.cc/docs/intro/)
