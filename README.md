
Git Tools
=========

## Install

Add `bin/` to PATH.

## Tools

### Rails: run rspec for modified specs

```bash
$ rspec-modified [rspec options]
```

Invokes `bundle exec rspec <modified specs>`

Assuming all specs match `spec/**/*_spec.rb`.

#### Examples

Invoke selected part of spec

**some_spec.rb**

```ruby
describe "foo", only: true do
  it "foo" ...
end
```

**run only tagged**
```bash
$ rspec-modified --tag only
```

### Git difftool for all modified

```bash
$ git-diffadd
```

 - Invokes `git difftool` for each modified file in current dir.
 - Then asks about adding it to commit [Y/n]
 - Goes to next file

NOTE: very primitive, works well only when no added to commit files
