# Asimov

Send files and texts between devices on the same network. 

Made with Rust for AxOS?

It uses the LocalSend protocol, a secure and efficient protocol to send files and texts between devices on the same network.

## Install

```bash
# clone the repo
$ git clone https://github.com/axos-project/asimov.git
# Go to the project directory
$ cd asimov
# Install the project
$ cargo install
```

Asimov is also installable via Epsilon with AxOS:

```bash
$ epsi install asimov
# or
$ epsi i asimov
```

## Usage

### Send

```bash
# send text only
$ asimov send "text to sent"

# send files
$ asimov send /path/to/file1 /path/to/file2 ...

# send mixed texts and files
$ asimov send "text to sent" /path/to/file ...
```

### Receive

```bash
# receive files and save to $(pwd)
$ asimov receive

# receive files and save to path
$ asimov receive --dest /path/to/save

# receive all files automatically
$ asimov receive --quick-save
```

## Roadmap

- [x] Settings
    - [x] Device alias
    - [x] Device fingerprint
    - [x] Multicast address
    - [x] Port
    - [ ] Enable https
    - [x] Quick Save
    - [x] Save directory
    - [ ] Non interactive mode
- [x] Discovery
    - [x] Multicast UDP
    - [ ] ~~HTTP(Legacy Mode)~~
- [x] File transfer
    - [x] Send files and texts
    - [ ] Send clipboard data
    - [x] Cancel sending
    - [x] File upload progress bar
    - [x] Fuzzy Select devices
    - [x] Receive files
- [ ] Reverse file transfer
    - [ ] Browser URL
    - [ ] ~~Receive request~~(not in plan)

## Credits

* [localsend/protocol](https://github.com/localsend/protocol)
* [notjedi/localsend-rs](https://github.com/notjedi/localsend-rs)
