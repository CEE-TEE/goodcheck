![Goodcheck logo](logo/goodcheck-horizontal.png)

# Goodcheck - Regexp based customizable linter

Are you reviewing a pull request if the change contains deprecated API calls?
Do you want to post a comment to ask the developer if a method call satisfies some condition for use without causing an issue?
What if a misspelling like `Github` for `GitHub` can be found automatically?

Give Goodcheck a try to do them instead of you! 🎉

Goodcheck is a customizable linter. You can define pairs of patterns and messages.
It checks your program and when it detects a piece of text matching with the defined patterns, it prints your message which tells your teammates why it should be revised and how.
Some part of the code reviewing process can be automated.
With Goodcheck the only thing you have to do is define the rules, pairing patterns with messages, and then those same patterns won’t bother you anymore. 😆

## Getting started

Goodcheck is provided as a Ruby gem. To install it, run:

```shell
gem install goodcheck
```

If you do not want to install it, you can run it via Docker instead:

```shell
docker run -t --rm -v "$(pwd):/work" sider/goodcheck
```

Check out the [documentation](docs/getstarted.md) or [website](https://sider.github.io/goodcheck/) for more details.

## Development

After checking out the repository, run `bin/setup` to install dependencies. Then, run `rake test` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

To install this gem onto your local machine, run `bundle exec rake install`.

### Website

To develop the website on your local machine, run:

```shell
npm start
```

### Releasing

To release a new version, follows the steps below:

1. Update [`lib/goodcheck/version.rb`](lib/goodcheck/version.rb).
2. Update [CHANGELOG.md](CHANGELOG.md).
3. Run `git add . && git commit -m 'Version <new_version>'`.
4. Run `bundle update`.
5. Run `bundle exec rake release`, which will create a tag, push the commit and tag, and publish the gem to [RubyGems.org](https://rubygems.org).
6. Run `npm ci`.
7. Run `GIT_USER=<GITHUB_USERNAME> [USE_SSH=true] npm run deploy`.
   - See also the [Docusaurus guide](https://docusaurus.io/docs/deployment#environment-settings).

## Contributing

Bug reports and pull requests are welcome on [GitHub](https://github.com/sider/goodcheck).
