# Kubernetes
Study notes
<h2>Resources</h2>
<p>
  <ul>
    <li>https://kubernetes.io/docs/tutorials/kubernetes-basics/</li>
    <li>https://www.freecodecamp.org/news/the-kubernetes-handbook/</li>
    <li>https://youtu.be/s_o8dwzRlu4?si=0ETpts53_m0569nG</li>
  </ul>
</p>
<p><img src="kubernetescluster.png"></p>
<h2>What is Kubernetes?</h2>
<p>
  <ul>
    <li>Kubernetes or K8, is an open source container orchestrator tool</li>
    <li>Help you manage thousands of applications</li>
    <li>Provides high availability, scalability, and disaster recovery</li>
    <li>Can be deployed on either physical or virtual machines</li>
    <li>Kubernetes places containers into Pods to run on Nodes.</li>
  </ul>
</p>

<h2>Kubernetes Architecture</h2>
<p>
  <ul>
    <li>Control Plane - Manages the cluster and the nodes that are used to host the running applications</li>
    <p>
    <ul>
      <li>API Server - This is the entry point to K8s cluster</li>
      <li>Controller Manager - keeps tracks of whats happening in the cluster</li>
      <li>Scheduler - decides on which node the new pod should be scheduled.</li>
      <li>etcd - key value store for backup and recovery</li>
      <li>cloud-controller-manger - allows you to link a cluster into a cloud provider's API</li>
    </ul>
  </p>
    </ul>
    <ul>
    <li>Node: Virtual or physical machine managed by the control plane.Components of the node: kubelet, container runtime, kube-proxy. The name of a Node, must be a valid DNS subdomain name. You can create and modify node objects using kubectl.</li>
      <p>
        <ul>
          <li>Container Runtime Interface (CRI) - plugin interface which enables the kubelet to use a wide variety of container runtimes. One is needed on each node in your cluster.</li>
          <li>kubelet - agent that runs on each node</li>
          <li>kube-proxy - network proxy that runs on each node in your cluster. The proxy maintains network runs on nodes and allows communication to Pods fron inside and outside of the cluster</li>
        </ul>
      </p>
    </ul>
  </ul>
</p>
