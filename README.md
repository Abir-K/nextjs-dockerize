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

For nginx congifuration this is official nginx config refer:https://nextjs.org/docs/app/building-your-application/deploying/static-exports 


'Final'

For multistage build with nginx add these 2 line in dockerfile

`COPY --from=build-stage /app/out/ /usr/share/nginx/html`
`COPY ./conf/nginx.conf /etc/nginx/conf.d/default.conf`

you must have to have nginx.conf file into your project directory in this case i use official nginx config which is referred on the upper link
