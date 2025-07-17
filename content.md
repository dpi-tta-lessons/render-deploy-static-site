# Deploying a Static Website on Render

Let's deploy our static portfolio website to cloud hosting platform [Render](https://render.com).

## Goals

In this lesson we'll use [Render](https://render.com) to deploy our portfolio website so it's available 24/7. By the end of this lesson your portfolio will be available at a url you can share with friends.

<aside class="tip">
  <strong>What does "deploy" mean?</strong>
  Deploying a website means uploading your files to a public server so others can view it online. Platforms like Render host your files in the cloud, so they're always available, even when your computer is off.
</aside>

<aside class="tip">
  <strong>What is the cloud?</strong>
  The cloud refers to powerful computers (servers) you can access over the internet. Instead of hosting your website on your personal machine (which shuts down when you do) the cloud keeps it running 24/7. This means your portfolio is always online and shareable.
</aside>

## Sign Up For Render

Head over to [Render](https://render.com) and click "get started" to create an account.

## Create a New Static Site

Now click on '+ New' -> 'Static Site' to open the [New Static Site](https://dashboard.render.com/static/new) form.

![click new static site](assets/render-new-static-site.png)

<aside class="tip">
  <strong>What is a static site?</strong> A static site is made up of simple files like HTML, CSS, and images. There’s no database or server logic involved—just files served directly to the browser.
</aside>

You'll need to connect your GitHub account to Render so they can access your repository.

![select git provider](assets/git-provider.png)

Now set the name of your static site. This name will be used to create your url. If you enter `app-name`, your site will be live at `app-name.onrender.com`.

![configure name](assets/render-name.png)

Now we need to tell render where to find our code. Since we put our `index.html` file in the project root, we'll enter `./`.

<aside class="tip">
  In UNIX systems, <code>.</code> is used to represent the current directory (or folder). <code>/</code> is used to represent a folder. Together, <code>./</code> means all files in the current directory (folder).
</aside>

![configure publish directory](assets/publish-directory.png)

With everything configured we're ready to deploy. Click "Deploy Static Site".

![deploy static site button](assets/deploy-button.png)

## Deploy

Once Render starts to deploy your site, you can monitor its progress in the events tab.

![events logs](assets/render-events.png)

You'll notice that Render "clones" (or copies) your code from GitHub then uploads it to the server. Static websites are pretty simple. Since this is connected to your GitHub repo, anytime you make a commit to 'main', Render will detect the change and start a new deploy automatically.

<aside class="tip">
  In the past, developers used FTP (File Transfer Protocol) to manually upload website files to a server. By connecting GitHub, Render skips that step. Every time you push changes to your repository, Render automatically grabs the latest code and redeploys your site for you. It’s like having automated FTP, but way smarter.
</aside>

## Custom Domains

In the next lesson we'll dive into domains. If you purchase your own domain you can configure it in the settings tab.

![configure custom domains](assets/render-custom-domains.png)

## Wrap-Up

You just deployed your first static site using Render! 🎉 Your portfolio is now live and ready to share.

In the next lesson, we’ll explore how to connect a **custom domain** so your site looks more professional (like `yourname.dev` instead of `yourname.onrender.com`).

Want to dive deeper?

- [What is static vs dynamic hosting?](https://www.cloudflare.com/learning/cdn/static-dynamic-content/)
- [Render Docs](https://render.com/docs/)
