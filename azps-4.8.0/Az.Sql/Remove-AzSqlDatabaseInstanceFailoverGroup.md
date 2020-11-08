---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 12bc26177a249995f748a879a9ae8d2f73900c99
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204795"
---
# <span data-ttu-id="84551-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="84551-101">Remove-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="84551-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84551-102">SYNOPSIS</span></span>
<span data-ttu-id="84551-103">인스턴스 장애 조치 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="84551-103">Removes an Instance Failover Group.</span></span>

## <span data-ttu-id="84551-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84551-104">SYNTAX</span></span>

### <span data-ttu-id="84551-105">RemoveIFGDefaultSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="84551-105">RemoveIFGDefaultSet (Default)</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84551-106">RemoveInstanceFailoverGroupByResourceId</span><span class="sxs-lookup"><span data-stu-id="84551-106">RemoveInstanceFailoverGroupByResourceId</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84551-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="84551-107">RemoveInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Remove-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84551-108">설명은</span><span class="sxs-lookup"><span data-stu-id="84551-108">DESCRIPTION</span></span>
<span data-ttu-id="84551-109">이 명령은 지정 된 이름의 인스턴스 장애 조치 (Failover) 그룹을 제거 하 고 모든 데이터베이스는 그대로 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="84551-109">This command removes the Instance Failover Group with the specified name, leaving all databases intact.</span></span> <span data-ttu-id="84551-110">수신기 끝점은 DNS에서 등록 취소 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84551-110">The listener endpoint will be unregistered from DNS.</span></span>

<span data-ttu-id="84551-111">명령을 실행 하려면 인스턴스 장애 조치 그룹의 기본 영역을 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="84551-111">The Instance Failover Group's primary region should be used to execute the command.</span></span>

## <span data-ttu-id="84551-112">예제의</span><span class="sxs-lookup"><span data-stu-id="84551-112">EXAMPLES</span></span>

### <span data-ttu-id="84551-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="84551-113">Example 1</span></span>
```
PS C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Remove-AzSqlDatabaseInstanceFailoverGroup
```

<span data-ttu-id="84551-114">인스턴스 장애 조치 (Failover) 그룹을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="84551-114">Remove a Instance Failover Group.</span></span>

## <span data-ttu-id="84551-115">변수</span><span class="sxs-lookup"><span data-stu-id="84551-115">PARAMETERS</span></span>

### <span data-ttu-id="84551-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84551-116">-DefaultProfile</span></span>
<span data-ttu-id="84551-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84551-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84551-118">-Force</span><span class="sxs-lookup"><span data-stu-id="84551-118">-Force</span></span>
<span data-ttu-id="84551-119">작업 수행에 대 한 건너뛰기 확인 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="84551-119">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="84551-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84551-120">-InputObject</span></span>
<span data-ttu-id="84551-121">제거할 인스턴스 장애 조치 (Failover) 그룹 개체</span><span class="sxs-lookup"><span data-stu-id="84551-121">The Instance Failover Group object to remove</span></span>

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

### <span data-ttu-id="84551-122">-위치</span><span class="sxs-lookup"><span data-stu-id="84551-122">-Location</span></span>
<span data-ttu-id="84551-123">인스턴스 장애 조치 (Failover) 그룹을 검색할 로컬 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84551-123">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="84551-124">-이름</span><span class="sxs-lookup"><span data-stu-id="84551-124">-Name</span></span>
<span data-ttu-id="84551-125">제거할 인스턴스 장애 조치 (Failover) 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84551-125">The name of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="84551-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84551-126">-PassThru</span></span>
<span data-ttu-id="84551-127">Cmdlet 실행 출력을 전달할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84551-127">Specifies whether to pass through cmdlet execution output.</span></span>

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

### <span data-ttu-id="84551-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84551-128">-ResourceGroupName</span></span>
<span data-ttu-id="84551-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84551-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="84551-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84551-130">-ResourceId</span></span>
<span data-ttu-id="84551-131">제거할 인스턴스 장애 조치 (Failover) 그룹의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="84551-131">The Resource ID of the Instance Failover Group to remove.</span></span>

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

### <span data-ttu-id="84551-132">-확인</span><span class="sxs-lookup"><span data-stu-id="84551-132">-Confirm</span></span>
<span data-ttu-id="84551-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="84551-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84551-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84551-134">-WhatIf</span></span>
<span data-ttu-id="84551-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="84551-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84551-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84551-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84551-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84551-137">CommonParameters</span></span>
<span data-ttu-id="84551-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84551-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84551-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="84551-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84551-140">입력</span><span class="sxs-lookup"><span data-stu-id="84551-140">INPUTS</span></span>

### <span data-ttu-id="84551-141">Microsoft. \*. AzureSqlInstanceFailoverGroupModel Failovergroup.</span><span class="sxs-lookup"><span data-stu-id="84551-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="84551-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="84551-142">System.String</span></span>

## <span data-ttu-id="84551-143">출력</span><span class="sxs-lookup"><span data-stu-id="84551-143">OUTPUTS</span></span>

### <span data-ttu-id="84551-144">Microsoft. \*. AzureSqlInstanceFailoverGroupModel Failovergroup.</span><span class="sxs-lookup"><span data-stu-id="84551-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="84551-145">상속자</span><span class="sxs-lookup"><span data-stu-id="84551-145">NOTES</span></span>

## <span data-ttu-id="84551-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84551-146">RELATED LINKS</span></span>
