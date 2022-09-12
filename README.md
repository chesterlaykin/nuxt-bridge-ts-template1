Nuxt2-ts-storybook : template 1

- [Installed dependencies + configurations](#installed-dependencies--configurations)
  - [**Nuxt bridge**](#nuxt-bridge)
    - [@nuxt/bridge-edge](#nuxtbridge-edge)
    - [**package.json change**](#packagejson-change)
    - [**Config changes**](#config-changes)
      - [Nuxt config](#nuxt-config)
        - [Auto imports](#auto-imports)
      - [Typescript fixes](#typescript-fixes)
      - [Run command:](#run-command)
      - [Add package](#add-package)
  - [**Typescript**](#typescript)
    - [nuxt-property-decorator](#nuxt-property-decorator)
  - [**Vite**](#vite)
    - [**Upgrade postcss-preset-env to v7**](#upgrade-postcss-preset-env-to-v7)
  - [**SASS**](#sass)
    - [**Sass**](#sass-1)
    - [**@nuxtjs/style-resources**](#nuxtjsstyle-resources)

Starter projects with different dependencies and setups, ready to use

# Installed dependencies + configurations

## **Nuxt bridge**

- Nuxt 2 (Created with `yarn create nuxt-app` )
  - Npm option: Javascript (Typescript is added manually)

### @nuxt/bridge-edge

Command:

yarn add --dev @nuxt/bridge@npm:@nuxt/bridge-edge

Current version: `3.0.0-27711990.d463650`

### **package.json change**

"scripts": {
"dev": "nuxi dev",
"build": "nuxi build",
"start": "nuxi preview"
},

### **Config changes**

- package.json - updated "scripts"
- nuxt config: use `"defineNuxtConfig"`
- tsconfig: add: `"extends": "./.nuxt/tsconfig.json"`

#### Nuxt config

##### Auto imports

```text
components: [
    'path: "~/components",'
```

#### Typescript fixes

Removed `@nuxt/typescript-build`:  and remove from from **buildModules** (config)

Added `.output` to the .gitignore file.

#### Run command:
**npx nuxi prepare** (generate .nuxt/tsconfig.json )

#### Add package
std-env (fix std-env error)

## **Typescript**

### nuxt-property-decorator

To use with class based components.
Compatibility:

Latest working: @nuxt/bridge-edge 3.0.0-27690335.da95eff

Latest tested non-working: @nuxt/bridge-edge@3.0.0-27611430.cf4761a

## **Vite**

Enabled in nuxt.config
### **Upgrade postcss-preset-env to v7**

Upgrade postcss-preset-env to v7 due to warning from Vite.


## **SASS**

### **Sass**

Sass

### **@nuxtjs/style-resources**

To enable use of sass variables etc in vue components.
NOTE: not working with vite.
