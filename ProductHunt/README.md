# Product Hunt Integration Template

This integration runs every hour and checks for new votes and comments on specific Product Hunt Products.

![](https://github.com/orbit-love/community-js-producthunt-orbit/raw/main/docs/activity.png)

This data will be added to your Orbit workspace as new activities.

> If you are a developer and want to incorporate this integration into your existing applications then please check out the [standalone JavaScript library](https://github.com/orbit-love/community-js-producthunt-orbit).

## Instructions

1. Go to your repository created during your [first-time setup](../FIRST_TIME_SETUP.md) and click on the Actions tab.
2. Click "set up a workflow yourself" and call it producthunt.yml - delete the content so it is blank.
3. Copy the contents of [producthunt.yml](producthunt.yml) into your new workflow.
4. Edit the items underneath line 11 to add your product ids to watch. IF you do not know yours refer to the second at the bottom of this guide.
5. This automation requires credentials from Product Hunt to be added to your GitHub repository secrets.
    1. Create a new [Product Hunt API Application](https://www.producthunt.com/v2/oauth/applications) (redirect URI can be any web address).
    2. Take note of your API Key and API Secret.
    3. Follow the steps in the [GitHub Actions Templates First Time Setup Guide](https://github.com/orbit-love/github-actions-templates/blob/main/FIRST_TIME_SETUP.md) and add `PRODUCT_HUNT_API_KEY` and `PRODUCT_HUNT_API_SECRET` values.

Once the workflow and credentials have been added to your GitHub repository, the workflow will be activated. You do not need to do anything else to activate it.

## Getting Product IDs

Product Hunt provides no simple way to see your Project ID (the one for Orbit's innitial release was 297453). If you have Node.js installed and you know the username of one of the 'makers' (visible on each product) - you can get their Product IDs by running:

```
$ npx @orbit-love/producthunt --products --user=THEIR_USERNAME
```
