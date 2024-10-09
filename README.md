# Algorithms

### DFS

<code-block lang="python">

def dfs(G,start, visited=None):
    if visited is None:
        visited = set()
    visited.add(start)
    for next in G[start]-visited:
        dfs(G,next,visited)
    return visited
  graph = {'0': set(['1', '2']),
         '1': set(['0', '3', '4']),
         '2': set(['0']),
         '3': set(['1']),
         '4': set(['2', '3'])}

dfs(graph, '0')
        
<code-block>
