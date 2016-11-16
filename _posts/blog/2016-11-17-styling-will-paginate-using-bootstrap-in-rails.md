---
layout: post
title: "Styling will_paginate using bootstrap themes in rails"
excerpt: "Give a beautiful UI to will_paginate in rails."
categories: articles
tags: [will_paginate, bootstrap, rails, UI, styling]
author: shilpi_agrawal
date:   '2016-11-17 01:14:11 +0530'
comments: true
share: true
modified: '2016-11-17 01:14:11 +0530'
image:
  feature: pagination.jpg
---

Implemented pagination in rails using will_paginate, struggling to design it beautifully but stuck with tradtional UI. Many gems js plugins are there, but confused on what to use and should work out in first go. There is an amazing gem which will solve your problem in minutes. [will_paginate-bootstrap](https://rubygems.org/gems/will_paginate-bootstrap) makes your task very easy.

Today we will see how to style our pagination using will_paginate-bootstrap.

Add required gem to your Gemfile

```ruby
 gem 'will_paginate-bootstrap'
```

and run this in your command line.

```shell
bundle install
```

Now, its time to expeience the real magic. If you have a variable ```@posts```, which your are using for pagination.

```
  <%= will_paginate @posts, renderer: BootstrapPagination::Rails %>
```

If everything goes successfully, you will get something like this

<figure>
	<img src="/images/pagination_result.png">
</figure>


For changing colors or design you have to override some defined classes. For example, to change the
color of text written in block.

```css
.pagination li a {
  color: red;
}
```

Similarly we can override everything defined under the class ```pagination```.

This has been tested with rails 4+ and rails 5+.

Thank you for reading it out. If it has worked for you. Don't forget to 'Share'.
