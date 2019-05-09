# P4A GRPC recipe

Testing migration of GRPC to Python for Android (p4a) recipe

# Provisional installation

In your Python P4A project:

``` bash
mkdir p4a-recipes && cd p4a-recipes
git clone git@github.com:hpsaturn/p4a_grpc_recipe.git grpc
cd ..
```

# Building

Please first build a [p4a Docker](https://python-for-android.readthedocs.io/en/latest/docker/) image in your system and then:

``` bash
docker run -it --rm -v $(pwd):/home/user/project p4a /bin/sh -c '. venv/bin/activate && cd /home/user/project && p4a apk --sdk-dir /opt/android/android-sdk --ndk-dir /opt/android/android-ndk --android_api 27 --private . --package=com.android.project --name "TEST P4A Grpc" --version 0.1.0 --bootstrap=sdl2 --requirements=grpc --permission INTERNET'
```

