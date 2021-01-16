---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 8bfcb3a96ee8db53a6a869a01441739ee9c503bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372247"
---
# <span data-ttu-id="45569-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="45569-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="45569-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45569-102">SYNOPSIS</span></span>
<span data-ttu-id="45569-103">Kusto 클러스터 데이터베이스 principalAssignment를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45569-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="45569-104">구문</span><span class="sxs-lookup"><span data-stu-id="45569-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="45569-105">설명</span><span class="sxs-lookup"><span data-stu-id="45569-105">DESCRIPTION</span></span>
<span data-ttu-id="45569-106">Kusto 클러스터 데이터베이스 principalAssignment를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45569-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="45569-107">예제</span><span class="sxs-lookup"><span data-stu-id="45569-107">EXAMPLES</span></span>

### <span data-ttu-id="45569-108">예제 1: Kusto 클러스터 데이터베이스 보안 주체 만들기</span><span class="sxs-lookup"><span data-stu-id="45569-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="45569-109">위의 명령은 Kusto 클러스터 데이터베이스 principalAssignment를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45569-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="45569-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45569-110">PARAMETERS</span></span>

### <span data-ttu-id="45569-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45569-111">-AsJob</span></span>
<span data-ttu-id="45569-112">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="45569-112">Run the command as a job</span></span>

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

### <span data-ttu-id="45569-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="45569-113">-ClusterName</span></span>
<span data-ttu-id="45569-114">Kusto 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="45569-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="45569-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="45569-115">-DatabaseName</span></span>
<span data-ttu-id="45569-116">Kusto 클러스터의 데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="45569-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="45569-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45569-117">-DefaultProfile</span></span>
<span data-ttu-id="45569-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45569-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45569-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="45569-119">-NoWait</span></span>
<span data-ttu-id="45569-120">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="45569-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="45569-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="45569-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="45569-122">Kusto principalAssignment의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="45569-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="45569-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="45569-123">-PrincipalId</span></span>
<span data-ttu-id="45569-124">데이터베이스 주체에 할당된 보안 주체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="45569-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="45569-125">사용자 전자 메일, 애플리케이션 ID 또는 보안 그룹 이름일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="45569-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="45569-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="45569-126">-PrincipalType</span></span>
<span data-ttu-id="45569-127">보안 주체 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="45569-127">Principal type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.PrincipalType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45569-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45569-128">-ResourceGroupName</span></span>
<span data-ttu-id="45569-129">Kusto 클러스터를 포함하는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="45569-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="45569-130">-Role</span><span class="sxs-lookup"><span data-stu-id="45569-130">-Role</span></span>
<span data-ttu-id="45569-131">데이터베이스 주체 역할입니다.</span><span class="sxs-lookup"><span data-stu-id="45569-131">Database principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DatabasePrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45569-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45569-132">-SubscriptionId</span></span>
<span data-ttu-id="45569-133">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="45569-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="45569-134">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="45569-134">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45569-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="45569-135">-TenantId</span></span>
<span data-ttu-id="45569-136">보안 주체의 테넌트 ID</span><span class="sxs-lookup"><span data-stu-id="45569-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="45569-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45569-137">-Confirm</span></span>
<span data-ttu-id="45569-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="45569-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45569-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45569-139">-WhatIf</span></span>
<span data-ttu-id="45569-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="45569-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45569-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="45569-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45569-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45569-142">CommonParameters</span></span>
<span data-ttu-id="45569-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="45569-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45569-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="45569-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45569-145">입력</span><span class="sxs-lookup"><span data-stu-id="45569-145">INPUTS</span></span>

## <span data-ttu-id="45569-146">출력</span><span class="sxs-lookup"><span data-stu-id="45569-146">OUTPUTS</span></span>

### <span data-ttu-id="45569-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="45569-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="45569-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="45569-148">NOTES</span></span>

<span data-ttu-id="45569-149">별칭</span><span class="sxs-lookup"><span data-stu-id="45569-149">ALIASES</span></span>

## <span data-ttu-id="45569-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45569-150">RELATED LINKS</span></span>

