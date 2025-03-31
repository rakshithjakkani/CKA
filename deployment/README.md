# Deployment cli commands
    # kubectl create deploy <deployName> --image <Image> --replicas 2
    # kubectl scale deploy <deploy> --replicas 3 
    # kubectl edit deploy <name> 
    # kubectl set image deploy <name> <containerName>=<Image> --> By default image name will be the container name
    # kubectl rollout history deploy <name>
    # kubectl rollout undo deploy <name> --> to swith back to previous revision
    # kubectl rollout undo deploy <name> --to-revision=2