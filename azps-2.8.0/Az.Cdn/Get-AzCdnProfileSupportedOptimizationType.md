---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnprofilesupportedoptimizationtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileSupportedOptimizationType.md
ms.openlocfilehash: 141f5b87807d2ad60f1dbe8555629bc3e117605d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697596"
---
# <span data-ttu-id="b04d7-101">Get-AzCdnProfileSupportedOptimizationType</span><span class="sxs-lookup"><span data-stu-id="b04d7-101">Get-AzCdnProfileSupportedOptimizationType</span></span>

## <span data-ttu-id="b04d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b04d7-102">SYNOPSIS</span></span>
<span data-ttu-id="b04d7-103">CDN 프로필에 대해 지원 되는 최적화 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b04d7-103">Gets the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="b04d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b04d7-104">SYNTAX</span></span>

### <span data-ttu-id="b04d7-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b04d7-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b04d7-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b04d7-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileSupportedOptimizationType -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b04d7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b04d7-107">DESCRIPTION</span></span>
<span data-ttu-id="b04d7-108">**AzCdnProfileSupportedOptimizationType** cmdlet은 현재 프로필에 지원 되는 최적화 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b04d7-108">The **Get-AzCdnProfileSupportedOptimizationType** cmdlet gets the supported optimization types for the current profile.</span></span> <span data-ttu-id="b04d7-109">사용자는 나열 된 값에서 최적화 유형의 끝점을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b04d7-109">A user can create an endpoint with an optimization type from the listed values.</span></span>

## <span data-ttu-id="b04d7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b04d7-110">EXAMPLES</span></span>

### <span data-ttu-id="b04d7-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b04d7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnProfileSupportedOptimizationType -ProfileName $profileName -ResourceGroupName $resourceGroupName
OptimizationType: GeneralWebDelivery
OptimizationType: DynamicSiteAcceleration
```

<span data-ttu-id="b04d7-112">CDN 프로필에 대해 지원 되는 최적화 유형을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b04d7-112">Get the supported optimization types for a CDN profile.</span></span>

## <span data-ttu-id="b04d7-113">변수</span><span class="sxs-lookup"><span data-stu-id="b04d7-113">PARAMETERS</span></span>

### <span data-ttu-id="b04d7-114">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="b04d7-114">-CdnProfile</span></span>
<span data-ttu-id="b04d7-115">Azure CDN 프로필 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b04d7-115">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="b04d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b04d7-116">-DefaultProfile</span></span>
<span data-ttu-id="b04d7-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b04d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b04d7-118">-/Profile</span><span class="sxs-lookup"><span data-stu-id="b04d7-118">-ProfileName</span></span>
<span data-ttu-id="b04d7-119">프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b04d7-119">The name of the profile.</span></span>

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

### <span data-ttu-id="b04d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b04d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="b04d7-121">프로필이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b04d7-121">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="b04d7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b04d7-122">CommonParameters</span></span>
<span data-ttu-id="b04d7-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b04d7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b04d7-124">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b04d7-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b04d7-125">입력</span><span class="sxs-lookup"><span data-stu-id="b04d7-125">INPUTS</span></span>

### <span data-ttu-id="b04d7-126">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="b04d7-126">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="b04d7-127">출력</span><span class="sxs-lookup"><span data-stu-id="b04d7-127">OUTPUTS</span></span>

### <span data-ttu-id="b04d7-128">PSOptimizationType의. m m.</span><span class="sxs-lookup"><span data-stu-id="b04d7-128">Microsoft.Azure.Commands.Cdn.Models.Profile.PSOptimizationType</span></span>

## <span data-ttu-id="b04d7-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b04d7-129">NOTES</span></span>

## <span data-ttu-id="b04d7-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b04d7-130">RELATED LINKS</span></span>
