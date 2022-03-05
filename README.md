![Digging into Turbo with Ruby on Rails 7](https://f001.backblazeb2.com/file/webcrunch/turbo-ror-7.jpg)

# Digging into Turbo with Ruby on Rails 7

When Rails 7 made its first appearance in December of 2021 a new default component was introduced called Turbo. If you have any history with Rails you might remember the Turbolinks library which is the predecessor of Turbo.

Unlike JavaScript-driven applications, Rails applications are historically server-side rendered. While you can have more real-time interactivity, it often requires a hodgepodge of techniques to make it work. Many developers were forced to reach for React or Vue.js to compensate.

Turbo is the answer to this problem.

Turbo brings new tooling to Rails apps that make them more reactive and stateful. You can still have a server-side application that responds in real-time to requests and reduce the need for a large amount of JavaScript (the main appeal for many Rails/Ruby developers).

This happens by working with specific types of requests and dynamically rendering content on a page.

With Turbo, we get the historical benefits of Turbolinks with the additional benefits of new features like Turboframes and Turbostreams. This guide is meant to give you a first look at using Turbo inside your app and how you can leverage it without needing to rely too heavily on JavaScript.

### Turbo definitions

At its core, Turbo sends HTML code over the request cycle instead of something like JSON. It's easy to confuse the different offerings of Turbo so I hope to debunk those in this guide. Let's start with some definitions.

- **Turbo Drive** - accelerates links and form submissions by negating the need for full page reloads.
- **Turbo Frames** - decompose pages into independent contexts, which scope navigation and can be lazily loaded.
- **Turbo Streams** - deliver page changes over WebSocket, SSE, or in response to form submissions using just HTML and a set of CRUD-like actions.
- **Turbo Native** - lets your majestic monolith form the center of your native iOS and Android apps, with seamless transitions between web and native sections.
For this guide, I'll be focusing on the first three in this list.
