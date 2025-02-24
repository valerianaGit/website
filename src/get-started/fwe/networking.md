---
title: Networking and data
description: Learn how to network your Flutter app.
prev:
  title: Handling user input
next:
    title: Local data and caching
---

While it's said that "no man is an island",
a Flutter app without any networking capability can feel a tad disconnected.
This page covers how to add networking features to your Flutter app.
Your app will retrieve data, parse JSON into usable in memory representations,
and then send data out again.

## Introduction to retrieving data over the network

The following two tutorials introduce you to the
[`http`][] package, which enables your app to make
[HTTP][] requests with ease, whether you are running on Android,
iOS, inside a web browser, or natively on Windows, macOS, or Linux. 
The first tutorial shows you how to make an unauthenticated `GET` request
to a website, parse the retrieved data as `JSON` and then display the resulting data.
The second tutorial builds on the first by adding authentication headers,
enabling access to web servers requiring authorization.
The article by the Mozilla Developer Network (MDN)
gives more background on how authorization works on the web.

* Tutorial: [Fetch data from the internet][]
* Tutorial: [Make authenticated requests][]
* Article: [MDN's article on Authorization for websites][]

## Making data retrived from the network useful

Once you retrieve data from the network,
you need a way to convert the data from the network
into something that you can easily work with in Dart.
The tutorials in the previous section used hand rolled Dart
to convert network data into an in-memory representation. 
In this section, you'll see other options for handling this conversion.
The first links to a YouTube video showing an overview of the [`freezed` package][]. 
The second links to a codelab that covers patterns and records
using a case study of parsing JSON. 

* YouTube video: [Freezed (Package of the Week)][]
* Codelab: [Dive into Dart's patterns and records][]

## Going both ways, getting data out again

Now that you've mastered the art of retrieving data, it's time to look at pushing data out.
This information starts with sending data to the network, but then dives into asynchronicity.
The truth is, once you are in a conversation over the network,
you'll need to deal with the fact that web servers that are physically far away
can take a while to respond, and you can't stop rendering to the screen
while you wait for packets to round trip.
Dart has really great support for asynchronicity, as does Flutter.
You'll learn all about Dart's support in a tutorial,
then see Flutter's capability covered in a Widget of the Week video.
Once you complete that, you'll learn how to debug
network traffic using DevTool's Network View.


* Tutorial: [Send data to the internet][]
* Tutorial: [Asynchronous programming: futures, async, await][]
* YouTube video: [FutureBuilder (Widget of the Week)][]
* Article: [Using the Network View][]

## Extension material

Now that you've mastered using Flutter's networking APIs,
it helps to see Flutter's network usage in context.
The first codelab (ostensibly on creating Adaptive Apps in Flutter),
uses a web server written in Dart to work around the web browsers'
[Cross-Origin Resource Sharing (CORS) restrictions][].
Next, a long-form YouTube video where Flutter DevRel alumnus,
Fitz, talks about how the location of data matters for Flutter apps.
Finally, a really useful series of articles by Flutter GDE
Anna (Domashych) Leushchenko covering advanced networking in Flutter.

* Codelab: [Adaptive Apps in Flutter][]
* Video: [Keeping it local: Managing a Flutter app's data][]
* Article series: [Basic and advanced networking in Dart and Flutter][]


[Adaptive Apps in Flutter]: {{site.codelabs}}/codelabs/flutter-adaptive-app
[Asynchronous programming: futures, async, await]: {{site.dart-site}}/codelabs/async-await
[Basic and advanced networking in Dart and Flutter]: {{site.medium}}/tide-engineering-team/basic-and-advanced-networking-in-dart-and-flutter-the-tide-way-part-0-introduction-33ac040a4a1c
[Cross-Origin Resource Sharing (CORS) restrictions]: https://developer.mozilla.org/en-US/docs/Web/HTTP/CORS
[Dive into Dart's patterns and records]: {{site.codelabs}}/codelabs/dart-patterns-records
[Fetch data from the internet]: /cookbook/networking/fetch-data
[Freezed (Package of the Week)]: {{site.youtube-site}}/watch?v=RaThk0fiphA
[`freezed` package]: {{site.pub-pkg}}/freezed
[FutureBuilder (Widget of the Week)]: {{site.youtube-site}}/watch?v=zEdw_1B7JHY
[`http`]: {{site.pub-pkg}}/http
[HTTP]: https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview
[Keeping it local: Managing a Flutter app's data]: {{site.youtube-site}}/watch?v=uCbHxLA9t9E
[Make authenticated requests]: /cookbook/networking/authenticated-requests
[MDN's article on Authorization for websites]: https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Authorization
[Using the Network View]: https://docs.flutter.dev/tools/devtools/network
[Send data to the internet]: https://docs.flutter.dev/cookbook/networking/send-data