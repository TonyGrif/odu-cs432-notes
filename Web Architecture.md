# Web Structure
[[The Web and Internet | The Web]] can be understood as a graph where web-pages are nodes & the links are directed edges. The **in-degree** of a page is the number of links to a node and the **out-degree** is the number of links pointing out of a node. The typical web graph follows a **power law distribution** where only a few web-pages contain a high in-degree. There exist many hubs (pages with many in-links) on the Web.
## Bow-Tie Structure
![](https://lh7-us.googleusercontent.com/b6P5bR4UUVpNdE-0iCCjScgTYaqhg-zXMIGylxF8HQCpU9jg7nKnkzD0IeN0VEzY4PAhBK8joYRGMpIuMvkB45480d7n0XQ0tTkdtDtVR3Iye-hHtR_JIY28O5ZEX8DqKXkw5o4ACCPovWLGqcYRnwr6=nw)

* SCC: strongly connected component, all nodes here can reach one another with directed links.
* IN: pages that can reach the SCC, but cannot be reached from it.
* OUT: pages accessible from the SCC, but cannot link back to it.
* Tendrils: pages that cannot reach the SCC or be reached from the SCC, can only be reached from IN, can only reach OUT.
* Tubes: connects a Tendril hanging off IN to a tendril leading to OUT.
* Disconnected: pages with no in-links or out-links.
# Web Size
The frequency of any page is inversely proportional to its rank in the frequency table. This is known as **Zipf's Law**. Relative change in quantity results in a proportional change in the other quantity. A small number of items are clustered at the top of a distribution. This is known as a **power law distribution** and is reflected on the Web.
## Link Rot
Phenomenon on the Web where links will cease to exist over time.
## Content Drift
Phenomenon on the Web where links are maintained and available, but the content found is different from when cited.