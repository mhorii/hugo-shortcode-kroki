A tiny script, called shortcode in Hugo, to create diagrams from textual descriptions with [Kroki](https://kroki.io/)

# Installation
Just put `kroki.html` in `layouts/shortcodes`.
See [here](https://gohugo.io/templates/shortcode-templates/#file-location) if you are not familier with that.

# Parameters
A shortcode takes two parameters, `type` and `name`, and one inner text.
Here's an example:
```
{{<kroki type="plantuml" name="test">}}
hoge -> piyo: fuga
{{</kroki>}}
```
`type` is a string that is a name of service or tool to draw diagrams with textual description like `"plantuml"` and `"graphviz"`.
It actually corresponds to `diagram_type` of [Kroki](https://kroki.io/). See the document of Kroki to see which string is acceptable.

`name` is a string to identify a diagram.

Inner text, `hoge -> piyo: fuga` in the previous example, is a diagram described with a text.

# Tips
Kroki provides a way to self-host the Kroki service. If you prefer self-hosting Korki, maybe due to security reason, you can easily change the host `kroki.io` to other hosts. See the source code.

