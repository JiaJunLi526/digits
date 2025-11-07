![](https://github.com/jiajunli526/digits/raw/main/doc/landingPage.png)


## Installation

First, [install PostgreSQL](https://www.postgresql.org/download/). Then create a database for your application.

```

$ createdb digits
Password:
$

```


$ npm install

```

Fifth, create a `.env` file from the `sample.env`. Set the `DATABASE_URL` variable to match your PostgreSQL database that you created in the first step. See the Prisma docs [Connect your database](https://www.prisma.io/docs/getting-started/setup-prisma/add-to-existing-project/relational-databases/connect-your-database-typescript-postgresql). Then run the Prisma migration `npx prisma migrate dev` to set up the PostgreSQL tables.

```

$ npx prisma migrate dev

Then seed the database with the `/config/settings.development.json` data using `npx prisma db seed`.

```

$ npx prisma db seed


```

## Running the system

Once the libraries are installed and the database seeded, you can run the application by invoking the "dev" script in the [package.json file](https://github.com/ics-software-engineering/nextjs-application-template/blob/master/app/package.json):

```

$ npm run dev

> nextjs-application-template-1@0.1.0 dev
> next dev

▲ Next.js 14.2.4

- Local: http://localhost:3000
- Environments: .env

✓ Starting...
✓ Ready in 1619ms

```

### Viewing the running app

If all goes well, the template application will appear at [http://localhost:3000](http://localhost:3000). You can login using the credentials in [settings.development.json](https://github.com/ics-software-engineering/nextjs-application-template/blob/main/config/settings.development.json), or else register a new account.


## Walkthrough

The following sections describe the major features of this application.

### Landing Page

When you first open the application at [http://localhost:3000](http://localhost:3000), the landing page appears. It provides a brief overview of the system’s purpose and capabilities, along with navigation links in the top menu bar.

![](https://github.com/jiajunli526/digits/raw/main/doc/landingPage.png)

Use the **Login** menu to either log into an existing account or register a new one.

---

### Register

If you don’t yet have an account, click on the **Login** link in the navbar, then select **Sign Up** to open the registration form.

![](https://github.com/jiajunli526/digits/raw/main/doc/register.png)

Fill in your information and submit the form to create a new user account in the system.

---

### Sign In

To access your account, click **Login** and then select **Sign In**. This page allows you to authenticate using your registered email and password.

![](https://github.com/jiajunli526/digits/raw/main/doc/signin.png)

Once signed in successfully, you’ll be redirected to your personalized home page.

---

### User Home Page

After logging in, you’ll be taken to your user home page. It looks similar to the landing page but includes additional navbar options that are only available to logged-in users — such as adding or viewing your records.

![](https://github.com/jiajunli526/digits/raw/main/doc/signinLand.png)

From here, you can access your main dashboard features.

---

### List Contacts

Selecting the **List Contacts** link from the navbar displays a table of all the contacts associated with your account.

![](https://github.com/jiajunli526/digits/raw/main/doc/listpage.png)

You can also add timestamped notes for each contact to document past interactions or updates.

---

### Edit Contacts

Each contact entry includes an **Edit** link. Clicking it opens a page that allows you to modify that contact’s information and save the changes.

![](https://github.com/jiajunli526/digits/raw/main/doc/edit.png)

This feature lets you keep your contact information accurate and up to date.

---

### Admin Mode

Some users are assigned the **Admin** role in the configuration settings. When logged in as an Admin, the navbar includes an additional link granting access to the Admin Dashboard.

Admins can view and manage data from all users in the system.

---

### Admin Dashboard

The Admin page displays a list of all contacts from every registered user. This provides a system-wide overview for administrative management and oversight.

![](https://github.com/jiajunli526/digits/raw/main/doc/admin.png)

Non-admin users cannot access this page, even by manually entering the URL.
