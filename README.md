# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).
Create app using this command:

### `npm create vite@latest `

# Select details while running command:

Project name: app-ssr-vite
✔ Select a framework: › Others
✔ Select a variant: › create-vite-extra
✔ Select a template: › ssr-react
✔ Select a variant: › JavaScript

# Run each step:

- cd app-ssr-vite
- npm install
- npm run dev

next build
next export

# at this point, we have an out directory as follows

# out/[all html files]

# out/\_next/[all next files]

# and we have a static directory as follows:

# static/$ASSET_PATH/$ASSET_NAME.$ASSET_EXT/$ASSET_HASH.$ASSET_EXT

# the goal is to be able to have this new directory structure reflect what

# we want in S3, so that we can do aws s3 cp ./out s3://$S3_BUCKET/$NAMESPACE/

# (even though, as you'll see, we don't exactly do that).

mv out/\_next . # out/ contains only html files.
Please talk with me once, do let me know ki hum without her kab baat krenge Isipe reply krke code push kr
mv out \_out
mkdir -p out/builds/$GITHASH
mv _out/* out/builds/$GITHASH
rm -rf \_out
mv \_next out/
