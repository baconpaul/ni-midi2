# v1.2.0

* add support for System Exclusive 8 messages
* introduce `sysex7_packet`, move payload members from `data_message` into `sysex7_packet`

## Migration guide

`make_sysex7_<XXX>_packet` factory functions now return `sysex7_packet` instead of `data_packet`.
This might require minor changes to variable types and function signatures.

# v1.1.1

* fix `device_identity` handling in MIDI CI and stream messages
* fix faulty assertions in `sysex7::add_uint14` / `sysex7::add_uint28`

# v1.1.0

* cherry-pick UMP specification `scaleUp` as `upsample_x_to_ybit`
* add `as_midi1_channel_voice_message` and `as_midi1_channel_voice_message`
* add `send_sysex7` and `send_xxx` stream messages
* introduce `sysex::data_type` and optional custom sysex data allocator
* improve MIDI-CI message creation to avoid redundant resizes/allocs of sysex data vector
* introduce sysex7_collector::set_max_sysex_data_size
* some more minor tweaks and improvements

# v1.0.0

* initial public release
