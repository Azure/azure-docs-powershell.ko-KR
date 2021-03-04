---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: ec35083cf4495d0bf262d841563f0dc4100dcdc8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974352"
---
# <span data-ttu-id="984df-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="984df-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="984df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="984df-102">SYNOPSIS</span></span>
<span data-ttu-id="984df-103">구독에 대한 애플리케이션 제어 VM/서버 그룹 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="984df-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="984df-104">구문</span><span class="sxs-lookup"><span data-stu-id="984df-104">SYNTAX</span></span>

### <span data-ttu-id="984df-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="984df-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="984df-106">설명</span><span class="sxs-lookup"><span data-stu-id="984df-106">DESCRIPTION</span></span>
<span data-ttu-id="984df-107">적응 애플리케이션 컨트롤은 Azure Security Center에서 자동으로 계산되며, 이 cmdlet을 사용하여 구독 범위에서 Adaptive Application Controls 리소스 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="984df-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="984df-108">예제</span><span class="sxs-lookup"><span data-stu-id="984df-108">EXAMPLES</span></span>

### <span data-ttu-id="984df-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="984df-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControl
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP2
Name       : GROUP2
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP3
Name       : GROUP3
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP4
Name       : GROUP5
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties

```
<span data-ttu-id="984df-110">구독에 대한 애플리케이션 제어 VM/서버 그룹 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="984df-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="984df-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="984df-111">PARAMETERS</span></span>

### <span data-ttu-id="984df-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="984df-112">-DefaultProfile</span></span>
<span data-ttu-id="984df-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="984df-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="984df-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="984df-114">-SubscriptionId</span></span>
<span data-ttu-id="984df-115">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="984df-115">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="984df-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="984df-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="984df-117">정책 규칙을 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="984df-117">Include the policy rules.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: IncludePathRecommendations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="984df-118">-요약</span><span class="sxs-lookup"><span data-stu-id="984df-118">-Summary</span></span>
<span data-ttu-id="984df-119">요약된 형태로 출력을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="984df-119">Return output in a summarized form.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: Summary
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="984df-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="984df-120">CommonParameters</span></span>
<span data-ttu-id="984df-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="984df-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="984df-122">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="984df-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="984df-123">입력</span><span class="sxs-lookup"><span data-stu-id="984df-123">INPUTS</span></span>

### <span data-ttu-id="984df-124">System.String</span><span class="sxs-lookup"><span data-stu-id="984df-124">System.String</span></span>

### <span data-ttu-id="984df-125">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="984df-125">System.Boolean</span></span>

## <span data-ttu-id="984df-126">출력</span><span class="sxs-lookup"><span data-stu-id="984df-126">OUTPUTS</span></span>

### <span data-ttu-id="984df-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="984df-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="984df-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="984df-128">NOTES</span></span>

## <span data-ttu-id="984df-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="984df-129">RELATED LINKS</span></span>
