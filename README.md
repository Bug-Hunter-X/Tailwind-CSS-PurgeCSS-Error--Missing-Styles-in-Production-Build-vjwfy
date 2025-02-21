# Tailwind CSS PurgeCSS Error: Missing Styles in Production Build

This repository demonstrates a common issue encountered when using Tailwind CSS with frameworks like Next.js or Nuxt.js: the purging of unused CSS classes during the build process resulting in missing styles in the production environment.  The example showcases the problem and its resolution.

## Problem

The `bug.js` file exhibits missing styles because the PurgeCSS configuration in `tailwind.config.js` (or its equivalent) does not correctly identify all the CSS classes used in the application. This often arises from dynamic component imports or complex routing structures.  The result is a production build that lacks essential styles.

## Solution

The `bugSolution.js` file presents a solution. The key is to ensure the `content` array in your `tailwind.config.js` correctly points to all template files where Tailwind classes are used.  This might involve using globbing patterns to include files from various directories or specifying components more explicitly.  Alternative approaches involve optimizing your framework's configuration for Tailwind integration, or disabling PurgeCSS for development (but enabling it for production).