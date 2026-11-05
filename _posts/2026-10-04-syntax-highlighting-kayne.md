---
title: "Syntax Highlighting Kayne"
description: "Showing off Nyx's code blocks, with a very accurate model of Kayne."
tags: [code, ruby, meta]
categories: [technical]
---

## The model

Nyx has really nice syntax highlighting with line numbers, so we modeled Kayne in Ruby to show it off.

```ruby
class Kayne
  attr_reader :calm, :kindness

  def initialize
    @calm     = Float::INFINITY
    @kindness = Float::INFINITY
  end

  def respond_to_incident(incident)
    stay_calm
    timeline = build_timeline(incident)
    contain(incident)
    write_report(timeline)
    thank_the_team
  end

  def help(person)
    person.confidence += 1
    person.knowledge  += 1
    person
  end

  def panic
    raise NotImplementedError, "Kayne does not panic"
  end
end
```

## Usage

```ruby
kayne = Kayne.new
kayne.help(you)  # => a slightly better you
kayne.panic      # => NotImplementedError
```

## Shell, too

```bash
#!/usr/bin/env bash
for person in $(cat club_members.txt); do
  echo "kayne helped $person today"
done
```
