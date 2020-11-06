---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.cdn/get-azurermcdnprofileresourceusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: 3d0f93a732739b94832a5e411580fb80958b27c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526263"
---
# <span data-ttu-id="7d1bc-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="7d1bc-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="7d1bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1bc-103">CDN 프로필의 리소스 사용 현황을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d1bc-103">Gets the resource usage of a CDN profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d1bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d1bc-104">SYNTAX</span></span>

### <span data-ttu-id="7d1bc-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7d1bc-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d1bc-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1bc-106">ByObjectParameterSet</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d1bc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7d1bc-107">DESCRIPTION</span></span>
<span data-ttu-id="7d1bc-108">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="7d1bc-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="7d1bc-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7d1bc-109">EXAMPLES</span></span>

### <span data-ttu-id="7d1bc-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d1bc-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7d1bc-111">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="7d1bc-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="7d1bc-112">변수</span><span class="sxs-lookup"><span data-stu-id="7d1bc-112">PARAMETERS</span></span>

### <span data-ttu-id="7d1bc-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="7d1bc-113">-CdnProfile</span></span>
<span data-ttu-id="7d1bc-114">Azure CDN 프로필 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1bc-114">The Azure CDN profile object.</span></span>

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

### <span data-ttu-id="7d1bc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1bc-115">-DefaultProfile</span></span>
<span data-ttu-id="7d1bc-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7d1bc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d1bc-117">-/Profile</span><span class="sxs-lookup"><span data-stu-id="7d1bc-117">-ProfileName</span></span>
<span data-ttu-id="7d1bc-118">프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1bc-118">The name of the profile.</span></span>

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

### <span data-ttu-id="7d1bc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1bc-119">-ResourceGroupName</span></span>
<span data-ttu-id="7d1bc-120">프로필이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="7d1bc-120">The resource group to which the profile belongs.</span></span>

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

### <span data-ttu-id="7d1bc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1bc-121">CommonParameters</span></span>
<span data-ttu-id="7d1bc-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d1bc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1bc-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d1bc-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1bc-124">입력</span><span class="sxs-lookup"><span data-stu-id="7d1bc-124">INPUTS</span></span>

### <span data-ttu-id="7d1bc-125">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="7d1bc-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>
<span data-ttu-id="7d1bc-126">매개 변수: CdnProfile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7d1bc-126">Parameters: CdnProfile (ByValue)</span></span>

## <span data-ttu-id="7d1bc-127">출력</span><span class="sxs-lookup"><span data-stu-id="7d1bc-127">OUTPUTS</span></span>

### <span data-ttu-id="7d1bc-128">Microsoft. Azure. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="7d1bc-128">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="7d1bc-129">상속자</span><span class="sxs-lookup"><span data-stu-id="7d1bc-129">NOTES</span></span>

## <span data-ttu-id="7d1bc-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d1bc-130">RELATED LINKS</span></span>
