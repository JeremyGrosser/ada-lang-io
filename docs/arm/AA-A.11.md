---
sidebar_position:  128
---

# A.11  Wide Text Input-Output and Wide Wide Text Input-Output

{AI95-00285-01} The packages Wide_Text_IO and Wide_Wide_Text_IO provide facilities for input and output in human-readable form. Each file is read or written sequentially, as a sequence of wide characters (or wide wide characters) grouped into lines, and as a sequence of lines grouped into pages. 


#### Static Semantics

{AI95-00285-01} {AI95-00301-01} The specification of package Wide_Text_IO is the same as that for Text_IO, except that in each Get, Look_Ahead, Get_Immediate, Get_Line, Put, and Put_Line subprogram, any occurrence of Character is replaced by Wide_Character, and any occurrence of String is replaced by Wide_String. Nongeneric equivalents of Wide_Text_IO.Integer_IO and Wide_Text_IO.Float_IO are provided (as for Text_IO) for each predefined numeric type, with names such as Ada.Integer_Wide_Text_IO, Ada.Long_Integer_Wide_Text_IO, Ada.Float_Wide_Text_IO, Ada.Long_Float_Wide_Text_IO.

{AI95-00285-01} {AI95-00301-01} The specification of package Wide_Wide_Text_IO is the same as that for Text_IO, except that in each Get, Look_Ahead, Get_Immediate, Get_Line, Put, and Put_Line subprogram, any occurrence of Character is replaced by Wide_Wide_Character, and any occurrence of String is replaced by Wide_Wide_String. Nongeneric equivalents of Wide_Wide_Text_IO.Integer_IO and Wide_Wide_Text_IO.Float_IO are provided (as for Text_IO) for each predefined numeric type, with names such as Ada.Integer_Wide_Wide_Text_IO, Ada.Long_Integer_Wide_Wide_Text_IO, Ada.Float_Wide_Wide_Text_IO, Ada.Long_Float_Wide_Wide_Text_IO.

{AI95-00285-01} {AI95-00428-01} {AI05-0004-1} {AI05-0092-1} The specification of package Wide_Text_IO.Wide_Bounded_IO is the same as that for Text_IO.Bounded_IO, except that any occurrence of Bounded_String is replaced by Bounded_Wide_String, and any occurrence of package Bounded is replaced by Wide_Bounded. The specification of package Wide_Wide_Text_IO.Wide_Wide_Bounded_IO is the same as that for Text_IO.Bounded_IO, except that any occurrence of Bounded_String is replaced by Bounded_Wide_Wide_String, and any occurrence of package Bounded is replaced by Wide_Wide_Bounded.

To be honest: {AI05-0005-1} "package Bounded" refers to both the package Ada.Strings.Bounded and the formal package parameter named Bounded. 

{AI95-00285-01} {AI95-00301-01} {AI05-0092-1} The specification of package Wide_Text_IO.Wide_Unbounded_IO is the same as that for Text_IO.Unbounded_IO, except that any occurrence of Unbounded_String is replaced by Unbounded_Wide_String, and any occurrence of package Unbounded is replaced by Wide_Unbounded. The specification of package Wide_Wide_Text_IO.Wide_Wide_Unbounded_IO is the same as that for Text_IO.Unbounded_IO, except that any occurrence of Unbounded_String is replaced by Unbounded_Wide_Wide_String, and any occurrence of package Unbounded is replaced by Wide_Wide_Unbounded. 


#### Extensions to Ada 83

Support for Wide_Character and Wide_String I/O is new in Ada 95. 


#### Extensions to Ada 95

{AI95-00285-01} Package Wide_Wide_Text_IO is new. Be glad it wasn't called Double_Wide_Text_IO (for use in trailer parks) or Really_Wide_Text_IO.

{AI95-00301-01} Packages Wide_Text_IO.Wide_Unbounded_IO and Wide_Wide_Text_IO.Wide_Wide_Unbounded_IO are also new.

{AI95-00428-01} Packages Wide_Text_IO.Wide_Bounded_IO and Wide_Wide_Text_IO.Wide_Wide_Bounded_IO are new as well. 


#### Wording Changes from Ada 2005

{AI05-0092-1} Correction: Corrected the names of various entities in the above description. Since the previously named entities don't exist and the intent is obvious, this is just considered a presentation change. 
