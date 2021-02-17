---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196044"
---
# <span data-ttu-id="6e2f5-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="6e2f5-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="6e2f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e2f5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e2f5-103">인스턴스 장애 조치(failover) 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="6e2f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="6e2f5-104">SYNTAX</span></span>

### <span data-ttu-id="6e2f5-105">RemoveIFGDefaultSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6e2f5-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e2f5-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="6e2f5-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e2f5-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="6e2f5-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e2f5-108">설명</span><span class="sxs-lookup"><span data-stu-id="6e2f5-108">DESCRIPTION</span></span>
<span data-ttu-id="6e2f5-109">이 명령은 지정된 이름의 인스턴스 장애 조치(failover) 그룹을 제거하고 모든 데이터베이스는 그대로 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="6e2f5-110">수신기 엔드포인트는 DNS에서 등록되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="6e2f5-111">인스턴스 장애 조치 그룹의 주 지역을 사용하여 명령을 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="6e2f5-112">예제</span><span class="sxs-lookup"><span data-stu-id="6e2f5-112">EXAMPLES</span></span>

### <span data-ttu-id="6e2f5-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="6e2f5-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="6e2f5-114">인스턴스 장애 조치(failover) 그룹을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="6e2f5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6e2f5-115">PARAMETERS</span></span>

### <span data-ttu-id="6e2f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e2f5-116">-DefaultProfile</span></span>
<span data-ttu-id="6e2f5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e2f5-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6e2f5-118">-Force</span></span>
<span data-ttu-id="6e2f5-119">작업을 수행하기 위한 확인 메시지를 건너뜁습니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="6e2f5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e2f5-120">-InputObject</span></span>
<span data-ttu-id="6e2f5-121">제거할 인스턴스 장애 조치 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="6e2f5-121">The Instance Failover Group object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2f5-122">-Location</span><span class="sxs-lookup"><span data-stu-id="6e2f5-122">-Location</span></span>
<span data-ttu-id="6e2f5-123">인스턴스 장애 조치(failover) 그룹을 검색할 로컬 지역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet, RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2f5-124">-Name</span><span class="sxs-lookup"><span data-stu-id="6e2f5-124">-Name</span></span>
<span data-ttu-id="6e2f5-125">제거할 인스턴스 장애 조치(failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-125">The name of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2f5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6e2f5-126">-PassThru</span></span>
<span data-ttu-id="6e2f5-127">cmdlet 실행 출력을 통과할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="6e2f5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e2f5-128">-ResourceGroupName</span></span>
<span data-ttu-id="6e2f5-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveIFGDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e2f5-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6e2f5-130">-ResourceId</span></span>
<span data-ttu-id="6e2f5-131">제거할 인스턴스 장애 조치 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-131">The Resource ID of the Instance Failover Group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveInstanceFailoverGroupByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e2f5-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e2f5-132">-Confirm</span></span>
<span data-ttu-id="6e2f5-133">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e2f5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e2f5-134">-WhatIf</span></span>
<span data-ttu-id="6e2f5-135">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6e2f5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e2f5-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e2f5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e2f5-137">CommonParameters</span></span>
<span data-ttu-id="6e2f5-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e2f5-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6e2f5-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e2f5-140">입력</span><span class="sxs-lookup"><span data-stu-id="6e2f5-140">INPUTS</span></span>

### <span data-ttu-id="6e2f5-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="6e2f5-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="6e2f5-142">System.String</span><span class="sxs-lookup"><span data-stu-id="6e2f5-142">System.String</span></span>

## <span data-ttu-id="6e2f5-143">출력</span><span class="sxs-lookup"><span data-stu-id="6e2f5-143">OUTPUTS</span></span>

### <span data-ttu-id="6e2f5-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="6e2f5-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="6e2f5-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6e2f5-145">NOTES</span></span>

## <span data-ttu-id="6e2f5-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e2f5-146">RELATED LINKS</span></span>
