## May 21, 2020

Today I have added two new public repositories:
 - [https://github.com/akolchin/tba-server](https://github.com/akolchin/tba-server)
 - [https://github.com/akolchin/tba-client](https://github.com/akolchin/tba-client)

and one project to manage issues:
[https://github.com/users/akolchin/projects/2](https://github.com/users/akolchin/projects/2).

I started to develop foundation level parts of the web application.

I decided to use [Google App Engine Java 11 Standard Environment](https://cloud.google.com/appengine/docs/standard/java11)

Let's see how much headache I will get from it. 

At least I already able to deploy as well as run locally the template example provided by Google 
[Spring Boot Application Google App Engine Standard with Java 11](https://github.com/GoogleCloudPlatform/java-docs-samples/tree/master/appengine-java11/springboot-helloworld)

But all these possible only by using `maven` commands - [Cloud Code for IntelliJ plugin](https://github.com/GoogleCloudPlatform/cloud-code-intellij)  don't understand how to work with such Java 11 Standard project. (Mostly because of absent of `appengine-web.xml` which replaced by `app.yaml` as I understand)

## May 20, 2020
It occurs that it is not easy to find suitable publicly available data sources, especially those updated periodically even if not in real-time. There are such [data sources provided by NASA](https://search.earthdata.nasa.gov/search?ff=Near%20Real%20Time) but to be honest, I have no idea how to make them useful for end-user.

The only interesting and suitable by technical requirements data sources I have found so far are the ones provided by [GDELT Project](https://www.gdeltproject.org/). They have interesting content ("events" from all around the world), updated frequently (at least once a day or every 15 minutes - not sure yet), can be linked to the end-user location, social attributes, and interests. 

"_... The GDELT Project is the largest open-access database on human society in existence. Its archives contain nearly 400M latitude/longitude geographic coordinates spanning over 12,900 days, making it one of the largest open-access **spatio-temporal** datasets as well...._"

They provide data in the form of [BigQuery datasets](https://cloudplatform.googleblog.com/2014/05/worlds-largest-event-dataset-now-publicly-available-in-google-bigquery.html) that allows to use it in my project with fewer efforts although it probably will not allow me to practice in streaming pipeline implementation. 

So, in the nearest days, I will dive deeper into exploring the content and formats of this data source. I will try to imagine what useful insights can get end-user (at least as me) from such content. I also need to understand in what status this project is now - it is still not clear fo me.

Meanwhile, I also will start to develop the foundation level parts of the web application as well as prepare required GCP infrastructure and development environment.

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

From a technical point of view, this part most likely will utilize [Google streaming solution: Pub/Sub, Dataflow, Bigquery.](https://cloud.google.com/solutions/stream-analytics)

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
