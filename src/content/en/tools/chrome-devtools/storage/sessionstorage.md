project_path: /web/tools/chrome-devtools/_project.yaml
book_path: /web/tools/chrome-devtools/_book.yaml
description: How to view and edit sessionStorage with the Session Storage pane and the Console.

{# wf_updated_on: 2020-07-10 #}
{# wf_published_on: 2019-03-14 #}
{# wf_blink_components: Platform>DevTools #}

# View And Edit Session Storage With Chrome DevTools {: .page-title }

{% include "web/_shared/contributors/kaycebasques.html" %}

[MDN]: https://developer.mozilla.org/en-US/docs/Web/API/Window/sessionStorage

This guide shows you how to use [Chrome DevTools](/web/tools/chrome-devtools/) to view, edit,
and delete [`sessionStorage`][MDN]{: .external } key-value pairs.

## View sessionStorage keys and values {: #view }

1. Click the **Application** tab to open the **Application** panel. The **Manifest** pane
   is shown by default.

     <figure>
       <img src="/web/tools/chrome-devtools/storage/imgs/manifest.png"
            alt="The Manifest pane"/>
       <figcaption>
         <b>Figure 1</b>. The Manifest pane
       </figcaption>
     </figure>

1. Expand the **Session Storage** menu.

     <figure>
       <img src="/web/tools/chrome-devtools/storage/imgs/sessionstoragemenu.png"
            alt="The Session Storage Menu"/>
       <figcaption>
         <b>Figure 2</b>. The <b>Session Storage</b> menu shows two domains:
         <b>https://developers.google.com</b> and <b>https://www.youtube.com</b>
       </figcaption>
     </figure>

1. Click a domain to view its key-value pairs.

     <figure>
       <img src="/web/tools/chrome-devtools/storage/imgs/sessionstorage.png"
            alt="The sessionStorage key-value pairs for the https://www.youtube.com domain"/>
       <figcaption>
         <b>Figure 3</b>. The <code>sessionStorage</code> key-value pairs for the
         <b>https://www.youtube.com</b> domain
       </figcaption>
     </figure>

1. Click a row of the table to view the value in the viewer below the table.

     <figure>
       <img src="/web/tools/chrome-devtools/storage/imgs/sessionstorageviewer.png"
            alt="Viewing the value of the yt-remote-cast-available key"/>
       <figcaption>
         <b>Figure 4</b>. Viewing the value of the <code>yt-remote-cast-available</code> key
       </figcaption>
     </figure>

## Create a new sessionStorage key-value pair {: #create }

1. [View a domain's `sessionStorage` key-value pairs](#view).
1. Double-click the empty part of the table. DevTools creates a new row and focuses your
   cursor in the **Key** column.

     <figure>
       <img src="/web/tools/chrome-devtools/storage/imgs/sessionstoragecreate.png"
            alt="The empty part of the table to double-click in order to create a new
                 key-value pair"/>
       <figcaption>
         <b>Figure 5</b>. The empty part of the table to double-click in order to create a new
         key-value pair
       </figcaption>
     </figure>

## Edit sessionStorage keys or values {: #edit }

1. [View a domain's `sessionStorage` key-value pairs](#view).
1. Double-click a cell in the **Key** or **Value** column to edit that key or value.

     <figure>
       <img src="/web/tools/chrome-devtools/storage/imgs/sessionstorageedit.png"
            alt="Editing a sessionStorage key"/>
       <figcaption>
         <b>Figure 6</b>. Editing a <code>sessionStorage</code> key
       </figcaption>
     </figure>

## Delete sessionStorage key-value pairs {: #delete }

1. [View a domain's `sessionStorage` key-value pairs](#view).
1. Click the key-value pair that you want to delete. DevTools highlights it blue to indicate
   that it's selected.

[delete]: /web/tools/chrome-devtools/images/shared/delete.png

1. Press the <kbd>Delete</kbd> key or click **Delete Selected**
   ![Delete Selected][delete]{: .inline-icon }.

## Delete all sessionStorage key-value pairs for a domain {: #deleteall }

1. [View a domain's `sessionStorage` key-value pairs](#view).

[clear]: /web/tools/chrome-devtools/images/shared/clear.png

1. Click **Clear All** ![Clear All][clear]{: .inline-icon }.

## Interact with sessionStorage from the Console {: #console }

Since you can run JavaScript in the **Console**, and since the **Console** has access to the
page's JavaScript contexts, it's possible to interact with `sessionStorage` from the **Console**.

1. Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if
   you want to access the `sessionStorage` key-value pairs of a domain other than the page
   you're on.

     <figure>
       <img src="/web/tools/chrome-devtools/storage/imgs/jscontext.png"
            alt="Changing the JavaScript context of the Console"/>
       <figcaption>
         <b>Figure 7</b>. Changing the JavaScript context of the <b>Console</b>
       </figcaption>
     </figure>

1. Run your `sessionStorage` expressions in the Console, the same as you would in your
   JavaScript.

     <figure>
       <img src="/web/tools/chrome-devtools/storage/imgs/sessionstorageconsole.png"
            alt="Interacting with sessionStorage from the Console"/>
       <figcaption>
         <b>Figure 8</b>. Interacting with <code>sessionStorage</code> from the <b>Console</b>
       </figcaption>
     </figure>

## Feedback {: #feedback }

{% include "web/_shared/helpful.html" %}
