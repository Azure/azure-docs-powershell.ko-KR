---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44c12e08ca66c19cf3541f4abb200e1ba0663208
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193164"
---
# <span data-ttu-id="cfaf8-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="cfaf8-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="cfaf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cfaf8-102">SYNOPSIS</span></span>
<span data-ttu-id="cfaf8-103">정책 수정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-103">Gets policy remediations.</span></span>

## <span data-ttu-id="cfaf8-104">구문</span><span class="sxs-lookup"><span data-stu-id="cfaf8-104">SYNTAX</span></span>

### <span data-ttu-id="cfaf8-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="cfaf8-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfaf8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cfaf8-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cfaf8-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="cfaf8-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfaf8-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="cfaf8-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfaf8-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="cfaf8-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfaf8-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cfaf8-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cfaf8-111">설명</span><span class="sxs-lookup"><span data-stu-id="cfaf8-111">DESCRIPTION</span></span>
<span data-ttu-id="cfaf8-112">**Get-AzPolicyRemediation** cmdlet은 범위 또는 특정 수정의 모든 정책 수정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="cfaf8-113">예제</span><span class="sxs-lookup"><span data-stu-id="cfaf8-113">EXAMPLES</span></span>

### <span data-ttu-id="cfaf8-114">예제 1: 현재 구독의 모든 정책 수정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="cfaf8-115">이 명령은 '내 구독'이라는 구독에서 또는 그 아래에 만들어진 모든 수정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="cfaf8-116">예제 2: 특정 정책 수정 및 배포 세부 정보 확인</span><span class="sxs-lookup"><span data-stu-id="cfaf8-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="cfaf8-117">이 명령은 리소스 그룹 'myResourceGroup'에서 'remediation1'이라는 수정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="cfaf8-118">수정되는 리소스의 세부 정보가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="cfaf8-119">예제 3: 선택적 필터를 사용하여 관리 그룹에서 10개 정책 수정</span><span class="sxs-lookup"><span data-stu-id="cfaf8-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="cfaf8-120">이 명령은 'mg1'이라는 관리 그룹에서 최대 10개 정책 수정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="cfaf8-121">주어진 정책 할당에 대한 정책 수정만 검색됩니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="cfaf8-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cfaf8-122">PARAMETERS</span></span>

### <span data-ttu-id="cfaf8-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfaf8-123">-DefaultProfile</span></span>
<span data-ttu-id="cfaf8-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfaf8-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="cfaf8-125">-Filter</span></span>
<span data-ttu-id="cfaf8-126">OData 표기어를 사용하여 식 필터링</span><span class="sxs-lookup"><span data-stu-id="cfaf8-126">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, GenericScope, ManagementGroupScope, ResourceGroupScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfaf8-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="cfaf8-127">-IncludeDetail</span></span>
<span data-ttu-id="cfaf8-128">수정에서 만든 배포의 세부 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-128">Include details of the deployments created by the remediation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cfaf8-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="cfaf8-129">-ManagementGroupName</span></span>
<span data-ttu-id="cfaf8-130">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-130">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfaf8-131">-Name</span><span class="sxs-lookup"><span data-stu-id="cfaf8-131">-Name</span></span>
<span data-ttu-id="cfaf8-132">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-132">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfaf8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfaf8-133">-ResourceGroupName</span></span>
<span data-ttu-id="cfaf8-134">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-134">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfaf8-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cfaf8-135">-ResourceId</span></span>
<span data-ttu-id="cfaf8-136">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-136">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfaf8-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="cfaf8-137">-Scope</span></span>
<span data-ttu-id="cfaf8-138">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-138">Scope of the resource.</span></span> <span data-ttu-id="cfaf8-139">예: '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GenericScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfaf8-140">-Top</span><span class="sxs-lookup"><span data-stu-id="cfaf8-140">-Top</span></span>
<span data-ttu-id="cfaf8-141">반환할 최대 레코드 수입니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="cfaf8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfaf8-142">CommonParameters</span></span>
<span data-ttu-id="cfaf8-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfaf8-144">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cfaf8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfaf8-145">입력</span><span class="sxs-lookup"><span data-stu-id="cfaf8-145">INPUTS</span></span>

### <span data-ttu-id="cfaf8-146">System.String</span><span class="sxs-lookup"><span data-stu-id="cfaf8-146">System.String</span></span>

## <span data-ttu-id="cfaf8-147">출력</span><span class="sxs-lookup"><span data-stu-id="cfaf8-147">OUTPUTS</span></span>

### <span data-ttu-id="cfaf8-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="cfaf8-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="cfaf8-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cfaf8-149">NOTES</span></span>

## <span data-ttu-id="cfaf8-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cfaf8-150">RELATED LINKS</span></span>
