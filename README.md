     .------..
     -          -
   /              \
 /                   \
/    .--._    .---.   |
|  /      -__-     \   |
| |                 |  |
 ||     ._   _.      ||
 ||      o   o       ||
 ||      _  |_      ||
 C|     (o\_/o)     |O     Uhhh, this computer
  \      _____      /       is like, busted or
    \ ( /#####\ ) /       something. So go away.
     \  `====='  /
      \  -___-  /
       |       |
       /-_____-\
     /           \
   /               \
  /__|  AC / DC  |__\
  | ||           |\ \

  1. local paths need to be bound to the correct volumes for the services in docker-compose.yml
  2. be sure that environment variables align properly in both services.
  3. sudo docker-compose up -d to run environment.
  4. sudo docker-compose down to shutdown containers.
  5. sudo docker system prune to remove all (non-running) containers.
  6. after changing file paths to bind volumes run:
    sudo docker-compose down -v --remove-orphans
    sudo docker-compose up -d -V --build --force-recreate
  to be sure that docker addresses the changes.