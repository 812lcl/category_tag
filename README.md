category_tag
============

categores list and cloud


Description:
------------
Easy output categores cloud and list.

Files:
------
    .
    ├── plugins
    │   ├── category_generator.rb
    │   ├── category_list.rb
    │   └── category_tag_cloud.rb
    └── source
        ├── _include
	│   └── custom
	│       └── asides
	│           ├── category_cloud.html
	│           └── category_list.html
	└── javascripts
	    └── tagcloud.swf

Syntax:
-------
    {% category_cloud [counter:true] %}
    {% category_list [counter:true] %}

Example:
--------
In some template files, you can add the following markups.

### source/_includes/custom/asides/category_list.html ###

    <section>
        <h1>Category List</h1>
            <ul id="categories">{% category_list %}</ul>
    </section>
    
### source/_includes/custom/asides/category_cloud.html ###

    <section>
        <h1>Category Cloud</h1>
            <span id="Category-cloud">{% category_cloud bgcolor:#f2f2f2 %}</span>
    </section>

Notes:
------
Be sure to insert above template files into `default_asides` array in `_config.yml`.
