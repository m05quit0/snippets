[В начало](README.md)

# Vagrant

#### Загрузить локальный конфиг, который не отслеживается VCS.
Добавить нижеследующий код в конец блока Vagrant.configure("2") do |config| и создать файл Vagrantfile.local в корне проекта.

```ruby
# Allow an untracked Vagrantfile to modify the configurations
project_dir = File.dirname(File.expand_path(__FILE__))
eval File.read "#{project_dir}/Vagrantfile.local" if File.exist?("#{project_dir}/Vagrantfile.local")
```
