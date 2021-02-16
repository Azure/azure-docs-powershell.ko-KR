---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: 3a5da7972e70e3ebf9c86df62b2bbc79651e72a5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196012"
---
# <span data-ttu-id="0a320-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0a320-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="0a320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a320-102">SYNOPSIS</span></span>
<span data-ttu-id="0a320-103">Azure SQL 동기화 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a320-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="0a320-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a320-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a320-105">설명</span><span class="sxs-lookup"><span data-stu-id="0a320-105">DESCRIPTION</span></span>
<span data-ttu-id="0a320-106">**Remove-AzSqlSyncGroup** cmdlet은 Azure SQL 데이터베이스 동기화 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a320-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="0a320-107">예제</span><span class="sxs-lookup"><span data-stu-id="0a320-107">EXAMPLES</span></span>

### <span data-ttu-id="0a320-108">예제 1: 동기화 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="0a320-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="0a320-109">이 명령은 syncGroup01이라는 Azure SQL 데이터베이스 동기화 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a320-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="0a320-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a320-110">PARAMETERS</span></span>

### <span data-ttu-id="0a320-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0a320-111">-DatabaseName</span></span>
<span data-ttu-id="0a320-112">Azure SQL 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a320-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="0a320-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a320-113">-DefaultProfile</span></span>
<span data-ttu-id="0a320-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0a320-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a320-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0a320-115">-Force</span></span>
<span data-ttu-id="0a320-116">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="0a320-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="0a320-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0a320-117">-Name</span></span>
<span data-ttu-id="0a320-118">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a320-118">The sync group name.</span></span>

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

### <span data-ttu-id="0a320-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a320-119">-PassThru</span></span>
<span data-ttu-id="0a320-120">제거된 동기화 그룹을 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="0a320-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="0a320-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a320-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a320-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a320-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="0a320-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0a320-123">-ServerName</span></span>
<span data-ttu-id="0a320-124">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0a320-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="0a320-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a320-125">-Confirm</span></span>
<span data-ttu-id="0a320-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a320-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a320-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a320-127">-WhatIf</span></span>
<span data-ttu-id="0a320-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0a320-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a320-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a320-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a320-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a320-130">CommonParameters</span></span>
<span data-ttu-id="0a320-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a320-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a320-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0a320-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a320-133">입력</span><span class="sxs-lookup"><span data-stu-id="0a320-133">INPUTS</span></span>

### <span data-ttu-id="0a320-134">System.String</span><span class="sxs-lookup"><span data-stu-id="0a320-134">System.String</span></span>

## <span data-ttu-id="0a320-135">출력</span><span class="sxs-lookup"><span data-stu-id="0a320-135">OUTPUTS</span></span>

### <span data-ttu-id="0a320-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="0a320-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="0a320-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a320-137">NOTES</span></span>

## <span data-ttu-id="0a320-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a320-138">RELATED LINKS</span></span>

[<span data-ttu-id="0a320-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0a320-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="0a320-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0a320-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="0a320-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0a320-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

