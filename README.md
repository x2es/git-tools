
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
