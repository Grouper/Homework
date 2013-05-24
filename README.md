## Sneaking from Word to Word

Find a path from one word to another. A step is defined as an alteration of a single letter in the word that produces another valid word

For example  `bat, man -> (bat, ban, man)`

Or a bit more intense `grouper, twister -> (grouper, grouser, grosser, grasser, glasser, classer, clasher, flasher, flasker, flanker, franker, tranker, thanker, thinker, thinner, twinner, twinter, twister)`

Use any language that you'd like, but make sure you pay attention to code structure and clarity. We like Ruby, Coffeescript, Scala, Objective-C and Python, but if you use something else we'll figure it out.

If you're in ruby world, you can use your machine's word list as follows:

```ruby
require 'set'
$words = Set.new
File.foreach('/usr/share/dict/words') {|w| $words << w.chomp.downcase}

# Now you can look up if a word is in your dictionary
$words.include?("fish") # true
```

For bonus points, get the shortest path.
