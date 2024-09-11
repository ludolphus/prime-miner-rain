This repository is setup in such a way that it functions as a file storage for a website hosted on a custom domain (https://rain.primeminer.xyz/)

---

To host a static webpage (HTML, CSS, and JS files) on GitHub and use a custom domain, follow these steps:

Step 1: Create a GitHub Repository

    Sign in to GitHub.
    Create a new repository:
        Go to your GitHub profile, click on the “Repositories” tab, and click the “New” button.
        Name the repository, e.g., my-website. Make sure it’s public.
    Upload your files:
        Upload your HTML, CSS, and JS files to this repository.
        You can either do this via drag-and-drop from the GitHub interface or by pushing the files using Git.

Step 2: Set Up GitHub Pages

    Enable GitHub Pages:
        Go to the settings of your repository.
        Scroll down to the "Pages" section in the sidebar.
        Under Source, choose the branch (often main or master) and the root directory (or /docs if your files are there).
        Click "Save".

    Access the website:
        After a few minutes, GitHub will publish your site. The URL will be https://username.github.io/repository-name.

Step 3: Purchase/Configure a Custom Domain

    Purchase a domain from a domain registrar.

    Add a CNAME file to your repository:
        In the root directory of your GitHub repository, create a new file called CNAME (without an extension).
        In this file, add your custom domain, e.g., www.example.com.

Step 4: Configure DNS Settings

    Go to your domain registrar’s DNS settings:
        Find the settings where you manage DNS records for your domain.

    Set up an A record to point to GitHub’s IP addresses:
        Set the host as @ (or leave it blank) and point it to these IP addresses:

        185.199.108.153
        185.199.109.153
        185.199.110.153
        185.199.111.153

    Set up a CNAME record for the www subdomain (if you want to use it):
        Host: www
        Value: username.github.io (replace username with your GitHub username).

    Wait for DNS propagation:
        This may take up to 24 hours.

Step 5: Verify Custom Domain on GitHub

    Return to your repository’s settings, and in the GitHub Pages section, enter your custom domain (e.g., www.example.com).
    Save the settings, and GitHub will verify that the domain is set up correctly.

Once DNS propagation completes, your website should be accessible through your custom domain.
