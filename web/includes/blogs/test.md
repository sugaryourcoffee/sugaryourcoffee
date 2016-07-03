<h2>sftp</h2>
<table class="table table-hover">
  <thead>
    <tr><th>Command</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr>
      <td><tt>$ sftp user@server</tt></td>
      <td>Establishes a connection to the remote server via sftp</td>
    </tr>
    <tr>
      <td><tt>$ cd server-directory</tt></td>
      <td>Changes the directory on the remote host</td>
    </tr>
    <tr>
      <td><tt>$ lcd local-directory</tt></td>
      <td>Changes the directory on the local machine</td>
    </tr>
    <tr>
      <td><tt>$ put local-directory/some-file.shtml</tt></td>
      <td>Copies the file on the local machine to the remote host</td>
    </tr>
    <tr>
      <td><tt>$ get server-directory/some-file.shtml</tt></td>
      <td>Copies the file on the server machine to the local machine</td>
    </tr>
  </tbody>
</table>

<h2>Vim</h2>
<h3>Spell</h3>
<table class="table table-hover">
  <thead>
    <tr><th>Command</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr>
      <td><tt>:set spell</tt></td>
      <td>Fires up spell and highlights misspelled words</td>
    </tr>
    <tr>
      <td><tt>]s</tt></td>
      <td>Moves to the next misspelled word</td>
    </tr>
    <tr>
      <td><tt>[s</tt></td>
      <td>Moves to the previous misspelled word</td>
    </tr>
    <tr>
      <td><tt>z=</tt></td>
      <td>Lists corrections for the misspelled word under the cursor</td>
    </tr>
  </tbody>
</table>

<h3>Vimgrep</h3>
<table class="table table-hover">
  <thead>
    <tr><th>Command</th><th>Description</th></tr>
  </thead>
  <tbody>
    <tr>
      <td><tt>:vimgrep /search-pattern/ file1 file2 file3</tt></td>
      <td>searches in the files and populates the quickfix list</td>
    </tr>
    <tr>
      <td><tt>:vimgrep /search-pattern/ **/*.shtml</tt></td>
      <td>searches all shtml files in the current and all subdirectories</td>
    </tr>
    <tr>
      <td><tt>:vimgrep // **/*.shtml</tt></td>
      <td>uses the last search pattern</td>
    </tr>
    <tr>
      <td><tt>:copen</tt></td>
      <td>opens the quickfix list</td>
    </tr>
    <tr>
      <td><tt>:cclose</tt></td>
      <td>closes the quickfix list</td>
    </tr>
    <tr>
      <td><tt>:cnext</tt></td>
      <td>jumps to the next search result</td>
    </tr>
    <tr>
      <td><tt>:cprevious</tt></td>
      <td>jumps to the previous search result</td>
    </tr>
  </tbody>
</table>
