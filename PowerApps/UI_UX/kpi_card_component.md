ComponentDefinitions:
  compDashboard_SummaryCards:
    DefinitionType: CanvasComponent
    AccessAppScope: true
    Properties:
      Height: =If(fxDeviceMode.DesktopMode, 240,800)
      Width: =App.Width
    Children:
      - Container8:
          Control: GroupContainer@1.5.0
          Variant: AutoLayout
          Properties:
            DropShadow: =DropShadow.None
            Height: '=Parent.Height  '
            LayoutAlignItems: =LayoutAlignItems.Stretch
            LayoutDirection: =LayoutDirection.Horizontal
            LayoutJustifyContent: =LayoutJustifyContent.SpaceBetween
            PaddingLeft: =-40
            Width: =Parent.Width
          Children:
            - Gallery2:
                Control: Gallery@2.15.0
                Variant: Horizontal
                Properties:
                  AlignInContainer: =AlignInContainer.SetByContainer
                  Items: |-
                    =Table(
                    {
                        Title: "Active Projects",
                        Icon: "Projects",
                        Totals:"12",
                        TrendValue: "+16.7%",
                        AdditonalInfo: "+2 from last month",
                        ColorText: "Blue"
                    },
                    {
                        Title: "Total Tasks",
                        Icon: "Tasks",
                        Totals:"248",
                        TrendValue: "+7.8%",
                        AdditonalInfo: "+18 this week",
                        ColorText: "Green"
                    },
                    {
                        Title: "Team Members",
                        Icon: "Teams",
                        Totals:"12",
                        TrendValue: "+10.3%",
                        AdditonalInfo: "+3 new hires",
                        ColorText: "Purple"
                    },
                    {
                        Title: "Completion Rate",
                        Icon: "Trend",
                        Totals:"12",
                        TrendValue: "+6.1%",
                        AdditonalInfo: "+5% improvement",
                        ColorText: "Red"
                    }
                    )
                  LayoutMaxHeight: =
                  LayoutMaxWidth: =
                  LayoutMinHeight: =0
                  LayoutMinWidth: =0
                  ShowScrollbar: =false
                  TemplatePadding: =0
                  TemplateSize: = If(fxDeviceMode.DesktopMode, (Gallery2.Width/Gallery2.AllItemsCount), Parent.Width)
                  Transition: =Transition.Pop
                  WrapCount: =If(fxDeviceMode.DesktopMode, 1,4)
                Children:
                  - Container33:
                      Control: GroupContainer@1.5.0
                      Variant: AutoLayout
                      Properties:
                        DropShadow: =DropShadow.None
                        Fill: =RGBA(166, 215, 153, 0)
                        Height: =Parent.TemplateHeight
                        LayoutAlignItems: =LayoutAlignItems.Stretch
                        LayoutDirection: =LayoutDirection.Vertical
                        LayoutJustifyContent: =LayoutJustifyContent.SpaceBetween
                        PaddingBottom: =Self.PaddingTop
                        PaddingLeft: =Self.PaddingTop
                        PaddingRight: =Self.PaddingTop
                        PaddingTop: =fxContainerDefaultPadding
                        Width: =Parent.TemplateWidth
                      Children:
                        - Container11:
                            Control: GroupContainer@1.5.0
                            Variant: AutoLayout
                            Properties:
                              AlignInContainer: =AlignInContainer.SetByContainer
                              DropShadow: =fxContainerDropShadow
                              Fill: =RGBA(255, 255, 255, 1)
                              Height: =100
                              LayoutAlignItems: =LayoutAlignItems.Stretch
                              LayoutDirection: =LayoutDirection.Vertical
                              LayoutGap: =fxDeviceMode.LayoutGap*2
                              LayoutJustifyContent: =LayoutJustifyContent.SpaceBetween
                              LayoutMaxHeight: =
                              LayoutMaxWidth: =
                              LayoutMinHeight: =0
                              LayoutMinWidth: =0
                              PaddingBottom: =Self.PaddingTop
                              PaddingLeft: =fxContainerDefaultPadding
                              PaddingRight: =fxDeviceMode.LayoutGap
                              PaddingTop: =fxDeviceMode.OuterContainerPadding
                              RadiusBottomLeft: =fxDeviceMode.CardRadius
                              RadiusBottomRight: =Self.RadiusBottomLeft
                              RadiusTopLeft: =Self.RadiusBottomLeft
                              RadiusTopRight: =Self.RadiusBottomLeft
                              Width: =100
                              X: =40
                              Y: =40
                            Children:
                              - Container12:
                                  Control: GroupContainer@1.5.0
                                  Variant: AutoLayout
                                  Properties:
                                    AlignInContainer: =AlignInContainer.SetByContainer
                                    DropShadow: =DropShadow.None
                                    FillPortions: =0
                                    Height: =40
                                    LayoutAlignItems: =LayoutAlignItems.Stretch
                                    LayoutDirection: =LayoutDirection.Horizontal
                                    LayoutJustifyContent: =LayoutJustifyContent.SpaceBetween
                                    LayoutMaxHeight: =
                                    LayoutMaxWidth: =
                                    LayoutMinHeight: =0
                                    LayoutMinWidth: =0
                                    PaddingLeft: =0//fxDeviceMode.LayoutGap
                                    PaddingRight: =5
                                  Children:
                                    - Container11_131:
                                        Control: GroupContainer@1.5.0
                                        Variant: AutoLayout
                                        Properties:
                                          AlignInContainer: =AlignInContainer.SetByContainer
                                          BorderStyle: =BorderStyle.Dashed
                                          DropShadow: =DropShadow.None
                                          Fill: =fxColorFade(ColorValue(fxStatusColor(ThisItem.ColorText)))
                                          FillPortions: =0
                                          Height: =55
                                          LayoutAlignItems: =LayoutAlignItems.Stretch
                                          LayoutDirection: =LayoutDirection.Vertical
                                          LayoutJustifyContent: =LayoutJustifyContent.SpaceBetween
                                          LayoutMinHeight: =0
                                          LayoutMinWidth: =0
                                          Width: =55
                                        Children:
                                          - Image2_51:
                                              Control: Image@2.2.3
                                              Properties:
                                                Fill: =//fxColorFade(ColorValue(fxStatusColor(ThisItem.ColorText)))
                                                FillPortions: =1
                                                Height: =Self.Width
                                                Image: =fxGetColoredSVG(ThisItem.Icon, fxStatusColor(ThisItem.ColorText))
                                                LayoutMinHeight: =0
                                                LayoutMinWidth: =0
                                                PaddingBottom: =Self.PaddingTop
                                                PaddingLeft: =Self.PaddingTop
                                                PaddingRight: =Self.PaddingTop
                                                PaddingTop: =8
                                                RadiusBottomLeft: =8
                                                RadiusBottomRight: =8
                                                RadiusTopLeft: =8
                                                RadiusTopRight: =8
                                                Width: =50
                                    - Container11_132:
                                        Control: GroupContainer@1.5.0
                                        Variant: AutoLayout
                                        Properties:
                                          AlignInContainer: =AlignInContainer.Center
                                          BorderStyle: =BorderStyle.Dashed
                                          DropShadow: =DropShadow.None
                                          Fill: =fxColorFade(ColorValue(fxStatusColor("Green")))
                                          FillPortions: =0
                                          Height: =20
                                          LayoutAlignItems: =LayoutAlignItems.Stretch
                                          LayoutDirection: =LayoutDirection.Horizontal
                                          LayoutMaxHeight: =Self.Height
                                          LayoutMaxWidth: =Self.Width
                                          LayoutMinHeight: =0
                                          LayoutMinWidth: =0
                                          PaddingLeft: =5
                                          PaddingRight: =5
                                          RadiusBottomLeft: =fxDeviceMode.btnRadius
                                          RadiusBottomRight: =Self.RadiusBottomLeft
                                          RadiusTopLeft: =Self.RadiusBottomLeft
                                          RadiusTopRight: =Self.RadiusBottomLeft
                                          Width: =80
                                        Children:
                                          - Image2_52:
                                              Control: Image@2.2.3
                                              Properties:
                                                Fill: =
                                                Height: =Self.Width
                                                Image: =fxGetColoredSVG("Arrow_TopLeft", fxStatusColor("Green"))
                                                LayoutMaxHeight: =
                                                LayoutMinHeight: =0
                                                LayoutMinWidth: =0
                                                PaddingBottom: =Self.PaddingTop
                                                PaddingLeft: =Self.PaddingTop
                                                PaddingRight: =Self.PaddingTop
                                                PaddingTop: =3
                                                RadiusBottomLeft: =8
                                                RadiusBottomRight: =8
                                                RadiusTopLeft: =8
                                                RadiusTopRight: =8
                                                Width: =15
                                          - lblHeading_14:
                                              Control: Text@0.0.51
                                              Properties:
                                                Align: ='TextCanvas.Align'.End
                                                AutoHeight: =true
                                                FillPortions: =1
                                                FontColor: =ColorValue(fxStatusColor("Green"))
                                                Height: =10
                                                LayoutMaxHeight: =Self.Height
                                                LayoutMaxWidth: =
                                                LayoutMinHeight: =0
                                                LayoutMinWidth: =0
                                                PaddingBottom: =0
                                                PaddingLeft: =0
                                                PaddingRight: =0
                                                PaddingTop: =0
                                                Size: =lblHeading_15.Size //fxDeviceMode.BodyTextSize_xsm
                                                Text: =ThisItem.TrendValue
                                                VerticalAlign: =VerticalAlign.Middle
                                                Weight: ='TextCanvas.Weight'.Regular
                                                Width: =Parent.Width
                                                Wrap: =false
                                                X: =20
                                                Y: =20
                              - Container12_1:
                                  Control: GroupContainer@1.5.0
                                  Variant: AutoLayout
                                  Properties:
                                    AlignInContainer: =AlignInContainer.SetByContainer
                                    DropShadow: =DropShadow.None
                                    FillPortions: =0
                                    Height: =80
                                    LayoutAlignItems: =LayoutAlignItems.Stretch
                                    LayoutDirection: =LayoutDirection.Vertical
                                    LayoutJustifyContent: =LayoutJustifyContent.SpaceBetween
                                    LayoutMaxHeight: =
                                    LayoutMaxWidth: =
                                    LayoutMinHeight: =0
                                    LayoutMinWidth: =0
                                  Children:
                                    - lblHeading_15:
                                        Control: Text@0.0.51
                                        Properties:
                                          Align: ='TextCanvas.Align'.Start
                                          AutoHeight: =true
                                          FontColor: =fxColors.LightGrey
                                          Height: =10
                                          LayoutMaxHeight: =Self.Height
                                          LayoutMaxWidth: =
                                          LayoutMinHeight: =0
                                          LayoutMinWidth: =0
                                          PaddingBottom: =0
                                          PaddingLeft: =0
                                          PaddingRight: =0
                                          PaddingTop: =0
                                          Size: =lblHeading_16.Size
                                          Text: =ThisItem.Title
                                          VerticalAlign: =VerticalAlign.Middle
                                          Weight: ='TextCanvas.Weight'.Bold
                                          Width: =Parent.Width
                                          Wrap: =false
                                          X: =20
                                          Y: =20
                                    - lblHeading_17:
                                        Control: Text@0.0.51
                                        Properties:
                                          Align: ='TextCanvas.Align'.Start
                                          AutoHeight: =true
                                          FontColor: =Color.Black
                                          Height: =10
                                          LayoutMaxHeight: =Self.Height
                                          LayoutMaxWidth: =
                                          LayoutMinHeight: =0
                                          LayoutMinWidth: =0
                                          PaddingBottom: =0
                                          PaddingLeft: =0
                                          PaddingRight: =0
                                          PaddingTop: =0
                                          Size: =fxDeviceMode.BodyTextSize_lg_2
                                          Text: =ThisItem.Totals
                                          VerticalAlign: =VerticalAlign.Middle
                                          Weight: ='TextCanvas.Weight'.Bold
                                          Width: =Parent.Width
                                          Wrap: =false
                                          X: =20
                                          Y: =20
                                    - lblHeading_16:
                                        Control: Text@0.0.51
                                        Properties:
                                          Align: ='TextCanvas.Align'.Start
                                          AutoHeight: =true
                                          FontColor: =fxColors.LightGrey
                                          Height: =10
                                          LayoutMaxHeight: =Self.Height
                                          LayoutMaxWidth: =
                                          LayoutMinHeight: =0
                                          LayoutMinWidth: =0
                                          PaddingBottom: =0
                                          PaddingLeft: =0
                                          PaddingRight: =0
                                          PaddingTop: =0
                                          Size: =fxDeviceMode.BodyTextSize_xsm
                                          Text: =ThisItem.AdditonalInfo
                                          VerticalAlign: =VerticalAlign.Middle
                                          Weight: ='TextCanvas.Weight'.Regular
                                          Width: =Parent.Width
                                          Wrap: =false
                                          X: =20
                                          Y: =20
