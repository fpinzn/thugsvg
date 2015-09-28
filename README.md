#THUG SVG

Goes through the DOM fetching the linked svg files, and copying them inline, so you can manipulate them with js and css.

Be careful about what you link. This thug will import everything verbatim.

Wow, much thug. So danger. Very power.

##Installation

    npm install thugsvg

##Usage

    thugsvg([selector,] [cb(element)])

If you want to do it with every svg currently present in your DOM

    thugsvg()

If you want to do it for a specific selector

    thugsvg(".myClassSelector")

The callback will receive the dom element that was replaced as a parameter.

##Yes, but why?

A lot of the potential of SVG is lost when you use it as an image in html, since it can't be manipulated using js or styled using css.
The alternative turns out to be super impractical and unusable in lots of cases (inlining it in the html).
It seemed to me this was the best solution.

##Security Concerns

This way of importing SVGs probably opens the path to security vulnerabilities in the form of arbitrary code injection.
Check your SVGs before trusting them. Or not, if you are into that 💀.
