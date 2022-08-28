# Why a website better be under 14kb

**TCP** (Transport Control Protocol) is built upon **IP** (Internet Protocol) which itself is just a system to send packets from point a to b over the Internet. TCP allows browser to tell which packets have arriwed. Browser and server talk like that unitll all packets have arriwed. 

Server start with a slow start sending only 10 packets of 1460 bytes which is equal to: `10 * 1460 bytes = 14600 bytes` or `14.6kb`. And then doubling the amount the packets until it does not get acknowledgement that browser recieved sent packets.

And that's why a website better by under 14kb, so that the server can send the whole website in one transition.

Of course, you should make your website as small as possible — you love your visitors and you want them to be happy. Aiming for each page to fit in under 14kB is good target.

That 14kB includes compression — so it could actually be more like ~50kB of uncompressed data — which is generous.

#TCP #IP #HTTP #Performance