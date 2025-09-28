# pirated-list

This project manages a list of domains, used for mihomo project.

## Purpose of this project

Block pirated software, games, movies, TV shows, and other similar content.

## Download links

- **github**: [https://raw.githubusercontent.com/malagebidi/pirated-list/refs/heads/release/pirated-list.txt](https://raw.githubusercontent.com/malagebidi/pirated-list/refs/heads/release/pirated-list.txt)
- **jsdelivr**：[https://testingcf.jsdelivr.net/gh/malagebidi/pirated-list@release/pirated-list.txt](https://testingcf.jsdelivr.net/gh/malagebidi/pirated-list@release/pirated-list.txt)

## Usage example

Import via <code>rule-providers</code>:

```yaml
rule-providers:
  pirated-list:
    type: http
    url: https://testingcf.jsdelivr.net/gh/malagebidi/pirated-list@release/pirated-list.txt
    path: ./pirated-list.txt
    interval: 43200
    proxy: DIRECT
    behavior: domain
    format: text
```

And configure it in <code>rules</code>:

```yaml
rules:
  - RULE-SET,pirated-list,REJECT
  - ...
```
