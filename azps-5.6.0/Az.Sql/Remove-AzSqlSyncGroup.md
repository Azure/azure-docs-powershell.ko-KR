---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqlsyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlSyncGroup.md
ms.openlocfilehash: ce69f6b087a7ed61f415e3d6a649f757bb10178f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995092"
---
# <span data-ttu-id="fc656-101">Remove-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fc656-101">Remove-AzSqlSyncGroup</span></span>

## <span data-ttu-id="fc656-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc656-102">SYNOPSIS</span></span>
<span data-ttu-id="fc656-103">Azure 데이터베이스 동기화 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fc656-103">Removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fc656-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc656-104">SYNTAX</span></span>

```
Remove-AzSqlSyncGroup [-Name] <String> [-Force] [-PassThru] [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc656-105">설명</span><span class="sxs-lookup"><span data-stu-id="fc656-105">DESCRIPTION</span></span>
<span data-ttu-id="fc656-106">**Remove-AzSqlSyncGroup** cmdlet은 Azure 데이터베이스 동기화 SQL 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fc656-106">The **Remove-AzSqlSyncGroup** cmdlet removes an Azure SQL Database Sync Group.</span></span>

## <span data-ttu-id="fc656-107">예제</span><span class="sxs-lookup"><span data-stu-id="fc656-107">EXAMPLES</span></span>

### <span data-ttu-id="fc656-108">예제 1: 동기화 그룹 제거</span><span class="sxs-lookup"><span data-stu-id="fc656-108">Example 1: Remove a sync group</span></span>
```
PS C:\>Remove-AzSqlSyncGroup -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "database01" -Name "syncGroup01"
```

<span data-ttu-id="fc656-109">이 명령은 syncGroup01이라는 azure SQL 데이터베이스 동기화 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fc656-109">This command removes the Azure SQL Database Sync Group named syncGroup01.</span></span>

## <span data-ttu-id="fc656-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fc656-110">PARAMETERS</span></span>

### <span data-ttu-id="fc656-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fc656-111">-DatabaseName</span></span>
<span data-ttu-id="fc656-112">Azure 데이터베이스의 SQL 데이터베이스입니다.</span><span class="sxs-lookup"><span data-stu-id="fc656-112">The name of the Azure SQL Database.</span></span>

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

### <span data-ttu-id="fc656-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc656-113">-DefaultProfile</span></span>
<span data-ttu-id="fc656-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fc656-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc656-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fc656-115">-Force</span></span>
<span data-ttu-id="fc656-116">작업을 수행하기 위한 확인 메시지 건너뛰기</span><span class="sxs-lookup"><span data-stu-id="fc656-116">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="fc656-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fc656-117">-Name</span></span>
<span data-ttu-id="fc656-118">동기화 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc656-118">The sync group name.</span></span>

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

### <span data-ttu-id="fc656-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc656-119">-PassThru</span></span>
<span data-ttu-id="fc656-120">제거된 동기화 그룹을 반환할지 여부를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="fc656-120">Defines Whether return the removed sync group</span></span>

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

### <span data-ttu-id="fc656-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc656-121">-ResourceGroupName</span></span>
<span data-ttu-id="fc656-122">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc656-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="fc656-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fc656-123">-ServerName</span></span>
<span data-ttu-id="fc656-124">The name of the Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fc656-124">The name of the Azure SQL Server.</span></span>

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

### <span data-ttu-id="fc656-125">-확인</span><span class="sxs-lookup"><span data-stu-id="fc656-125">-Confirm</span></span>
<span data-ttu-id="fc656-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc656-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc656-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc656-127">-WhatIf</span></span>
<span data-ttu-id="fc656-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fc656-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc656-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc656-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc656-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc656-130">CommonParameters</span></span>
<span data-ttu-id="fc656-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc656-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc656-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fc656-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc656-133">입력</span><span class="sxs-lookup"><span data-stu-id="fc656-133">INPUTS</span></span>

### <span data-ttu-id="fc656-134">System.String</span><span class="sxs-lookup"><span data-stu-id="fc656-134">System.String</span></span>

## <span data-ttu-id="fc656-135">출력</span><span class="sxs-lookup"><span data-stu-id="fc656-135">OUTPUTS</span></span>

### <span data-ttu-id="fc656-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span><span class="sxs-lookup"><span data-stu-id="fc656-136">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncGroupModel</span></span>

## <span data-ttu-id="fc656-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc656-137">NOTES</span></span>

## <span data-ttu-id="fc656-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc656-138">RELATED LINKS</span></span>

[<span data-ttu-id="fc656-139">New-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fc656-139">New-AzSqlSyncGroup</span></span>](./New-AzSqlSyncGroup.md)

[<span data-ttu-id="fc656-140">Update-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fc656-140">Update-AzSqlSyncGroup</span></span>](./Update-AzSqlSyncGroup.md)

[<span data-ttu-id="fc656-141">Get-AzSqlSyncGroup</span><span class="sxs-lookup"><span data-stu-id="fc656-141">Get-AzSqlSyncGroup</span></span>](./Get-AzSqlSyncGroup.md)

