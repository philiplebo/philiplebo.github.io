---
author: philiplebo
comments: true
date: 2018-08-11 11:45:00+00:00
layout: post
link: https://philiplebo.wordpress.com/2018/08/11/this-is-about-programming/
slug: this-is-about-programming
title: This Is About Programming
category: [ blog, prog ]
---
Hi
This is testing markdown formatting
# H1
## H2
### H3
#### H4
##### H5
code snippets!

~~~ python
class Article(models.Model):
    """
    Model representing an article
    """
    headline = models.CharField(max_length=2000, help_text='Headline of the article')
    description = models.TextField(help_text='Description of the article', null=True)
    source = models.ForeignKey(Source, on_delete=models.SET_NULL, null=True)
    author = models.CharField(max_length=1000, blank=True, null=True, help_text='Author(s) of the article')
    url = models.CharField(max_length=1000, help_text='URL to the article')
    md5_url = models.CharField(max_length=32, unique=True, help_text='MD5 hash of the url')
    image_url = models.CharField(max_length=1000, blank=True, null=True, help_text='URL to the image associated with the article')
    published_at = models.DateTimeField(help_text='Datetime of the article being published')
    seen_at = models.DateTimeField(auto_now_add=True, help_text='Datetime of the article being processed')
    similarity_link = models.ManyToManyField('self', through='Similarity', symmetrical=False)
    story = models.ManyToManyField(Story, blank=True)

    class Meta:
        ordering = ['-seen_at']

    def __str__(self):
        return self.headline
~~~

try ruby now
~~~ ruby
def what?
  42
end
~~~


weeeee