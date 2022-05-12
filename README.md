# RegEnumVal
 Func _RegEnumVal($sKey)     Local $i = 1, $sVal, $sResult      While 1         $sVal = RegEnumVal($sKey, $i)         If @error Then ExitLoop         $i += 1         $sResult &amp;= $sVal &amp; "|"     WEnd      Return StringRegExpReplace($sResult, " \(.*?\)", "")  EndFunc   ;==>_RegEnumVal
