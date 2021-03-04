---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnProfileResourceUsage.md
ms.openlocfilehash: 1a4e3f08653f6c7bda799b55618caff4e77fe7bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004587"
---
# <span data-ttu-id="e2cb0-101">Get-AzCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e2cb0-101">Get-AzCdnProfileResourceUsage</span></span>

## <span data-ttu-id="e2cb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2cb0-102">SYNOPSIS</span></span>
<span data-ttu-id="e2cb0-103">CDN 프로필의 리소스 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb0-103">Gets the resource usage of a CDN profile.</span></span>

## <span data-ttu-id="e2cb0-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2cb0-104">SYNTAX</span></span>

### <span data-ttu-id="e2cb0-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e2cb0-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2cb0-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2cb0-106">ByObjectParameterSet</span></span>
```
Get-AzCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2cb0-107">설명</span><span class="sxs-lookup"><span data-stu-id="e2cb0-107">DESCRIPTION</span></span>
<span data-ttu-id="e2cb0-108">{{Description}} 채우기}</span><span class="sxs-lookup"><span data-stu-id="e2cb0-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="e2cb0-109">예제</span><span class="sxs-lookup"><span data-stu-id="e2cb0-109">EXAMPLES</span></span>

### <span data-ttu-id="e2cb0-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2cb0-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="e2cb0-111">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="e2cb0-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="e2cb0-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e2cb0-112">PARAMETERS</span></span>

### <span data-ttu-id="e2cb0-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="e2cb0-113">-CdnProfile</span></span>
<span data-ttu-id="e2cb0-114">Azure CDN 프로필 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb0-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="e2cb0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2cb0-115">-DefaultProfile</span></span>
<span data-ttu-id="e2cb0-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e2cb0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2cb0-117">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="e2cb0-117">-ProfileName</span></span>
<span data-ttu-id="e2cb0-118">프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb0-118">The name of the profile.</span></span>

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

### <span data-ttu-id="e2cb0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2cb0-119">-ResourceGroupName</span></span>
<span data-ttu-id="e2cb0-120">프로필이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb0-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="e2cb0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2cb0-121">CommonParameters</span></span>
<span data-ttu-id="e2cb0-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2cb0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2cb0-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2cb0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2cb0-124">입력</span><span class="sxs-lookup"><span data-stu-id="e2cb0-124">INPUTS</span></span>

### <span data-ttu-id="e2cb0-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span><span class="sxs-lookup"><span data-stu-id="e2cb0-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="e2cb0-126">출력</span><span class="sxs-lookup"><span data-stu-id="e2cb0-126">OUTPUTS</span></span>

### <span data-ttu-id="e2cb0-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="e2cb0-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="e2cb0-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2cb0-128">NOTES</span></span>

## <span data-ttu-id="e2cb0-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2cb0-129">RELATED LINKS</span></span>
