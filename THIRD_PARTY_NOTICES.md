# Third-party notices

## we-mp-rss

The `we-mp-rss/` directory is derived from
[rachelos/we-mp-rss](https://github.com/rachelos/we-mp-rss) and includes local
integration changes for 21世纪内阁.

The upstream project is distributed under the MIT License. Its original
license text is preserved at [`we-mp-rss/LICENSE`](we-mp-rss/LICENSE).

The V1.0 baseline was derived from upstream version 1.5.3. Local changes cover
article metadata, article-content retrieval, collector maintenance, and the
subscription workflow used by the Cabinet application.

## Ivory Tower desktop extension

The desktop extension is based on wanshijiaaaa-star/21st-century-cabinet,
baseline commit 17c5513f98adb494eaf257fed85a4922fe52e327. Original repository
licenses and notices are retained; the application is locally renamed 象牙塔.

pywebview 6.2.1 (Roman Sirokov) is distributed under the BSD 3-Clause License.
Its copyright notice, conditions and disclaimer are retained in the bundled
Python distribution's pywebview dist-info license/metadata files. pythonnet,
clr-loader, Bottle and proxy-tools retain their respective bundled notices.
Windows uses the separately installed Microsoft WebView2 runtime.

Desktop installers do not bundle Chromium. The optional browser component is
downloaded through Playwright into the user's application data directory and
retains the Chromium distribution's associated third-party notices. Existing
compatible Chrome or Edge installations retain their own licenses and notices.
Python and other bundled dependencies retain their licenses within the private
Runtime directory.
