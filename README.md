[![Build Status](https://api.travis-ci.org/koalyptus/TableFilter.svg?branch=master)](https://travis-ci.org/koalyptus/TableFilter)
[![Document](http://koalyptus.github.io/TableFilter/docs/badge.svg)](https://koalyptus.github.io/TableFilter/docs/source)

# TableFilter

> A Javascript library making HTML tables filterable

TableFilter is a modernised version of the [HTML Table Filter generator](http://tablefilter.free.fr) javascript plugin.
This library adds to any html table a "filter by column" feature that enables
users to filter and limit the data displayed within a long table. By default, the script automatically adds a filter grid bar at the top of the desired table.

## Features
* Convert a regular HTML table into an advanced grid component providing:
    * Advanced columns filtering model
    * Sorting and pagination facilities
    * Complete selection model ([ezEditTable](http://codecanyon.net/item/ezedittable-enhance-html-tables/2425123?ref=koalyptus) extension)
    * Extended keyboard navigation ([ezEditTable](http://codecanyon.net/item/ezedittable-enhance-html-tables/2425123?ref=koalyptus) extension)
    * Inline cell or row editing ([ezEditTable](http://codecanyon.net/item/ezedittable-enhance-html-tables/2425123?ref=koalyptus) extension)
    * Row insertion or deleting ([ezEditTable](http://codecanyon.net/item/ezedittable-enhance-html-tables/2425123?ref=koalyptus) extension)
    * And even more features...
* Attach to an existing HTML table
* Integration with any server-side technology as this is a pure client-side
solution
* Exhaustive documentation and poweful API

## Getting started
* Clone the repo using Git:
```shell
git clone --bare https://github.com/koalyptus/TableFilter.git
```

* You can [download](https://github.com/koalyptus/TableFilter/archive/master.zip) this repository.

* Alternatively, install TableFilter files in your npm enabled project using:
```shell
npm install tablefilter --save
``` 
* or get the future features from the ``next`` release channel:
```shell
npm install tablefilter@next --save
```
* If you don't use `npm`, you can also 
[access these files on unpkg](https://unpkg.com/tablefilter/), download them 
or point your package manager to them.

## Setup
Copy the ``tablefilter`` directory under ``dist`` and place it at desired location in your project. Then include the main js file in your page:
```shell
<script src="path/to/my/scripts/tablefilter/tablefilter.js"></script>
```
Place the following snippet just under the HTML table and always define a ``base_path`` property in the configuration object to reflect the path to the script
```shell
<script>
var tf = new TableFilter(document.querySelector('.my-table'), {
    base_path: 'path/to/my/scripts/tablefilter/'
});
tf.init();
</script>
```
If the ``base_path`` property is not specified, it will default to ``/tablefilter`` directory:
```shell
your-page.html
 |— tablefilter
``` 

## Development
This project requires node.js and Grunt to be installed:
- install [node.js](https://nodejs.org/)
- install [Grunt](http://gruntjs.com/getting-started) from the command line using npm (comes with node.js):
```shell
npm install -g grunt-cli
```
Once ``Grunt`` is sorted out you can follow the instructions below.
Start by installing any dependencies.

```shell
npm install
```
Use ``npm run dev`` command to launch a build / watch cycle and start the local
sever on port ``8080``.

Use ``npm run build`` command to generate a production build.

The ``npm run build-all`` command will create a production build, run the tests and finally generate the demos:

To run all the tests:

```shell
npm test
```

and to run specific test(s):

```shell
grunt test-only:test.html
grunt test-only:test.html,test-sort.html
```

## Demos
Check out the online [examples](http://koalyptus.github.io/TableFilter/examples) or generate the demos locally:
```shell
npm run build-demos
```
then run the local webserver:
```shell
npm start
```
then pick a demo from:
```shell
http://localhost:8080/demos/
```

## Documentation
Find exhaustive documentation on the configuration options in the [WIKI](https://github.com/koalyptus/TableFilter/wiki) section.

Autogenerated documentation of the ES6 modules is available on the website: [docs](http://koalyptus.github.io/TableFilter/docs)

If you previously used the HTML Table Filter Generator plugin, verify the configuration
options you are using are still supported: [Obsolete](https://github.com/koalyptus/TableFilter/wiki/Obsolete)

Run this task to generate the documentation in the ``docs/docs`` directory:
```shell
npm run esdoc
```

## Support
* GitHub for reporting bugs and feature requests.

## License
[MIT](LICENSE)






