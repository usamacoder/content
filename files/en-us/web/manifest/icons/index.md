---
title: icons
slug: Web/Manifest/icons
browser-compat: html.manifest.icons
---

{{QuickLinksWithSubpages("/en-US/docs/Web/Manifest")}}

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">Type</th>
      <td><code>Array</code></td>
    </tr>
    <tr>
      <th scope="row">Mandatory</th>
      <td>Yes</td>
    </tr>
  </tbody>
</table>

The `icons` member specifies an array of objects representing image files that can serve as application icons for different contexts. For example, they can be used to represent the web application amongst a list of other applications, or to integrate the web application with an OS's task switcher and/or system preferences.

## Examples

```json
"icons": [
  {
    "src": "icon/lowres.webp",
    "sizes": "48x48",
    "type": "image/webp"
  },
  {
    "src": "icon/lowres",
    "sizes": "48x48"
  },
  {
    "src": "icon/hd_hi.ico",
    "sizes": "72x72 96x96 128x128 256x256"
  },
  {
    "src": "icon/hd_hi.svg",
    "sizes": "any"
  }
]
```

## Values

Image objects may contain the following values:

<table class="fullwidth-table standard-table">
  <thead>
    <tr>
      <th scope="col">Member</th>
      <th scope="col">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><code>sizes</code></td>
      <td>
        A string containing space-separated image dimensions using the same syntax as the
        {{ htmlattrxref("sizes", "link") }}
        attribute.
      </td>
    </tr>
    <tr>
      <td><code>src</code></td>
      <td>
        The path to the image file. If <code>src</code> is a relative URL, the
        base URL will be the URL of the manifest.
      </td>
    </tr>
    <tr>
      <td><code>type</code></td>
      <td>
        A hint as to the media type of the image. The purpose of this member is
        to allow a user agent to quickly ignore images with media types it does
        not support.
      </td>
    </tr>
    <tr>
      <td><code>purpose</code></td>
      <td>
        <p>
          Defines the purpose of the image, for example if the image is intended
          to serve some special purpose in the context of the host OS (i.e., for
          better integration).
        </p>
        <p>
          <a href="https://w3c.github.io/manifest/#purpose-member"
            ><code>purpose</code></a
          >
          can have one or more of the following values, separated by spaces:
        </p>
        <ul>
          <li>
            <code>monochrome</code>: A user agent can present this icon where a
            <a
              href="https://w3c.github.io/manifest/#monochrome-icons-and-solid-fills"
              >monochrome icon with a solid fill</a
            >
            is needed. The color information in the icon is discarded and only
            the alpha data is used. The icon can then be used by the user agent
            like a mask over any solid fill.
          </li>
          <li>
            <code>maskable</code>: The image is designed with
            <a href="https://w3c.github.io/manifest/#icon-masks"
              >icon masks and safe zone</a
            >
            in mind, such that any part of the image outside the safe zone can
            safely be ignored and masked away by the user agent.
          </li>
          <li>
            <code>any</code>: The user agent is free to display the icon in any
            context (this is the default value).
          </li>
        </ul>
      </td>
    </tr>
  </tbody>
</table>

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}
