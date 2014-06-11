##Overview of the Gem

1. Bourbon is a SASS mixin library.
..*SASS (Syntactically Awesome Stylesheets Sass) is a CSS extension language that lets you use features that don't yet exist in CSS, such as variables, nesting, mixins and inheritance. It offers object-oriented mechanisms that aren't available in CSS3. Basically, it's syntactic sugar for CSS.

2. Bourbon eliminates vendor prefixes. Some are -webkit-(Android), -moz-(Firefox), and -ms- (Internet Explorer).

3. Some sites that use it are **Disney**, **Thoughtbot**, and **Breaking Bad's Danish website**.


##Examples

Bourbon<br>
`font-family: $helvetica;`<br>
CSS<br>
`font-family: "Helvetica-Neue", Helvetica, Roboto, Arial, sans-serif;`<br><br>
Bourbon<br>
`@include transition(all 0.8s);`<br>
CSS<br>
`-webkit-transition: all 0.8s;
-moz-transition: all 0.8s;
transition: all 0.8s;`<br><br>
Bourbon<br>
`section {
  @include linear-gradient(to top, red,orange);
}`<br>
CSS<br>
`section {
  background-color: red;
  background-image: -webkit-linear-gradient(bottom, red, orange);
  background-image: linear-gradient(to top, red, orange);
}`


##How to use it in Rails

1. It's available for rails 3.1+
2. Put gem 'bourbon' in Gemfile
3. Run bundle install
4. Restart server, then rename application.css to application.css.scss
5. All additional stylesheets must be imported below Bourbon, like so:
..*@import 'bourbon';
..*@import 'home';
..*@import 'users';

