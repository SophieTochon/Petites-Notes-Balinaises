**🚀 Devise 🚀**

- Set up :

Juste après la création de l’app et du bundle install :
**$ rails g devise:install**

- Routes, models, migrations :

Pour générer automatiquement model et migration :
**$ rails g devise User**

😃 Avec cette méthode, pas besoin de controller User
😃 Aussi, les routes ont intégré devise_for :users

**$ rails db:migrate** pour créer / modifier le schéma 

✔️ Pour checker les routes créées ➡️ **$ rails routes**

- Views :

Générer les views ➡️ **$ rails g devise:views**

➕ Pour ajouter une ou plusieurs données à l’inscription : exemple ici avec une adresse : 

**$ rails g migration AddAddressToUsers address:string**
Puis **rails db:migrate**

Dans l’ ApplicationController :

  before_action :sanitize_devise_params, if: :devise_controller?

  def sanitize_devise_params
  	devise_parameter_sanitizer.permit(:sign_up, keys: [:address])
  end

On modifie le formulaire dans la view registrations > new

__

Aller plus loin : https://www.sitepoint.com/devise-authentication-in-depth/
