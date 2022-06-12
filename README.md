A sample command-line application with an entrypoint in `bin/`, library code
in `lib/`.

The addressbook files and the google folder are generated running the command:
protoc \
 --dart_out=grpc:./some_output_folder \
 -I./folder_with_proto_files ./addressbook.proto google/protobuf/timestamp.proto

And this files are based on addressbook.proto file.

After generate all files, you can run and test the project running the commands:

dart add_person.dart ADDRESS_BOOK_FILE (to add person on a list)

dart list_people.dart ADDRESS_BOOK_FILE (to show the list content)
