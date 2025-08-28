## [Movie Reservation System (nestjs)](https://roadmap.sh/projects/movie-reservation-system)

#### Build a system that allows users to reserve movie tickets.

#

# Tech Stack

- Nodejs
- TypeScript
- Nestjs
- Postgresql
- Stripe (payment gateway)

##

# Features

- [x] User Authentication and Authorization
  - login
  - register
  - JWT Authorization
- [x] Roles (super-admin, admin, user)
  - super-admin can promote users to admin and demote them back
- [x] Movie Management

  - super-admin and admin can create, update, and delete movies
  - Movies are categorized by genre.
  - users can filter movies by name, category, showtime, and between two dates
  - paginated responses for performance

- [x] Firebase integration
  - to upload movie posters as image or video
- [x] Reservation Management

  - users can create an order for a movie and make a payment
  - after payment success, users receive an email with ticket details
  - users can cancel a reservation and receive a refund

- [x] Scheduling
  - An hour before the movie is shown, an email is sent to users to remind them of the showtime.
- [x] Email Notifications
  - send emails to users (order created, payment success, refund issued, and movie showtime reminder)
- [x] Integration Testing (Jest)
  - created tests for all services and controllers in the app

## How To Install

```bash
> npm i -g pnpm
> pnpm install
```

## Run App (in dev env)

```bash
> pnpm start:dev
```

## Run App (in production)

```bash
> pnpm build
> pnpm start:prod
```

# Env file

```js
// APP
PORT: number;
JWT_KEY: string;
NODE_ENV: 'test' | 'dev' | 'prod';
HOST: string;
// DB
DB_NAME: string;
DB_HOST: string;
DB_PORT: number;
DB_USERNAME: string;
DB_PASSWORD: string;
// payment
STRIPE_SK: string;
STRIPE_PK: string;
STRIPE_WEBHOOK_SK: string;
// email smtp
EMAIL_USER: string;
EMAIL_SK: string;
```

#
#### With thanks and appreciation to [roadmap.sh](https://roadmap.sh/)

## [Project Page](https://roadmap.sh/projects/movie-reservation-system)