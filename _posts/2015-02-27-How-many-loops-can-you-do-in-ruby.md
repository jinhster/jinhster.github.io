---
layout: post
title:  "How many loops can you do in ruby?"
date:   2015-02-27
categories: ruby
---

I was wondering how many different ways can you write loop in ruby.

The first and most common has to be the loop keyword:
1. Loop
```ruby
placeholder = 0
loop do
  break if placeholder > 5
  puts "Inside the loop: #{placeholder}"
  placeholder += 1
end
```

2. The for loop (Coming from a C like programming languages, I have to say this is the most common one people uses)
```ruby
for i in 1..5 do
  puts i
end
```

3. While loop is pretty common in C like languages.
```ruby
placeholder = 0
while placeholder < 5 do
  puts "Inside the while loop: #{placeholder}"
  placeholder += 1
end
```

4. Until, for me works like a reverse while loop (the direct opposite).
```ruby
until placeholder > 5
  puts "Inside the until: #{placeholder}"
  placeholder += 1
end
```
5. Times
```ruby
5.times { |x| puts x}
```

6. Times, doing it with block.
```ruby
placeholder = "Hello there";
5 times do |placeholder|
  puts "Inside the time loop: #{placeholder}"
```

7. Each
```ruby
array = [1, 3, 5, 7, 9]
array.each do |x|
  puts "Inside the each loop: #{x}"
end
```
8. UpTo (You can also use downto)
```ruby
1.upto 5 do
  puts "Hello there"
end
```

The author once said:
>Ruby inherited the Perl philosophy of having more than one way to do the same thing. I inherited that philosophy from Larry Wall, who is my hero actually. I want to make Ruby users free. I want to give them the freedom to choose.
 -- <cite>Yukihiro Matsumoto </cite>

Maybe thats why there's so many different way to write loops, just use one that you like, there's no right or wrong answer.
