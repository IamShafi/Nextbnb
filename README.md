# Nextbnb
 An online marketplace that connects people who want to rent out their homes with people looking for accommodations in specific locales.
 This is a repository for a Full Stack application with Next.js 13 App Router: React, Tailwind, Prisma, MongoDB, NextAuth.
 
Features:

- Tailwind design
- Tailwind animations and effects
- Full responsiveness
- Credential authentication
- Google authentication
- Github authentication
- Image upload using Cloudinary CDN
- Client form validation and handling using react-hook-form
- Server error handling using react-toast
- Calendars with react-date-range
- Page loading state
- Page empty state
- Booking / Reservation system
- Guest reservation cancellation
- Owner reservation cancellation
- Creation and deletion of properties
- Pricing calculation
- Advanced search algorithm by category, date range, map location, number of guests, rooms and bathrooms
    - For example we will filter out properties that have a reservation in your desired date range to travel
- Favorites system

  
### Prerequisites

**Node version 14.x**


### Install packages

```shell
npm i
```

### Setup .env file


```js
DATABASE_URL= ->MongoDB
GOOGLE_CLIENT_ID= ->console.cloud.google.com/apis/credentials
GOOGLE_CLIENT_SECRET=
GITHUB_ID= ->https://github.com/settings/developers
GITHUB_SECRET=
NEXTAUTH_SECRET= "anystring"
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME= ->https://console.cloudinary.com/settings/..../upload
```

### Setup Prisma

```shell
npx prisma db push

```

### Start the app

```shell
npm run dev
```
