!SLIDE
<!--
How to watch this presentation:

gem install showoff
showoff serve
-->

Hi
==

!SLIDE

Ruby classes
============

!SLIDE

    @@@ ruby
    class Character
    end

    ogden = Character.new

!SLIDE

Constructors
------------

!SLIDE

    @@@ ruby
    class Character
      def initialize(name)
      end
    end

    blacksmith = Character.new('Griswold')

!SLIDE

Instance variables
------------------

!SLIDE

    @@@ ruby
    class Character
      def initialize(name)
        @name = name
      end

      def walk_north
        puts "#{@name} walks north"
      end
    end

    elder = Character.new('Cain')
    elder.walk_north

!SLIDE

Class variables
---------------

!SLIDE

    @@@ ruby
    class Character
      @@count = 0

      def self.count
        @@count
      end

      def initialize
        @@count += 1
      end
    end

    3.times { Character.new }
    Character.count

!SLIDE

Inheritance
===========

!SLIDE center

![Inheritance](/file/images/inheritance.png)

!SLIDE center

![Inheritance no-no](/file/images/inheritance-no-no.png)

!SLIDE

Base class
------------

!SLIDE

    @@@ruby
    class Character
      def name
        'Somebody'
      end

      def walk_north
        puts '#{name} is walking north'
      end

      def walk_west
        puts '#{name} is walking west'
      end

      # ...
    end

!SLIDE

Derived class
-------------

!SLIDE

    @@@ ruby
    class Player < Character
      def name
        'Player'
      end

      def equip(item)
        puts '#{name} equipped #{item}'
      end
    end

!SLIDE

Action!
-------

!SLIDE

    @@@ ruby
    player = Player.new
    player.equip('chocolate bar')
    player.walk_north
    player.walk_west
    player.walk_south
    player.walk_east

!SLIDE

Modules
-------

!SLIDE

Pair of classes
---------------

!SLIDE

    @@@ ruby
    class Cat
    end

    class Dog
    end

!SLIDE

Common attribute
----------------

!SLIDE

    @@@ ruby
    module Whiskers
      def sense_things_in_darkness?
        true
      end
    end

!SLIDE

    @@@ ruby
    class Cat
      include Whiskers
    end

    class Dog
      include Whiskers
    end

    cat = Cat.new
    dog = Dog.new

    cat.sense_things_in_darkness?
    dog.sense_things_in_darkness?

!SLIDE

ActiveRecord && Models
======================

Blah blah
