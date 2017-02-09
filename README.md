# datauri
contains uri

Keterangan format data URL scheme ada di:
http://www.ietf.org/rfc/rfc2397

       dataurl    := "data:" [ mediatype ] [ ";base64" ] "," data
       mediatype  := [ type "/" subtype ] *( ";" parameter )
       data       := *urlchar
       parameter  := attribute "=" value
-----------------------------------------------------
data:[<mediatype>][;base64],<data>
-----------------------------------------------------
 data:text/plain;charset=iso-8859-7,%be%fg%be
------------------------------------------------------
application/vnd-xxx-query
------------------------------------------------------
data:application/vnd-xxx-
query,select_vcount,fcol_from_fieldtable/local
-------------------------------------------------------
1. <iframe width="600" height="200" src="data:text/html;charset=utf-8;base64,PCFET0...C9odG1sPg==" ></iframe>
2. <b> data:text/plain;charset=utf-8;base64,bWFrYW4gbmFzaQ== </b>
3. <IMG
   SRC="data:image/gif;base64,R0lGODdhMAAwAPAAAAAAAP///ywAAAAAMAAw
   AAAC8IyPqcvt3wCcDkiLc7C0qwyGHhSWpjQu5yqmCYsapyuvUUlvONmOZtfzgFz
   ByTB10QgxOR0TqBQejhRNzOfkVJ+5YiUqrXF5Y5lKh/DeuNcP5yLWGsEbtLiOSp
   a/TPg7JpJHxyendzWTBfX0cxOnKPjgBzi4diinWGdkF8kjdfnycQZXZeYGejmJl
   ZeGl9i2icVqaNVailT6F5iJ90m6mvuTS4OK05M0vDk0Q4XUtwvKOzrcd3iq9uis
   F81M1OIcR7lEewwcLp7tuNNkM3uNna3F2JQFo97Vriy/Xl4/f1cf5VWzXyym7PH
   hhx4dbgYKAAA7"
   ALT="Larry">
4. data:application/vnd-xxx-
   query,select_vcount,fcol_from_fieldtable/local
5. data:application/x-msdownload;base64,TVqQAAMAAAAEAAAA//8A
   Ini saya coba ubah jadi:
	data:application/octet-stream
		<iframe width="100%" height="100%" src="TVqQAAMAAAAEAAAA//8A"></iframe>
		tidak berhasil, tetap saja terjadi x-msdownload
