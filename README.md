# app-icon
A command-line tool to retrieve icon URLs of apps from [Google Play](https://play.google.com/) or [F-Droid](https://f-droid.org/en/packages/).



## Contents
- [Installation](#installation)
- [Available options](#available-options)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)



## Installation
**1. Clone this repo:**
```
git clone https://github.com/the-weird-aquarian/app-icon.git
```

**2. Move into the project directory:**
```
cd app-icon
```

**3. Give executable permissions to the script:**
```
chmod +x app-icon
```



## Available options
```
  -h, --help            Show this help message
  -o, --output          Write output to a specified file
  -p, --parallel        Retrieve multiple icons in parallel (Check note below)
  -W, --Width           Specify a width for the icon (requires -H/--Height too)
  -H, --Height          Specify a height for the icon (requires -W/--Width too)
```

**NOTE:** 
1. `-W/--width` and `-H/--height` options are only valid for Google Play URLs.
2. If `-p/--parallel` option is used, multiple icon URLs will be retrieved in parallel.
This will be faster, however, it might use a lot of system resources if too many packages are provided.



## Usage
```
app-icon <package>
```
```
app-icon <package1> <package2> <package3>
```

The output can be written to a specified file using the `-o` or `--output` option:
```
app-icon <package> -o <file>
```

**Examples:**
```
app-icon com.android.twitter
```

```
app-icon com.android.twitter com.spotify.music org.telegram.messenger
```

By default, the icons from Google Play will be 512x512 px. To change the dimensions, use `-W` and `-H`:
```
app-icon com.spotify.music -W 480 -H 960
```



## Contributing
Pull requests can be submitted [here](https://github.com/the-weird-aquarian/app-icon/pulls). Any contribution to the project will be highly appreciated.


## License
This project is licensed under the [MIT License](https://github.com/the-weird-aquarian/app-icon/blob/main/LICENSE).
