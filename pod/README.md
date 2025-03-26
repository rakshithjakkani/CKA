# kubectl run <PodName> --image <image> --> pod creation
# kubectl run <podName> --image -o yaml --dry-run=client --command -- ping -c 60 google.com 
# kubectl explain pod --> will give you yaml order of pod. You can fetch it for any other object in kubernetes
# kubectl run <podName> --image <Image> --port=8080 -o yaml --dry-run=client --> To expose the container port
    # to create a yaml file for the command-pod.yaml
# docker build -t <ImageName> . --> build the docker image
# docker run <ImageName> 
    # This command will execute both the ENTRYPOINT and CMD and prints "hello world" in the terminal
# docker run <ImageName> hey rakshith 
    # This will print the hey rakshith

# Key points
    # We can override the CMD in run time but ENTRYPOINT not
    # Behind the scenes the container execute the command like:- /bin/echo hey rakshith
    # /bin/echo is standerd that will not change as we pass it in ENTRYPOINT

# In kubernetes command and args can override the docker image's ENTRYPOINT and CMD
    # command can override ENTRYPOINT and CMD
    # args can only override CMD
# In kubernetes, when defining command and args for the container in pods, there are 2 primary ways to define them 
    # Array(json array notation, square brakets[])
    # Multi-line YAML list(- for each new item)

# Exposing ports in kubernetes 
    # we can expose the application port in kubernetes in pod manifest using "ports.-containerPort"
    # This will not impact the application port that is running in the container. It is just like Docker EXPOSE instruction