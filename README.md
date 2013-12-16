test
====

```pascal
procedure TLayerViewer.InitialDisplayParams;
begin
  FRealRange:=Rect(0, 0, FPaintBoxRef.Width, FPaintBoxRef.Height); // åå§ååè¨­è·ç«å¸ä¸æ¨£
  FViewRange:=Rect(0, 0, FPaintBoxRef.Width, FPaintBoxRef.Height);

  FVertiCurViewPosition   := 0;
  FVertiMinViewPosition   := 0;
  FVertiMaxViewPosition   := 0;
  FVertiPositionPerChange := FVertiScrollbarRef.SmallChange;

  FViewRange.Top:=FViewRange.Top + FVertiCurViewPosition;
  FViewRange.Bottom:=FViewRange.Bottom + FVertiCurViewPosition;

  if FHoriScrollbarOn then
  begin
    FHoriCurViewPosition   := 0;
    FHoriMinViewPosition   := 0;
    FHoriMaxViewPosition   := 0;
    FHoriPositionPerChange := FHoriScrollbarRef.SmallChange;

    FViewRange.Left:=FViewRange.Left + FHoriCurViewPosition;
    FViewRange.Right:=FViewRange.Right + FHoriCurViewPosition;
  end;
end; 
```
