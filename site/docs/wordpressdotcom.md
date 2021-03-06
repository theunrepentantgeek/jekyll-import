---
layout: docs
title: WordPress.com
prev_section: wordpress
link_source:  wordpressdotcom
next_section: third-party
permalink: /docs/wordpressdotcom/
---

To import your posts from a [WordPress.com](http://wordpress.com) blog, run:

{% highlight bash %}
$ ruby -rubygems -e 'require "jekyll-import";
    JekyllImport::Importers::WordpressDotCom.run({
      "source" => "wordpress.xml"
    })'
{% endhighlight %}

The `source` field is not required. Its default is what you see above.

<div class="note">
  <h5>ProTip™: WordPress.com Export Tool</h5>
  <p markdown="1">If you are migrating from a WordPress.com account, you can
  access the export tool at the following URL:
  `https://YOUR-USER-NAME.wordpress.com/wp-admin/export.php`.</p>
</div>

### Further WordPress migration alternatives

While the above method works, it does not import much of the metadata that is
usually stored in WordPress posts and pages. If you need to export things like
pages, tags, custom fields, image attachments and so on, the following resources
might be useful to you:

- [Exitwp](https://github.com/thomasf/exitwp) is a configurable tool written in
  Python for migrating one or more WordPress blogs into Jekyll (Markdown) format
  while keeping as much metadata as possible. Exitwp also downloads attachments
  and pages.
- [A great
  article](http://vitobotta.com/how-to-migrate-from-wordpress-to-jekyll/) with a
  step-by-step guide for migrating a WordPress blog to Jekyll while keeping most
  of the structure and metadata.
- [wpXml2Jekyll](https://github.com/theaob/wpXml2Jekyll) is an executable
  windows application for creating Markdown posts from your WordPress XML file.
