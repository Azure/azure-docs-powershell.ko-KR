---
external help file: ''
Module Name: Az.Confluent
online version: https://docs.microsoft.com/powershell/module/az.confluent/new-azconfluentorganization
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Confluent/help/New-AzConfluentOrganization.md
ms.openlocfilehash: 546b4e56f2a932a6d7f17bda8484db8cd1c3c593
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012571"
---
# <span data-ttu-id="c6cc4-101">New-AzConfluentOrganization</span><span class="sxs-lookup"><span data-stu-id="c6cc4-101">New-AzConfluentOrganization</span></span>

## <span data-ttu-id="c6cc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="c6cc4-103">조직 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="c6cc4-103">Create Organization resource</span></span>

## <span data-ttu-id="c6cc4-104">구문</span><span class="sxs-lookup"><span data-stu-id="c6cc4-104">SYNTAX</span></span>

```
New-AzConfluentOrganization -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Location <String>] [-OfferDetailId <String>] [-OfferDetailPlanId <String>] [-OfferDetailPlanName <String>]
 [-OfferDetailPublisherId <String>] [-OfferDetailStatus <SaaSOfferStatus>] [-OfferDetailTermUnit <String>]
 [-Tag <Hashtable>] [-UserDetailEmailAddress <String>] [-UserDetailFirstName <String>]
 [-UserDetailLastName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="c6cc4-105">설명</span><span class="sxs-lookup"><span data-stu-id="c6cc4-105">DESCRIPTION</span></span>
<span data-ttu-id="c6cc4-106">조직 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="c6cc4-106">Create Organization resource</span></span>

## <span data-ttu-id="c6cc4-107">예제</span><span class="sxs-lookup"><span data-stu-id="c6cc4-107">EXAMPLES</span></span>

### <span data-ttu-id="c6cc4-108">예제 1: 혼성 조직 만들기</span><span class="sxs-lookup"><span data-stu-id="c6cc4-108">Example 1: Create a confluent organization</span></span>
```powershell
PS C:\> New-AzConfluentOrganization -ResourceGroupName azure-rg-test -Name confluentorg-02-pwsh -Location eastus -OfferDetailId "confluent-cloud-azure-prod" -OfferDetailPlanId "confluent-cloud-azure-payg-prod" -OfferDetailPlanName "Confluent Cloud - Pay as you Go" -OfferDetailPublisherId "confluentinc" -OfferDetailTermUnit "P1M" -UserDetailEmailAddress "xxxx@microsoft.com"

