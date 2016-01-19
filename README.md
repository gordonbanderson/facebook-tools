##Functionality
[![Build Status](https://travis-ci.org/gordonbanderson/facebook-tools.svg?branch=master)](https://travis-ci.org/gordonbanderson/facebook-tools)
[![Scrutinizer Code Quality](https://scrutinizer-ci.com/g/gordonbanderson/facebook-tools/badges/quality-score.png?b=master)](https://scrutinizer-ci.com/g/gordonbanderson/facebook-tools/?branch=master)
[![Code Coverage](https://scrutinizer-ci.com/g/gordonbanderson/facebook-tools/badges/coverage.png?b=master)](https://scrutinizer-ci.com/g/gordonbanderson/facebook-tools/?branch=master)
[![Build Status](https://scrutinizer-ci.com/g/gordonbanderson/facebook-tools/badges/build.png?b=master)](https://scrutinizer-ci.com/g/gordonbanderson/facebook-tools/build-status/master)
[![codecov.io](https://codecov.io/github/gordonbanderson/facebook-tools/coverage.svg?branch=master)](https://codecov.io/github/gordonbanderson/facebook-tools?branch=master)

[![Latest Stable Version](https://poser.pugx.org/weboftalent/facebook-tools/version)](https://packagist.org/packages/weboftalent/facebook-tools)
[![Latest Unstable Version](https://poser.pugx.org/weboftalent/facebook-tools/v/unstable)](//packagist.org/packages/weboftalent/facebook-tools)
[![Total Downloads](https://poser.pugx.org/weboftalent/facebook-tools/downloads)](https://packagist.org/packages/weboftalent/facebook-tools)
[![License](https://poser.pugx.org/weboftalent/facebook-tools/license)](https://packagist.org/packages/weboftalent/facebook-tools)
[![Monthly Downloads](https://poser.pugx.org/weboftalent/facebook-tools/d/monthly)](https://packagist.org/packages/weboftalent/facebook-tools)
[![Daily Downloads](https://poser.pugx.org/weboftalent/facebook-tools/d/daily)](https://packagist.org/packages/weboftalent/facebook-tools)

[![Dependency Status](https://www.versioneye.com/php/weboftalent:facebook-tools/badge.svg)](https://www.versioneye.com/php/weboftalent:facebook-tools)
[![Reference Status](https://www.versioneye.com/php/weboftalent:facebook-tools/reference_badge.svg?style=flat)](https://www.versioneye.com/php/weboftalent:facebook-tools/references)

![codecov.io](https://codecov.io/github/gordonbanderson/facebook-tools/branch.svg?branch=master)
* Add a like button to any page
* Add a facebook like box to any page
* Add facebook metadata to any page

## Installation
    composer require "weboftalent/facebook-tools:~1"

The name of the output directory does not matter

## Usage
### Site Configuration
A 'Facebook Metadata' tab will now appear in the Site Config.  There you can upload an image that will be shown in Facebook when a link from the site is provided.  Otherwise facebook tries to guess from the content.

### Templates

#### Facebook API
Add the following to your Page templates, after the body tag.

    <% include DownloadFacebookJS %>

This will provide the Javascript required to load the Facebook API.  It is a necessary step for what follows.

#### Like Button
Insert the following where you would like the Like Button to appear

	<% include FacebookLikeButton %>

#### Facebook Metadata
In the head section of your Page template, insert the following:

	<% include FacebookMetadata %>

This will provide basic metadata extracted from existing page information, and also add the logo if you have provided one in the SiteConfig 'Facebook Metadata' tab.

### Content Types
#### FacebookLikeBoxPage
Create a page of type 'Facebook Like Box Page'.  In the Facebook tab, enter the URL of your page (e.g. http://www.facebook.com/WebOfTalentLtd).  If you do not do this an error message will appear on the page in the public version of the site.


## Silverstripe Version Compatibility
2.4 only (tested with 2.4.5+) - stable24 branch
3.1
