# Locale-specific links

Locale codes, such as `en-us`, should not be included in links to certain Microsoft sites. If you include a locale code in a link in English content, it will also be included in localized links, which leads to a bad localized experience. For example, if a link in German localized content includes `en-us`, German customers will find themselves linking to the English article, even if a German version is available.

Remove locale codes from links to Microsoft sites. The following is an example.

Before:

`https://docs.microsoft.com/en-us/vsts/load-test/app-service-web-app-performance-test`

After:

`https://docs.microsoft.com/vsts/load-test/app-service-web-app-performance-test`

The following sites are in scope for this validation:

- azure.microsoft.com
- docs.microsoft.com
- msdn.microsoft.com
- technet.microsoft.com