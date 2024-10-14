#step-1

create your nextjs app or refer a complete project.

#step 2

for optimised build make sure next.config.mjs (current: nextjs14) must include below line inside const NextCOnfig ={};

`const nextConfig = {
    output: 'export'};`

this will allow to create a folder named "out" with some static files those helps in nginx redirection

#step 3 

on the terminal run the build command

'yarn build' or 'npm run build'


#final 

refer this repository's 'Dockerfile' if you need