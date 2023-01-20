# jellyfin-mpc-tampermonkey
Tampermonkey scripts to use MPC with Jellyfin

This works for me using Tampermonkey 4.18.1 on Firefox.

It generates and downloads an m3u file. You have to tell Firefox to open the file directly with MPC instead of saving the m3u.

the script using GM_xmlhttpRequest should work for the current release of MPC-HC. It bypasses errors with CORS.

The script using fetch works for me using the allow-origin header modified MPC.

I'm trying to refactor the code to use Jellyfin ApiClient.ajax calls instead of fetch.

Note: I had to do a PR on MPC to update the headers and allow CORS requests. The PR has been merged, but the script probably won't be able to update Jellyfin with MPC progress until the merged version of MPC is released.

Or you can compile it from my MPC repository.

I have no idea how any of this stuff works or what I'm doing.
