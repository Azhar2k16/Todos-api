# A Todo list App with React Frontend With Rails Api
A simple Todo list written ``` api``` performing crud operations using React as Frontend.
I also used [ant.design](https://ant.design/) for style components.
# Key Challenges

Cross-Origin Resource Sharing (CORS) is an HTTP-header based mechanism that allows a server to indicate any origins (domain, scheme, or port) other than its own from which a browser should permit loading resources. By default it's not handled by the framework which will not allow our frontend to make request to the api.

Some changes needs to be done at the back-end side(api):

* Add ``` gem "rack-cors", "~> 1.1" ``` to your GemFile
* In your cors.rb file do the following:
``` Rails.application.config.middleware.insert_before 0, Rack::Cors do
  allow do
    origins 'https://your-url.com'

    resource '*',
      headers: :any,
      methods: [:get, :post, :put, :patch, :delete, :options, :head]
  end
end
```
* Enable ``` config.force_ssl = true ``` from your ```production.rb``` file


## 🔗 [Demo](https://todos-api-frontend.herokuapp.com/)


# Tech Stack
![React](https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361DAFB)
![Ruby](https://img.shields.io/badge/ruby-%23CC342D.svg?style=for-the-badge&logo=ruby&logoColor=white)
![Rails](https://img.shields.io/badge/rails-%23CC0000.svg?style=for-the-badge&logo=ruby-on-rails&logoColor=white) ![Postgres](https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white)
![Heroku](https://img.shields.io/badge/heroku-%23430098.svg?style=for-the-badge&logo=heroku&logoColor=white)
![Sublime Text](https://img.shields.io/badge/sublime_text-%23575757.svg?style=for-the-badge&logo=sublime-text&logoColor=important)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
