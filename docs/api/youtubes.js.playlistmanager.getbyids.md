<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [youtubes.js](./youtubes.js.md) &gt; [PlaylistManager](./youtubes.js.playlistmanager.md) &gt; [getByIds](./youtubes.js.playlistmanager.getbyids.md)

## PlaylistManager.getByIds() method

Fetches a playlist by its ID.

**Signature:**

```typescript
getByIds(ids: string[], pageToken?: string): Promise<Result<Pagination<Playlist[]>, YouTubesJsErrors>>;
```

## Parameters

<table><thead><tr><th>

Parameter


</th><th>

Type


</th><th>

Description


</th></tr></thead>
<tbody><tr><td>

ids


</td><td>

string\[\]


</td><td>

The IDs of the playlist.


</td></tr>
<tr><td>

pageToken


</td><td>

string


</td><td>

_(Optional)_ The token for pagination.


</td></tr>
</tbody></table>
**Returns:**

Promise&lt;Result&lt;[Pagination](./youtubes.js.pagination.md)<!-- -->&lt;[Playlist](./youtubes.js.playlist.md)<!-- -->\[\]&gt;, [YouTubesJsErrors](./youtubes.js.youtubesjserrors.md)<!-- -->&gt;&gt;

## Remarks

- This operation uses 1 quota unit. - Note: The YouTube API returns empty data instead of an error when a playlist with the specified ID is not found.

[YouTube Data API Reference](https://developers.google.com/youtube/v3/docs/playlists/list)

## Example


```ts
import { ApiClient, StaticOAuthProvider } from "youtubes.js";

const oauth = new StaticOAuthProvider({
 accessToken: "ACCESS_TOKEN",
});
const client = new ApiClient({ oauth });
const playlists = await client.playlists.getByIds(["ID1", "ID2"]) // Result<Pagination<Playlist[]>, YouTubesJsErrors>
```

