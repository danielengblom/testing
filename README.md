<style>
    .summary {
    color: #808080;
    border-left: 5px solid #ED1951;
    font-size:16px;
}


h3 {color: #ED1951; }
h4 {color: #808080; }

.nav-tabs > li.active > a, .nav-tabs > li.active > a:hover, .nav-tabs > li.active > a:focus {
    background-color: #248ec2;
    color: white;
}

.nav > li.active > a {
    background-color: #347DBE;
}

.nav > li > a:hover {
    background-color: #248ec2;
}

div.navbar-collapse .dropdown-menu > li > a:hover {
    background-color: #347DBE;
}

.nav li.thirdlevel > a {
    background-color: #FAFAFA !important;
    color: #248EC2;
    font-weight: bold;
}

a[data-toggle="tooltip"] {
    color: #649345;
    font-style: italic;
    cursor: default;
}

.navbar-inverse {
    background-color: #347DBE;
    border-color: #015CAE;
}
.navbar-inverse .navbar-nav>li>a, .navbar-inverse .navbar-brand {
    color: white;
}

.navbar-inverse .navbar-nav>li>a:hover, a.fa.fa-home.fa-lg.navbar-brand:hover {
     color: #f0f0f0;
}

a.navbar-brand:hover {
  color: #f0f0f0;
}

.navbar-inverse .navbar-nav > .open > a, .navbar-inverse .navbar-nav > .open > a:hover, .navbar-inverse .navbar-nav > .open > a:focus {
    color: #015CAE;
}

.navbar-inverse .navbar-nav > .open > a, .navbar-inverse .navbar-nav > .open > a:hover, .navbar-inverse .navbar-nav > .open > a:focus {
    background-color: #015CAE;
    color: #ffffff;
}

.navbar-inverse .navbar-collapse, .navbar-inverse .navbar-form {
    border-color: #248ec2 !important;
}

.btn-primary {
    color: #ffffff;
    background-color: #347DBE;
    border-color: #347DBE;
}

.navbar-inverse .navbar-nav > .active > a, .navbar-inverse .navbar-nav > .active > a:hover, .navbar-inverse .navbar-nav > .active > a:focus {
    background-color: #347DBE;
}

.btn-primary:hover,
.btn-primary:focus,
.btn-primary:active,
.btn-primary.active,
.open .dropdown-toggle.btn-primary {
    background-color: #248ec2;
    border-color: #347DBE;
}

.printTitle {
    color: #015CAE !important;
}

body.print h1 {color: #015CAE !important; font-size:28px !important;}
body.print h2 {color: #595959 !important; font-size:20px !important;}
body.print h3 {color: #E50E51 !important; font-size:14px !important;}
body.print h4 {color: #679DCE !important; font-size:14px; font-style: italic !important;}

.anchorjs-link:hover {
    color: #216f9b;
}

div.sidebarTitle {
    color: #015CAE;
}

li.sidebarTitle {
  margin-top:20px;
    font-weight:normal;
    font-size:130%;
    color: #ED1951;
    margin-bottom:10px;
    margin-left: 5px;

}

.navbar-inverse .navbar-toggle:focus, .navbar-inverse .navbar-toggle:hover {
    background-color: #015CAE;
}

.navbar-inverse .navbar-toggle {
    border-color: #015CAE;
}

</style>


## Welcome to GitHub Pages 1.2

You can use the [editor on GitHub](https://github.com/danielengblom/testing/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/danielengblom/testing/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://help.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

<ul id="profileTabs" class="nav nav-tabs">
    <li class="active"><a href="#profile" data-toggle="tab">Profile</a></li>
    <li><a href="#about" data-toggle="tab">About</a></li>
    <li><a href="#match" data-toggle="tab">Match</a></li>
</ul>
  <div class="tab-content">
<div role="tabpanel" class="tab-pane active" id="profile">
    <h2>Profile</h2>
<p>Praesent sit amet fermentum leo....</p>
</div>

<div role="tabpanel" class="tab-pane" id="about">
    <h2>About</h2>
    <p>Lorem ipsum ...</p></div>

<div role="tabpanel" class="tab-pane" id="match">
    <h2>Match</h2>
    <p>Vel vehicula ....</p>
</div>
</div>


<script>
    $('#mysidebar').height($(".nav").height());


$( document ).ready(function() {

    //this script says, if the height of the viewport is greater than 800px, then insert affix class, which makes the nav bar float in a fixed
    // position as your scroll. if you have a lot of nav items, this height may not work for you.
    var h = $(window).height();
    //console.log (h);
    if (h > 800) {
        $( "#mysidebar" ).attr("class", "nav affix");
    }
    // activate tooltips. although this is a bootstrap js function, it must be activated this way in your theme.
    $('[data-toggle="tooltip"]').tooltip({
        placement : 'top'
    });

    /**
     * AnchorJS
     */
    anchors.add('h2,h3,h4,h5');

});

// needed for nav tabs on pages. See Formatting > Nav tabs for more details.
// script from http://stackoverflow.com/questions/10523433/how-do-i-keep-the-current-tab-active-with-twitter-bootstrap-after-a-page-reload
$(function() {
    var json, tabsState;
    $('a[data-toggle="pill"], a[data-toggle="tab"]').on('shown.bs.tab', function(e) {
        var href, json, parentId, tabsState;

        tabsState = localStorage.getItem("tabs-state");
        json = JSON.parse(tabsState || "{}");
        parentId = $(e.target).parents("ul.nav.nav-pills, ul.nav.nav-tabs").attr("id");
        href = $(e.target).attr('href');
        json[parentId] = href;

        return localStorage.setItem("tabs-state", JSON.stringify(json));
    });

    tabsState = localStorage.getItem("tabs-state");
    json = JSON.parse(tabsState || "{}");

    $.each(json, function(containerId, href) {
        return $("#" + containerId + " a[href=" + href + "]").tab('show');
    });

    $("ul.nav.nav-pills, ul.nav.nav-tabs").each(function() {
        var $this = $(this);
        if (!json[$this.attr("id")]) {
            return $this.find("a[data-toggle=tab]:first, a[data-toggle=pill]:first").tab("show");
        }
    });
});
</script>
