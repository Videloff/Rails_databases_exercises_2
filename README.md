# README

This README would normally document whatever steps are necessary to get the
application up and running.

Things you may want to cover:

* Ruby version

* System dependencies

* Configuration

* Database creation

* Database initialization

* How to run the test suite

* Services (job queues, cache servers, search engines, etc.)

* Deployment instructions

* ...

## REPONSES

a/
1. Album.count
2. Track.find_by(title: "White Room") => Eric Clapton
3. Track.find_by(duration: "188133") => Perfect
4. Album.find_by(title: "Use Your Illusion II") => Guns N' Roses

b/
1. Album.where("title like ?", "%great%").count
2. Album.delete_by(title: "%music%")
3. Album.where(artist: "AC/DC").count => 2
4. Track.where(duration: "158589") => 0

c/
```
1.  acdc_songs = Track.where(artist: "AC/DC")
    acdc_songs.each do |i|
      puts i.title
    end

2.  songs = Track.where(album: "Let There Be Rock")
    songs.each do |i|
      puts i.title
    end  

3.  songs.sum(:duration)

4.  deep = Track.where("artist like ?", "Deep Purple")
    val = 0
    deep.each do |i|
      val = +i.price
    end
    puts val => 91.08(round)

5.  brit = Track.where("artist like ?", "Eric Clapton")
    brit.each do |i|
      i.update(artist: "Britney Spears")
    end
