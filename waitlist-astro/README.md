# Waitlist Astro

This template shows how EnaLog can be used to create a waitlist for your startup and provides a minimal landing page for people to join your waitlist.

### Usage

1. Clone this repo, since this is a monorepo you may want to clone the whole repo then copy just this directory to a separate directory. Find out how to do that [here](/README.md#how-to-clone-a-single-template)
2. Copy the contents of `.env.example` to a new file called `.env` 
3. [Register](https://dash.enalog.app/signup) for a free account on EnaLog. Complete the onboarding process where you will create your organisation and first project
4. In the EnaLog dashboard head to the 'Organisation' page and copy your API token
5. In the newly created `.env` file paste the copied token after `PUBLIC_ENALOG_API_TOKEN=`
6. Open up `src/components/WaitlistForm.astro` and update the following code in the file:
  1. Replace the project value with the name of the project you created earlier
  2. Optionally change the name, description, icon, push, and tags values
  3. Optionally add more keys to the meta object **but DO NOT remove the user value** as this is how we will send new waitlist users to EnaLog
```js
await pushEvent(`${import.meta.env.PUBLIC_ENALOG_API_TOKEN}`, {
    project: "merge-tree-waitlist",
    name: "user-joined-waitlist",
    description: "User joined the waitlist!",
    icon: "🥳",
    push: false,
    tags: ["waitlist", "landing-page", "mergetree"],
    meta: { user: email !== null ? email.value : "" },
})
```

