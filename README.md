
for node, neighbors in graph.items():
    for neighbor, weight in neighbors.items():
        G.add_edge(node, neighbor, weight=weight)

pos = nx.spring_layout(G)

nx.draw_networkx_nodes(G, pos)

nx.draw_networkx_edges(G, pos)

labels = {node: node for node in G.nodes()}
nx.draw_networkx_labels(G, pos, labels)

path_edges = [(path[i], path[i + 1]) for i in range(len(path) - 1)]
nx.draw_networkx_edges(G, pos, edgelist=path_edges, edge_color='r', width=2)

plt.axis('off')
plt.show()
