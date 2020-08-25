CHIRP for FoundryVTT

Docker setup
Place VTT in ./foundry/
docker buid ./docker -t foundryvtt
docker run --detach --privileged --hostname foundryvtt --name foundryvtt -p 30000:30000 foundryvtt