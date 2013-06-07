---
layout: post
title: "Ruby单例"
date: 2013-05-20 02:20
comments: true
categories: Ruby
---
Ruby是一种面向对象的语言，下面是写的一个Ruby版本的单例模式：
{% codeblock lang:ruby %}
class RubySingleton
  private_class_method :new
  @@instance = nil

  def RubySingleton.instance
    @@instance = RubySingleton.new unless !@@instance
  end
end

puts RubySingleton.instance.object_id
puts RubySingleton.instance.object_id
{% endcodeblock %}
