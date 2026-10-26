EX NO 10 – FIFO Page Replacement Algorithm
Aim
To implement the FIFO page replacement algorithm.
Domain / Use Case
Google Maps – route navigation and map tile caching.
Files
File	Description
`ex10_partA_bfs_route.c`	Part A – BFS route from A to F (route navigation)
`ex10_partB_optimal_page_replacement.c`	Part B – page replacement that evicts the page used farthest in the future
`ex10_partC_fifo_cache.c`	Part C – FIFO page replacement (map tile cache)
`ex10_partA_output.png`, `ex10_partB_output.png`, `ex10_partC_output.png`	Program outputs
Part A – BFS Route Navigation
Six locations A–F are stored as an adjacency matrix. Breadth-first search finds the route from A to F and traces it back using predecessor links.
```bash
gcc ex10_partA_bfs_route.c -o bfs
./bfs
```
![Part A output](ex10_partA_output.png)
Part B – Page Replacement (look-ahead)
Reference string `7 0 1 2 0 3 0 4 2 3 0 3 2` with 3 frames. On a fault with all frames full, the page whose next use is farthest away is replaced. Total page faults = 7.
```bash
gcc ex10_partB_optimal_page_replacement.c -o page
./page
```
![Part B output](ex10_partB_output.png)
Part C – FIFO Page Replacement
Same reference string and 3 frames. The oldest page in memory is replaced first. Total page faults = 10.
```bash
gcc ex10_partC_fifo_cache.c -o fifo
./fifo
```
![Part C output](ex10_partC_output.png)
Definition
FIFO page replacement – when a page fault occurs and all frames are full, the page that has been in memory the longest is replaced, regardless of how often or how recently it was used.
Result
Successfully implemented page replacement using the FIFO algorithm.
