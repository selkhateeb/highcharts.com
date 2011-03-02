# Fork of Highcharts JS
this is a fork from the hightcharts repo .. the main point of it is to add support for iframes.

### Whats the problem with Highcharts?
Highcharts uses *the main* docuemnt and window objects to create dom elements and attach events.
However, this approach gets messy when we start using iframes.
Since iframes have their own document and window objects, using parent.Highcharts
from within the iframe miss fires events and breaks a bunch of
other browser rules such as 'wrong_document_err dom exception 4'

### How to fix it
The approach to solve this issue is by providing a way to pass in the
document and window objects when creating the charts.
Here is a sample code to demonstrate the idea:
`
new parent.Highcharts.Chart({
    /* passing in the iframe window and document objects */
    win: window, 
    doc: document,
    ... //rest of options
});
`

# Highcharts JS 
  a JavaScript charting library based on SVG and VML rendering.

Use the Highslide Software forum at [http://highslide.com/forum/viewforum.php?f=9](http://highslide.com/forum/viewforum.php?f=9 ) for support and bug reports.

- Official website:  [www.highcharts.com](www.highcharts.com)
- Official download: [www.highcharts.com](www.highcharts.com)
- Licensing:         [www.highcharts.com/license](www.highcharts.com/license)
- Support:           [www.highcharts.com](www.highcharts.com)
