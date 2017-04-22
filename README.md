# npmtest-git-stats

#### basic test coverage for  [git-stats (v2.10.5)](https://github.com/IonicaBizau/git-stats)  [![npm package](https://img.shields.io/npm/v/npmtest-git-stats.svg?style=flat-square)](https://www.npmjs.org/package/npmtest-git-stats) [![travis-ci.org build-status](https://api.travis-ci.org/npmtest/node-npmtest-git-stats.svg)](https://travis-ci.org/npmtest/node-npmtest-git-stats)

#### Local git statistics including GitHub-like contributions calendars.

[![NPM](https://nodei.co/npm/git-stats.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/git-stats)

| git-branch : | [alpha](https://github.com/npmtest/node-npmtest-git-stats/tree/alpha)|
|--:|:--|
| coverage : | [![istanbul-coverage](https://npmtest.github.io/node-npmtest-git-stats/build/coverage.badge.svg)](https://npmtest.github.io/node-npmtest-git-stats/build/coverage.html/index.html)|
| test-report : | [![test-report](https://npmtest.github.io/node-npmtest-git-stats/build/test-report.badge.svg)](https://npmtest.github.io/node-npmtest-git-stats/build/test-report.html)|
| build-artifacts : | [![build-artifacts](https://npmtest.github.io/node-npmtest-git-stats/glyphicons_144_folder_open.png)](https://github.com/npmtest/node-npmtest-git-stats/tree/gh-pages/build)|

- [https://npmtest.github.io/node-npmtest-git-stats/build/coverage.html/index.html](https://npmtest.github.io/node-npmtest-git-stats/build/coverage.html/index.html)

[![istanbul-coverage](https://npmtest.github.io/node-npmtest-git-stats/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fcoverage.lib.html.png)](https://npmtest.github.io/node-npmtest-git-stats/build/coverage.html/index.html)

- [https://npmtest.github.io/node-npmtest-git-stats/build/test-report.html](https://npmtest.github.io/node-npmtest-git-stats/build/test-report.html)

[![test-report](https://npmtest.github.io/node-npmtest-git-stats/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Ftest-report.html.png)](https://npmtest.github.io/node-npmtest-git-stats/build/test-report.html)

- [https://npmdoc.github.io/node-npmdoc-git-stats/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-git-stats/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-git-stats/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-git-stats/build/apidoc.html)

![npmPackageListing](https://npmtest.github.io/node-npmtest-git-stats/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmtest.github.io/node-npmtest-git-stats/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ionică Bizău",
        "url": "https://ionicabizau.net"
    },
    "bin": {
        "git-stats": "bin/git-stats"
    },
    "blah": {
        "h_img": "http://i.imgur.com/Q7TQYHx.png",
        "description": [
            {
                "p": "I'd be curious to see your calendar with all your commits. Ping me on Twitter ([**@IonicaBizau**](https://twitter.com/IonicaBizau)). :smile: Until then, here's my calendar:"
            },
            {
                "img": {
                    "source": "http://i.imgur.com/PpM0i3v.png"
                }
            },
            {
                "h2": "Contents"
            },
            {
                "ul": [
                    "[Installation](#installation)",
                    [
                        "[Usage](#usage)",
                        {
                            "ul": [
                                "[Importing and deleting commits](#importing-and-deleting-commits)",
                                "[Importing all the commits from GitHub and BitBucket](#importing-all-the-commits-from-github-and-bitbucket)",
                                "[What about the GitHub Contributions calendar?](#what-about-the-github-contributions-calendar)"
                            ]
                        }
                    ],
                    "[Documentation](#documentation)",
                    "[How to contribute](#how-to-contribute)"
                ]
            }
        ],
        "installation_command": {
            "language": "sh",
            "content": [
                "# Install the package globally",
                "npm i -g git-stats",
                "# Initialize git hooks",
                "# This is for tracking the new commits",
                "curl -s https://raw.githubusercontent.com/IonicaBizau/git-stats/master/scripts/init-git-post-commit | bash"
            ]
        },
        "installation": [
            {
                "h2": "Usage"
            },
            {
                "h3": "Importing and deleting commits"
            },
            {
                "p": [
                    "I know it's not nice to start your git commit calendar from scratch. That's why I created ['git-stats-importer'](https://github.com/IonicaBizau/git-stats-importer)–a tool which imports or deletes the commits from selected repositories.",
                    "Check it out here: https://github.com/IonicaBizau/git-stats-importer",
                    "The usage is simple:"
                ]
            },
            {
                "code": {
                    "language": "sh",
                    "content": [
                        "# Install the importer tool",
                        "$ npm install -g git-stats-importer",
                        "",
                        "# Go to the repository you want to import",
                        "$ cd path/to/my-repository",
                        "",
                        "# Import the commits",
                        "$ git-stats-importer",
                        "",
                        "# ...or delete them if that's a dummy repository",
                        "$ git-stats-importer --delete"
                    ]
                }
            },
            {
                "h3": "Importing all the commits from GitHub and BitBucket"
            },
            {
                "p": "Yes, that's also possible. I [built a tool which downloads and then imports all the commits you have pushed to GitHub and BitBucket](https://github.com/IonicaBizau/repository-downloader)!"
            },
            {
                "code": {
                    "language": "sh",
                    "content": [
                        "# Download the repository downloader",
                        "$ git clone https://github.com/IonicaBizau/repository-downloader.git",
                        "",
                        "# Go to repository downloader",
                        "$ cd repository-downloader",
                        "",
                        "# Install the dependencies",
                        "$ npm install",
                        "",
                        "# Start downloading and importing",
                        "$ ./start"
                    ]
                }
            },
            {
                "h3": "What about the GitHub Contributions calendar?"
            },
            {
                "p": "If you want to visualize the calendars that appear on GitHub profiles, you can do that using ['ghcal'](https://github.com/IonicaBizau/ghcal)."
            },
            {
                "code": {
                    "language": "sh",
                    "content": [
                        "# Install ghcal",
                        "$ npm install -g ghcal",
                        "",
                        "# Check out @alysonla's contributions",
                        "$ ghcal -u alysonla"
                    ]
                }
            },
            {
                "p": [
                    "For more detailed documentation, check out the repository: https://github.com/IonicaBizau/ghcal.",
                    "If want to get even more GitHub stats in your terminal, you may want to try ['github-stats'](https://github.com/IonicaBizau/github-stats)--this is like 'git-stats' but with data taken from GitHub."
                ]
            },
            {
                "h2": "Using the configuration file"
            },
            {
                "p": [
                    "You can tweak the git-stats behavior using a configuration file in your home directory: '~/.git-stats-config.js'.",
                    "This file should export an object, like below (defaults are listed):"
                ]
            },
            {
                "code": {
                    "language": "js",
                    "content": [
                        "module.exports = {",
                        "    // \"DARK\", \"LIGHT\" or an object interpreted by IonicaBizau/node-git-stats-colors",
                        "    \"theme\": \"DARK\"",
                        "",
                        "    // The file where the commit hashes will be stored",
                        "  , \"path\": \"~/.git-stats\"",
                        "",
                        "    // First day of the week",
                        "  , first_day: \"Sun\"",
                        "",
                        "    // This defaults to *one year ago*",
                        "    // It can be any parsable date",
                        "  , since: undefined",
                        "",
                        "    // This defaults to *now*",
                        "    // It can be any parsable date",
                        "  , until: undefined",
                        "",
                        "    // Don't show authors by default",
                        "    // If true, this will enable the authors pie",
                        "  , authors: false",
                        "",
                        "    // No global activity by default",
                        "    // If true, this will enable the global activity calendar in the current project",
                        "  , global_activity: false",
                        "};"
                    ]
                }
            },
            {
                "p": "Since it's a js file, you can 'require' any other modules there."
            },
            {
                "h2": "Saving the data as HTML and images"
            },
            {
                "p": [
                    "'git-stats --raw' outputs raw JSON format which can be consumed by other tools to generate results such as HTML files or images.",
                    "['git-stats-html'](https://github.com/IonicaBizau/git-stats-html) interprets the JSON data and generates an HTML file. Example:",
                    {
                        "code": {
                            "content": [
                                "# Install git-stats-html",
                                "npm install -g git-stats-html",
                                "",
                                "# Export the data from the last year (generate out.html)",
                                "git-stats --raw | git-stats-html -o out.html",
                                "",
                                "# Export data since 2015 (save the results in out.html)",
                                "git-stats --since '1 January 2015' --raw | ./bin/git-stats-html -o out.html --big"
                            ],
                            "language": "sh"
                        }
                    },
                    "After we have the HTML file, we can generate an image file using ['pageres'](https://github.com/sindresorhus/pageres) by [**@sindresorhus**](https://github.com/sindresorhus/):",
                    {
                        "code": {
                            "content": [
                                "# Install pageres",
                                "npm install -g pageres-cli",
                                "",
                                "# Generate the image from HTML",
                                "pageres out.html 775x250"
                            ],
                            "language": "sh"
                        }
                    }
                ]
            },
            {
                "h2": "Cross-platform compatibility"
            },
            {
                "p": [
                    "'git-stats' is working fine in terminal emulators supporting ANSI styles. It should work fine on Linux and OS X.",
                    "If you run 'git-stats' to display graph on Windows, please use a terminal that can properly display ANSI colors.",
                    "Cygwin Terminal is known to work, while Windows Command Prompt and Git Bash do not. Improvements are more than welcome! :dizzy:"
                ]
            }
        ],
        "press": {
            "ul": [
                "[*A GitHub-like contributions calendar, but locally, with all your git commits*, The Changelog](https://changelog.com/github-like-contributions-calendar-locally-git-commits/)"
            ]
        }
    },
    "bugs": {
        "url": "https://github.com/IonicaBizau/git-stats/issues"
    },
    "contributors": [
        {
            "name": "Gnab"
        },
        {
            "name": "William Boman"
        },
        {
            "name": "Fabian Furger"
        }
    ],
    "dependencies": {
        "abs": "^1.0.0",
        "bug-killer": "^4.0.0",
        "cli-gh-cal": "^1.4.0",
        "cli-pie": "^2.0.0",
        "deffy": "^2.2.2",
        "gitlog-parser": "0.0.4",
        "gry": "^5.0.4",
        "is-there": "^4.0.0",
        "iterate-object": "^1.1.0",
        "moment": "^2.9.0",
        "r-json": "^1.0.0",
        "tilda": "^4.3.3",
        "typpy": "^2.1.0",
        "ul": "^5.0.0",
        "w-json": "^1.0.0"
    },
    "description": "Local git statistics including GitHub-like contributions calendars.",
    "devDependencies": {},
    "directories": {},
    "dist": {
        "shasum": "91c5376435995b2ecef0a5dd86f18e13239640ca",
        "tarball": "https://registry.npmjs.org/git-stats/-/git-stats-2.10.5.tgz"
    },
    "files": [
        "bin/",
        "app/",
        "lib/",
        "dist/",
        "src/",
        "scripts/",
        "resources/",
        "menu/",
        "cli.js",
        "index.js"
    ],
    "gitHead": "b0ddc16e71924947338782d8ead4ad3f322d18ef",
    "homepage": "https://github.com/IonicaBizau/git-stats",
    "keywords": [
        "git",
        "stats",
        "github",
        "cli"
    ],
    "license": "MIT",
    "main": "lib/index.js",
    "maintainers": [
        {
            "name": "ionicabizau"
        }
    ],
    "name": "git-stats",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git+https://github.com/IonicaBizau/git-stats.git"
    },
    "scripts": {
        "postinstall": "node scripts/migration/2.0.0.js",
        "test": "node test"
    },
    "version": "2.10.5"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
