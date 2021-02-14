---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightsaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsAccessPolicy.md
ms.openlocfilehash: b9024c0d5105344fa505832a0357c55393c55ed8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197289"
---
# <span data-ttu-id="0c5da-101">New-AzTimeSeriesInsightsAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0c5da-101">New-AzTimeSeriesInsightsAccessPolicy</span></span>

## <span data-ttu-id="0c5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c5da-102">SYNOPSIS</span></span>
<span data-ttu-id="0c5da-103">지정된 환경에서 액세스 정책을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-103">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="0c5da-104">구문</span><span class="sxs-lookup"><span data-stu-id="0c5da-104">SYNTAX</span></span>

```
New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-Description <String>] [-PrincipalObjectId <String>] [-Role <AccessPolicyRole[]>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0c5da-105">설명</span><span class="sxs-lookup"><span data-stu-id="0c5da-105">DESCRIPTION</span></span>
<span data-ttu-id="0c5da-106">지정된 환경에서 액세스 정책을 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-106">Create or update an access policy in the specified environment.</span></span>

## <span data-ttu-id="0c5da-107">예제</span><span class="sxs-lookup"><span data-stu-id="0c5da-107">EXAMPLES</span></span>

### <span data-ttu-id="0c5da-108">예제 1: 지정된 환경에 대한 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="0c5da-108">Example 1: Create an access policy for a specified environment</span></span>
```powershell
PS C:\> New-AzTimeSeriesInsightsAccessPolicy -EnvironmentName tsitest001 -ResourceGroupName testgroup -PrincipalObjectId ce74a389-b5e8-4f16-89c7-787031ddd903 -Role Contributor -Name policy001

Name      Type
----      ----
policy001 Microsoft.TimeSeriesInsights/Environments/AccessPolicies
```

<span data-ttu-id="0c5da-109">이 명령은 지정된 환경에 대한 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-109">This command creates an access policy for a specified environment.</span></span>

## <span data-ttu-id="0c5da-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c5da-110">PARAMETERS</span></span>

### <span data-ttu-id="0c5da-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c5da-111">-DefaultProfile</span></span>
<span data-ttu-id="0c5da-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c5da-113">-Description</span><span class="sxs-lookup"><span data-stu-id="0c5da-113">-Description</span></span>
<span data-ttu-id="0c5da-114">액세스 정책에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-114">An description of the access policy.</span></span>

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

### <span data-ttu-id="0c5da-115">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="0c5da-115">-EnvironmentName</span></span>
<span data-ttu-id="0c5da-116">지정된 리소스 그룹과 연결된 Time Series Insights 환경의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-116">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="0c5da-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0c5da-117">-Name</span></span>
<span data-ttu-id="0c5da-118">액세스 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-118">Name of the access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccessPolicyName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c5da-119">-PrincipalObjectId</span><span class="sxs-lookup"><span data-stu-id="0c5da-119">-PrincipalObjectId</span></span>
<span data-ttu-id="0c5da-120">Azure Active Directory에서 보안 주체의 objectId입니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-120">The objectId of the principal in Azure Active Directory.</span></span>

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

### <span data-ttu-id="0c5da-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c5da-121">-ResourceGroupName</span></span>
<span data-ttu-id="0c5da-122">Azure 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-122">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="0c5da-123">-Role</span><span class="sxs-lookup"><span data-stu-id="0c5da-123">-Role</span></span>
<span data-ttu-id="0c5da-124">환경에 주체가 할당된 역할 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-124">The list of roles the principal is assigned on the environment.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.AccessPolicyRole[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c5da-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c5da-125">-SubscriptionId</span></span>
<span data-ttu-id="0c5da-126">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-126">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="0c5da-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c5da-127">-Confirm</span></span>
<span data-ttu-id="0c5da-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c5da-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c5da-129">-WhatIf</span></span>
<span data-ttu-id="0c5da-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0c5da-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c5da-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c5da-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c5da-132">CommonParameters</span></span>
<span data-ttu-id="0c5da-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c5da-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c5da-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0c5da-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c5da-135">입력</span><span class="sxs-lookup"><span data-stu-id="0c5da-135">INPUTS</span></span>

## <span data-ttu-id="0c5da-136">출력</span><span class="sxs-lookup"><span data-stu-id="0c5da-136">OUTPUTS</span></span>

### <span data-ttu-id="0c5da-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span><span class="sxs-lookup"><span data-stu-id="0c5da-137">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IAccessPolicyResource</span></span>

## <span data-ttu-id="0c5da-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c5da-138">NOTES</span></span>

<span data-ttu-id="0c5da-139">별칭</span><span class="sxs-lookup"><span data-stu-id="0c5da-139">ALIASES</span></span>

## <span data-ttu-id="0c5da-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c5da-140">RELATED LINKS</span></span>

