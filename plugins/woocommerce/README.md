# [![WooCommerce](https://woo.com/wp-content/themes/woo/images/logo-woocommerce@2x.png 'WooCommerce')](https://woo.com/)

[![License](https://poser.pugx.org/woocommerce/woocommerce/license 'License')](https://packagist.org/packages/woocommerce/woocommerce)
![WordPress.org downloads](https://img.shields.io/wordpress/plugin/dt/woocommerce.svg 'WordPress.org downloads')
![WordPress.org rating](https://img.shields.io/wordpress/plugin/r/woocommerce.svg 'WordPress.org rating')
[![Build Status](https://github.com/woocommerce/woocommerce/actions/workflows/ci.yml/badge.svg?branch=trunk 'Build Status')](https://github.com/woocommerce/woocommerce/actions/workflows/ci.yml)
[![codecov](https://codecov.io/gh/woocommerce/woocommerce/branch/trunk/graph/badge.svg 'codecov')](https://codecov.io/gh/woocommerce/woocommerce)

This is the WooCommerce Core plugin. Here you can browse the source and keep track of development. We recommend all developers to follow the [WooCommerce development blog](https://woocommerce.wordpress.com/) to stay up to date about everything happening in the project. You can also [follow @DevelopWC](https://twitter.com/DevelopWC) on Twitter for the latest development updates.

If you are not a developer, please use the [WooCommerce plugin page](https://wordpress.org/plugins/woocommerce/) on WordPress.org.

## Getting Started

Please make sure you follow the [repository's getting started guide](../../README.md#getting-started) first!

```bash
# Make sure that WooCommerce Core and all of its dependencies are built
pnpm run --filter=woocommerce build 
# Make sure you're in the WooCommerce Core directory
cd plugins/woocommerce
# Start the development environment
pnpm -- wp-env start
```

You should now be able to visit `http://localhost:8888/` and access WooCommerce environment.

## Building Components

There are two major client-side components included in WooCommerce Core that can be built, linted, and tested independently. We've organized these components
in this way to take advantage of caching to prevent unnecessarily performing expensive rebuilds when only working in one of them.

### `plugins/woocommerce/client/legacy`

This directory contains the CSS and jQuery code for WooCommerce.

```bash
# Build the assets.
pnpm run --filter=woocommerce/client/legacy build 
# Lint the assets.
pnpm run --filter=woocommerce/client/legacy lint 
```

### `plugins/woocommerce-admin`

This directory contains the React-based admin interface.

```bash
# Build the React-based admin client.
pnpm run --filter=woocommerce/client/admin build 
# Lint the React-based admin client.
pnpm run --filter=woocommerce/client/admin lint 
# Test the React-based admin client.
pnpm run --filter=woocommerce/client/admin test 
```

#### Helper Scripts

Here is a collection of scripts that can help when developing the React-based admin interface.

```bash
# Create a develoment build of the React-based admin client.
pnpm --filter=woocommerce/client/admin dev 
# Create and watch a development build of the React-based admin client.
pnpm --filter=woocommerce/client/admin start 
# Watch the tests of the React-based admin client.
pnpm --filter=woocommerce/client/admin test:watch 
# Run a type check over the React-based admin client's TypeScript files.
pnpm --filter=woocommerce/client/admin ts:check 
```

## Documentation

* [WooCommerce Documentation](https://woo.com/)
* [WooCommerce Developer Documentation](https://github.com/woocommerce/woocommerce/wiki)
* [WooCommerce Code Reference](https://woo.com/wc-apidocs/)
* [WooCommerce REST API Docs](https://woocommerce.github.io/woocommerce-rest-api-docs/)

## Reporting Security Issues

To disclose a security issue to our team, [please submit a report via HackerOne here](https://hackerone.com/automattic/).