Location Name                   Type
-------- ----                   ----
eastus   confluentorg-02-pwsh Microsoft.Confluent/organizations
```

<span data-ttu-id="c6cc4-109">이 명령은 혼성 조직을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6cc4-109">This command creates a confluent organization.</span></span>

## <span data-ttu-id="c6cc4-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c6cc4-110">PARAMETERS</span></span>

### <span data-ttu-id="c6cc4-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6cc4-111">-AsJob</span></span>
<span data-ttu-id="c6cc4-112">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c6cc4-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c6cc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6cc4-113">-DefaultProfile</span></span>
<span data-ttu-id="c6cc4-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6cc4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6cc4-115">-Location</span><span class="sxs-lookup"><span data-stu-id="c6cc4-115">-Location</span></span>
<span data-ttu-id="c6cc4-116">조직 리소스의 위치</span><span class="sxs-lookup"><span data-stu-id="c6cc4-116">Location of Organization resource</span></span>

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

### <span data-ttu-id="c6cc4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c6cc4-117">-Name</span></span>
<span data-ttu-id="c6cc4-118">조직 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="c6cc4-118">Organization resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: OrganizationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6cc4-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c6cc4-119">-NoWait</span></span>
<span data-ttu-id="c6cc4-120">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="c6cc4-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c6cc4-121">-OfferDetailId</span><span class="sxs-lookup"><span data-stu-id="c6cc4-121">-OfferDetailId</span></span>
<span data-ttu-id="c6cc4-122">제품 ID</span><span class="sxs-lookup"><span data-stu-id="c6cc4-122">Offer Id</span></span>

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

### <span data-ttu-id="c6cc4-123">-OfferDetailPlanId</span><span class="sxs-lookup"><span data-stu-id="c6cc4-123">-OfferDetailPlanId</span></span>
<span data-ttu-id="c6cc4-124">제품 계획 ID</span><span class="sxs-lookup"><span data-stu-id="c6cc4-124">Offer Plan Id</span></span>

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

### <span data-ttu-id="c6cc4-125">-OfferDetailPlanName</span><span class="sxs-lookup"><span data-stu-id="c6cc4-125">-OfferDetailPlanName</span></span>
<span data-ttu-id="c6cc4-126">제품 계획 이름</span><span class="sxs-lookup"><span data-stu-id="c6cc4-126">Offer Plan Name</span></span>

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

### <span data-ttu-id="c6cc4-127">-OfferDetailPublisherId</span><span class="sxs-lookup"><span data-stu-id="c6cc4-127">-OfferDetailPublisherId</span></span>
<span data-ttu-id="c6cc4-128">게시자 ID</span><span class="sxs-lookup"><span data-stu-id="c6cc4-128">Publisher Id</span></span>

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

### <span data-ttu-id="c6cc4-129">-OfferDetailStatus</span><span class="sxs-lookup"><span data-stu-id="c6cc4-129">-OfferDetailStatus</span></span>
<span data-ttu-id="c6cc4-130">SaaS 제품 상태</span><span class="sxs-lookup"><span data-stu-id="c6cc4-130">SaaS Offer Status</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Confluent.Support.SaaSOfferStatus
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6cc4-131">-OfferDetailTermUnit</span><span class="sxs-lookup"><span data-stu-id="c6cc4-131">-OfferDetailTermUnit</span></span>
<span data-ttu-id="c6cc4-132">제품 계획 기간 단위</span><span class="sxs-lookup"><span data-stu-id="c6cc4-132">Offer Plan Term unit</span></span>

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

### <span data-ttu-id="c6cc4-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6cc4-133">-ResourceGroupName</span></span>
<span data-ttu-id="c6cc4-134">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="c6cc4-134">Resource group name</span></span>

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

### <span data-ttu-id="c6cc4-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6cc4-135">-SubscriptionId</span></span>
<span data-ttu-id="c6cc4-136">Microsoft Azure 구독 ID</span><span class="sxs-lookup"><span data-stu-id="c6cc4-136">Microsoft Azure subscription id</span></span>

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

### <span data-ttu-id="c6cc4-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6cc4-137">-Tag</span></span>
<span data-ttu-id="c6cc4-138">조직 리소스 태그</span><span class="sxs-lookup"><span data-stu-id="c6cc4-138">Organization resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6cc4-139">-UserDetailEmailAddress</span><span class="sxs-lookup"><span data-stu-id="c6cc4-139">-UserDetailEmailAddress</span></span>
<span data-ttu-id="c6cc4-140">전자 메일 주소</span><span class="sxs-lookup"><span data-stu-id="c6cc4-140">Email address</span></span>

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

### <span data-ttu-id="c6cc4-141">-UserDetailFirstName</span><span class="sxs-lookup"><span data-stu-id="c6cc4-141">-UserDetailFirstName</span></span>
<span data-ttu-id="c6cc4-142">이름</span><span class="sxs-lookup"><span data-stu-id="c6cc4-142">First name</span></span>

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

### <span data-ttu-id="c6cc4-143">-UserDetailLastName</span><span class="sxs-lookup"><span data-stu-id="c6cc4-143">-UserDetailLastName</span></span>
<span data-ttu-id="c6cc4-144">성</span><span class="sxs-lookup"><span data-stu-id="c6cc4-144">Last name</span></span>

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

### <span data-ttu-id="c6cc4-145">-확인</span><span class="sxs-lookup"><span data-stu-id="c6cc4-145">-Confirm</span></span>
<span data-ttu-id="c6cc4-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6cc4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6cc4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6cc4-147">-WhatIf</span></span>
<span data-ttu-id="c6cc4-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c6cc4-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6cc4-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6cc4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6cc4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6cc4-150">CommonParameters</span></span>
<span data-ttu-id="c6cc4-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c6cc4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6cc4-152">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c6cc4-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6cc4-153">입력</span><span class="sxs-lookup"><span data-stu-id="c6cc4-153">INPUTS</span></span>

## <span data-ttu-id="c6cc4-154">출력</span><span class="sxs-lookup"><span data-stu-id="c6cc4-154">OUTPUTS</span></span>

### <span data-ttu-id="c6cc4-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span><span class="sxs-lookup"><span data-stu-id="c6cc4-155">Microsoft.Azure.PowerShell.Cmdlets.Confluent.Models.Api20200301.IOrganizationResource</span></span>

## <span data-ttu-id="c6cc4-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c6cc4-156">NOTES</span></span>

<span data-ttu-id="c6cc4-157">별칭</span><span class="sxs-lookup"><span data-stu-id="c6cc4-157">ALIASES</span></span>

## <span data-ttu-id="c6cc4-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6cc4-158">RELATED LINKS</span></span>

