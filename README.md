# extended
Func _GDIPlus_GraphicsSetInterpolationMode($hGraphics, $iInterpolationMode)     Local $aResult = DllCall($__g_hGDIPDll, "int", "GdipSetInterpolationMode", "handle", $hGraphics, "int", $iInterpolationMode)     If @error Then Return SetError(@error, @extended, False)     If $aResult[0] Then Return SetError(10, $aResult[0], False)      Return True
