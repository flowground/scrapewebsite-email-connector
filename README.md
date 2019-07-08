# ![LOGO](logo.png) Scrape Website Email API **flow**ground Connector

## Description

A generated **flow**ground connector for the Scrape Website Email API API (version 0.1).

Generated from: https://api.apis.guru/v2/specs/scrapewebsite.email/0.1/swagger.json<br/>
Generated at: 2019-07-08T14:35:57+03:00

## API Description

ScrapeWebsiteEmail is a service that exposes an api to fetch e-mails from a website.<br/>

## Authorization

This API does not require authorization.

## Actions

### Returns whether the system is up.
<blockquote><p>Returns 'pong' if the site is up</p></blockquote>

*Tags:* `ping`

### Returns a list of emails scraped by priority (ie. e-mails appear on top level pages are first). Please note that subsequent calls to the same url will be fetched from the <b>cache</b> (14 day flush). <br/><br/>Will also parse patterns such as hello[at]site.com, hello[at]site[dot]com, hello(at)site.com, hello(at)site(dot)com, hello @ site.com, hello @ site . com. <br/><br/>Please do note we cannot parse sites that require a login (for now), so for some Facebook pages it is not possible at the moment to fetch the e-mail.<br/><br/>Finally, please note that the api will fetch links for up to 2 minutes. After that time it will start analysing the pages which have been scraped. <b>Therefore</b> please ensure that your client has a timeout of at least <b>150 seconds</b> (2 mins to fetch and the rest to parse). <br/><br/><b>Please note</b> that due to the fact that the api goes out to fetch the pages, the server allows only 1 concurrent request/ip. Requests which are made while the 1 request is still processing will result in a 429 code.<br/><br/><b>Please note</b> that as of May 25, 2014, the main mechanism of tracking usage will be done via Mashape. You can get the free calls by signing up with the FREE plan.<br/><br/>Please visit <a href='https://www.mashape.com/tommytcchan/scrape-website-email'>https://www.mashape.com/tommytcchan/scrape-website-email</a>.<br/><br/><b>There is now a limit of 5 requests per day using this sample interface.</b><br/><br/>

*Tags:* `scrape_emails`

#### Input Parameters
* `website` - _required_ - <p>The website (ie. www.soundflair.com)</p>
* `must_include` - _optional_ - <table>
  <tbody>
    <tr>
      <td>Optional. The word(s) that the webpage must include (otherwise it will skip scraping that page). Good if you want to scrape only contact pages. Takes regex (ie. about</td>
      <td>contact).</td>
    </tr>
  </tbody>
</table>

### Attempts to grab the google store url or the ios store url for a site, after searching through the site.

*Tags:* `scrape_store_links`

#### Input Parameters
* `website` - _required_ - <p>The website (ie. www.soundflair.com)</p>

## License

**flow**ground :- Telekom iPaaS / scrapewebsite-email-connector<br/>
Copyright © 2019, [Deutsche Telekom AG](https://www.telekom.de)<br/>
contact: flowground@telekom.de

All files of this connector are licensed under the Apache 2.0 License. For details
see the file LICENSE on the toplevel directory.
