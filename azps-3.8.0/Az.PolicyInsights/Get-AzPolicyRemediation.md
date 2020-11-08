---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44c12e08ca66c19cf3541f4abb200e1ba0663208
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044471"
---
# <span data-ttu-id="a05b1-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a05b1-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="a05b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a05b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a05b1-103">정책 remediations를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-103">Gets policy remediations.</span></span>

## <span data-ttu-id="a05b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a05b1-104">SYNTAX</span></span>

### <span data-ttu-id="a05b1-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a05b1-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a05b1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a05b1-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a05b1-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="a05b1-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a05b1-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="a05b1-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a05b1-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="a05b1-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a05b1-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a05b1-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a05b1-111">설명은</span><span class="sxs-lookup"><span data-stu-id="a05b1-111">DESCRIPTION</span></span>
<span data-ttu-id="a05b1-112">**AzPolicyRemediation** cmdlet은 범위 또는 특정 재구성에 대 한 모든 정책 remediations를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="a05b1-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a05b1-113">EXAMPLES</span></span>

### <span data-ttu-id="a05b1-114">예제 1: 현재 구독에서 모든 정책 remediations 가져오기</span><span class="sxs-lookup"><span data-stu-id="a05b1-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="a05b1-115">이 명령은 ' My Subscription ' 이라는 구독 또는 그 아래에 생성 된 remediations를 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="a05b1-116">예제 2: 특정 정책 수정 및 배포 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="a05b1-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="a05b1-117">이 명령은 리소스 그룹 ' myResourceGroup '에서 ' remediation1 ' 라는 수정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="a05b1-118">재구성 되는 리소스에 대 한 세부 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="a05b1-119">예제 3: 관리 그룹에서 선택적 필터를 사용 하 여 10 개의 정책 remediations 가져오기</span><span class="sxs-lookup"><span data-stu-id="a05b1-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="a05b1-120">이 명령은 ' mg1 ' (이) 라는 관리 그룹에서 최대 10 개의 정책 remediations를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="a05b1-121">지정 된 정책 할당에 대 한 정책 remediations 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="a05b1-122">변수</span><span class="sxs-lookup"><span data-stu-id="a05b1-122">PARAMETERS</span></span>

### <span data-ttu-id="a05b1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a05b1-123">-DefaultProfile</span></span>
<span data-ttu-id="a05b1-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a05b1-125">-필터</span><span class="sxs-lookup"><span data-stu-id="a05b1-125">-Filter</span></span>
<span data-ttu-id="a05b1-126">OData 표시법을 사용 하 여 식을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="a05b1-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="a05b1-127">-IncludeDetail</span></span>
<span data-ttu-id="a05b1-128">업데이트 관리에서 만든 배포에 대 한 세부 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="a05b1-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a05b1-129">-ManagementGroupName</span></span>
<span data-ttu-id="a05b1-130">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-130">Management group ID.</span></span>

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

### <span data-ttu-id="a05b1-131">-이름</span><span class="sxs-lookup"><span data-stu-id="a05b1-131">-Name</span></span>
<span data-ttu-id="a05b1-132">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-132">Resource name.</span></span>

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

### <span data-ttu-id="a05b1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a05b1-133">-ResourceGroupName</span></span>
<span data-ttu-id="a05b1-134">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-134">Resource group name.</span></span>

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

### <span data-ttu-id="a05b1-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a05b1-135">-ResourceId</span></span>
<span data-ttu-id="a05b1-136">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-136">Resource ID.</span></span>

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

### <span data-ttu-id="a05b1-137">-범위</span><span class="sxs-lookup"><span data-stu-id="a05b1-137">-Scope</span></span>
<span data-ttu-id="a05b1-138">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-138">Scope of the resource.</span></span> <span data-ttu-id="a05b1-139">예를 들면 '/subscriptions/{subscriptionId}/resourceGroups/{rgName} '입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="a05b1-140">-위쪽</span><span class="sxs-lookup"><span data-stu-id="a05b1-140">-Top</span></span>
<span data-ttu-id="a05b1-141">반환할 레코드의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="a05b1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a05b1-142">CommonParameters</span></span>
<span data-ttu-id="a05b1-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a05b1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a05b1-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a05b1-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a05b1-145">입력</span><span class="sxs-lookup"><span data-stu-id="a05b1-145">INPUTS</span></span>

### <span data-ttu-id="a05b1-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a05b1-146">System.String</span></span>

## <span data-ttu-id="a05b1-147">출력</span><span class="sxs-lookup"><span data-stu-id="a05b1-147">OUTPUTS</span></span>

### <span data-ttu-id="a05b1-148">Microsoft. Azure. m. m. m. 업데이트. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="a05b1-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="a05b1-149">상속자</span><span class="sxs-lookup"><span data-stu-id="a05b1-149">NOTES</span></span>

## <span data-ttu-id="a05b1-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a05b1-150">RELATED LINKS</span></span>
