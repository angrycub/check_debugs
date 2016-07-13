# Riak Debug Preprocessor

check_debugs is a bash script that performs some pre-analysis to the folder structures created in riak-debug artifacts.

## How to use

1. Put check_debugs into a folder in your path.

2. Create a subdirectory containing the tarballs generated by running riak-debug on each of your nodes.

3. Untar each of the riak-debug files.

4. Run check_debug

## What it creates

**combined_console.log** - A combination of all of the console logs files and their rotations from every node in timestamp order 
**combined_console.log.nospam** - **combined_console.log** with some of the more spammy log events removed.
**combined_error.log** - A combination of all of the error logs files and their rotations from every node in timestamp order 
**corruption.log** - A list of all the AAE vnodes indicating corruption
**large_object.log** - A list of all of the objects logged as being large objets.
**siblings.log** - A list of all of the objects with high sibling counts.
```
