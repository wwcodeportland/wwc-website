# wwc-website
Project repo for the WWC PDX website 

* Development project link: https://wwcodeportland.github.io/wwc-website/)
* Project Trello board: https://trello.com/b/p1GOexLQ/wwc-website-project

[this is a work in progress - check back soon for updated versions]

### SETUP
How to get this project running on your machine.

1. [Install Git.](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)

    Open terminal (Mac) or command prompt (Windows) and check that it's installed:

      ```sh
      which git
      ```

    That should return a path (e.g., `/usr/local/bin/git`).

2. Install Python 3.

    - Download the latest version of Python (which as of this writing is 3.6.3). The downloadable installer should work for any operating system: https://www.python.org/downloads/

    - Once installed, check that it's installed:

        ```sh
        which python3
        ```

        That should return a path (e.g., `/usr/local/bin/python3`).
        If you're using Windows and get an error message, try using `python` without the 3.

3. [Fork this repository.](https://github.com/wwcodeportland/wwc-website#fork-destination-box) This creates a copy of the repository on your GitHub account.
        

4. Clone git repository. This creates a copy of the repository's files on your machine.

      ```sh
      git clone git@github.com:YOUR_GITHUB_USERNAME/wwc-website.git
      ```

5. Move into that repository. Depending on where you put it, you may have to `cd` into other folders first.

      ```sh
      cd wwc-website
      ```

6. Set up and activate a [Python virtual environment](https://docs.python.org/3/library/venv.html):

    ```sh
    python3 -m venv venv
    source venv/bin/activate
    ```
    
    You should see `(venv)` prefixed in front of your terminal prompt, letting you know the virtual environment is active.


7. Install the requirements using `pip`. `pip` is a tool for installing and managing Python packages and is included in every virtual environment.

    ```sh
    pip install -r requirements.txt
    ```
    
8. Run the app:

    ```sh
    python manage.py runserver
    ```

    Open your browser and go to [http://localhost:8000/].

    The admin dashboard is available at [http://localhost:8000/admin].


### WEBSITE PROPOSED REDESIGN
[Current desktop mockup prototype](https://xd.adobe.com/view/e20a88af-fcee-441d-a2b5-2493744d2247/)

[Current mobile mockup prototype](https://xd.adobe.com/view/16d03437-a576-4108-969d-38c4a99804e7/)

### OLD WEBPAGE
![Current desktop site](/screenshots/WWCode-current-site.png)

#### ATTRIBUTIONS
* [patternlab-node](https://github.com/pattern-lab/patternlab-node)
* [starterkit-mustache-demo](https://github.com/pattern-lab/starterkit-mustache-demo)
