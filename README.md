# Saudi Junior Science Team
### powered by [WebsiteBuilder](https://github.com/informatics-sa/WebsiteBuilder)
Saudi IJSO participant and individual-result archive, based directly on WebsiteTemplate.

This website includes: olympiads, participations, members and contact.

## Documentation
Read Website [public data files documentation](https://sainformatics.org/data/).

You might also refer to [Developer documentation](https://sainformatics.org/data/dev).


## Local Build
### Prerequisites
You need:

- [Python Interpreter](https://python.org)
- [Ruby Interpreter](https://www.ruby-lang.org)
- Python dependencies [requests](https://pypi.org/project/requests/) and [semver](https://pypi.org/project/semver/); install using pip (or your system's python package manager):
  ```sh
  pip install requests semver
  ```
- Install Ruby dependencies using [Bundler](https://bundler.io):
  ```sh
  bundle install
  ```

<details>
    <summary>How does it work?</summary>
    `bundle` is a package manager, `Gemfile` contains the packages list.
    Jekyll latest version is 4.4.1, but the current version used in Github pages is 
</details>

### Building & Local Serving
```sh
python prebuild.py && python build.py && bundle exec jekyll serve -s ./root
```

If you have WebsiteBuilder locally you can do:
```sh
python prebuild.py --path ../WebsiteBuilder && python build.py && bundle exec jekyll serve -s ./root
```

## License
This project is licensed under the GNU General Public License v3.0.

Check [LICENSE](/LICENSE)

## IJSO data and hosting

This copy retains WebsiteTemplate's original prebuild.py, GitHub Actions workflow, shared-core dependency, and build instructions. It contains no local layouts, custom build scripts, or template example contestants/exams.

The maintained data contains 48 named people, 49 participant entries and nine editions from 2015–2025. There are 29 individual medals in that period (one gold, three silver, 25 bronze). Three 2018 experimental-team silver awards are separate and are not included in individual results. The 2024 roster contains one of six names. The six recovered 2009 contestants are preserved in people.json; their edition is omitted because the bronze recipient is unresolved. Null individual awards must not be used to encode unknown results. English-name fields retain verified Arabic names where English spellings were not recovered. Training levels, graduation years and numerical scores are not invented.

Enable GitHub Pages with GitHub Actions. Like the other shared-core sites, this setup uses root-relative links and expects hosting at a domain root. Set your own domain in GitHub Pages settings; WebsiteTemplate's CNAME was removed because its domain belongs to the example site. The build and deployment architecture is otherwise unchanged.
