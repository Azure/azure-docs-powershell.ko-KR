---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControl.md
ms.openlocfilehash: cc86d7262270a253c9e77f0aec923c2a9fad693a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309893"
---
# <span data-ttu-id="b8a2d-101">Get-AzSecurityAdaptiveApplicationControl</span><span class="sxs-lookup"><span data-stu-id="b8a2d-101">Get-AzSecurityAdaptiveApplicationControl</span></span>

## <span data-ttu-id="b8a2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a2d-103">구독에 대 한 응용 프로그램 컨트롤 VM/서버 그룹의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8a2d-103">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="b8a2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8a2d-104">SYNTAX</span></span>

### <span data-ttu-id="b8a2d-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8a2d-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControl [-SubscriptionId <String>] [-IncludePathRecommendation <Boolean>] [-Summary <Boolean>] 
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8a2d-106">설명은</span><span class="sxs-lookup"><span data-stu-id="b8a2d-106">DESCRIPTION</span></span>
<span data-ttu-id="b8a2d-107">적응 응용 프로그램 컨트롤은 Azure 보안 센터에서 자동으로 계산 되며,이 cmdlet을 사용 하 여 구독 범위에서 적응 응용 프로그램 컨트롤 리소스의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8a2d-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Application Controls resources in the scope of a subscription.</span></span>

## <span data-ttu-id="b8a2d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="b8a2d-108">EXAMPLES</span></span>

### <span data-ttu-id="b8a2d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8a2d-109">Example 1</span></span>
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
<span data-ttu-id="b8a2d-110">구독에 대 한 응용 프로그램 컨트롤 VM/서버 그룹의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b8a2d-110">Gets a list of application control VM/server groups for the subscription.</span></span>

## <span data-ttu-id="b8a2d-111">변수</span><span class="sxs-lookup"><span data-stu-id="b8a2d-111">PARAMETERS</span></span>

### <span data-ttu-id="b8a2d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a2d-112">-DefaultProfile</span></span>
<span data-ttu-id="b8a2d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8a2d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8a2d-114">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b8a2d-114">-SubscriptionId</span></span>
<span data-ttu-id="b8a2d-115">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b8a2d-115">Azure subscription ID.</span></span>

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

### <span data-ttu-id="b8a2d-116">-IncludePathRecommendations</span><span class="sxs-lookup"><span data-stu-id="b8a2d-116">-IncludePathRecommendations</span></span>
<span data-ttu-id="b8a2d-117">정책 규칙을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a2d-117">Include the policy rules.</span></span>

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

### <span data-ttu-id="b8a2d-118">-요약</span><span class="sxs-lookup"><span data-stu-id="b8a2d-118">-Summary</span></span>
<span data-ttu-id="b8a2d-119">요약 된 형식으로 출력을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a2d-119">Return output in a summarized form.</span></span>

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

### <span data-ttu-id="b8a2d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a2d-120">CommonParameters</span></span>
<span data-ttu-id="b8a2d-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8a2d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a2d-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8a2d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a2d-123">입력</span><span class="sxs-lookup"><span data-stu-id="b8a2d-123">INPUTS</span></span>

### <span data-ttu-id="b8a2d-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8a2d-124">System.String</span></span>

### <span data-ttu-id="b8a2d-125">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b8a2d-125">System.Boolean</span></span>

## <span data-ttu-id="b8a2d-126">출력</span><span class="sxs-lookup"><span data-stu-id="b8a2d-126">OUTPUTS</span></span>

### <span data-ttu-id="b8a2d-127">AdaptiveApplicationControls. PSSecurityAdaptiveApplicationControls에 대 한 Microsoft</span><span class="sxs-lookup"><span data-stu-id="b8a2d-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="b8a2d-128">상속자</span><span class="sxs-lookup"><span data-stu-id="b8a2d-128">NOTES</span></span>

## <span data-ttu-id="b8a2d-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8a2d-129">RELATED LINKS</span></span>
