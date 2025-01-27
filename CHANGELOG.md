# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.1] - 14-06-2023

### Fixed
- You can now create new feeds again after fixing a JavaScript error in the admin module.
## [2.0.0] - 13-06-2023

> ### BREAKING
> **Be aware that this is a breaking change! Besides that you need to reconfigure the frontend (see changed), the URL of your feed will also change. You can find the right URL of the feed in the Feed settingw**

### Added
- You can now define one or more feeds and decide which sales channel domains should be included. With this option you can make sure only the information that is needed will be exported to Tweakwise.
- Besides having the option to create one or more feeds, you can also create multiple frontends. These frontends holds the configuration with the instance key as well as the way of frontend implementation. As well as with feeds, you can also select sales channel domains to enable the implementation only for certain languages.

### Changed
- Some massive performance updates are done. Especially feeds with 25k products or more will benefit from this update
- The configuration of the plugin is moved from the custom fields in the sales channel properties, to the Settings > Extension module. You will find two new modules there to manage the feeds and the frontends. 

## [1.0.4] - 24-04-2023

### Fixed
- Added fallback in progressbar content to prevent critical error

### Changed
- Changed the way of defining the categories so the order of categories is as it is defined and disabled categories will not show up in the feed.
- Feed will only be generated by console command to prevent realtime generation of feed and causing performance issues

## [1.0.3] - 20-04-2023

### Changed
- Optimized the feed to only link products to categories that are exported
- Improved performance of feed generation

## [1.0.2] - 12-04-2023

### Changed
- Make the extension work from Shopware v6.4.6

### Fixed
- Removed wrong association to customField
- In the template of the feed, the price was rounded while this was already done in the generation of data which could lead to wrongly rounded prices. In the template we don't do any rounding of prices anymore.

## [1.0.1] - 31-03-2023

### Fixed
- Search is now only searching in the root category of the current shop

### Changed
- Labels on the result pages are now translated based on the language of the domain
- By changing a bit of code, we are now supporting Shopware 6.4.10 and higher
- Some inline Javascript is moved towards a dedicated JS file


## [1.0.0] - 28-03-2023

### Added
- Added automatic checks to find bugs earlier
- Made ready for Shopware store

## [0.9.6] - 28-03-2023

### Changed
- **[BREAKING]** The extension key is changed from RhTweakwise to RhaeTweakwise to comply to the rules of the Shopware store. Please make sure to install and activate the right plugin after you update the extension. 

## [0.9.5] - 27-03-2023

### Fixed
- Added right annotation for translator to prevent errors in logs 

## [0.9.4] - 27-03-2023

### Added
- Added translator to make sure labels can be translated even when the feed is built on CLI

## [0.9.3] - 27-03-2023

### Changed
- Generation of the feed is done different now. The feed is not based on a product comparison feed, but it is based on code within the plugin. If you are using the old way, this will still work, but please be aware of the new possibility of the feed. See the documentation for more information.

### Fixed
- Added some checks if we can add the custom fields of the sales channel to the page

## [0.9.2] - 07-03-2023

### Added
- A label property is now added to the product feed

### Fixed
- Fixed issue that was hiding results when submitting search form with basic javascript integration
- Resolved an issue with the subscriber throwing an error on async reloads of the frontend

## [0.9.1] - 03-03-2023

### Added
- Possibility to enable standard javascript implementation
- Added attributes new, discount and topseller to product feed

### Changed
- Added link to this changelog to the readme of the extension
- **[BREAKING]** Changed extension key from Tweakwise to RhTweakwise

### Fixed
- Exclude property group when one of the properties of that group was already set as a variant option.

## [0.9.0] - 24-02-2023

### Added
- Sales channel templates for Tweakwise product feed
