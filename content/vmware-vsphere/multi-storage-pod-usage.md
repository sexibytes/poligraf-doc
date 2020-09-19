Using Storage Pod aka Datastore Cluster? In PoliGraf 0.99f we’ve introduced an early **Storage Pod Usage** dashboard with a computed uncommitted metric from the child datastores, very handy. We called it “early support” because we didn’t linked the pods to the clusters but to the datacenters because it’s the way it is in the VMware API world, you can have a pod for many clusters. So until we figure out a smart way to do it, we’ll stick to that. We’re sure you’ll love it anyway 😉

[![](/media/multi_storage_pod_usage.png)](http://www.poligraf.io/multi_storage_pod_usage/)
