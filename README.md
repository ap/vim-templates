This is a Vim plugin for providing filetype-dependent templates for new files, using a simple but effective mechanism.


Usage
-----

When you start a fresh buffer, setting a `filetype` on it will load the corresponding template. E.g. open Vim and issue

    :setf html

You should find a skeleton HTML file, ready to fill in.

One new command has been added for convenience: it is called `:New` and takes exactly one argument. It will open a new empty window and set the filetype for it to the argument given.

A handful of templates are included, but the real purpose of the plugin is to allow you to easily create your own.


Creating templates
------------------

Templates are kept in `.vim/templates`. The template filename must be equal to the `filetype`. So when you set the filetype of an empty buffer to `html`, `.vim/templates/html` will be loaded. It's that simple.

In the templates, you can use a `cursorline` directive to specify a position for the cursor after loading the template. Such a cursorline works much like a modeline: the word `cursor:` must appear, followed by one or two numbers and opionally the word `del`, all separated by whitespace. The first number specifies the line the cursor will be placed in. The second, if present, specifies a column. The optional word `del` directs the script to remove the cursorline at load time. Take a look at the templates supplied in the package, it should be fairly self-explanatory.
