---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: db6520ae16d114fdcad85daf3e0742589fa0fbbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357330"
---
# <span data-ttu-id="76194-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="76194-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="76194-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76194-102">SYNOPSIS</span></span>
<span data-ttu-id="76194-103">CDN 프로필에 대해 지원되는 최적화 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76194-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="76194-104">구문</span><span class="sxs-lookup"><span data-stu-id="76194-104">SYNTAX</span></span>

### <span data-ttu-id="76194-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="76194-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76194-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76194-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76194-107">설명</span><span class="sxs-lookup"><span data-stu-id="76194-107">DESCRIPTION</span></span>
<span data-ttu-id="76194-108">**Get-AzCdnProfileSupportedOptimizationType** cmdlet은 현재 프로필에 대해 지원되는 최적화 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76194-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="76194-109">사용자는 나열된 값에서 최적화 형식을 사용하여 엔드포인트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="76194-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="76194-110">예제</span><span class="sxs-lookup"><span data-stu-id="76194-110">EXAMPLES</span></span>

### <span data-ttu-id="76194-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="76194-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="76194-112">CDN 프로필에 대해 지원되는 최적화 유형을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="76194-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="76194-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="76194-113">PARAMETERS</span></span>

### <span data-ttu-id="76194-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="76194-114">-CdnProfile</span></span>
<span data-ttu-id="76194-115">Azure CDN 프로필 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="76194-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="76194-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76194-116">-DefaultProfile</span></span>
<span data-ttu-id="76194-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76194-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76194-118">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="76194-118">-ProfileName</span></span>
<span data-ttu-id="76194-119">프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76194-119">The name of the profile.</span></span>

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

### <span data-ttu-id="76194-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76194-120">-ResourceGroupName</span></span>
<span data-ttu-id="76194-121">프로필이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="76194-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="76194-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76194-122">CommonParameters</span></span>
<span data-ttu-id="76194-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76194-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76194-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="76194-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76194-125">입력</span><span class="sxs-lookup"><span data-stu-id="76194-125">INPUTS</span></span>

### <span data-ttu-id="76194-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="76194-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="76194-127">출력</span><span class="sxs-lookup"><span data-stu-id="76194-127">OUTPUTS</span></span>

### <span data-ttu-id="76194-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span><span class="sxs-lookup"><span data-stu-id="76194-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="76194-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76194-129">NOTES</span></span>

## <span data-ttu-id="76194-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76194-130">RELATED LINKS</span></span>
