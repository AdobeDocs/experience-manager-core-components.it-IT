---
title: Componente Pagina (v1)
description: Il componente Pagina è una pagina estensibile concepita per funzionare con l’editor di modelli e consentire l’assemblaggio di intestazione/piè di pagina e altri componenti della struttura della pagina.
index: n
role: Architect, Developer, Admin, User
exl-id: 522f32f0-fc06-4ca0-ada2-61bdbc8761e0
source-git-commit: 92a3ec273a5be6751c1503835b9c2e5cbd61bb9e
workflow-type: ht
source-wordcount: '454'
ht-degree: 100%

---


# Componente Pagina (v1) {#page-component-v}

Il componente Pagina è una pagina estensibile concepita per funzionare con l’[editor di modelli](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/siteandpage/templates.html?lang=it) e consentire l’assemblaggio di intestazione/piè di pagina e altri componenti della struttura della pagina.

## Utilizzo {#usage}

Il componente Pagina costituisce la base di tutte le pagine progettate con i Componenti core e i modelli modificabili. Utilizzando il componente Pagina, le intestazioni, i piè di pagina e la struttura della pagina possono essere definiti in un modello utilizzando gli altri Componenti core.

Nella [finestra di dialogo per progettazione](#design-dialog) è possibile definire le librerie client della pagina. A differenza di altri componenti che hanno una finestra di dialogo per modifica accessibile direttamente dal componente, poiché il componente Pagina è la pagina stessa, la [finestra di dialogo per modifica](#edit-dialog) del componente Pagina è la finestra delle proprietà della pagina.

## Versione e compatibilità {#version-and-compatibility}

Questo documento descrive la versione 1 del componente Pagina, originariamente introdotto con la versione 1.0.0 dei Componenti core in AEM 6.3.

La tabella che segue riporta la compatibilità della versione 1 del componente Pagina.

| Versione di AEM | Componente Pagina v1 |
|--- |--- |
| 6.3 | Compatibile |
| 6.4 | Compatibile |

>[!CAUTION]
>
>Questo documento descrive la versione 1 del componente Pagina.
>
>Per informazioni dettagliate sulla versione corrente del componente Pagina, vedi il documento [Componente Pagina](/help/components/page.md).

>[!NOTE]
>
>La versione 1 del componente Pagina non supporta il reindirizzamento delle pagine. Utilizza la [versione corrente del componente Pagina](/help/components/page.md) per il supporto del reindirizzamento delle pagine.

## Esempio di output del componente {#sample-component-output}

Di seguito è riportato un esempio tratto da [We.Retail](https://experienceleague.adobe.com/docs/experience-manager-64/developing/bestpractices/we-retail/we-retail.html?lang=it).

### Schermata {#screenshot}

![](/help/assets/chlimage_1-93.png)

### HTML {#html}

```
<!DOCTYPE HTML>
<html lang="en">
    <head>
    <meta http-equiv="content-type" content="text/html; charset=UTF-8"/>
   
    <meta name="template" content="hero-page"/>
    
<link rel="stylesheet" href="/etc.clientlibs/weretail/clientlibs/clientlib-dependencies.css" type="text/css">
<script type="text/javascript" src="/etc.clientlibs/weretail/clientlibs/clientlib-dependencies.js"></script>
    
<link rel="stylesheet" href="/etc.clientlibs/clientlibs/granite/jquery-ui.css" type="text/css">
<link rel="stylesheet" href="/etc.clientlibs/weretail/clientlibs/clientlib-base.css" type="text/css">

<script src="https://use.typekit.net/dje4ayd.js"></script>
<script>try {
    Typekit.load({async: true});
} catch (e) {
}</script>

<script type="text/javascript">
            (function() {
                window.ContextHub = window.ContextHub || {};

                /* setting paths */
                ContextHub.Paths = ContextHub.Paths || {};
                ContextHub.Paths.CONTEXTHUB_PATH = "/etc/cloudsettings/default/contexthub";
                ContextHub.Paths.RESOURCE_PATH = "\/content\/we\u002Dretail\/us\/en\/equipment\/_jcr_content\/contexthub";
                ContextHub.Paths.SEGMENTATION_PATH = "\/etc\/segmentation\/contexthub";
                ContextHub.Paths.CQ_CONTEXT_PATH = "";

                /* setting initial constants */
                ContextHub.Constants = ContextHub.Constants || {};
                ContextHub.Constants.ANONYMOUS_HOME = "/home/users/l/l5mcNzhlwJ663w4ZSrI_";
                ContextHub.Constants.MODE = "no-ui";
            }());
        </script><script src="/etc/cloudsettings/default/contexthub.kernel.js" type="text/javascript"></script>
    
    <link href="/etc/designs/we-retail.css" rel="stylesheet" type="text/css"/>
    
        <!--[if IE]><link rel="shortcut icon" href="/etc/designs/we-retail/favicon.ico"/><![endif]-->
    
    <link rel="icon" type="image/png" href="/etc/designs/we-retail/favicon_32.png"/>

    <link rel="apple-touch-icon" sizes="60x60" href="/etc/designs/we-retail/touch-icon_60.png"/>

    <link rel="apple-touch-icon" sizes="76x76" href="/etc/designs/we-retail/touch-icon_76.png"/>

    <link rel="apple-touch-icon" sizes="120x120" href="/etc/designs/we-retail/touch-icon_120.png"/>

    <link rel="apple-touch-icon" sizes="152x152" href="/etc/designs/we-retail/touch-icon_152.png"/>

    <title>Equipment</title>
</head>
    <body>
    
<div class="container">
    <div class="root responsivegrid">
<div class="aem-Grid aem-Grid--12 aem-Grid--default--12  ">
    
    <div class="header aem-GridColumn aem-GridColumn--default--12">

    <div class="we-retail-header" data-we-header-content="/content/we-retail/us/en/equipment.header_include.html">
        <div class="we-SearchModal modal fade" id="navbar-search" role="dialog" data-color="primary">
            <div class="modal-dialog">
                <div class="modal-content">
                    <div class="modal-header">
                        <span><i class="we-Icon we-Icon--search"></i>Search anything</span>
                        <button type="button" class="close" data-dismiss="modal"><span>Close search</span><i class="we-Icon we-Icon--close-alt"></i></button>
                    </div>
                    <div class="modal-body">
                        <div class="row">
                            <div class="col-md-12">
                                <form id="form-search-input-inline" data-paths="[/content/we-retail/us/en]" class="scf-js-searchform navbar-form navbar-left" role="search">
                                    <div class="scf-quicksearch-form-group form-group">
                                        <input type="search" id="scf-js-quicksearch-input-inline" placeholder="Start typing..." data-dropdown="drop_search" aria-controls="drop_search" aria-expanded="false" name="input_value" class="we-SearchModal-input" value="" required="" autocomplete="off">
                                        <span role="status" aria-live="polite" class="ui-helper-hidden-accessible"></span>
                                        <input type="hidden" name="resultPage" class="scf-js-seach-resultPage" value="/content/we-retail/us/en/community/search"/>
                                        <input type="hidden" name="searchEndpoint" class="scf-js-search-endpoint" value="/content/we-retail/us/en/community/search/jcr:content/content/primary/searchresult"/>
                                    </div>
                                </form>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <!-- /.we-SearchModal -->

        <div class="we-LanguageModal modal fade" tabindex="-1" role="dialog" data-color="primary">
            <div class="modal-dialog modal-center modal-sm">
                <div class="modal-content">
                    <div class="modal-header">
                        <h3 class="modal-title text-center">CHOOSE YOUR COUNTRY</h3>
                    </div>
                    <div class="modal-body">
                        <ul class="we-LanguagesList">
                            <li>
                                <i class="we-lang-icon we-lang-icon-ca"></i><span><a href="/content/we-retail/ca/en.html">English</a> | <a href="/content/we-retail/ca/fr.html">French</a></span>
                            </li>
                        
                            <li>
                                <i class="we-lang-icon we-lang-icon-ch"></i><span><a href="/content/we-retail/ch/de.html">German</a> | <a href="/content/we-retail/ch/fr.html">French</a> | <a href="/content/we-retail/ch/it.html">Italian</a></span>
                            </li>
                        
                            <li>
                                <i class="we-lang-icon we-lang-icon-de"></i><span><a href="/content/we-retail/de/de.html">German</a></span>
                            </li>
                        
                            <li>
                                <i class="we-lang-icon we-lang-icon-es"></i><span><a href="/content/we-retail/es/es.html">Spanish</a></span>
                            </li>
                        
                            <li>
                                <i class="we-lang-icon we-lang-icon-fr"></i><span><a href="/content/we-retail/fr/fr.html">French</a></span>
                            </li>
                        
                            <li>
                                <i class="we-lang-icon we-lang-icon-it"></i><span><a href="/content/we-retail/it/it.html">Italian</a></span>
                            </li>
                        
                            <li>
                                <i class="we-lang-icon we-lang-icon-us"></i><span><a href="/content/we-retail/us/en.html" class="active">English</a> | <a href="/content/we-retail/us/es.html">Spanish</a></span>
                            </li>
                        </ul>
                    </div>
                </div>
                <div class="modal-after">
                    <a href="#" data-dismiss="modal"><i class="we-Icon we-Icon--close-alt"></i> Close</a>
                </div>
            </div>
        </div><!-- /.we-LanguageModal -->
    </div>
</div>
<div class="heroimage image aem-GridColumn aem-GridColumn--default--12">

    <div class="we-HeroImage width-full jumbotron" style="background-image: url(\2f content\2fwe-retail\2fus\2f en\2f equipment\2fjcr%3acontent\2froot\2fhero_image.img.jpeg);">
        <div class="container cq-dd-image">
            <div class="we-HeroImage-wrapper">
                <p class="h3"></p>
                <strong class="we-HeroImage-title h1">Equipment</strong>

            </div>
        </div>
    </div>
</div>
<div class="responsivegrid aem-GridColumn aem-GridColumn--default--12">
<div class="aem-Grid aem-Grid--12 aem-Grid--default--12  ">
    
    <div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
<h2>Welcome our finest equipment</h2>

</div>
<div class="categoryteaser aem-GridColumn aem-GridColumn--default--6">
<div class="we-CategoryTeaser cq-dd-image">
    <div class="crop crop-16_9">
        <img class="crop__content" data-lazy-src="/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser.img.jpeg"/>
    </div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/hiking.html" class="btn btn-action btn-primary">Hiking</a>
</div>
</div>
<div class="categoryteaser aem-GridColumn aem-GridColumn--default--6">
<div class="we-CategoryTeaser cq-dd-image">
    <div class="crop crop-16_9">
        <img class="crop__content" data-lazy-src="/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_2082536754.img.jpeg"/>
    </div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/running.html" class="btn btn-action btn-primary">Running</a>
</div>
</div>
<div class="categoryteaser aem-GridColumn aem-GridColumn--default--4">
<div class="we-CategoryTeaser cq-dd-image">
    <div class="crop crop-16_9">
        <img class="crop__content" data-lazy-src="/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_647414391.img.jpeg"/>
    </div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/biking.html" class="btn btn-action btn-primary">Biking</a>
</div>
</div>
<div class="categoryteaser aem-GridColumn aem-GridColumn--default--4">
<div class="we-CategoryTeaser cq-dd-image">
    <div class="crop crop-16_9">
        <img class="crop__content" data-lazy-src="/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1341949589.img.jpeg"/>
    </div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/surfing.html" class="btn btn-action btn-primary">Surfing</a>
</div>
</div>
<div class="categoryteaser aem-GridColumn aem-GridColumn--default--4">
<div class="we-CategoryTeaser cq-dd-image">
    <div class="crop crop-16_9">
        <img class="crop__content" data-lazy-src="/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_1398042708.img.jpeg"/>
    </div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/snow-sports.html" class="btn btn-action btn-primary">Snow Sports</a>
</div>
</div>
<div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
<h2>Featured products</h2>

</div>
<div class="cmp cmp-list aem-GridColumn aem-GridColumn--default--12">
<div class="we-product-grid-container">
    <ul class="foundation-ordered-list-container">
        
<li class="foundation-list-item">
    <we-product-item price="$110.00" size="11,12,7,8,9,10" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="cmp cmp-image">

        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/products/equipment/biking/marin-mountain-bike-shoes/_jcr_content/root/product/image.img.jpg" alt/>
        </noscript>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">Marin Mountain Bike Shoes</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">footwear</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$110.00</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/biking/marin-mountain-bike-shoes.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>

<li class="foundation-list-item">
    <we-product-item price="$65.00" size="11,13,9" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="cmp cmp-image">

        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/products/equipment/running/fleet-cross-training-shoe/_jcr_content/root/product/image.img.jpg" alt/>
        </noscript>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">Fleet Cross-Training Shoe</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">footwear</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$65.00</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/running/fleet-cross-training-shoe.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>

<li class="foundation-list-item">
    <we-product-item price="$75.00" size="S,XL,L,M" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="cmp cmp-image">

        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/products/equipment/biking/sequoia-bike-helmet/_jcr_content/root/product/image.img.jpg" alt/>
        </noscript>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">Sequoia Bike Helmet</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">helmet</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$75.00</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/biking/sequoia-bike-helmet.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>

<li class="foundation-list-item">
    <we-product-item price="$39.00" size="XXS,S,XL,L,M,XXL" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="cmp cmp-image">

        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/products/equipment/hiking/rios-t-shirt/_jcr_content/root/product/image.img.jpg" alt/>
        </noscript>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">Rios T Shirt</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">shirt</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$39.00</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/hiking/rios-t-shirt.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>

<li class="foundation-list-item">
    <we-product-item price="$900.00" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="cmp cmp-image">

        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/products/equipment/surfing/the-stretch-longboard/_jcr_content/root/product/image.img.png" alt/>
        </noscript>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">The Stretch Longboard</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">equipment</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$900.00</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/surfing/the-stretch-longboard.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>

<li class="foundation-list-item">
    <we-product-item price="$39.99" inline-template>
        <div class="we-ProductsGrid-item">
            <div class="we-ProductsGrid-item-image img-center">
                <div class="cmp cmp-image">

        <noscript data-cmp-image="{&#34;smartImages&#34;:[],&#34;smartSizes&#34;:[],&#34;lazyEnabled&#34;:true}">
            <img src="/content/we-retail/us/en/products/equipment/running/faba-running-pants/_jcr_content/root/product/image.img.jpg" alt/>
        </noscript>

</div>

            </div>

            <h3 class="we-ProductsGrid-item-title h4">Faba Running Pants</h3>
            <span class="we-ProductsGrid-item-subtitle small text-muted">pants</span>

            <strong class="we-ProductsGrid-item-price">
                <span>$39.99</span>
                <span class="we-ProductsGrid-item-price-new"></span>
                <s class="we-ProductsGrid-item-price-old"></s>
            </strong>

            <span class="we-ProductsGrid-item-discount hidden"><span></span>off</span>
            <a href="/content/we-retail/us/en/products/equipment/running/faba-running-pants.html" class="we-ProductsGrid-item-link"></a>

        </div>
        <!-- /.we-ProductsGrid-item -->
    </we-product-item>
</li>
    </ul>
</div>

</div>
<div class="button aem-GridColumn aem-GridColumn--default--12">
<a class="btn btn-primary btn-action cq-dd-linkTo " href="/content/we-retail/us/en/products/equipment.html" role="button">All equipment</a>
</div>
<div class="cmp cmp-title aem-GridColumn aem-GridColumn--default--12">
<h2>Winter is coming, get ready</h2>

</div>
<div class="categoryteaser aem-GridColumn aem-GridColumn--default--6">
<div class="we-CategoryTeaser cq-dd-image">
    <div class="crop crop-16_9">
        <img class="crop__content" data-lazy-src="/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_643606949.img.jpeg"/>
    </div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/snow-sports.html" class="btn btn-action btn-primary">Snow Sports</a>
</div>
</div>
<div class="categoryteaser aem-GridColumn aem-GridColumn--default--6">
<div class="we-CategoryTeaser cq-dd-image">
    <div class="crop crop-16_9">
        <img class="crop__content" data-lazy-src="/content/we-retail/us/en/equipment/jcr%3acontent/root/responsivegrid/category_teaser_883210151.img.jpeg"/>
    </div>

    <h2></h2>
    <h3></h3>
    
    <a href="/content/we-retail/us/en/products/equipment/snow-sports.html" class="btn btn-action btn-primary">Snowboarding</a>
</div>
</div>

    <div class="new newpar section aem-Grid-newComponent">

</div>

</div></div>
<div class="footer aem-GridColumn aem-GridColumn--default--12">

    <footer class="we-Footer width-full">
        <div class="container">

            <div class="row">

                <div class="col-md-4">
                    <div class="we-Logo we-Logo--big">
                        we.<strong>Retail</strong>
                    </div>
                </div>

                <div class="col-md-8 col-xs-12">
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/experience.html">Experience</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/men.html">Men</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/women.html">Women</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/equipment.html">Equipment</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/about-us.html">About Us</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/products.html">Products</a>
                                </h2>
                            </div>
                        </div>
                    
                        <div class="col-lg-2 col-md-2 col-xs-3">
                            <div class="we-Footer-nav">
                                <h2 class="h4">
                                    <a href="/content/we-retail/us/en/community.html">community</a>
                                </h2>
                            </div>
                        </div>
                    
                </div>

            </div>

            <div class="row we-Footer-section we-Footer-section--sub">
                <div class="we-Footer-section-item">
                    <span class="text-uppercase text-muted">&copy;  All rights reserved</span>
                </div>
                <div class="we-Footer-section-item">
                    <a href="#" class="text-uppercase text-muted">Terms of use & privacy policy</a>
                </div>
            </div>

            <div class="row">
                <div class="col-md-12">
                    <div class="text-center">
                        <a href="#top" class="btn btn-action btn-action-up btn-primary">Ride to the top</a>
                    </div>
                </div>
            </div>

        </div>
    </footer>

</div>

    <div class="new newpar section aem-Grid-newComponent">

</div>

</div></div>

</div>

<script type="text/javascript" src="/etc.clientlibs/clientlibs/granite/jquery-ui.js"></script>
<script type="text/javascript" src="/etc.clientlibs/weretail/clientlibs/clientlib-base.js"></script>

    </body>
</html>
```

### JSON {#json}

```
{
  "designPath": "/etc/designs/we-retail",
  "title": "Equipment",
  "lastModifiedDate": 1507623887022,
  "templateName": "hero-page",
  "cssClassNames": "page",
  "language": "en",
  ":type": "weretail/components/structure/page",
  ":items": {
    "root": {
      "columnCount": 12,
      "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
      ":items": {
        "header": {
          "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
          ":type": "weretail/components/structure/header",
          "theme": "inverse"
        },
        "hero_image": {
          "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
          "smartSizes": [],
          "smartImages": [],
          "lazyEnabled": true,
          ":type": "weretail/components/content/heroimage"
        },
        "responsivegrid": {
          "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
          "columnCount": 12,
          "gridClassNames": "aem-Grid aem-Grid--12 aem-Grid--default--12",
          ":items": {
            "title": {
              "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
              ":type": "weretail/components/content/title",
              "jcr:title": "Welcome! Our finest equipment!",
              "type": "h2"
            }
          },
          ":itemsOrder": [
            "title"
          ],
          ":type": "wcm/foundation/components/responsivegrid"
        },
        "footer": {
          "columnClassNames": "aem-GridColumn aem-GridColumn--default--12",
          ":type": "weretail/components/structure/footer"
        }
      },
      ":itemsOrder": [
        "header",
        "hero_image",
        "responsivegrid",
        "footer"
      ],
      ":type": "wcm/foundation/components/responsivegrid"
    }
  },
  ":itemsOrder": [
    "root"
  ]
}
```

>[!NOTE]
>
>L’esportazione JSON dai Componenti core richiede la versione 1.1.0 dei Componenti core. Per ulteriori informazioni, vedi le [informazioni sulla compatibilità dei Componenti core v1](/help/versions.md).

## Finestra di dialogo per modifica {#edit-dialog}

Poiché il componente rappresenta l’intera pagina, le impostazioni normalmente presenti in una finestra di dialogo per modifica si trovano invece nella finestra [Proprietà della pagina](https://experienceleague.adobe.com/docs/experience-manager-64/authoring/authoring/editing-page-properties.html?lang=it).

## Finestra di dialogo per progettazione {#design-dialog}

Poiché il componente rappresenta l’intera pagina, la finestra di dialogo per progettazione è accessibile tramite **Informazioni pagina -> Progettazione pagina**.

![](/help/assets/chlimage_1-94.png)

La finestra Progettazione pagina consente di definire le librerie lato client da caricare con la pagina.

* Per aggiungere un nuovo campo, tocca o fai clic sul pulsante **Aggiungi** sotto ciascuno dei due campi.
* Per rimuovere un campo, tocca o fai clic sull’icona cestino accanto al campo da rimuovere.
* Per cambiare l’ordine di caricamento, tocca o fai clic e trascina la maniglia che si trova accanto al campo da spostare.

Per ulteriori informazioni sull’utilizzo delle librerie client, vedi [Utilizzo delle librerie client](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=it).

![](/help/assets/chlimage_1-95.png)

## Dettagli tecnici {#technical-details}

La documentazione tecnica più recente sul componente Pagina [è disponibile su GitHub](https://github.com/adobe/aem-core-wcm-components/tree/master/content/src/content/jcr_root/apps/core/wcm/components/page/v1/page).

L’intero progetto dei Componenti core può essere scaricato da GitHub.

Per ulteriori informazioni sullo sviluppo di Componenti core, vedi la [documentazione per gli sviluppatori di Componenti core](/help/developing/overview.md).
