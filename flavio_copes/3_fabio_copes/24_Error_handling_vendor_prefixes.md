## 43. Error handling

CSS is resilient. When it finds an error, it does not act like JavaScript which packs up all its things and goes away altogether, terminating all the script execution after the error is found.

CSS tries very hard to do what you want.

If a line has an error, it skips it and jumps to the next line without any error. If you forget the semicolon on one line:

```css
p { 
  font-size: 20px 
  color: black; 
  border: 1px solid black; 
} 
```

The line with the error AND the next one will not be applied, but the third rule will be successfully applied on the page. Basically, it scans all until it finds a semicolon, but when it reaches it, the rule is now `color: black;`, which is invalid, so it skips it.

Sometimes it's tricky to realize there is an error somewhere, and where that error is, because the browser won't tell us.

This is why tools like **CSS Lint** exist.

## 44. Vendor prefixes

Vendor prefixes are one way browsers use to give us CSS developers access to newer features not yet considered stable.

Before going on, keep in mind this approach is declining in popularity, in favor of using experimental flags, which must be enabled explicitly in the user's browser.

Why? Because developers, instead of considering vendor prefixes as a way to preview features, shipped them in production - something considered harmful by the CSS Working Group.

Mostly because once you add a flag and developers start using it in production, browsers are in a bad position if they realize something must change. With flags, you can't ship a feature unless you can push all your visitors to enable that flag in their browser (just joking, don't try).

That said, let's see what vendor prefixes are.

I specifically remember them for working with CSS Transitions in the past. Instead of just using the `transition` property, you had to do this:

```css
.myClass { 
  -webkit-transition: all 1s linear; 
  -moz-transition: all 1s linear; 
  -ms-transition: all 1s linear; 
  -o-transition: all 1s linear; 
  transition: all 1s linear; 
} 
```

Now you just use:

```css
.myClass { 
  transition: all 1s linear; 
} 
```

Since the property is now well supported by all modern browsers.

The prefixes used are:
- `-webkit-` (Chrome, Safari, iOS Safari / iOS WebView, Android)
- `-moz-` (Mozilla Firefox)
- `-ms-` (Edge, Internet Explorer)
- `-o-` (Opera, Opera Mini)

Since Opera is Chromium-based and Edge will soon be too, `-o-` and `-ms-` will probably go out of fashion. But as we said, vendor prefixes as a whole are going out of fashion, too.

Writing prefixes is hard, mostly because of uncertainty. Do you actually need a prefix for one property? Several online resources are outdated, too, which makes it even harder to do right. Projects like **Autoprefixer** can automate the process in its entirety without us needing to find out if a prefix is needed anymore, or if the feature is now stable and the prefix should be dropped. It uses data from **caniuse.com**, a very good reference site for all things related to browser support.

If you use React or Vue, projects like **create-react-app** and **Vue CLI**, two common ways to start building an application, use Autoprefixer out of the box, so you don't even have to worry about it.

