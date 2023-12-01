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
      <li>Scheduler - decides on which node the new pod should be scheduled.56</li>
      <li>etcd - backup and recovery</li>
    </ul>
  </p>
    </ul>
    <ul>
    <li>Node</li>
    </ul>
  </ul>
</p>
