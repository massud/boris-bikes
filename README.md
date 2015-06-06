:page_facing_up: Boris Bikes Tutorial :page_facing_up:
===========
This is the first tutorial from week 1 at Makers Academy! It was also my first experience with pair-programming; I partnered with [Massud](https://github.com/massud).

Boris Bikes is a Bike rental system in London, that allow users to rent and drop off bikes all over the city.

Objectives of exercise
----
Learn about Test-driven development, rspec and pair-programming for the first time.

Technologies used
----
- Ruby
- Rspec
- Git

How to run it
----
```
git clone git@github.com:GBouffard/Boris-bikes-tutorial.git
cd Boris-bikes-tutorial
irb
```
The tutorial being quite long, in our first try, we only had the time to do the bike and the docking station.
You can now play around in IRB. These are examples of commands that can be done:
```
require './lib/bike.rb'
require './lib/docking_station.rb'
bike = Bike.new
bike.broken?
ds = DockingStation.new
ds.dock bike
ds.release_bike
ds.release_bike
```

How to run tests
----
```
cd Boris-bikes-tutorial
rspec
```

The tutorial started with a feature test. We followed each chapter and running 'rspec -fd' gives the following results:
```
Bike
  should respond to #broken?
  can break
  when created
    should not be broken

DockingStation
  should respond to #release_bike
  releases bikes that are not broken
  can dock a bike
  raises error when no bikes available
  raises an error when full
  does not release broken bikes

member of public accesses bike
  docking station releases a bike that is not broken
  docking station unable to release as none available
  docking station will not make broken bikes available

member of public docks bike
  docking station unable to receive as full
```