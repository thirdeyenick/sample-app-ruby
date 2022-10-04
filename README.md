# Kontent.ai Rails Sample Application

[![Kontent.ai Discord](https://img.shields.io/discord/821885171984891914?color=%237289DA&label=Kontent%20Discord&logo=discord)](https://discord.gg/SKCxwPtevJ) [![Stack Overflow](https://img.shields.io/badge/Stack%20Overflow-ASK%20NOW-FE7A16.svg?logo=stackoverflow&logoColor=white)](https://stackoverflow.com/tags/kontent-ai)

This basic Rails application demonstrates how to create a Rails application using the [Kontent.ai Ruby SDK](https://github.com/kontent-ai/delivery-sdk-ruby) and a [sample project](https://docs.kontent.ai/tutorials/manage-kontent/projects/manage-projects#a-create-a-sample-project).

See [Build your first Ruby on Rails app](https://docs.kontent.ai/tutorials/develop-apps/get-started/build-your-first-app?tech=ruby) for a detailed walkthrough of how the sample application was developed.

![Screenshot](/screenshot.png)

## Install & Run

- Clone the repository
- Run `bundle install`
- You can change the source Kontent.ai project to your own project to be able to change the content. If you don't have your own Sample Project, any admin of a Kontent.ai subscription [can generate one](https://app.kontent.ai/sample-site-configuration).
  - If you want to connect to custom project ID, Open the **app/controllers/application_controller.rb** file and set your project ID on this line:  
    `PROJECT_ID = '<your-project-ID>'.freeze`
- Run `rails server`. Your application will be accessible at **localhost:3000**

## Features

- Loads articles from Kontent.ai asynchronously via [render_async](https://github.com/renderedtext/render_async)
- Rich text component rendering via [`InlineContentItemResolver`](https://github.com/kontent-ai/delivery-sdk-ruby#resolving-inline-content)
- Content item link resolution via [`ContentLinkResolver`](https://github.com/kontent-ai/delivery-sdk-ruby#resolving-links)
