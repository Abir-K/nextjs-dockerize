'Step-1'

Create your nextjs app or refer a complete project.

'Step 2'

for optimised build make sure next.config.mjs (current: nextjs14) must include below line inside const NextCOnfig ={};

`const nextConfig = {
    output: 'export'};`

this will allow to create a folder named "out" with some static files those helps in nginx redirection

'Step 3'

on the terminal run the build command

'yarn build' or 'npm run build'

'Step 4'

nginx congifuration file should looks like this 


'Final'

refer this repository's 'Dockerfile' if you need
