## REPONSES


a/
1.
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    Album.count
  ```
  
</details>
2. 
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    Track.find_by(title: "White Room") => Eric Clapton
  ```
  
</details>
3. 
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    Track.find_by(duration: "188133") => Perfect
  ```
  
</details>
4. 
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    Album.find_by(title: "Use Your Illusion II") => Guns N' Roses
  ```
  
</details>


b/
1. 
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    Album.where("title like ?", "%great%").count
  ```
  
</details>
2. 
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    Album.delete_by(title: "%music%")
  ```
  
</details>
3. 
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    Album.where(artist: "AC/DC").count => 2
  ```
  
</details>
4. 
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    Track.where(duration: "158589") => 0
  ```
  
</details>


c/

1.  
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    acdc_songs = Track.where(artist: "AC/DC")
    (acdc_songs.length).time do |i|
      puts acdc_songs[i].title
    end
  ```
  
</details>
2.  
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    songs = Track.where(album: "Let There Be Rock")
    songs.each do |i|
      puts i.title
    end  
  ```
  
</details>
3.  
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    songs.sum(:duration)
  ```
  
</details>
4.  
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    deep = Track.where("artist like ?", "Deep Purple")
    val = 0
    deep.each do |i|
      val = +i.price
    end
    puts val => 91.08(round)
  ```
  
</details>
5.  
<details>
  <summary>Spoiler warning</summary>
  
  
  ```ruby
    brit = Track.where("artist like ?", "Eric Clapton")
    brit.each do |i|
      i.update(artist: "Britney Spears")
    end
  ```
  
</details>
