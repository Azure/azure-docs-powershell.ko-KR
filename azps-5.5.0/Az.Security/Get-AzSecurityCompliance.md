---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityCompliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityCompliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityCompliance.md
ms.openlocfilehash: 6009ec12b50e1960cbe241bf936d9cfedf2fea2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192689"
---
# <span data-ttu-id="5c8be-101">Get-AzSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="5c8be-101">Get-AzSecurityCompliance</span></span>

## <span data-ttu-id="5c8be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c8be-102">SYNOPSIS</span></span>
<span data-ttu-id="5c8be-103">시간 경과에 따라 구독의 보안 준수를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c8be-103">Get the security compliance of a subscription over time</span></span>

## <span data-ttu-id="5c8be-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c8be-104">SYNTAX</span></span>

### <span data-ttu-id="5c8be-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="5c8be-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityCompliance [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c8be-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="5c8be-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityCompliance -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c8be-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c8be-107">ResourceId</span></span>
```
Get-AzSecurityCompliance -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c8be-108">설명</span><span class="sxs-lookup"><span data-stu-id="5c8be-108">DESCRIPTION</span></span>
<span data-ttu-id="5c8be-109">이 구독의 현재 정상 및 비보안 리소스 비율에 따라 구독의 보안 준수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c8be-109">Gets the security compliance of a subscription based on the current healthy and non secured resources ratio on this subscription.</span></span>
<span data-ttu-id="5c8be-110">보안 준수는 매일 계산되고 기록이 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c8be-110">The security compliance is calculated every day and the history is saved.</span></span>

## <span data-ttu-id="5c8be-111">예제</span><span class="sxs-lookup"><span data-stu-id="5c8be-111">EXAMPLES</span></span>

### <span data-ttu-id="5c8be-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="5c8be-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityCompliance


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-19Z
Name                       : 2018-08-19Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 19/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-18Z
Name                       : 2018-08-18Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 18/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-17Z
Name                       : 2018-08-17Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 17/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-16Z
Name                       : 2018-08-16Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 16/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-15Z
Name                       : 2018-08-15Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 15/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-14Z
Name                       : 2018-08-14Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 14/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-13Z
Name                       : 2018-08-13Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 13/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-12Z
Name                       : 2018-08-12Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 12/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-11Z
Name                       : 2018-08-11Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 11/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-10Z
Name                       : 2018-08-10Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 10/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-09Z
Name                       : 2018-08-09Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 09/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-08Z
Name                       : 2018-08-08Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 08/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}

Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-07Z
Name                       : 2018-08-07Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 07/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="5c8be-113">지난 14일 동안 구독의 보안 준수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c8be-113">Gets the security compliance of a subscription for the last 14 days</span></span>

### <span data-ttu-id="5c8be-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="5c8be-114">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityCompliance -Name "2018-08-20Z"


Id                         : /subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/compliances/2018-08-20Z
Name                       : 2018-08-20Z
ResourceCount              : 18
AssessmentTimestampUtcDate : 20/08/2018 00:00:00
AssessmentResult           : {Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityComplianceSegment}
```

<span data-ttu-id="5c8be-115">특정 날짜에 구독의 보안 준수를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="5c8be-115">Gets the security compliance of a subscription on a specific date</span></span>

## <span data-ttu-id="5c8be-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c8be-116">PARAMETERS</span></span>

### <span data-ttu-id="5c8be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c8be-117">-DefaultProfile</span></span>
<span data-ttu-id="5c8be-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c8be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c8be-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5c8be-119">-Name</span></span>
<span data-ttu-id="5c8be-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c8be-120">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c8be-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c8be-121">-ResourceId</span></span>
<span data-ttu-id="5c8be-122">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5c8be-122">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c8be-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c8be-123">CommonParameters</span></span>
<span data-ttu-id="5c8be-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c8be-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c8be-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c8be-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c8be-126">입력</span><span class="sxs-lookup"><span data-stu-id="5c8be-126">INPUTS</span></span>

### <span data-ttu-id="5c8be-127">System.String</span><span class="sxs-lookup"><span data-stu-id="5c8be-127">System.String</span></span>

## <span data-ttu-id="5c8be-128">출력</span><span class="sxs-lookup"><span data-stu-id="5c8be-128">OUTPUTS</span></span>

### <span data-ttu-id="5c8be-129">Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityCompliance</span><span class="sxs-lookup"><span data-stu-id="5c8be-129">Microsoft.Azure.Commands.Security.Models.Compliances.PSSecurityCompliance</span></span>

## <span data-ttu-id="5c8be-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c8be-130">NOTES</span></span>

## <span data-ttu-id="5c8be-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c8be-131">RELATED LINKS</span></span>
