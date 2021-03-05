---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: f26e1bd19b9856df7bf68de6c8afddefb3ee64a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988484"
---
# <span data-ttu-id="88e07-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="88e07-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="88e07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88e07-102">SYNOPSIS</span></span>
<span data-ttu-id="88e07-103">CDN 프로필에 대해 지원되는 최적화 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88e07-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="88e07-104">구문</span><span class="sxs-lookup"><span data-stu-id="88e07-104">SYNTAX</span></span>

### <span data-ttu-id="88e07-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="88e07-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88e07-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88e07-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="88e07-107">설명</span><span class="sxs-lookup"><span data-stu-id="88e07-107">DESCRIPTION</span></span>
<span data-ttu-id="88e07-108">**Get-AzCdnProfileSupportedOptimizationType** cmdlet은 현재 프로필에 대해 지원되는 최적화 유형을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="88e07-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="88e07-109">사용자는 나열된 값에서 최적화 유형이 있는 엔드포인트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88e07-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="88e07-110">예제</span><span class="sxs-lookup"><span data-stu-id="88e07-110">EXAMPLES</span></span>

### <span data-ttu-id="88e07-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="88e07-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="88e07-112">CDN 프로필에 대해 지원되는 최적화 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="88e07-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="88e07-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="88e07-113">PARAMETERS</span></span>

### <span data-ttu-id="88e07-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="88e07-114">-CdnProfile</span></span>
<span data-ttu-id="88e07-115">Azure CDN 프로필 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="88e07-115">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88e07-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88e07-116">-DefaultProfile</span></span>
<span data-ttu-id="88e07-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88e07-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88e07-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="88e07-118">-ProfileName</span></span>
<span data-ttu-id="88e07-119">프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88e07-119">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e07-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88e07-120">-ResourceGroupName</span></span>
<span data-ttu-id="88e07-121">프로필이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="88e07-121">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88e07-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88e07-122">CommonParameters</span></span>
<span data-ttu-id="88e07-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88e07-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88e07-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88e07-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88e07-125">입력</span><span class="sxs-lookup"><span data-stu-id="88e07-125">INPUTS</span></span>

### <span data-ttu-id="88e07-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="88e07-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="88e07-127">출력</span><span class="sxs-lookup"><span data-stu-id="88e07-127">OUTPUTS</span></span>

### <span data-ttu-id="88e07-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="88e07-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="88e07-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88e07-129">NOTES</span></span>

## <span data-ttu-id="88e07-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88e07-130">RELATED LINKS</span></span>
