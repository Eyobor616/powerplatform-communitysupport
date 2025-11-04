ClearCollect(colInvApprovalDetails_Indexed,
    ForAll(Sequence(CountRows(colInvApprovalDetails),1),
        {

            Index: Value,
            Email: Last(FirstN(colInvApprovalDetails, Value)).Email,
            Position: Last(FirstN(colInvApprovalDetails, Value)).Position,
            Status: Last(FirstN(colInvApprovalDetails, Value)).Status,
            Date: Last(FirstN(colInvApprovalDetails, Value)).Date

        }
            
))
