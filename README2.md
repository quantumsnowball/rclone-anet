# Patch using anet

1. add anet as a module, run: 
`go get github.com/wlynxg/anet`

2. build the binary, run:
`go build -ldflags "-checklinkname=0"`

# Remarks

After this custom build rclone, the SSDP service is still not working properly,
so I found another solution is to write my own SSDP server using Python, which
will manually broadcast message and answer clients' SSDP request to discover
rclone dlna server. While I expect this rclone or golang bug will eventually be
fixed. Meanwhile this is the temp solution.
