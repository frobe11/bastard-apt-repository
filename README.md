# bastard-apt-repository
for bastard packages only
## add this repository to apt
run commands below
```bash
curl -fsSL https://frobe11.github.io/bastard-apt-repository/repo.key  | sudo gpg --dearmor -o /usr/share/keyrings/basrepo-archive-keyring.gpg
echo "deb [signed-by=/usr/share/keyrings/basrepo-archive-keyring.gpg] https://frobe11.github.io/bastard-apt-repository/  focal main" | sudo tee /etc/apt/sources.list.d/basfetch.list
sudo apt update
```
### Commands will:
- download public gpg key
- add this repo at apt
- update apt (lol)  

## Packages

### Basfetch
instal any cpp libary from github (only if repo have CMakeLists.txt)
```bash
sudo apt install basfetch -y
basfetch -t https://github.com/laserpants/dotenv-cpp.git
```
