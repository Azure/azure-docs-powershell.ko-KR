---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlSyncGroup.md
ms.openlocfilehash: 512ed43ac1770a7a1a026c5a64d20a25016d547e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698871"
---
# <span data-ttu-id="96751-101">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96751-101">New-AzSqlSyncGroup</span></span>

## <span data-ttu-id="96751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96751-102">SYNOPSIS</span></span>
<span data-ttu-id="96751-103">Azure SQL Database 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96751-103">Creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="96751-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96751-104">SYNTAX</span></span>

```
New-AzSqlSyncGroup [-Name] <String> -SyncDatabaseName <String> -SyncDatabaseServerName <String>
 -SyncDatabaseResourceGroupName <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-ConflictResolutionPolicy <String>] [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96751-105">설명은</span><span class="sxs-lookup"><span data-stu-id="96751-105">DESCRIPTION</span></span>
<span data-ttu-id="96751-106">**AzSqlSyncGroup** Cmdlet은 Azure SQL 데이터베이스 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96751-106">The **New-AzSqlSyncGroup** cmdlet creates an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="96751-107">예제의</span><span class="sxs-lookup"><span data-stu-id="96751-107">EXAMPLES</span></span>

### <span data-ttu-id="96751-108">예제 1: Azure SQL 데이터베이스에 대 한 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96751-108">Example 1: Create a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> New-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01" -ConflictResolutionPolicy "HubWin"
-DatabaseCredential $credential -IntervalInSeconds 100 -SyncDatabaseServerName "syncDatabaseServer01" -SyncDatabaseName "syncDatabaseName01"
-SyncDatabaseResourceGroupName "syncDatabaseResourceGroup01" -Schema ".\schema.json" | Format-List
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

<span data-ttu-id="96751-109">이 명령은 Azure SQL 데이터베이스에 대 한 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96751-109">This command creates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="96751-110">"schema.js켜기"는 로컬 디스크의 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="96751-111">Json 형식의 shema 페이로드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="96751-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="96751-112">스키마 json의 예로는 {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "이 있습니다. b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2": null}</span><span class="sxs-lookup"><span data-stu-id="96751-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="96751-113">변수</span><span class="sxs-lookup"><span data-stu-id="96751-113">PARAMETERS</span></span>

### <span data-ttu-id="96751-114">-ConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="96751-114">-ConflictResolutionPolicy</span></span>
<span data-ttu-id="96751-115">동기화 그룹의 허브와 구성원 데이터베이스 간의 confliction를 확인 하는 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-115">The policy of resolving confliction between hub and member database in the sync group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: HubWin, MemberWin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96751-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="96751-116">-DatabaseCredential</span></span>
<span data-ttu-id="96751-117">허브 데이터베이스의 SQL 인증 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="96751-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="96751-118">-DatabaseName</span></span>
<span data-ttu-id="96751-119">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-119">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="96751-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96751-120">-DefaultProfile</span></span>
<span data-ttu-id="96751-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="96751-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96751-122">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="96751-122">-IntervalInSeconds</span></span>
<span data-ttu-id="96751-123">데이터 동기화의 빈도 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-123">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="96751-124">기본값은-1 이며,이는 자동 동기화가 활성화 되지 않았음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="96751-124">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="96751-125">-이름</span><span class="sxs-lookup"><span data-stu-id="96751-125">-Name</span></span>
<span data-ttu-id="96751-126">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-126">The sync group name.</span></span>

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

### <span data-ttu-id="96751-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96751-127">-ResourceGroupName</span></span>
<span data-ttu-id="96751-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="96751-129">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="96751-129">-SchemaFile</span></span>
<span data-ttu-id="96751-130">스키마 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-130">The path of the schema file.</span></span>

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

### <span data-ttu-id="96751-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="96751-131">-ServerName</span></span>
<span data-ttu-id="96751-132">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-132">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="96751-133">-SyncDatabaseName</span><span class="sxs-lookup"><span data-stu-id="96751-133">-SyncDatabaseName</span></span>
<span data-ttu-id="96751-134">동기화 관련 메타 데이터를 저장 하는 데 사용 되는 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-134">The database used to store sync related metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96751-135">-SyncDatabaseResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96751-135">-SyncDatabaseResourceGroupName</span></span>
<span data-ttu-id="96751-136">동기화 메타 데이터 데이터베이스가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-136">The resource group the sync metadata database belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96751-137">-SyncDatabaseServerName</span><span class="sxs-lookup"><span data-stu-id="96751-137">-SyncDatabaseServerName</span></span>
<span data-ttu-id="96751-138">동기화 메타 데이터 데이터베이스가 호스팅되는 서버입니다.</span><span class="sxs-lookup"><span data-stu-id="96751-138">The server on which the sync metadata database is hosted.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96751-139">-확인</span><span class="sxs-lookup"><span data-stu-id="96751-139">-Confirm</span></span>
<span data-ttu-id="96751-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="96751-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96751-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96751-141">-WhatIf</span></span>
<span data-ttu-id="96751-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="96751-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96751-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96751-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96751-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96751-144">CommonParameters</span></span>
<span data-ttu-id="96751-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96751-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96751-146">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="96751-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96751-147">입력</span><span class="sxs-lookup"><span data-stu-id="96751-147">INPUTS</span></span>

### <span data-ttu-id="96751-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="96751-148">System.String</span></span>

## <span data-ttu-id="96751-149">출력</span><span class="sxs-lookup"><span data-stu-id="96751-149">OUTPUTS</span></span>

### <span data-ttu-id="96751-150">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="96751-150">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="96751-151">상속자</span><span class="sxs-lookup"><span data-stu-id="96751-151">NOTES</span></span>

## <span data-ttu-id="96751-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96751-152">RELATED LINKS</span></span>

[<span data-ttu-id="96751-153">Set-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96751-153">Set-AzSqlSyncGroup</span></span>](./Set-AzSqlSyncGroup.md)

[<span data-ttu-id="96751-154">제거-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96751-154">Remove-AzSqlSyncGroup</span></span>](./Remove-AzSqlSyncGroup.md)

[<span data-ttu-id="96751-155">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="96751-155">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

