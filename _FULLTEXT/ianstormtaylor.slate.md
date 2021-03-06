A completely customizable framework for building rich text editors. Why? · Principles · Demo · Examples · Plugins · Documentation · Contributing! Slate lets you build rich, intuitive editors like those in Medium, Dropbox Paper or Google Docs—which are becoming table stakes for applications on the web—without your codebase getting mired in complexity. It can do this because all of its logic is implemented with a series of plugins, so you arent ever constrained by what is or isnt in "core". You can think of it like a pluggable implementation of contenteditable built on top of React and Immutable. It was inspired by libraries like Draft.js, Prosemirror and Quill. Slate is currently in beta. Its useable now, but you might need to pull request a fix or two for advanced use cases. Why? Why create Slate? Well... (Beware: this section has a few of my opinions!) Before creating Slate, I tried a lot of the other rich text libraries out there—Draft.js, Prosemirror, Quill, etc. What I found was that while getting simple examples to work was easy enough, once you started trying to build something like Medium, Dropbox Paper or Google Docs, you ran into deeper issues... The editors "schema" was hardcoded and hard to customize. Things like bold and italic were supported out of the box, but what about comments, or embeds, or even more domain-specific needs? Transforming the documents programmatically was very convoluted. Writing as a user may have worked, but making programmatic changes, which is critical for building advanced behaviors, was needlessly complex. Serializing to HTML, Markdown, etc. seemed like an afterthought. Simple things like transforming a document to HTML or Markdown involved writing lots of boilerplate code, for what seemed like very common use cases. Re-inventing the view layer seemed inefficient and limiting. Most editors rolled their own views, instead of using existing technologies like React, so you have to learn a whole new system with new "gotchas". Collaborative editing wasnt designed for in advance. Often the editors internal representation of data made it impossible to use to for a realtime, collaborative editing use case without basically rewriting the editor. The repostories were monolithic, not small and reusable. The code bases for many of the editors often didnt expose the internal tooling that could have been re-used by developers, leading to having to reinvent the wheel. Building complex, nested documents was impossible. Many editors were designed around simplistic "flat" documents, making things like tables, embeds and captions difficult to reason about and sometimes impossible. Of course not every editor exhibits all of these issues, but if youve tried using another editor you might have run into similar problems. To get around the limitations of their APIs and achieve the user experience youre after, you have to resort to very hacky things. And some experiences are just plain impossible to achieve. If that sounds familiar, you might like Slate. Which brings me to how Slate solves all of that... Principles Slate tries to solve the question of "Why?" with a few principles: First-class plugins. The most important part of Slate is that plugins are first-class entities—the core editor logic is even implemented as its own plugin. That means you can completely customize the editing experience, to build complex editors like Mediums or Dropboxs, without having to fight against the librarys assumptions. Schema-less core. Slates core logic doesnt assume anything about the schema of the data youll be editing, which means that there are no assumptions baked into the library thatll trip you up when you need to go beyond the most basic use cases. Nested document model. The document model used for Slate is a nested, recursive tree, just like the DOM itself. This means that creating complex components like tables or nested block quotes are possible for advanced use cases. But its also easy to keep it simple by only using a single level of hierarchy. Parallel to the DOM. Slates data model is based on the DOM—the document is a nested tree, it uses selections and ranges, and it exposes all the standard event handlers. This means that advanced behaviors like tables or nested block quotes are possible. Pretty much anything you can do in the DOM, you can do in Slate. Stateless views and immutable data. By using React and Immutable.js, the Slate editor is built in a stateless fashion using immutable data structures, which leads to much easier to reason about code, and a much easier time writing plugins. Intuitive changes. Slate documents are edited using "changes", that are designed to be high-level and extremely intuitive to write and read, so that custom functionality is as expressive as possible. This greatly increases your ability to reason about your code. Collaboration-ready data model. The data model Slate uses—specifically how changes are applied to the document—has been designed to allow for collaborative editing to be layered on top, so you wont need to rethink everything if you decide to make your editor collaborative. Clear "core" boundaries. With a plugin-first architecture, and a schema-less core, it becomes a lot clearer where the boundary is between "core" and "custom", which means that the core experience doesnt get bogged down in edge cases. Demo Check out the live demo of all of the examples! Examples To get a sense for how you might use Slate, check out a few of the examples: Plain text — showing the most basic case: a glorified <textarea>. Rich text — showing the features youd expect from a basic editor. Auto-markdown — showing how to add key handlers for Markdown-like shortcuts. Links — showing how wrap text in inline nodes with associated data. Images — showing how to use void (text-less) nodes to add images. Hovering menu — showing how a contextual hovering menu can be implemented. Tables — showing how to nest blocks to render more advanced components. Paste HTML — showing how to use an HTML serializer to handle pasted HTML. Code Highlighting — showing how to use decorators to dynamically mark text. See all the examples... If you have an idea for an example that shows a common use case, pull request it! Plugins Slate encourages you to write small, reusable modules. Check out the public ones you can use in your project! slate-auto-replace auto-replaces text as the user types. Useful for "smart" typography! slate-collapse-on-escape simply collapses the selection when escape is pressed. slate-edit-code adds code editing behavior like tab-to-indent, and enter-to-soft-break. slate-edit-list adds rich, nested list editing behavior. slate-edit-table adds complex table editing behavior! slate-paste-linkify wraps the selected text in a link when a URL is pasted from the clipboard. slate-prism highlights code blocks with Prism.js! slate-soft-break adds a soft break when enter is pressed. slate-drop-or-paste-images lets users drop or paste images to insert them! See all the plugins... Documentation If youre using Slate for the first time, check out the Getting Started walkthroughs and the Guides to familiarize yourself with Slates architecture and mental models. Once youve gotten familiar with those, youll probably want to check out the full API Reference. Walkthroughs Guides Reference FAQ Resources If even thats not enough, you can always read the source itself, which is heavily commented. There are also translations of the documentation into other languages: 中文 If youre maintaining a translation, feel free to pull request it here! Contributing! All contributions are super welcome! Check out the Contributing instructions for more info! Slate is MIT-licensed.