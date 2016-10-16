```diff
- WARNING: We are currently in the process of writing the minimum installation specifications for Hypercycle, and will publish the actual source code after we have completed the documentation below. We don't expect this to take too much longer. If you have any questions, comments, or issues, please feel free to ask away. If you would like to contribute, get in touch!
```

<hr>

![alt tag](https://gallery.mailchimp.com/d793ae062926c63262e96e99c/images/4367f220-3a28-4ad4-9e9b-f7055f4ed9cd.png)

# Hypercycle - A Social Network for Custom Clothing Design
The Hypercycle social network was first launched on December 19, 2014. It is truly the labor of my love. I hope you will have fun playing around, and perhaps create something totally new as a result. More to the point, Hypercycle is a social marketplace for custom product design. It is a fun, easy way to create t-shirts and more. Hypercycle users can upload their art, share their designs with their friends, and open their own storefronts to sell their creations to the world.

| ![alt tag](https://www.elgami.com/images/elgami-pattern.png) | ![alt tag](https://www.elgami.com/images/amarna-leggings.png) |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| Artwork by ELGAMI: https://www.elgami.com/#/elgami | Model: Amarna Miller (https://www.instagram.com/amarnamiller/) |

# Table of Contents  
* [0.0 Vision](#vision)
* [1.0 Team & Past Contributors](#team)
* [2.0 Installation & Documentation](#installation)
  * [2.1 Trello](#trello)
  * [2.2 Back4App Registration](#back4app)
  * [2.3 Application Configuration](#config)
* [3.0 Database Schema](#schema)
  * [3.1 Classes](#classes)
    * [3.1.0 Installation](#installation)
    * [3.1.1 Role](#role)
    * [3.1.2 Session](#session)
    * [3.1.3 User](#user)
    * [3.1.4 Comment](#comment)
    * [3.1.5 Feed](#feed)
    * [3.1.6 Design](#design)
    * [3.1.7 MarketFeed](#marketfeed)
    * [3.1.8 MarketDesign](#marketdesign)
    * [3.1.9 Inventory](#inventory)
      * [3.1.9.0 Group Number](#groupnumbers)
      * [3.1.9.1 Size Options](#sizeoptions)
      * [3.1.9.2 Product Templates](#producttemplates)
    * [3.1.10 Notification](#notification)
    * [3.1.11 Orders](#orders)
    * [3.1.12 UserMetadata](#usermetadata)
* [4.0 Payment Processing](#payment)
  * [4.1 Stripe](#stripe)
  * [4.2 PayPal](#paypal)
* [5.0 Push Notifications](#push)
* [6.0 Roadmap](#needs)
* [7.0 Conclusion](#conclusion)

<hr>

<a name="vision"/>
## 0.0 Vision

Although we may (in an alternate Universe, of course) enjoy pilfering your hard work, laughing maniacally and sipping Champagne Framboise from deep within our evil underground lair, that is simply not conducive to the long-term vision of Hypercycle. Hypercycle is committed to remaining **open-source forever**, with the ultimate aim of democratizing design the world over by **connecting everyone with makers** (Read more: http://www.elgami.com/blog/the-twenty-year-plan/).

Back in the day, c. 2001-02, having a dynamic blog with posts that could be generated from a simple GUI blew most people's minds. I make no exaggeration when I say that as a twelve year old I literally had the coolest website within a 5 mile radius. So what problem did Content Management Systems ultimately solve? Obviously, millions of people love to write, but at the time they lacked a medium with which to share their ideas effectively on the web without having to learn all sorts of boring and Byzantine code. Then came WordPress. Why should delivering a mobile storefront for personalized goods be any different? According to MIT's Smart Customization Group, mass customization will be a $37.5B industry by 2020 in the US alone, with 15% of clothing purchased by Americans being customized (Bain & Company, 2016); applying this same logic to worldwide B2C e-commerce apparel sales, a few crude assumptions and a rough estimate later, suggests a total market size of $294B (Statista, 2016).

Believe it or not, it doesn't take a giant factory to offer this kind of platform. Firms with as few as 10 employees are capable of providing customization services for both common and niche products alike, such as swimwear (http://www.postcardswimwear.com/) or racing drone skins (www.droneskinz.com), but often lack the technological means to deliver the product creation portion of their fulfillment service to their customers, i.e. their front-end application. This is why I created the Hypercycle social network, to help manufacturers of customized goods build up and leverage their own communities of artists, designers, and promoters to grow their brand. By constrast, brands that lack manufacturing capacity themselves can tap into various order fulfillment APIs, such as Printful's Orders API (https://www.theprintful.com/docs/orders) to sell customizable products without having to own a printer or understand the technical details of the order fulfillment process.

If you are interested in contributing to the main repository here, you could very well see your changes reflected in the Hypercycle demo app at https://play.google.com/store/apps/details?id=com.elgami.customizer&hl=en. Currently, monetization is limited to native Facebook advertisements and clothing purchases. Until further notice, 100% of all proceeds will be directly reinvested into Hypercycle software development. If you love Hypercycle and want to buy us some coffee, send some beans this a-way: https://www.paypal.me/hypercycle

| ![alt tag](http://www.elgami.com/images/hypercycle-car.jpg) |
|-----------------------------------------------------------------------------|
| Why stop at clothing? Hypercycle Supercar designed by <a href="https://ca.linkedin.com/in/parker-langlois-02592bb5">Parker Langlois</a> |

Open-source is tantalizing for precisely the reason that you can never possibly predict what might emerge as a result of your contributions. In time we might reach out to new platforms, from Android to iOS, to Google Daydream, Oculus and the rest. In the end, I believe that everyone should be able to have their say when it comes to designing the products they love. So why stop at clothing? Currently, Hypercycle connects designers of original art with producers of all-over sublimation print and screen-printed apparel, including yoga pants, t-shirts, racing drone skins, sweatshirts, and more. For the less artistically inclined, our users are able to leverage simple procedural algorithms to create wild and whacky pieces of art with just a swipe and a tap. I can only imagine what we come up with next.

* ###### Bain & Company. 2013. Making it personal: Rules for success in product customization. http://www.bain.com/Images/BAIN_BRIEF_Making_it_personal.pdf

* ###### Statista. 2016. Statistics and Facts about Global E-Commerce. http://www.statista.com/topics/871/online-shopping/

| ![alt tag](http://www.elgami.com/blog/wp-content/uploads/2015/10/blog-image-7.png) |
|-----------------------------------------------------------------------------|
| Capri Leggings designed in Hypercycle™. Model: Kayla DeLancey (https://www.instagram.com/kayladelancey/), photographed by Bryon Adkins (https://www.instagram.com/badkinsmedia/) |

<hr>

```diff
- WARNING: We are currently in the process of writing the minimum installation specifications for Hypercycle, and will publish the actual source code after we have completed the documentation below. We don't expect this to take too much longer. If you have any questions, comments, or issues, please feel free to ask away. If you would like to contribute, get in touch!
```
