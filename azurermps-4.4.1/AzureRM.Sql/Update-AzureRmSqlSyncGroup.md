---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Update-AzureRmSqlSyncGroup.md
ms.openlocfilehash: a530a9e99c698ca6b827df94b1966e4df065790d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532207"
---
# <span data-ttu-id="f3096-101">Update-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f3096-101">Update-AzureRmSqlSyncGroup</span></span>

## <span data-ttu-id="f3096-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3096-102">SYNOPSIS</span></span>
<span data-ttu-id="f3096-103">Azure SQL 데이터베이스 동기화 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-103">Updates an Azure SQL Database Sync Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3096-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3096-104">SYNTAX</span></span>

```
Update-AzureRmSqlSyncGroup [-Name] <String> [-IntervalInSeconds <Int32>] [-DatabaseCredential <PSCredential>]
 [-SchemaFile <String>] [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3096-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f3096-105">DESCRIPTION</span></span>
<span data-ttu-id="f3096-106">**업데이트 AzureRmSqlSyncGroup** Cmdlet은 Azure SQL 데이터베이스 동기화 그룹의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-106">The **Update-AzureRmSqlSyncGroup** cmdlet modifies properties of an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="f3096-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f3096-107">EXAMPLES</span></span>

### <span data-ttu-id="f3096-108">예제 1: Azure SQL 데이터베이스에 대 한 동기화 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-108">Example 1: Update a sync group for an Azure SQL Database.</span></span>
```
PS C:\> $credential = Get-Credential
PS C:\> Update-AzureRmSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -Name "SyncGroup01"
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

<span data-ttu-id="f3096-109">이 명령은 Azure SQL Database에 대 한 동기화 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-109">This command updates a sync group for an Azure SQL Database.</span></span> <span data-ttu-id="f3096-110">"schema.js켜기"는 로컬 디스크의 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-110">"schema.json" is a file in the local disk.</span></span> <span data-ttu-id="f3096-111">Json 형식의 shema 페이로드를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-111">It contains the shema payload in json format.</span></span> <span data-ttu-id="f3096-112">스키마 json의 예로는 {"Tables": [{"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "이 있습니다. b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable1"}, {"Columns": [{"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName": "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName": "MayQuotedTable2": null}</span><span class="sxs-lookup"><span data-stu-id="f3096-112">An example of the schema json is: {"Tables":  [{"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable1"}, {"Columns":  [{"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column1"}, {"QuotedName":  "b3ee3a7f-7614-4644-ad07-afa832620b4bManualTestsm4column2"}], "QuotedName":  "MayQuotedTable2"}], "MasterSyncMemberName":  null }</span></span>

## <span data-ttu-id="f3096-113">변수</span><span class="sxs-lookup"><span data-stu-id="f3096-113">PARAMETERS</span></span>

### <span data-ttu-id="f3096-114">-확인</span><span class="sxs-lookup"><span data-stu-id="f3096-114">-Confirm</span></span>
<span data-ttu-id="f3096-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3096-116">-DatabaseCredential</span><span class="sxs-lookup"><span data-stu-id="f3096-116">-DatabaseCredential</span></span>
<span data-ttu-id="f3096-117">허브 데이터베이스의 SQL 인증 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-117">The SQL authentication credential of the hub database.</span></span>

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

### <span data-ttu-id="f3096-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="f3096-118">-DatabaseName</span></span>
<span data-ttu-id="f3096-119">SQL 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-119">SQL Database name.</span></span>

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

### <span data-ttu-id="f3096-120">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="f3096-120">-IntervalInSeconds</span></span>
<span data-ttu-id="f3096-121">데이터 동기화의 빈도 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-121">The frequency (in seconds) of doing data synchronization.</span></span>
<span data-ttu-id="f3096-122">기본값은-1 이며,이는 자동 동기화가 활성화 되지 않았음을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-122">Default is -1, which means the auto synchronization is not enabled.</span></span>

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

### <span data-ttu-id="f3096-123">-이름</span><span class="sxs-lookup"><span data-stu-id="f3096-123">-Name</span></span>
<span data-ttu-id="f3096-124">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-124">The sync group name.</span></span>

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

### <span data-ttu-id="f3096-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3096-125">-ResourceGroupName</span></span>
<span data-ttu-id="f3096-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-126">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3096-127">-SchemaFile</span><span class="sxs-lookup"><span data-stu-id="f3096-127">-SchemaFile</span></span>
<span data-ttu-id="f3096-128">스키마 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-128">The path of the schema file.</span></span>

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

### <span data-ttu-id="f3096-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="f3096-129">-ServerName</span></span>
<span data-ttu-id="f3096-130">Azure SQL Server의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-130">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="f3096-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3096-131">-WhatIf</span></span>
<span data-ttu-id="f3096-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3096-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3096-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3096-134">-DefaultProfile</span></span>
<span data-ttu-id="f3096-135">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3096-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3096-136">CommonParameters</span></span>
<span data-ttu-id="f3096-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3096-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3096-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3096-139">입력</span><span class="sxs-lookup"><span data-stu-id="f3096-139">INPUTS</span></span>

## <span data-ttu-id="f3096-140">출력</span><span class="sxs-lookup"><span data-stu-id="f3096-140">OUTPUTS</span></span>

### <span data-ttu-id="f3096-141">AzureSqlSyncGroupModel (\*)를 호출 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3096-141">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="f3096-142">상속자</span><span class="sxs-lookup"><span data-stu-id="f3096-142">NOTES</span></span>

## <span data-ttu-id="f3096-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3096-143">RELATED LINKS</span></span>

[<span data-ttu-id="f3096-144">새로운 AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f3096-144">New-AzureRmSqlSyncGroup</span></span>](./New-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="f3096-145">제거-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f3096-145">Remove-AzureRmSqlSyncGroup</span></span>](./Remove-AzureRmSqlSyncGroup.md)

[<span data-ttu-id="f3096-146">Get-AzureRmSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="f3096-146">Get-AzureRmSqlSyncGroup</span></span>](./Get-AzureRmSqlSyncGroup.md)

