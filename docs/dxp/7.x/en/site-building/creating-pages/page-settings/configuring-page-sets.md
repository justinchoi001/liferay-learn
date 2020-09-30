# Configuring Page Sets

Page Sets are a grouping of pages in a DXP Site; these pages can be either Public or Private pages. Users can configure Page Set settings which apply to all its pages and thus override options at the Site level. However, [customizations to an individual page](./page-configuration-ui-reference.md) override those for the Page Set.

To access the Page Sets' settings:

1. Navigate to the _Product_ (![Product menu](../../../images/icon-product-menu.png)) menu &rarr; _Site Builder_ &rarr; _Pages_.
1. Click the Gear icon next _Public Pages_. (Alternately, you can also modify the site's _Private Pages_ Page Set.)

![Navigate to the Public Pages' Page Sets Options.](./configuring-page-sets/images/01.png)

## Configuring the Page Set's Look and Feel

On the _Look and Feel_ tab, you can customize your site's Page Sets' Look and Feel and the Site Logo.

### Look and Feel

Themes create the overall feel for the Site and can transform the look entirely. The _Current Theme_ section displays the Theme currently applied to the Page Set, along with any configurable theme settings and color schemes that the Theme has. Many Themes include more than one color scheme, which keeps the existing look and feel while giving the Site a different flavor.

![Figure 2: The Look and Feel interface allows you to choose a theme for the current site.](./configuring-page-sets/images/02.png)

To change the current theme:

1. Click the _Change Current Theme_ button and select the Theme from the window that appears.
1. Select your desired theme.

    ![Choose from one of the available themes.](./configuring-page-sets/images/05.png)

1. Click _Save_ to apply the new Theme to the Page Set.

You can enter custom CSS in the *CSS* section for modifying your theme. You can apply Themes to the entire Site (described here) or to individual pages (described in [Configuring Pages](./page-configuration-ui-reference.md#look-and-feel))

### Logo

By default, the Liferay logo is used for your Site's pages. To use your own logo for a Site:

1. Expand the _Logo_ section.
1. Click the _Change_ button.
1. Browse to the location of your logo. Make sure your logo fits the space in the top left corner of the Theme you're using for your Site. If you don't, you could wind up with a Site that's difficult to navigate, as other page elements are pushed aside to make way for the logo.
1. Choose whether to display the Site name on the Site. When _Show Site Name_ is enabled, the Site name appears next to the logo.

  ```note::
    This option is enabled by default and can't be disabled if the *Allow Site Administrators to set their own logo* option is disabled in *Instance Settings*. Removing the Site name is not available for the default Liferay Site---you can configure this only for new Sites and User pages.
  ```

1. Click *Save* to apply the changes.

The Site's logo settings are now configured.

## Configuring the Page Set's Advanced Settings

The _Advanced_ tab contains several options that could be impact the site and overall performance. Administrators should proceed with caution.

![The Advanced tab contains multiple options that enhances your site.](./configuring-page-sets/images/03.png)

### Javascript

On the _Javascript_ tab, you can paste JavaScript in the Javascript editor. Code entered here is executed at the bottom of every page in the Site. Your site's JavaScript is most likely (and should be) included with the Theme. However, this may be a good place to quickly test JavaScript code while not in production.

### Advanced Settings

If you have multiple Sites on your Liferay Portal instance, one Site is marked as the _Default Site_ that visitors are shown when they visit the Site. By default, only the default Site's Public Pages are displayed in the navigation.

You can display the other Site's Public Pages in the default Site's navigation as well by enabling the _Merge public pages_ option for that Site.

```tip::
   Adding too many pages to the main navigation can make it become unwieldy very quickly.
```

To merge the site:

1. Check the _Merge Liferay DXP public pages_ box.

    ![You can merge your site's top level with the DXP Guest site.](./configuring-page-sets/images/04.png)

1. Click _Save_ when finished.

### Mobile Device Rules

You can add _Mobile Device Rules_ to configure behaviors for specific mobile devices or types for the Page Set. Mobile device rules are inherited from your Public Pages, but you can define specific rules per page. You can edit the Look and Feel of specific pages for mobile devices, including the theme. See [Mobile Device Rules]() for more information.

### Robots

On the _Robots_ tab, you can configure search and indexing rules in the `robots.txt` rules for the domain's public and private pages. The `robots.txt` file provides instructions to search engines and other tools that are automatically crawling and indexing your Site. For example, you can specify not to index certain pages.

### Sitemap

The _Sitemap_ section generates a sitemap you can send to some search engines so they can crawl your site. It uses the industry standard sitemap protocol. Select a search engine link to send the sitemap to it (only required once per Site), or select the _preview_ link to see the generated XML that is sent to search engines.

## Using the Page Tree Menu

In Liferay DXP 7.3, you can access the same settings from the _Page Tree_ menu. To access the Page Sets options from the _Page Tree_ menu:

1. Click the (![icon-page-tree](../../../images/icon-page-tree.png)) icon.
1. Select _Public Pages_ or _Private Pages_ from the dropdown menu.
1. Click the Gear icon.

    ![You can access the same Page Sets options from the Page Tree menu.](./configuring-page-sets/images/06.png)

## Additional Information

* [Page Configuration UI Reference](./page-configuration-ui-reference.md)
