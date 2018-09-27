# BeekeeperCore

BeekeeperCore is a part of [BEEKEEPER](https://github.com/vinfinit/Beekeeper) project
1. [BeekeeperNative](https://github.com/vinfinit/BeekeeperNative) - react-native application for mobile platforms
2. [beekeeperServer](https://github.com/vinfinit/BeekeeperServer) - main node.js server
3. [beekeeperCore](https://github.com/vinfinit/BeekeeperCore) - core application for hangover face recognition

### Workflow
1. Get image from http request
2. Apply [openfaceAlignDlib](https://github.com/cmusatyalab/openface) for face detection
3. Apply [openfaceAlignDlib](https://github.com/cmusatyalab/openface) for face alignment
4. Extract features from aligned Face
5. Use trained model for hangover face recognition

### Deploy
```bash
cd beekeeper-core
docker build -t beekeeper-core .
docker run --rm --name beekeeper-core -p 8000:8000 -ti beekeeper-core
```

### Usage
```bash
curl --form file=@someimage.png http://localhost:8000/upload
```
