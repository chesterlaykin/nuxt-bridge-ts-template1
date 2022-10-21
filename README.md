Nuxt-bridge-ts-template1

- [Installed dependencies + configurations](#installed-dependencies--configurations)
  - [**Nuxt bridge**](#nuxt-bridge)
    - [@nuxt/bridge-edge](#nuxtbridge-edge)
    - [**package.json change**](#packagejson-change)
    - [**Config changes**](#config-changes)
      - [Nuxt config](#nuxt-config)
        - [Auto imports](#auto-imports)
      - [Typescript fixes](#typescript-fixes)
      - [Run command](#run-command)
      - [Add package](#add-package)
    - [nuxt-property-decorator](#nuxt-property-decorator)
      - [This package needs to be transpiled](#this-package-needs-to-be-transpiled)
  - [**Vite**](#vite)
    - [**Upgrade postcss-preset-env to v7, and postcss to v8**](#upgrade-postcss-preset-env-to-v7-and-postcss-to-v8)
  - [**SASS**](#sass)
    - [**Sass**](#sass-1)
    - [**@nuxtjs/style-resources**](#nuxtjsstyle-resources)

Starter projects with different dependencies and setups, ready to use

# Installed dependencies + configurations

## **Nuxt bridge**

- Nuxt 2 (Created with `yarn create nuxt-app` )
  - Npm option: Javascript (Typescript is added manually)

### @nuxt/bridge-edge

Commands:
`yarn add nuxt-edge`

`yarn add --dev @nuxt/bridge@npm:@nuxt/bridge-edge`

Current nuxt-bridge version: `3.0.0-27711990.d463650`

Nuxt: v3.0.0-rc.8

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

Add to nuxt config: `"extends": "./.nuxt/tsconfig.json",`

#### Run command

**npx nuxi prepare** (generate .nuxt/tsconfig.json )

#### Add package

std-env (fix std-env error)

### nuxt-property-decorator

yarn add nuxt-property-decorator

#### This package needs to be transpiled

Add to nuxt config:

```code
build: {
  transpile: ["nuxt-property-decorator", "vue-class-component"]
}
```

## **Vite**

Enabled in nuxt.config

### **Upgrade postcss-preset-env to v7, and postcss to v8**

Upgrade postcss-preset-env to v7 due to warning from Vite.

This in turn requires upgrade to postcss v8.

## **SASS**

### **Sass**

Sass

### **@nuxtjs/style-resources**

To enable use of sass variables etc in vue components.
NOTE: not working with vite.
