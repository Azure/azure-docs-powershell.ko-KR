---
external help file: Microsoft.Azure.Commands.PolicyInsights.dll-Help.xml
Module Name: AzureRM.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.policyinsights/get-azurermpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PolicyInsights/Commands.PolicyInsights/help/Get-AzureRmPolicyRemediation.md
ms.openlocfilehash: e69ad25800dbf6aada7111a1093b4c878f3c0f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534224"
---
# <span data-ttu-id="a9e19-101">Get-AzureRmPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a9e19-101">Get-AzureRmPolicyRemediation</span></span>

## <span data-ttu-id="a9e19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9e19-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e19-103">정책 remediations를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-103">Gets policy remediations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9e19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9e19-104">SYNTAX</span></span>

### <span data-ttu-id="a9e19-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a9e19-105">SubscriptionScope (Default)</span></span>
```
Get-AzureRmPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9e19-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a9e19-106">ByName</span></span>
```
Get-AzureRmPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a9e19-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="a9e19-107">GenericScope</span></span>
```
Get-AzureRmPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9e19-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="a9e19-108">ManagementGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9e19-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="a9e19-109">ResourceGroupScope</span></span>
```
Get-AzureRmPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a9e19-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e19-110">ByResourceId</span></span>
```
Get-AzureRmPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a9e19-111">설명은</span><span class="sxs-lookup"><span data-stu-id="a9e19-111">DESCRIPTION</span></span>
<span data-ttu-id="a9e19-112">**AzureRmPolicyRemediation** cmdlet은 범위 또는 특정 재구성에 대 한 모든 정책 remediations를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-112">The **Get-AzureRmPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="a9e19-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a9e19-113">EXAMPLES</span></span>

### <span data-ttu-id="a9e19-114">예제 1: 현재 구독에서 모든 정책 remediations 가져오기</span><span class="sxs-lookup"><span data-stu-id="a9e19-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzureRmSubscription -Subscription "My Subscription"
PS C:\> Get-AzureRmPolicyRemediation
```

<span data-ttu-id="a9e19-115">이 명령은 ' My Subscription ' 이라는 구독 또는 그 아래에 생성 된 remediations를 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="a9e19-116">예제 2: 특정 정책 수정 및 배포 세부 정보 가져오기</span><span class="sxs-lookup"><span data-stu-id="a9e19-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="a9e19-117">이 명령은 리소스 그룹 ' myResourceGroup '에서 ' remediation1 ' 라는 수정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="a9e19-118">재구성 되는 리소스에 대 한 세부 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="a9e19-119">예제 3: 관리 그룹에서 선택적 필터를 사용 하 여 10 개의 정책 remediations 가져오기</span><span class="sxs-lookup"><span data-stu-id="a9e19-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzureRmPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="a9e19-120">이 명령은 ' mg1 ' (이) 라는 관리 그룹에서 최대 10 개의 정책 remediations를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="a9e19-121">지정 된 정책 할당에 대 한 정책 remediations 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="a9e19-122">변수</span><span class="sxs-lookup"><span data-stu-id="a9e19-122">PARAMETERS</span></span>

### <span data-ttu-id="a9e19-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e19-123">-DefaultProfile</span></span>
<span data-ttu-id="a9e19-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9e19-125">-필터</span><span class="sxs-lookup"><span data-stu-id="a9e19-125">-Filter</span></span>
<span data-ttu-id="a9e19-126">OData 표시법을 사용 하 여 식을 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="a9e19-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="a9e19-127">-IncludeDetail</span></span>
<span data-ttu-id="a9e19-128">업데이트 관리에서 만든 배포에 대 한 세부 정보를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="a9e19-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e19-129">-ManagementGroupName</span></span>
<span data-ttu-id="a9e19-130">관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-130">Management group ID.</span></span>

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

### <span data-ttu-id="a9e19-131">-이름</span><span class="sxs-lookup"><span data-stu-id="a9e19-131">-Name</span></span>
<span data-ttu-id="a9e19-132">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-132">Resource name.</span></span>

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

### <span data-ttu-id="a9e19-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e19-133">-ResourceGroupName</span></span>
<span data-ttu-id="a9e19-134">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-134">Resource group name.</span></span>

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

### <span data-ttu-id="a9e19-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9e19-135">-ResourceId</span></span>
<span data-ttu-id="a9e19-136">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-136">Resource ID.</span></span>

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

### <span data-ttu-id="a9e19-137">-범위</span><span class="sxs-lookup"><span data-stu-id="a9e19-137">-Scope</span></span>
<span data-ttu-id="a9e19-138">리소스의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-138">Scope of the resource.</span></span> <span data-ttu-id="a9e19-139">예를 들면 '/subscriptions/{subscriptionId}/resourceGroups/{rgName} '입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="a9e19-140">-위쪽</span><span class="sxs-lookup"><span data-stu-id="a9e19-140">-Top</span></span>
<span data-ttu-id="a9e19-141">반환할 레코드의 최대 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="a9e19-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e19-142">CommonParameters</span></span>
<span data-ttu-id="a9e19-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9e19-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e19-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9e19-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e19-145">입력</span><span class="sxs-lookup"><span data-stu-id="a9e19-145">INPUTS</span></span>

### <span data-ttu-id="a9e19-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a9e19-146">System.String</span></span>

## <span data-ttu-id="a9e19-147">출력</span><span class="sxs-lookup"><span data-stu-id="a9e19-147">OUTPUTS</span></span>

### <span data-ttu-id="a9e19-148">Microsoft. Azure. m. m. m. 업데이트. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="a9e19-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="a9e19-149">상속자</span><span class="sxs-lookup"><span data-stu-id="a9e19-149">NOTES</span></span>

## <span data-ttu-id="a9e19-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9e19-150">RELATED LINKS</span></span>
