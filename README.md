For AWS task-8 FE app was adapted to work with Cart, served from Elastic Beanstalk.

Serverless deploy on S3 (Cloudfront is still closed for me): http://igorpex-rs-app.s3-website-eu-west-1.amazonaws.com/
Alternate deploy on netlify : https://shop-react-redux-aws.netlify.app/ 
(comment for me to remember: to deploy I used command 'netlify deploy --prod', then enter 'build' dir)

Cart address http://igorpex-cart-api-develop.eu-west-1.elasticbeanstalk.com/api/profile/cart

Products are downloaded dynamically from APi backend.
Sources are changed at: src\components\pages\PageProducts\components\Products.tsx 
at line 39: axios.get(`${API_PATHS.ts}/dev/products`)
ts - is one of paths in Paths file.
Two choises, working similary: 'ts' and 'commonjs'

Paths are here: src\constants\apiPaths.ts

To start locally, use `npm run start` or `yarn start`.

The app can be built and deployed by running npm script command: 
 `yarn build:deploy` OR  `npm run build:deploy`

In the project directory, you can run:  
You can use NPM instead of YARN (Up to you)  

### `yarn start` OR `npm run start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test` OR `npm run test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build` OR `npm run build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `yarn eject` OR `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).
