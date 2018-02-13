# 🚀 Devise 🚀


### Set up

Après la création de l’app et bundle install :

    `$ rails g devise:install`

### Routes, models, migrations

Générer automatiquement model et migration :

    `$ rails g devise User`

😃 Avec cette méthode, pas besoin de g controller Users
😃 Aussi, les routes ont intégré **devise_for :users**

Créer / modifier le schéma :

    `$ rails db:migrate`

✔️ Checker les routes créées 

    `$ rails routes`

### Views

Générer les views : 

    `$ rails g devise:views`

➕ Ajouter des données à l’inscription, un exemple avec l'adresse de l'utilisateur : 

    `$ rails g migration AddAddressToUsers address:string`
    `rails db:migrate`

Dans l’ ApplicationController `app/controllers/application_controller.rb`

    `before_action :sanitize_devise_params, if: :devise_controller?

     def sanitize_devise_params
  	 devise_parameter_sanitizer.permit(:sign_up, keys: [:address])
     end`

On modifie le formulaire dans la view `views/devise/registrations/new.html.erb`

__

Aller plus loin : https://www.sitepoint.com/devise-authentication-in-depth/
