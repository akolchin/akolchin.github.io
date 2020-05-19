## May 19, 2020

It is a good time to start a new "hobby" project. 

As usual, it will be based on the Google Cloud Platform. 

It will contain a classic web app part. But in this time it will be implemented by using mainstream tools like Angular for front-end and Spring for the back-end (as far as it will be possible taking into account that I plan to use Google App Engine as a platform for it). Yes, I plan to host a web application on the [GAE (Java 11, standard)](https://cloud.google.com/appengine/docs/standard/java11).

The core idea of the project is to find some interesting publicly available data sources and try to extract from them information useful for the end-user like me or anybody else. It also very desirable that the data will update in real-time. Obviously the pretenders are the weather or flight tracking data, but itis too obvious and already boring examples. 
[https://darksky.net/dev](https://darksky.net/dev)
[https://developer.flightstats.com/api-docs/flightstatus/v2](https://developer.flightstats.com/api-docs/flightstatus/v2)

To make the data end-user related - the obvious solution is filtering data by using the current user location, it could make it useful for this user.  Another even more straightforward solution is to use the user ID or other personal attributes but I don't think that such data can be really publicly accessible. 

So this part still completely is not clear: 
- what data can be interesting? 
- where can I get them? 
- how to make them to the end-user related?

From a technical point of view, this part most likely will utilize [Google streaming solution: PubSub, Dataflow, Bigquery.](https://cloud.google.com/solutions/stream-analytics)

Google Data Studio could also be used to visualize collected data, but maybe I just integrate visualization into a web application. In the lucky case, I will try to utilize Google AI/ML services as well.


------------------------------------------------------------------------------------------------------------------
## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/akolchin/akolchin.github.io/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/akolchin/akolchin.github.io/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
