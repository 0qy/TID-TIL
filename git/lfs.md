## Git Large File Storage (LFS)

### to use: 
`git lfs install`
`git lfs track "*.mp4"`
`git add .gitattributes`

then add, commit, and push as usual 

note: lfs tracking sometime don't work if the commit has lots of files changes, seems to work best with the clean commit that only tracks the one file. 

### to uninstall
`git lfs uninstall`

### note
I wanted to use lfs to store a video that I am using for a web app, after some research I realised that it is a bad idea to self-host videos. Some reasons are [here](https://www.wp101.com/10-reasons-why-you-should-never-host-your-own-videos/).

[git lfs](https://git-lfs.github.com/)