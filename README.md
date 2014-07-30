bukkit-bootstrap
================

A bootstrap to create new Bukkit plugins quicker.

## Setup
First, ensure you have a *nix OS, Git, and Gradle. Then proceed.

1. Clone this repository and `cd` to it.
2. Edit `src/main/resources/plugin.yml` with your plugin's information.
3. Run `gradle scaffold`. This will set up your plugin directories and files and rename the `git remote` so you can push to your own Git repository.
4. Edit your `gradle.properties` and set the `testPluginDir` and `remotePluginDir` variables. Make sure you use an absolute path instead of `~` for your home directory.
5. Add your Git origin remote with `git remote add origin <your Git URL>` and run `git push -u origin --all`. This will make it so you push to your origin by default.

## Usage
**bukkit-bootstrap** provides the following Gradle tasks:

* `scaffold` - Sets things up.
* `testCopy` - Copies the JAR to the test directory at whatever `testPluginDir` is set to.
* `remoteCopy` - Copies the JAR via SCP to a remote directory of your choice.

To add external libraries as JARs, simply put them in a `libs/` directory. Gradle will automatically set them as dependencies.

## License
This license can also be found in the attached `LICENSE.txt` in the `bootstrap/` directory.

```
The MIT License (MIT)

Copyright (c) 2014 Ian Macalinao

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```

