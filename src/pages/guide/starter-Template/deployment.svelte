<script>
  import Prism from "svelte-prism";
  import Note from "@/components/Note.svelte";
  import { url } from "@sveltech/routify";
</script>

<!-- routify:options index=40 -->
<div class="c-content">
  <div class="c-container-vertical--small">
    <h1 class="c-h1">Overview</h1>
    <p>Deployments can be done in a few different ways.</p>
  </div>
  <div class="c-container-vertical--small">
    <h3 class="c-h3">Netlify</h3>
    <ul>
      <li>
        <strong>Github connection</strong>
        (recommended)
        <p>
          Connect the repository to Netlify and go to
          <code>Site settings</code>
          ->
          <code>Build & deploy</code>
          .
        </p>
        <p>Then update the settings to</p>
        <table>
          <tr>
            <td>
              <strong>Base directory</strong>
            </td>
            <td>
              <code>scripts/netlify</code>
            </td>
          </tr>
          <tr>
            <td>
              <strong>Build command</strong>
            </td>
            <td>
              <code>npm run build</code>
            </td>
          </tr>
        </table>

      </li>
      <li>
        <strong>Command line</strong>
        <p>
          To deploy directly from the command line, run
          <code>npm run deploy:netlify</code>
          from the project folder.
        </p>
      </li>
      <li>
        <strong>Github actions</strong>
        <p>
          Please refer to Google for information on how to setup Github actions
          for netlify.
        </p>
      </li>
    </ul>

  </div>
  <div class="c-container-vertical--small">
    <h3 class="c-h3">Now</h3>
    <ul>
      <li>
        <strong>Command line</strong>
        <p>
          To deploy directly from the command line, run
          <code>npm run deploy:now</code>
          from the project folder.
        </p>
      </li>
      <li>
        <strong>Github actions</strong>
        <p>
          Example of Github action can be seen
          <a
            href="https://github.com/sveltech/routify-site-2020/blob/434c3510455f5b1e255a41e18e324b046b95cf44/.github/workflows/deploy-master.yml">
            here.
          </a>
          The Now tokens can be found in the
          <code>scripts/now/.now</code>
          folder . If they're not present, they can be generated by running
          <code>npm run deploy:now</code>
          from the project root.
        </p>
      </li>
    </ul>
  </div>
  <div class="c-container-vertical--small">
    <h3 class="c-h3">Custom</h3>
    <p>
      It's possible to host Routify on your own server. We recommend
      <a href="https://github.com/sveltech/spassr">spassr</a>
      which can serve your app as both SPA and SSR.
    </p>
  </div>
</div>


<!-- TODO the options look too much like steps which  -->
