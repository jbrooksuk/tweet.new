# tweet.new

> I ([@jbrooksuk](https://x.com/jbrooksuk)) bought a `.new` domain to simplify tweeting—say hello to tweet.new, your shortcut to posting faster on X!
> [Read the full post](https://james.brooks.page/blog/tweet-new).

This repository serves as documentation on how to use the link and how it works.

## Usage

### Direct Link

Accessing `tweet.new` will redirect you straight to https://x.com/intent/post

### Tweet Sharing

Accessing `tweet.new/?text=Hello` will redirect you straight to https://x.com/intent/post but with the text already prefilled.

> [!IMPORTANT]
> You **must** URL encode the `text` query parameter.

## How does this work?

The `tweet.new` domain is configured in Cloudflare. There is a dummy DNS record so that Cloudflare can run redirect rule.

![Cloudflare DNS](https://github.com/user-attachments/assets/1550a73b-bd04-4966-b764-c9424e12a3f5)

A single redirect rule is then configured to redirect all requests from `tweet.new` to `x.com`

![Cloudflare Redirect Rule](https://github.com/user-attachments/assets/46f34351-7920-47c8-b9f8-ac16e0cab31e)

The important part here is the "Preserve query string" option being checked. This ensures that `?text={tweet}` is forwarded to the redirecting page.

## Sponsors

`.new` TLDs cost ~$400/yr. It's kind of dumb to think that we spent all of our time making browser extensions to act as shortcuts to other websites, when it's now as simple as typing `doc.new` to get a new Google Sheet, or `repo.new` to start a new GitHub repository. As funny as it was to buy this domain, I do believe there to be value in it. Websites around the internet can now link to it to easily share tweets and links alike.

I'm happy to pay to add value to the internet, but if you'd like to help keep this domain alive (and by proxy, the other things that I do), please consider [sponsoring](https://github.com/sponsors/jbrooksuk). We'll also maintain a list of sponsors here 👇
