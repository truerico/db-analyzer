
@startuml
skinparam titleBorderRoundCorner 15
skinparam titleBorderThickness 2
skinparam titleBorderColor black
skinparam titleBackgroundColor #DDDDDD
title **:: table erd1- © ::**
!theme _none_
skinparam shadowing False
top to bottom direction
skinparam linetype ortho
skinparam packageStyle rectangle
hide circle



entity "<&grid-three-up>** db_logs**" as db_logs { 
  + **(pk) _id : string**
  - @message : text
  - @tags : text
  - @timestamp : date
  - @version : text
  - agent : text
  - bytes : long
  - clientip : text
  - extension : text
  - geo.coordinates.lat : float
  - geo.coordinates.lon : float
  - geo.dest : text
  - geo.src : text
  - geo.srcdest : text
  - headings : text
  - host : text
  - ip : text
  - links : text
  - machine.os : text
  - machine.ram : long
  - memory : long
  - phpmemory : long
  - referer : text
  - relatedContent.article:modified_time : date
  - relatedContent.article:published_time : date
  - relatedContent.article:section : text
  - relatedContent.article:tag : text
  - relatedContent.og:description : text
  - relatedContent.og:image : text
  - relatedContent.og:image:height : text
  - relatedContent.og:image:width : text
  - relatedContent.og:site_name : text
  - relatedContent.og:title : text
  - relatedContent.og:type : text
  - relatedContent.og:url : text
  - relatedContent.twitter:card : text
  - relatedContent.twitter:description : text
  - relatedContent.twitter:image : text
  - relatedContent.twitter:site : text
  - relatedContent.twitter:title : text
  - relatedContent.url : text
  - request : text
  - response : text
  - spaces : text
  - url : text
  - utc_time : date
  - xss : text
  ==
  <&pie-chart>** stats**
      **total documents     : 14,005**
      **primary index size  : 36,776 KB**
      **all index size      : 36,776 KB**
      total attributes      : 47
      total objects         : 0
      max depth level       : 2
  --
}


entity "<&grid-three-up>** db_movies**" as db_movies { 
  + **(pk) _id : string**
  - Actors : text
  - Awards : text
  - Country : text
  - Director : text
  - Error : text
  - Genre : text
  - Language : text
  - Metascore : text
  - Plot : text
  - Poster : text
  - Rated : text
  - Released : text
  - Response : text
  - Runtime : text
  - Title : text
  - Type : text
  - Writer : text
  - Year : text
  - imdbID : text
  - imdbRating : text
  - imdbVotes : text
  - totalSeasons : text
  ==
  <&pie-chart>** stats**
      **total documents     : 113**
      **primary index size  : 209 KB**
      **all index size      : 209 KB**
      total attributes      : 23
      total objects         : 0
      max depth level       : 0
  --
}


entity "<&grid-three-up>** db_accounts**" as db_accounts { 
  + **(pk) _id : string**
  - account_number : long
  - address : text
  - age : long
  - balance : long
  - city : text
  - email : text
  - employer : text
  - firstname : text
  - gender : text
  - lastname : text
  - state : text
  ==
  <&pie-chart>** stats**
      **total documents     : 1,000**
      **primary index size  : 384 KB**
      **all index size      : 384 KB**
      total attributes      : 12
      total objects         : 0
      max depth level       : 0
  --
}


entity "<&grid-three-up>** db_shakespeare**" as db_shakespeare { 
  + **(pk) _id : string**
  - line_id : long
  - line_number : text
  - play_name : text
  - speaker : text
  - speech_number : text
  - text_entry : text
  - type : text
  ==
  <&pie-chart>** stats**
      **total documents     : 111,396**
      **primary index size  : 19,458 KB**
      **all index size      : 19,458 KB**
      total attributes      : 8
      total objects         : 0
      max depth level       : 0
  --
}


'# manual relation section 
tbl_aaa .. tbl_bbb

@enduml