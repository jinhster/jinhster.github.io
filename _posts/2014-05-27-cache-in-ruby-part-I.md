---
layout: post
title:  "Cache in Ruby part I"
date:   2014-05-27
categories: coding
---

1. Client cache
	The client will most likely revisit(get) the same resource over and over again. Like a borowse will visit the home page or an article on a web page over and over again. If there isn't any changes on the resource we could use the http's "304 Not Modified". You can use the client cache for this and don't have to ask the server to recreate the same resource over. YOu can use fresh when in rails to do so.

	When the client revisit the same page it will look at http's request header and if the If-Modified-Since and if the If-None-Match is found it will return 304.

	More to come...

	class PagesController
  		def show
    		@page = page.find(params[:id])
    		fresh_when :last_modified => @page.updated_at
 		end
	end 


