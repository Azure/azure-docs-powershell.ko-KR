---
external help file: Microsoft.Azure.Commands.Cdn.dll-Help.xml
Module Name: AzureRM.Cdn
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Cdn/Commands.Cdn/help/Get-AzureRmCdnProfileResourceUsage.md
ms.openlocfilehash: f8b85088ac05cb118cf443eb54f28508727bd335
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537872"
---
# <span data-ttu-id="05b13-101">Get-AzureRmCdnProfileResourceUsage</span><span class="sxs-lookup"><span data-stu-id="05b13-101">Get-AzureRmCdnProfileResourceUsage</span></span>

## <span data-ttu-id="05b13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05b13-102">SYNOPSIS</span></span>
<span data-ttu-id="05b13-103">{{Synopsis 채우기}}</span><span class="sxs-lookup"><span data-stu-id="05b13-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05b13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05b13-104">SYNTAX</span></span>

### <span data-ttu-id="05b13-105">필드 매개 변수에 대해 설정 되는 매개 변수 (기본값)</span><span class="sxs-lookup"><span data-stu-id="05b13-105">Parameter Set for fields parameters (Default)</span></span>
```
Get-AzureRmCdnProfileResourceUsage -ProfileName <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="05b13-106">개체 매개 변수에 대해 설정 되는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="05b13-106">Parameter Set for object parameters</span></span>
```
Get-AzureRmCdnProfileResourceUsage -CdnProfile <PSProfile> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05b13-107">설명은</span><span class="sxs-lookup"><span data-stu-id="05b13-107">DESCRIPTION</span></span>
<span data-ttu-id="05b13-108">{{설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="05b13-108">{{Fill in the Description}}</span></span>

## <span data-ttu-id="05b13-109">예제의</span><span class="sxs-lookup"><span data-stu-id="05b13-109">EXAMPLES</span></span>

### <span data-ttu-id="05b13-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="05b13-110">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="05b13-111">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="05b13-111">{{ Add example description here }}</span></span>

## <span data-ttu-id="05b13-112">변수</span><span class="sxs-lookup"><span data-stu-id="05b13-112">PARAMETERS</span></span>

### <span data-ttu-id="05b13-113">-CdnProfile</span><span class="sxs-lookup"><span data-stu-id="05b13-113">-CdnProfile</span></span>
<span data-ttu-id="05b13-114">Azure CDN 프로필 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="05b13-114">The Azure CDN profile object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile
Parameter Sets: Parameter Set for object parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05b13-115">-/Profile</span><span class="sxs-lookup"><span data-stu-id="05b13-115">-ProfileName</span></span>
<span data-ttu-id="05b13-116">프로필의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05b13-116">The name of the profile.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b13-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05b13-117">-ResourceGroupName</span></span>
<span data-ttu-id="05b13-118">프로필이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="05b13-118">The resource group to which the profile belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameter Set for fields parameters
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05b13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b13-119">-DefaultProfile</span></span>
<span data-ttu-id="05b13-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05b13-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05b13-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b13-121">CommonParameters</span></span>
<span data-ttu-id="05b13-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05b13-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b13-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05b13-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b13-124">입력</span><span class="sxs-lookup"><span data-stu-id="05b13-124">INPUTS</span></span>

### <span data-ttu-id="05b13-125">Microsoft. Cdn. 프로필. PSProfile</span><span class="sxs-lookup"><span data-stu-id="05b13-125">Microsoft.Azure.Commands.Cdn.Models.Profile.PSProfile</span></span>

## <span data-ttu-id="05b13-126">출력</span><span class="sxs-lookup"><span data-stu-id="05b13-126">OUTPUTS</span></span>

### <span data-ttu-id="05b13-127">Microsoft. Azure. PSResourceUsage</span><span class="sxs-lookup"><span data-stu-id="05b13-127">Microsoft.Azure.Commands.Cdn.Models.PSResourceUsage</span></span>

## <span data-ttu-id="05b13-128">상속자</span><span class="sxs-lookup"><span data-stu-id="05b13-128">NOTES</span></span>

## <span data-ttu-id="05b13-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05b13-129">RELATED LINKS</span></span>

