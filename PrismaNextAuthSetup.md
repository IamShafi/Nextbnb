01. setup prisma
```
npm i -D prisma

npx prisma init
```

02. create Schema models
```
id String @id @default(auto()) @map("_id") @db.ObjectId
```

03.
```
npx prisma db push
```

04. NextAuth setup
```
npm install next-auth @prisma/client
@next-auth/prisma-adapter
```

05. Create Global Prisma Client

06. Folder pages/api/[...nextauth].ts

07. import AuthOptions from next-auth

08. import PrismaAdapter from @next-auth/prisma-adapter

09. import Providers
```
 providers: [
    GithubProvider({
      clientId: process.env.GITHUB_ID as string,
      clientSecret: process.env.GITHUB_SECRET as string
    }),
    GoogleProvider({
      clientId: process.env.GOOGLE_CLIENT_ID as string,
      clientSecret: process.env.GOOGLE_CLIENT_SECRET as string
    }),
    CredentialsProvider({
      name: 'credentials',
      credentials: {
        email: { label: 'email', type: 'text' },
        password: { label: 'password', type: 'password' }
      },
      async authorize(credentials) {
        if (!credentials?.email || !credentials?.password) {
          throw new Error('Invalid credentials');
        }

        const user = await prisma.user.findUnique({
          where: {
            email: credentials.email
          }
        });

        if (!user || !user?.hashedPassword) {
          throw new Error('Invalid credentials');
        }

        const isCorrectPassword = await bcrypt.compare(
          credentials.password,
          user.hashedPassword
        );

        if (!isCorrectPassword) {
          throw new Error('Invalid credentials');
        }

        return user;
      }
    })
  ],
```

10. folder app/api/register/route.ts -->  axios.post('/api/register', data)

