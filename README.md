# Goal: Run DNA metabarcoding data analysis in a cloud computer

## Step 1

Create cloud computer on Nectar cloud per the instructions and code in the following repo

https://github.com/mitchac/ansible-nectar

## Step 2

[Installing-software.md](Installing-software.md)

## Step 3

[Getting-data.md](Getting-data.md)

## Step 4

[Running-analysis.md](Running-analysis.md)

## Step 5

#### Copy your results 
Copy your results to cloud storage
```
rclone copy results remote:emri-files/projects/nextflow-test/results
```

#### Detach volume from the cloud computer 
Detach volume
```
openstack server remove volume [your-instance-id] \
  [your-volume-id]
```
#### Delete volume from the cloud computer 
Delete volume
```
openstack volume delete [your-volume-id]
```

#### Delete cloud computer 
Delete cloud computer 
```
openstack server delete [your-server-id]
