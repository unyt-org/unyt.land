<h1 align="center">unyt.land - TypeScript for web</h1>

<p align="center">
  <img src="https://cdn.unyt.org/unyt-resources/logos/unyt/light-transparent.svg" alt="unyt.land-logo" width="128px" height="128px"/>
  <br>
  <i>
    Our super-fast CDN that enables seamless TypeScript module loading directly in the browser.<br/>
    Use <a href="https://deno.com">Deno</a> modules from <a href="https://jsr.io">JSR</a> or <a href="https://deno.land">deno.land</a> and open-source TypeScript code in your browser in a matter of seconds.
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
  <a href="https://unyt.org/twitter">Twitter</a>
  ·
  <a href="https://unyt.org/discord">Discord</a>
  <br>
  <br>
</p>


<hr>


[unyt.land](https://unyt.land) is a free CDN with automatic TypeScript / SCSS transpilation. Our goal is to provide a reliable CDN service for open-source web projects out there.


# Why unyt.land?
In the world of web development, one of the most significant hurdles we face is the need to transpile TypeScript to JavaScript before running it in the browser.
We want to eliminate this step altogether and work directly with TypeScript imports that are compiled on the fly via our CDN.

# Features
Our service comes equipped with those exciting features:
* Automatic on-the-fly compilation
* TypeScript support
* SCSS support
* JSX support ([UIX](https://uix.unyt.org) import source)
* ~~SourceMaps~~ (currently in development)

This means you can effortlessly load modules from common providers such as [JSR](https://jsr.io), [deno.land](https://deno.land) or [GitHub](https://github.com) in the browser.


# How to use unyt.land?

## deno.land
This one is pretty easy - refactor your `deno.land` imports to use `unyt.land` instead!

```ts
import mod from "https://deno.land/x/mod.ts"
```
to
```ts
import mod from "https://unyt.land/x/mod.ts"
```

> [!Warning]
> `unyt.land` automatically injects [a polyfill](https://github.com/unyt-org/deno-web-polyfill) to provide `Deno.*` APIs in the browser.
> This polyfill is experimental and does not yet implement all Deno APIs correctly.


### Load a specific version (xml2js@1.0.0)
```Email
https://unyt.land/x/xml2js@1.0.0/mod.ts
```

### Load std modules (csv@0.208.0)
```Email
https://unyt.land/std@0.208.0/csv/mod.ts
```

### Load latest version
```Email
https://unyt.land/x/xml2js/mod.ts
```

```Email
https://unyt.land/std/csv/mod.ts
```

### Load without deno polyfill (not recommended)
```Email
https://unyt.land/x/xml2js@1.0.0/mod.ts?raw
```

## JSR
You can load any JSR release via `https://unyt.land/@<scope>/<package>/<version>/<path>` by passing scope, package and optionally the package version and file path.


> [!Warning]
> `unyt.land` automatically injects [a polyfill](https://github.com/unyt-org/deno-web-polyfill) to provide `Deno.*` APIs in the browser.
> This polyfill is experimental and does not yet implement all Deno APIs correctly.

### Load a specific release (@luca/flag) in version 1.0.0
```Email
https://unyt.land/@luca/flag/1.0.0/main.ts
```

### Load latest version (@oxi/core)
```Email
https://unyt.land/@oxi/core
```

## GitHub
You can load any GitHub release, commit, or branch via `https://unyt.land/gh/` by passing user, repo, version and file path.

### Load any GitHub file
```Email
https://unyt.land/gh/user/repo@version/file
```

### Load a specific verion (command-line-args@v0.0.3)
```Email
https://unyt.land/gh/unyt-org/command-line-args@v0.0.3/main.ts
```

### Load latest version
```Email
https://unyt.land/gh/unyt-org/command-line-args/main.ts
```


## Other
You can load any other web import using `https://unyt.land/web/` with the URL appended to the path.<br/>
Load the icon under "https://unyt.org/favicon.ico" throught the unyt.land proxy:
```q
https://unyt.land/web/https://unyt.org/favicon.ico
```

**We appreciate your feedback.** Please report issues if you encounter bugs or unexpected behaviour.<br/>Feel free to hit us up if you have an idea you'd like to discuss! ❤️


# Privacy Policy

unyt.land might use information about downloaded files to build download stats per project and per file. We don't store user data and do never track users in any way.<br/>
Read more [here](https://unyt.org/privacy).

---



<sub>&copy; unyt 2024 • [unyt.org](https://unyt.org)</sub>
