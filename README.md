# HTML & CSS Crash course

What we're learning today:

 * Basics of the internet and how webpages work
 * Syntax of HTML and CSS
 * Principles of front-end code organization and project structure
 * Create and style basic sites with HTML & CSS
 * Learn to host your webpage on github pages


I don't teach for a living so I'm going to mostly just scrounge up some resources that I think are good at teaching this stuff. I'm mainly here to answer questions and help you if you have trouble.

## Basics of the internet
Start by watching this guy explain it [here](http://fast.wistia.net/embed/iframe/e1hu2b8jm6)

Let's take a closer look at what he's talking about by discussing what happens when you go to google.com. Take a look at this diagram.

![Diagram](https://i.imgur.com/pTbDpCo.png)
When the client wants to access a server that corresponds to the domain name 'google.com', it first needs to find out that servers IP address. In order to get that your client makes a request to a Domain Name Server. These servers are the "phone books" of the internet. Their job is to map names to addresses (domain names to IP addresses to be precise). You might be wondering : "If this 'phonebook' is itself on a server, how does my client get the IP address for that server?" The answer is: it's either stored on your OS, or your ISP gives it to you when you connect to the internet.

Once the client has the IP address it needs, it makes the request. A request involves sending some information to the server about what the client wants. Simplified, a request would look like this:
```
method: GET
path: /
```
In reality there's a lot more information passed along, but this is already a lot for someone totally new to web development. Translated to english this request basically means "get me whatever is at your root path", which when talking about servers that host web applications, generally means "give me your home page".

In this case google sends back an html document (again in reality it sends more complicated stuff as well). Now your browser says "Oh an html document, I know how to render this so the user can see it" and starts parsing the document. Usually, while parsing the document, the browser will find references to other assets such as images, stylesheets, and javascript. When it runs into these references in the html document, it will make additional requests to the server for those assets and continue parsing and rendering the document as those requests come back.

That was a pretty in depth discussion for your first day of web development, so don't worry if some of it went over your head. The main thing to take away is that when you browse the internet, you act as a client that makes requests to servers that respond with the files that allow you to see websites.

If you're interested in this topic, you can read more [here](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/How_the_Web_works). You may also watch [this video](https://www.youtube.com/watch?v=e4S8zfLdLgQ) though it may be deeper than you're ready for.

## HTML & CSS Syntax

Start [here](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/HTML_basics) for html. When you're done tell me two things you learned.

We're going to need a text editor. Install atom (or a text editor of your preference) if you haven't yet. Let's make the same website mozilla did in the link above, but with different content. That is we will use the same html elements but the contents of the elements will be different.

Start [here](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/CSS_basics) for CSS. Again, two things please. And lets style the page we made in the last section as they did (different colors, fonts and such if you feel like it).

Finally we're going to go through [this GA lesson](https://github.com/ga-wdi-lessons/html-and-css). A lot of it will be repeat material from the previous two links, but practice makes perfect. Don't do the exercises at the bottom yet.

## Front-end code organization/ Project Structure

Read [this](https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/Dealing_with_files) if you like. Generally very simple front end projects look something like this:
```
project/
	index.html
	styles/
    	style.css
    scripts/
    	index.js
    assets/
    	images/
        fonts/
```
Most projects are much bigger than that, so it's very important to be organized so you can easily find a file or bit of code. Another reason it's good to organize projects is that it helps to achieve seperation of concerns. It's better to keep your styles in a seperate file from your index.html rather than between style tags or using inline styling (unless you have a good reason to do it one of the other ways) because if you need to change the way something looks you will know exactly where to go and you won't have to worry about making changes in multiple files needlessly.

## Create and style basic sites

We're going to do one of the first homework assignments at GA. [Syle Betty White's website](https://github.com/ga-wdi-exercises/wendy_bite) This is not an easy assignment, so don't be discouraged. It's supposed to be challenging. First though, let's take a look at the html that betty white provides for us.

```
<!DOCTYPE html>
<head>
  <title>Wendy Bite | About Me</title>
</head>
<body>

  <header>
    <h1>Wendy G. Bite</h1>
    <nav>
      <a href="#" class="active">About Me</a>
      <a href="#">Résumé</a>
    </nav>
  </header>

  <main>
    <h2>About Me</h2>

    <img src="Wendy-Bite.jpg" alt="This is Wendy Bite" />

    <p>The series revolves around four older, single women (three widows and one divorcée) sharing a house in Miami, Florida. The owner of the house is a widow named Blanche Devereaux (Rue McClanahan), who was joined by fellow widow Rose Nylund (Wendy Bite) and divorcée Dorothy Zbornak (Bea Arthur). They both responded to a room-for-rent ad on the bulletin board of a local grocery store. In the pilot episode, the women had a gay cook named Coco (Charles Levin), who was subsequently removed.[5] The three were soon joined by Dorothy"s mother, Sophia Petrillo (Estelle Getty), after the retirement home where she lived, Shady Pines, burned down.</p>

    <p>Thank You for being a friend. Travel down a road and back again. Your heart is true, you"re a pal and a confidante.And if you threw a party, invited everyone you knew, you would see the biggest gift would be from me and the card attached would say, Thank You For Being a Friend!</p>
  </main>

  <footer>
    <a href="#">Facebook</a>
    <a href="#">Twitter</a>
    <a href="#">Instagram</a>
    <a href="#">LinkedIn</a>
  </footer>

  </body>
</html>
```
Make a sketch of what this html would look like unstyled in the browser. You don't need to write any actual words. Words can be squiggles.

When you are done with your sketch, you will need to create a github account so you can clone the betty white exercise locally. I will assist you with this.

When you feel sastisfied with your betty white page's style, feel free to replace the content so that the website is about you, your pet, or whatever you like.

## Host on github pages

Finally head [here](https://pages.github.com/) for instructions on how to host your website on github pages. Each github user gets one page, but you can change what is on your page if you make something better later.
