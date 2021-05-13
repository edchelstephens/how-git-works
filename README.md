# Pratice Repository for Git mastery

## Blob

    - Not really a file
    - The content of a file
    - The file name and file permission are not stored in the blob
    - But on the TREE that points to the blob

## Commit

    - A commit is just a piece of content

    - Example:

    >> git log
    commit 2eb4d64cb86d13829672b6744660d8b5cfffa564
    Author: Edchel Stephen <yahshua.ninies@gmail.com>
    Date: Tue May 11 08:22:36 2021 +0800

    First commit message on the stupid content tracker! :)

    **Printing the commit**
    >> git cat-file -p 2eb4d64cb86d13829672b6744660d8b5cfffa564

    tree 63f0152369be1137dd9513bf600690f740111d51
    author Edchel Stephen <yahshua.ninies@gmail.com> 1620692556 +0800
    committer Edchel Stephen <yahshua.ninies@gmail.com> 1620692556 +0800

    First commit message on the stupid content tracker! :)

    **The commit points to a tree with the following contents**
    >> git cat-file -p 63f0152369be1137dd9513bf600690f740111d51

    100644 blob 402eeec6649f38a4486254b2cf2f557c23ff2c23	README.md
    100644 blob 23991897e13e47ed0adb91a0082c31c82fe0cbe5	menu.txt
    040000 tree 3c47a1f346ce6bf101bdd16ff95790ae04ed8f60	recipes


    **Adding another commit**
    >> git log
    commit 4264fec50563f68244136121bb61e7495708d25f
    Author: Edchel Stephen <yahshua.ninies@gmail.com>
    Date:   Tue May 11 09:44:46 2021 +0800

        README notes on course.


    **Showing the contents of the second commit**
    >> git cat-file -p 4264fec50563f68244136121bb61e7495708d25f
    tree 83abe5341aba3b898914d723154676f7f87a9006
    parent 2eb4d64cb86d13829672b6744660d8b5cfffa564
    author Edchel Stephen <yahshua.ninies@gmail.com> 1620697486 +0800
    committer Edchel Stephen <yahshua.ninies@gmail.com> 1620697486 +0800

    README notes on course.

## Tags

    - tags are just a label attached to an object

## Names of objects

    - The names of blobs and trees are not in the objects themselves
    - They are on the tree that are pointing to them
    - Note that tree objects are recursive in nature
    - A tree can point to a tree which points to another tree that points to ablob

## Branches

    - A branch is nothing else that a simple reference
    - A branch is just a reference to a commit!
    - That's why the directory containing branches is called `refs` for references
    - The default `master` branch has NO special status on git,
    - Git created the master branch by default for our first commit but it's just like
      any other branch

## REFS

    - HEAD is just a reference to a branch, the current head branch
