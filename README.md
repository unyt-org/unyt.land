<h1 align="center">unyt.land - Open Source CDN</h1>

<p align="center">
  <img src="https://cdn.unyt.org/unyt-resources/logos/unyt/light-transparent.svg" alt="unyt.land-logo" width="128px" height="128px"/>
  <br>
  <i>
    A super-fast CDN, that acts as the gateway to seamless TypeScript module loading directly in the browser.<br/>
    Use Deno modules and open-source TypeScript code in your browser in a matter of seconds.
  </i>
  <br>
</p>

<p align="center">
  <a href="https://unyt.land"><strong>unyt.land</strong></a>
  <br>
</p>

<p align="center">
  <a href="https://docs.unyt.org">Public Docs</a>
  ·
  <a href="https://unyt.blog/">Blog</a>
  ·
  <a href="https://unyt.org/twitter">@jsDelivr</a>
  ·
  <a href="https://unyt.org/discord">Discord</a>
  <br>
  <br>
</p>
<hr>

**We appreciate your feedback.** Please report issues if you encounter bugs or unexpected behaviour.<br/>Feel free to hit us up if you have an idea you'd like to discuss! ❤️

unyt.land is a free CDN for open-source files with included TypeScript / SASS transpiler. Our goal is to provide a reliable CDN service to open-source web projects out there.


# Why unyt.land?
In the world of web development, one of the most significant hurdles we face is the need to transpile TypeScript to JavaScript before running it in the browser.
We want to eliminate this step altogether and work directly with TypeScript imports that are compiled on the fly via our CDN.

# Features
Our service comes equipped with those exciting features:
* Automatic on-the-fly compilation
* TypeScript support
* SASS support
* JSX support ([UIX](https://uix.unyt.org) import source)
* ~~SourceMaps~~ (currently in development)

This means you can effortlessly load modules from common providers such as [deno.land](https://deno.land) or [GitHub](https://github.com) in the browser - just rename deno.land to unyt.land!


# How to use unyt.land?
1. Refactor your `deno.land` imports to use `unyt.land` instead:
	
2. If you plan to run a module on both *deno* and *browser* environments, please make sure that the module **does not** use [deno-only APIs](https://deno.land/api@v1.37.2) (such as FileSystem or Network). Otherwise please polyfill those functionality for the browser environment to avoid runtime exceptions.
3. *You are ready!* Enjoy improved performance, reusability and efficiency with automatic TypeScript compilation provides by [unyt.land](https://unyt.land).

## Deno
This one is pretty easy - refactor your `deno.land` imports to use `unyt.land` instead!

```ts
import mod from "https://deno.land/x/mod.ts"
```
to
```ts
import mod from "https://unyt.land/x/mod.ts"
```


### Load any deno release
You may pass module, version and file path to `https://unyt.land/x/` to request the corresponding deno module.
The Deno namespace polyfill for browsers gets automaticially injected.
```
https://unyt.land/x/module@version/file.ts
```

### Load a specific verion (xml2js@1.0.0)
```
https://unyt.land/x/xml2js@1.0.0/mod.ts
```

### Load without deno polyfill (not recommended)
```
https://unyt.land/x/xml2js@1.0.0/mod.ts?raw
```

### Load latest version
```
https://unyt.land/x/xml2js/mod.ts
```


## GitHub
You may load any GitHub release, commit, or branch via `https://unyt.land/gh/` by passing user, repo, version and file path.

### Load any GitHub file
```
https://unyt.land/gh/user/repo@version/file
```

### Load a specific verion (command-line-args@v0.0.3)
```
https://unyt.land/gh/unyt-org/command-line-args@v0.0.3/main.ts
```

### Load latest version
```
https://unyt.land/gh/unyt-org/command-line-args/main.ts
```


## Other
You may load any other web import using `https://unyt.land/web/` by passing the URL.<br/>
Load the icon under "https://unyt.org/favicon.ico" throught the unyt.land proxy:
```
https://unyt.land/web/https://unyt.org/favicon.ico
```

# Conclusion
In an age where efficient development is paramount, "unyt.land" emerges as a powerful ally for web developers. It bridges the gap between TypeScript and the browser, facilitating smoother, faster, and more efficient development. Give "unyt.land" a try and experience the future of web development today ❤️!


# Privacy Policy

unyt.land might use information about downloaded files to build download stats per project and per file. We don't store user data and do never track users in any way.<br/>
Read more [here](https://unyt.org/privacy).


---

<sub>&copy; unyt 2023 • [unyt.org](https://unyt.org)</sub>
