# todosh
A lightweight to do list for managing tasks in a shell.  

<p align="center">
  <img src="https://i.ibb.co/Drqt65X/Screenshot-2022-05-13-at-18-06-36.png">
</p>


Tasks stored in local `.todo` file.  
<br/>
I made this for personal use because I find myself in Terminal so often that it made sense to keep track of tasks in it, rather than having to tab out to another program to see them. It also means that tasks are stored alongside projects.  
\
I plan to rewrite this in Rust and distribute it through homebrew in future because adding any more features seems to be beyond the scope of what is already a very hacky bash script.


## Installation

```shell
wget -O todo https://raw.githubusercontent.com/JonLinkens/todosh/main/todo
```

You might find you need to change the permissions to execute it:
```shell
chmod +rwx todo
```
If you want ``todo`` to be a global command, then move it to ``usr/local/bin``:
```shell
sudo mv todo /usr/local/bin/todo
```

## Commands

- **Creating a list**  
  ```shell
  todo # in a directory that does not have a list already
  ```
- **Adding a task**
  ```shell
  todo -a "Some Task Here"
  ```
- **Finishing a task**  
  ```shell
  todo -f task_number # this will delete it from the .todo file!
  ```
- **Deleting a list**
  ```shell
  todo -d 
  ```
- **Version info**
  ```shell
  todo -V
  ```
