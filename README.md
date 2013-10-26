category_tag
============

categores/tags list and cloud


Description:
------------
Easy output categores/tag cloud and list.

Files:
------

    .
    ├─ plugins/
    │  └── category_generator.rb
    │  └── category_list.rb
    │  └── category_tag_cloud.rb
    │  └── tag_generator.rb
    │  └── tag_list.rb
    └─ source/
       └─ _includes/
          └─ custom/
             └─ asides/
                ├─ category_cloud.html
                ├─ category_list.html
                ├─ tag_cloud.html
                └─ tag_list.html

Syntax:
-------
    {% category_cloud [counter:true] %}
    {% category_list [counter:true] %}
    {% tag_cloud [counter:true] %}
    {% tag_list [counter:true] %}

Example:
--------
In some template files, you can add the following markups.

### source/_includes/custom/asides/tag_list.html ###

    <section>
        <h1>标签列表</h1>
            <ul class="tag-cloud">{% tag_list font-size: 90-210%, limit: 10, style: para %}</ul>
    </section>

### source/_includes/custom/asides/category_list.html ###

    <section>
        <h1>分类目录</h1>
            <ul id="categories">{% category_list %}</ul>
    </section>
    
### source/_includes/custom/asides/tag_cloud.html ###

    <section>
        <h1>标签云</h1>
            <span id="Tag-cloud">{% tag_cloud bgcolor:#f2f2f2 %}</span>
    </section>
    
### source/_includes/custom/asides/category_cloud.html ###

    <section>
        <h1>Tag Cloud</h1>
            <span id="Category-cloud">{% category_cloud bgcolor:#f2f2f2 %}</span>
    </section>

Notes:
------
Be sure to insert above template files into `default_asides` array in `_config.yml`.
And also you can define styles for 'tag-cloud' or 'category-list' in a `.scss` file.
(ex: `sass/custom/_styles.scss`)
