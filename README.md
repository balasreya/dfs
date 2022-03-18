# dfs
#include<stdio.h>
#define max 20
int graph[max][max];
int visited[max];
int i,j,n;
void readGraph()
{
    printf("enter the size of the adjacent matrix");
    scanf("%d",&n);
    printf("enter the adjacent matrix");
    for(int i=0;i<=n;i++)
    {
        for(int j=0;j<=n;j++)
        {
            scanf("%d",&graph[i][j]);
        }
    }
}
void dfs(int v)
{
    visited [v]=1;
    scanf("%d",v);
    for(int i=0;i<=n;i++)
    {
        if(visited[i]==0&&graph[v][i]==1)
        {
            visited [i]=1;
            dfs(i);
        }
    }
}
void main()
{
    readGraph();
    printf("depth of first search\n");
    for(int i=0;i<=n;i++)
    {
    printf("graph started at vertex %d\n,j");
    for(int j=0;j<=n;j++)
    {
        visited [i]=0;
    }
    }
    dfs(j) ;
    
    printf("\n");
}
