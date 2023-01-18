# Settings template for Eslint with Prettier

## Eslint

Start settings:
### `npm init @eslint/config`

Install eslint, eslint-plugin-import, eslint-plugin-react, eslint-plugin-react-hooks, and eslint-plugin-jsx-a11y:
### `npx install-peerdeps --dev eslint-config-airbnb`

### Package.json

    "scripts": {
        "lint": "eslint ./src",
        "lint:fix": "eslint ./src --fix",
        "format": "prettier --write"
    },
    "husky": {
        "hooks": {
        "pre-commit": "lint-staged"
        }
    },
    "lint-staged": {
        "*(.js|jsx)": [
        "npm run lint:fix",
        "git add"
        ]
    }

### .Eslintrc

For @babel/eslint-parser: `"parser": "@babel/eslint-parser"`
