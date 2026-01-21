With(
    { keywords: Split(Trim(txtEquipmentSearch_5.Text), " ") },
Sort(
    Filter(
        Filter(col_AllEquipment, Not('Equipment Name' in ShowColumns(AddColumns( col_JobEquipDetails, CustomEquipName, 'Equipment Name'.'Equipment Name'),CustomEquipName ))),
        CountIf(
            keywords,
            Lower(Trim(Value)) in Lower('Equipment Name')
        ) = CountRows(keywords)
    ),
    'Equipment Name')
)
