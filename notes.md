HTML
- An HTML document is just a Text Document.

Agent [CONCEPTUAL ASIDE]
- Something that acts on someone else's behalf

User Agent [CONCEPTUAL ASIDE] 
- Software that acts on user's behalf.
- User needs to access documents on the internet. User agent facilitates making request and delivering response to user. 
- "User" <-> "User Agent" <-> "Documents on the internet"
- User agent can deliver information in a number of format(NOT JUST DIGITAL WEB PAGE TO SEE)
- Browsers: Delivers digital info
- Screen readers:Delivers info via spoken word
- Google bot: Reads info on internet, categorizes it and makes it available for Google search engine.

- Using HTML, we'll be creating documents which will be requested by Users.
- Our job is to help "User Agents" deliver the contents of our document in the most understandable, accurate way possible so that all users can benifit from it.

M in HTML
- ![image](https://user-images.githubusercontent.com/7345634/206625959-a66bfbbd-a832-4e79-aca2-1eff64e71cd6.png)
- Consider the text document above, how do we add more meaning to it? What does different sections/lines represent?
- Tags: (start tag and end tag)
  - A way to "markup" the document that is friendly to "user agents" and easy for "humans" to read and write.
  - The "markup" describes the document.
  - By "marking up" a document, you are trying to add meaning.

L in HTML
- What if different people use different markup to mean same thing? It would cause a consistency problem.
- We need to speak the same language. Hence we need a "markup language" to "communicate meaning", which will provide:
- Consistent vocabulary
- Can convey meaning clearly
- Exists to facilitate communication
- When learning, we can got to a dictionary and look it up!

Semantics [CONCEPTUAL ASIDE]
- Having to do with meaning
- "Sachin Jogi" - consider this line in the doc. They are just words.
- <name>Sachin Jogi</name> - we're using tag to convey that this is the name of something.
- Thus this markup(Tag) is semantic.
- It's not saying let's make it big, make it yellow.
- It is describing the document conceptually.
- Even if I don't write the name, I'm contributing to the authorship of the document, by adding tags. So I'm Authoring

Author [CONCEPTUAL ASIDE]
- To contribute to writing a document.
- Adding meaning(being concerned with semantics) is a part of authoring.
- We're not just writing content. We're also making sure that the content is understood and that's a part of authoring.

Vocabulary of Markup: TAGS, ATTRIBUTES, ELEMENTS
- TAGS:
  - Sachin - some text in our document
  - <name>Sachin</name> - we've added some meaning to the text via TAG
- ATTRIBUTES:
  - We can add other related pieces of information/instructions to the tag via attributes. e.g., type="first" nickname="true"
- ELEMENTS:
  - <name type="first" nickname="true">Sachin</name> - this entire block of tags with attributes and its content is called an Element.

ELEMETS and TREES
- <name><firstname>Sachin</firstname><lastname>Jogi</lastname></name>
- Though our name is marked up, it's not formatted. It's difficult to see the tree structure.
- A well formatted mark up makes the relationship with the underlying data structure easy to see at just a glance.. e.g., below:
```
  <name>
      <firstname>
        Sachin
      </firstname>
      <lastname>
        Jogi
      </lastname>
  </name>
```

Markup is Everywhere
- If you rename a .docx file to .zip and open it in an editor, you can see that it consists of a number of files.
- If you open one of the .xml files within it, you can see the markup language used by word - which is specific to Word files(wordML)
- So markup language is a proven technology.

Specification["spec"] [CONCEPTUAL ASIDE]
- A Standard of precise requirements
- Internet technologies are governed by many specs. E.g., HTML spec, CSS spec.

Normative, Non normative [BIG WORD]
- Normative: Establishing a standard. Rules that we must be following
- Non-normative: this is not the actual spec, this is us just explaining the spec to you with great examples.

Author and Implementor [CONCEPTUAL ASIDE]
- Author: WRiting and adding meaning to the document.
- Implementor: Creating a user agent which will communicate the document to the user.

Content model:
- What is allowed to go inside "each element" - <name>what should be allowed here.</name>

Document Types:
<!DOCTYPE html>
- Required for Legacy reason(for older version of HTML)
- If not specified, browsers tend to use a different rendering mode which is not compatible with some specs.
- If specified, browsers makes best effort to follow the relevant specs.

The Root:
<html></html>
- html element is the root of the HTML document.
- Authors are encouraged to specify "lang" attr on the root html element.
  - This aids in speech synthesis(what pronunciations to use)
  - Translation tools(what rules to use).

Metadata:
<head></head>
