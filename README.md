# Nextbnb
 An online marketplace that connects people who want to rent out their homes with people looking for accommodations in specific locales.

 ## <a name="tech-stack">⚙️ Tech Stack</a>

- Next.js 13
- TypeScript
- TailwindCSS
- Prisma
- MongoDB
- Axios
- NextAuth
- React Hook Form
- Zustand

 ### Screenshot
 <img src="https://github.com/IamShafi/Nextbnb/blob/main/public/image_2023-12-19_181500147.png"/>

## <a name="features">🔋 Features</a>


- Full responsiveness
- Credential authentication
- Google authentication
- Github authentication
- Image upload using Cloudinary CDN
- Client form validation and handling using react-hook-form
- Server error handling using react-toast
- Calendars with react-date-range
- Booking / Reservation system
- Guest reservation cancellation
- Owner reservation cancellation
- Creation and deletion of properties
- Pricing calculation
- Advanced search algorithm by category, date range, map location, number of guests, rooms and bathrooms
- Favorites system

  
### Prerequisites

**Node version 14.x**


Follow these steps to set up the project locally on your machine.


**Cloning the Repository**

```bash
git clone https://github.com/your-username/your-project.git
cd your-project
```

### Install packages

```shell
npm i
```

**Set Up Environment Variables**

Create a new file named `.env` in the root of your project and add the following content:

```js
DATABASE_URL= ->MongoDB
GOOGLE_CLIENT_ID= ->console.cloud.google.com/apis/credentials
GOOGLE_CLIENT_SECRET=
GITHUB_ID= ->https://github.com/settings/developers
GITHUB_SECRET=
NEXTAUTH_SECRET= "anystring"
NEXT_PUBLIC_CLOUDINARY_CLOUD_NAME= ->https://console.cloudinary.com/settings/..../upload
```
Replace the placeholder values with your actual credentials 

### Setup Prisma

```shell
npx prisma db push

```

### Start the app

```shell
npm run dev
```
