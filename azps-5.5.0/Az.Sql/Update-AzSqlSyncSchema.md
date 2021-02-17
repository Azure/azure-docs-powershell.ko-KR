---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/update-azsqlsyncschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlSyncSchema.md
ms.openlocfilehash: 571bef6b10420f08e7b1a00bdfddd4415ba0e033
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187937"
---
# <span data-ttu-id="40b0d-101">Update-AzSqlSyncSchema</span><span class="sxs-lookup"><span data-stu-id="40b0d-101">Update-AzSqlSyncSchema</span></span>

## <span data-ttu-id="40b0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40b0d-102">SYNOPSIS</span></span>
<span data-ttu-id="40b0d-103">동기화 멤버 데이터베이스 또는 동기화 허브 데이터베이스에 대한 동기화 SCHEMA를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-103">Update the sync schema for a sync member database or a sync hub database.</span></span>
<span data-ttu-id="40b0d-104">실제 데이터베이스에서 최신 데이터베이스를 다운로드한 다음 동기화 메타데이터 데이터베이스에서 캐시한 스마마를 새로 고쳐 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-104">It will get the latest database schema from the real database and then use it refresh the schema cached by Sync metadata database.</span></span>
<span data-ttu-id="40b0d-105">"SyncMemberName"이 지정되어 있는 경우 멤버 데이터베이스를 새로 고침합니다. 그렇지 않은 경우 허브 데이터베이스 스마마를 새로 고침합니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-105">If "SyncMemberName" is specified, it will refresh the member database schema; if not, it will refresh the hub database schema.</span></span>

## <span data-ttu-id="40b0d-106">구문</span><span class="sxs-lookup"><span data-stu-id="40b0d-106">SYNTAX</span></span>

```
Update-AzSqlSyncSchema [-SyncGroupName] <String> [-SyncMemberName <String>] [-PassThru] [-ServerName] <String>
 [-DatabaseName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40b0d-107">설명</span><span class="sxs-lookup"><span data-stu-id="40b0d-107">DESCRIPTION</span></span>
<span data-ttu-id="40b0d-108">**Update-AzSqlSyncSchema** cmdlet은 동기화 멤버 데이터베이스 또는 동기화 허브 데이터베이스에 대한 동기화 schema를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-108">The **Update-AzSqlSyncSchema** cmdlet updates the sync schema for a sync member database or a sync hub database.</span></span>

## <span data-ttu-id="40b0d-109">예제</span><span class="sxs-lookup"><span data-stu-id="40b0d-109">EXAMPLES</span></span>

### <span data-ttu-id="40b0d-110">예제 1: 허브 데이터베이스에 대한 동기화 SCHEMA 업데이트</span><span class="sxs-lookup"><span data-stu-id="40b0d-110">Example 1: Update the sync schema for a hub database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01"
```

<span data-ttu-id="40b0d-111">이 명령은 동기화 그룹 syncGroup01에서 허브 데이터베이스에 대한 동기화 SCHEMA를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-111">This command updates the sync schema for the hub database in the sync group syncGroup01</span></span>

### <span data-ttu-id="40b0d-112">예제 2: 구성원 데이터베이스에 대한 동기화 SCHEMA 업데이트</span><span class="sxs-lookup"><span data-stu-id="40b0d-112">Example 2: Update the sync schema for a member database</span></span>
```
PS C:\>Update-AzSqlSyncSchema -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -SyncGroupName "syncGroup01" -SyncMemberName "syncMember01"
```

<span data-ttu-id="40b0d-113">이 명령은 동기화 멤버 syncMember01에서 멤버 데이터베이스에 대한 동기화 SCHEMA를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-113">This command updates the sync schema for the member database in the sync member syncMember01</span></span>

## <span data-ttu-id="40b0d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40b0d-114">PARAMETERS</span></span>

### <span data-ttu-id="40b0d-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="40b0d-115">-DatabaseName</span></span>
<span data-ttu-id="40b0d-116">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-116">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="40b0d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b0d-117">-DefaultProfile</span></span>
<span data-ttu-id="40b0d-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="40b0d-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40b0d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="40b0d-119">-PassThru</span></span>
<span data-ttu-id="40b0d-120">이 cmdlet이 작동하는 동기화 그룹을 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-120">Defines Whether return the sync group this cmdlet works on</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b0d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b0d-121">-ResourceGroupName</span></span>
<span data-ttu-id="40b0d-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="40b0d-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="40b0d-123">-ServerName</span></span>
<span data-ttu-id="40b0d-124">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="40b0d-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="40b0d-125">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="40b0d-125">-SyncGroupName</span></span>
<span data-ttu-id="40b0d-126">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-126">The sync group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b0d-127">-SyncMemberName</span><span class="sxs-lookup"><span data-stu-id="40b0d-127">-SyncMemberName</span></span>
<span data-ttu-id="40b0d-128">동기화 멤버 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-128">The sync member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40b0d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40b0d-129">-Confirm</span></span>
<span data-ttu-id="40b0d-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40b0d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40b0d-131">-WhatIf</span></span>
<span data-ttu-id="40b0d-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="40b0d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40b0d-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40b0d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b0d-134">CommonParameters</span></span>
<span data-ttu-id="40b0d-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40b0d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b0d-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="40b0d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b0d-137">입력</span><span class="sxs-lookup"><span data-stu-id="40b0d-137">INPUTS</span></span>

### <span data-ttu-id="40b0d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="40b0d-138">System.String</span></span>

## <span data-ttu-id="40b0d-139">출력</span><span class="sxs-lookup"><span data-stu-id="40b0d-139">OUTPUTS</span></span>

### <span data-ttu-id="40b0d-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="40b0d-140">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="40b0d-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40b0d-141">NOTES</span></span>

## <span data-ttu-id="40b0d-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40b0d-142">RELATED LINKS</span></span>
