---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Get-AzSecurityLocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityLocation.md
ms.openlocfilehash: b835113b07fb2295193b89fd817ba82ceca71655
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995955"
---
# <span data-ttu-id="b2130-101">Get-AzSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="b2130-101">Get-AzSecurityLocation</span></span>

## <span data-ttu-id="b2130-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2130-102">SYNOPSIS</span></span>
<span data-ttu-id="b2130-103">Azure Security Center에서 특정 구독에 대한 데이터를 자동으로 저장하는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b2130-103">Gets the location where Azure Security Center will automatically save data for the specific subscription</span></span>

## <span data-ttu-id="b2130-104">구문</span><span class="sxs-lookup"><span data-stu-id="b2130-104">SYNTAX</span></span>

### <span data-ttu-id="b2130-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="b2130-105">SubscriptionScope (Default)</span></span>
```
Get-AzSecurityLocation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2130-106">SubscriptionLevelResource</span><span class="sxs-lookup"><span data-stu-id="b2130-106">SubscriptionLevelResource</span></span>
```
Get-AzSecurityLocation -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b2130-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2130-107">ResourceId</span></span>
```
Get-AzSecurityLocation -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2130-108">설명</span><span class="sxs-lookup"><span data-stu-id="b2130-108">DESCRIPTION</span></span>
<span data-ttu-id="b2130-109">Azure Security Center는 일부 데이터를 저장할 위치를 자동으로 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="b2130-109">Azure Security Center will automatically decide on a location to save some of your data.</span></span>
<span data-ttu-id="b2130-110">이 cmdlet을 사용하여 해당 위치를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b2130-110">Use this cmdlet to discover that location.</span></span>

## <span data-ttu-id="b2130-111">예제</span><span class="sxs-lookup"><span data-stu-id="b2130-111">EXAMPLES</span></span>

### <span data-ttu-id="b2130-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="b2130-112">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityLocation
Id                                                                                                   Name
--                                                                                                   ----
/subscriptions/487bb485-b5b0-471e-9c0d-10717612f869/providers/Microsoft.Security/locations/centralus centralus
```

<span data-ttu-id="b2130-113">Azure Security Center에서 계산된 보안 데이터를 저장하는 위치를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b2130-113">Gets the location where Azure Security Center saves the calculated security data.</span></span>

## <span data-ttu-id="b2130-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b2130-114">PARAMETERS</span></span>

### <span data-ttu-id="b2130-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2130-115">-DefaultProfile</span></span>
<span data-ttu-id="b2130-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2130-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b2130-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b2130-117">-Name</span></span>
<span data-ttu-id="b2130-118">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b2130-118">Resource name.</span></span>

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

### <span data-ttu-id="b2130-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b2130-119">-ResourceId</span></span>
<span data-ttu-id="b2130-120">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b2130-120">Resource ID.</span></span>

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

### <span data-ttu-id="b2130-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2130-121">CommonParameters</span></span>
<span data-ttu-id="b2130-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b2130-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2130-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2130-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2130-124">입력</span><span class="sxs-lookup"><span data-stu-id="b2130-124">INPUTS</span></span>

### <span data-ttu-id="b2130-125">System.String</span><span class="sxs-lookup"><span data-stu-id="b2130-125">System.String</span></span>

## <span data-ttu-id="b2130-126">출력</span><span class="sxs-lookup"><span data-stu-id="b2130-126">OUTPUTS</span></span>

### <span data-ttu-id="b2130-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span><span class="sxs-lookup"><span data-stu-id="b2130-127">Microsoft.Azure.Commands.Security.Models.Locations.PSSecurityLocation</span></span>

## <span data-ttu-id="b2130-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b2130-128">NOTES</span></span>

## <span data-ttu-id="b2130-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2130-129">RELATED LINKS</span></span>
