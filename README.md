# Reproduce error:

Run  
`nx r the-next-app:serve`

Vs. build:
`nx r the-next-app:build`
`cd dist/apps/the-next-app/`
`../../../node_modules/.bin/next start`

Problem:

The inital load of build version contains wrong CSS classes (still makeStyle from material-ui, and not the compiled jss1)
