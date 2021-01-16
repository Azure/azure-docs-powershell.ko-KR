---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveApplicationControlGroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveApplicationControlGroup.md
ms.openlocfilehash: 9d36169439a2466ca50858f5b438822461259cf3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344450"
---
# <span data-ttu-id="7fcc5-101">Get-AzSecurityAdaptiveApplicationControlGroup</span><span class="sxs-lookup"><span data-stu-id="7fcc5-101">Get-AzSecurityAdaptiveApplicationControlGroup</span></span>

## <span data-ttu-id="7fcc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fcc5-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcc5-103">애플리케이션 제어 VM/서버 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-103">Gets an application control VM/server group.</span></span>

## <span data-ttu-id="7fcc5-104">구문</span><span class="sxs-lookup"><span data-stu-id="7fcc5-104">SYNTAX</span></span>

### <span data-ttu-id="7fcc5-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="7fcc5-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityAdaptiveApplicationControlGroup  -GroupName <String> -AscLocation <String> [-SubscriptionId <String>]
[-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fcc5-106">설명</span><span class="sxs-lookup"><span data-stu-id="7fcc5-106">DESCRIPTION</span></span>
<span data-ttu-id="7fcc5-107">적응형 애플리케이션 제어는 Azure Security Center에서 자동으로 계산되며, 이 cmdlet을 사용하여 애플리케이션 제어 VM/서버 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-107">Adaptive Application Controls are automatically calculated by Azure Security Center, use this cmdlet to get an application control VM/server group.</span></span>

## <span data-ttu-id="7fcc5-108">예제</span><span class="sxs-lookup"><span data-stu-id="7fcc5-108">EXAMPLES</span></span>

### <span data-ttu-id="7fcc5-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="7fcc5-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveApplicationControlGroup -GroupName GROUP1 -AscLocation centralus
Id         : /subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/providers/Microsoft.Security/locations/centralus/applicationWhitelistings/GROUP1
Name       : GROUP1
Type       : Microsoft.Security/applicationWhitelistings
Location   : centralus
Properties : Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControlsProperties
```
<span data-ttu-id="7fcc5-110">애플리케이션 제어 VM/서버 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-110">Gets an application control VM/server group.</span></span>


## <span data-ttu-id="7fcc5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fcc5-111">PARAMETERS</span></span>

### <span data-ttu-id="7fcc5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fcc5-112">-DefaultProfile</span></span>
<span data-ttu-id="7fcc5-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fcc5-114">-AscLocation</span><span class="sxs-lookup"><span data-stu-id="7fcc5-114">-AscLocation</span></span>
<span data-ttu-id="7fcc5-115">ASC가 구독의 데이터를 저장하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-115">The location where ASC stores the data of the subscription.</span></span> <span data-ttu-id="7fcc5-116">위치 Get에서 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-116">can be retrieved from Get locations.</span></span>

```yaml
Type: System.String
Parameter Sets: AscLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fcc5-117">-GroupName</span><span class="sxs-lookup"><span data-stu-id="7fcc5-117">-GroupName</span></span>
<span data-ttu-id="7fcc5-118">애플리케이션 제어 VM/서버 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-118">Name of an application control VM/server group.</span></span>

```yaml
Type: System.String
Parameter Sets: GroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fcc5-119">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fcc5-119">-SubscriptionId</span></span>
<span data-ttu-id="7fcc5-120">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-120">Azure subscription ID.</span></span>

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


### <span data-ttu-id="7fcc5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcc5-121">CommonParameters</span></span>
<span data-ttu-id="7fcc5-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcc5-123">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7fcc5-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcc5-124">입력</span><span class="sxs-lookup"><span data-stu-id="7fcc5-124">INPUTS</span></span>

### <span data-ttu-id="7fcc5-125">System.String</span><span class="sxs-lookup"><span data-stu-id="7fcc5-125">System.String</span></span>

## <span data-ttu-id="7fcc5-126">출력</span><span class="sxs-lookup"><span data-stu-id="7fcc5-126">OUTPUTS</span></span>

### <span data-ttu-id="7fcc5-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span><span class="sxs-lookup"><span data-stu-id="7fcc5-127">Microsoft.Azure.Commands.Security.Models.AdaptiveApplicationControls.PSSecurityAdaptiveApplicationControls</span></span>

## <span data-ttu-id="7fcc5-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7fcc5-128">NOTES</span></span>

## <span data-ttu-id="7fcc5-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fcc5-129">RELATED LINKS</span></span>