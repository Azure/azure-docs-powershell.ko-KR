---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/update-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncGroup.md
ms.openlocfilehash: c95b6a7a42327b7380e19ff333453f956797dcdc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008352"
---
# <span data-ttu-id="fc100-101">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fc100-101">Update-AzSqlSyncGroup</span></span>

## <span data-ttu-id="fc100-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc100-102">SYNOPSIS</span></span>
<span data-ttu-id="fc100-103">Azure 데이터베이스 SQL 동기화 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-103">Updates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fc100-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc100-104">SYNTAX</span></span>

```
Update-AzSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-UsePrivateLinkConnection <Boolean>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc100-105">설명</span><span class="sxs-lookup"><span data-stu-id="fc100-105">DESCRIPTION</span></span>
<span data-ttu-id="fc100-106">**Update-AzSqlSyncGroup** cmdlet은 Azure 데이터베이스 동기화 그룹의 속성을 SQL 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-106">The **Update-AzSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fc100-107">예제</span><span class="sxs-lookup"><span data-stu-id="fc100-107">EXAMPLES</span></span>

### <span data-ttu-id="fc100-108">예제 1: Azure SQL 데이터베이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
-DatabaseCredential $credential -IntervalInSeconds 100 -Schema ".\schema.json" | Format-List
ResourceId                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroup01}/servers/{Server01}/databases/{Database01}/syncGroups/{SyncGroup01}
ResourceGroupName           : ResourceGroup01
ServerName                  : Server01
DatabaseName                : Database01
SyncGroupName               : SyncGroup01
SyncDatabaseId              : subscriptions/{subscriptionId}/resourceGroups/{syncDatabaseResourceGroup01}/servers/{syncDatabaseServer01}/databases/{syncDatabaseName01}
IntervalInSeconds           : 100
ConflictResolutionPolicy:   : HubWin
HubDatabaseUserName         : myAccount
HubDatabasePassword         : 
SyncState                   : NotReady
LastSyncTime                : 1/1/0001 12:00:00 AM
Schema                      :
```

<span data-ttu-id="fc100-109">이 명령은 Azure SQL 동기화 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="fc100-110">"schema.js"은 로컬 디스크의 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="fc100-111">json 형식의 schema 페이로드가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-111">It contains the schema payload in json format.</span></span> <span data-ttu-id="fc100-112">schema json의 예로 {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}]: "MayQuotedTable2"}], "MasterSyncMemberName": null }</span><span class="sxs-lookup"><span data-stu-id="fc100-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="fc100-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fc100-113">PARAMETERS</span></span>

### <span data-ttu-id="fc100-114">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="fc100-114">-DatabaseCredential</span></span>
<span data-ttu-id="fc100-115">허브 SQL 인증 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-115">The SQL authentication credential of the hub database.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc100-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc100-116">-DatabaseName</span></span>
<span data-ttu-id="fc100-117">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-117">SQL Database name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc100-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc100-118">-DefaultProfile</span></span>
<span data-ttu-id="fc100-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fc100-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc100-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="fc100-120">-IntervalInSeconds</span></span>
<span data-ttu-id="fc100-121">데이터 동기화를 수행하는 빈도(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="fc100-122">기본값은 -1입니다. 즉, 자동 동기화가 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc100-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fc100-123">-Name</span></span>
<span data-ttu-id="fc100-124">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-124">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SyncGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc100-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc100-125">-ResourceGroupName</span></span>
<span data-ttu-id="fc100-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-126">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc100-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="fc100-127">-SchemaFile</span></span>
<span data-ttu-id="fc100-128">schema 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-128">The path of the schema file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc100-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fc100-129">-ServerName</span></span>
<span data-ttu-id="fc100-130">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fc100-130">The name of the Azure SQL Server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc100-131">-UsePrivateLinkConnection</span><span class="sxs-lookup"><span data-stu-id="fc100-131">-UsePrivateLinkConnection</span></span>
<span data-ttu-id="fc100-132">이 동기화 그룹의 허브에 연결할 때 개인 링크 연결을 사용할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-132">Whether to use a private link connection when connecting to the hub of this sync group.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc100-133">-확인</span><span class="sxs-lookup"><span data-stu-id="fc100-133">-Confirm</span></span>
<span data-ttu-id="fc100-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc100-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc100-135">-WhatIf</span></span>
<span data-ttu-id="fc100-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc100-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc100-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc100-138">CommonParameters</span></span>
<span data-ttu-id="fc100-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc100-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc100-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc100-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc100-141">입력</span><span class="sxs-lookup"><span data-stu-id="fc100-141">INPUTS</span></span>

### <span data-ttu-id="fc100-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fc100-142">System.String</span></span>

## <span data-ttu-id="fc100-143">출력</span><span class="sxs-lookup"><span data-stu-id="fc100-143">OUTPUTS</span></span>

### <span data-ttu-id="fc100-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="fc100-144">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="fc100-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc100-145">NOTES</span></span>

## <span data-ttu-id="fc100-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc100-146">RELATED LINKS</span></span>

[<span data-ttu-id="fc100-147">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fc100-147">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="fc100-148">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fc100-148">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="fc100-149">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fc100-149">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

