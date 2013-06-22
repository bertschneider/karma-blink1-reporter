# karma-blink-reporter

karma-blink-reporter uses a [blink(1)][1] device to display [Karam][0] test results.

Only works with **Karma 0.9 or later** which enables custom plugins.

## Usage

0. Make sure you're using Karma 0.9+ `karma --version`. You may install the latest (unstable) version using `npm install -g karma@canary`

1. Install the blink(1) software from the [blink(1) homepage][1]

2. Install [karma-blink-reporter][4]

```bash
  $ npm install -g karma-blink-reporter
```

3. Add a dependency to the plugin section in the [Karma config file][5] (Karma 0.9.0 - 0.9.2):

```js
  plugins = [
    ...
    'karma-blink1-reporter',
    ...
  ];
```
or, if you're using the new module-based config file format (Karma 0.9.3+):

```js
  karma.configure({
    ...
    plugins: [
      'karma-blink1-reporter'
    ],
    ...
  })
```

4. Add the plugin too reporters

```js
  reporters = ['blink1'];
```

5. Start the blink(1) software

6. Run your tests

## Configuration

Some properties of the plugin can be changes in the Karma config file by adding the `blink1` key.

```js
   /* Default vales */
   blink1 = {
        baseUrl: 'http://localhost:8934/blink1/',
        fault: 'FF0000',
        error: 'FFA500',
        success: '00FF00',
        duration: 1.5
   },
```

## License

karma-blink-reporter is licensed under the [MIT License][4].

  [0]: http://karma-runner.github.com
  [1]: http://thingm.com/products/blink-1.html
  [2]: https://github.com/bertschneider/karma-blink-reporter
  [3]: http://karma-runner.github.io/0.8/config/configuration-file.html
  [4]: http://opensource.org/licenses/MIT





