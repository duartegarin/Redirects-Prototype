# Overview
This small proof of concept prototype illustrates an approach where we have multiple websites from different domains and we want to redirect specific urls to a specific urls in the one destination site.

We basically leverage the new If conditional where have a set of redirects within each domain.

# Examples
To illustrate this scenario I create some examples, but before you can run this you need to:

- Configure the source domains in your hosts file (in my case au.redirects.com and nz.redirects.com)
- Configure the source domains in your virtual hosts (so that requests from that domain get redirected to your webroot)

Once you have this in place you can test the examples:

## Redirect old url in AU sites to new url in new site
- If you access au.redirects.com.au/oldfile.html then you should get directed to redirect.dev/test_au.html
- If you access au.redirects.com.au/oldfile2.html then you should get directed to redirect.dev/test_au2.html

## Redirect old url in NZ sites to new url in new site
- If you access nz.redirects.com.au/oldfile.html then you should get directed to redirect.dev/test_nz.html
- If you access nz.redirects.com.au/oldfile2.html then you should get directed to redirect.dev/test_nz2.html
