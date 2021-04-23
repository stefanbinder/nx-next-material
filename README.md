# Reproduce error:

### Run to see how it looks like:  
`nx r the-next-app:serve`

### Vs. nx build:  
`nx r the-next-app:build`  
`cd dist/apps/the-next-app/`  
`../../../node_modules/.bin/next start`

Problem:

The inital load of build version contains wrong CSS classes (still makeStyle from material-ui, and not the compiled jss1)

### Vs. correct build:  
comment in the line in `apps/the-next-app/next.config.js`

`distDir: '../../dist/apps/the-next-app/.next',`

cd' into the src folder:
`cd apps/the-next-app`
execute build:
`../../node_modules/.bin/next build`

go to the dist folder and execute there:
`../../node_modules/.bin/next start`

That build is working fine.
