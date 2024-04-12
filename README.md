# Micro-Frontend with Next.js  and Webpack Module Federation
This Shopping Cart application showcases micro frontend architecture with features for both server-side and client-side rendering in Next.js. It leverages Webpack 5 Module Federation for sharing micro frontends and utilizes Next.js 14 along with @module-federation/nextjs-mf.

## Getting Started

run `pnpm run start` and browse to `http://localhost:3002` or one of the others
## Context

There are three Next.js applications in three different repositories, and they are working together as microfrontend applications. Hosted URLs and repository URLs are as follows.

### `checkout Micro-Frontend` 
- git repository : https://github.com/abhimax/next-js-micro-frontend-shopping-cart_checkout
- Hosted URL: https://next-js-micro-frontend-shopping-cart-checkout-mhwma9wus.vercel.app/
### `home  Micro-Frontend`
- git repository : https://github.com/abhimax/next-js-micro-frontend-shopping-cart_home
- Hosted URL: https://next-js-micro-frontend-shopping-cart-home-mjlltjnr9.vercel.app/
### `shop  Micro-Frontend`
- git repository : https://github.com/abhimax/next-js-micro-frontend-shopping-cart_shop
- Hosted URL: https://next-js-micro-frontend-shopping-cart-shop-c6bggjh1v.vercel.app/

The applications utilize omnidirectional routing and pages or components are able to be federated between applications like a SPA

It has used hooks here to ensure multiple copies of react are not loaded into scope on server or client.

The omnidirectional routing now hooks into webpack federation loading functions, so when dynamically loading remotes - you can use the same functions that webpack uses to load remotes when theres a know static import like `home/title`


### Sharing

Next.js has all its internal modules pre-shared vis `@module-federation/nextjs-mf` you do need to share react via the plugin in order to ensure that the share scope runtime requirements are included - since you cannot share modules in a normal manner, like nextjs internls, the pre-shared modules are attached at runtime to the share scope.

### Deployment
This Micro-frontend app has been successfully deployed on Vercel! Each Apps – Home, Checkout, and Host – operates independently as microfrontend apps, seamlessly running on the Vercel platform. Ready to explore? Check out the Home app at [here](https://next-js-micro-frontend-shopping-cart-home-mjlltjnr9.vercel.app/). Let the digital adventures begin! 🚀



