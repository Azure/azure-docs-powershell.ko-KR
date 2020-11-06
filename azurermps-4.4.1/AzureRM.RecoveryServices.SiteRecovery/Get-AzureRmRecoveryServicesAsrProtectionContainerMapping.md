---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 06dca346610af2f5ba54eef1c509d18a3465f34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536219"
---
# <span data-ttu-id="2bdd9-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2bdd9-101">Get-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>

## <span data-ttu-id="2bdd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bdd9-102">SYNOPSIS</span></span>
<span data-ttu-id="2bdd9-103">Azure Site Recovery 보호 컨테이너 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bdd9-103">Gets Azure Site Recovery Protection Container mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2bdd9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2bdd9-104">SYNTAX</span></span>

### <span data-ttu-id="2bdd9-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="2bdd9-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer <ASRProtectionContainer>
 [<CommonParameters>]
```

### <span data-ttu-id="2bdd9-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="2bdd9-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -Name <String>
 -ProtectionContainer <ASRProtectionContainer> [<CommonParameters>]
```

## <span data-ttu-id="2bdd9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="2bdd9-107">DESCRIPTION</span></span>
<span data-ttu-id="2bdd9-108">**AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet은 지정 된 ASR 보호 컨테이너에 대 한 자격 증명 모음의 복제 정책 매핑 (연결)에 대 한 보호 컨테이너에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bdd9-108">The **Get-AzureRmRecoveryServicesAsrProtectionContainerMapping** cmdlet gets information about the protection container to replication policy mappings(association) in the vault for the specified ASR protection container.</span></span>

## <span data-ttu-id="2bdd9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="2bdd9-109">EXAMPLES</span></span>

### <span data-ttu-id="2bdd9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2bdd9-110">Example 1</span></span>
```
PS C:\> $ProtectionContainerMappings = Get-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainer $Container
```

<span data-ttu-id="2bdd9-111">지정 된 보호 컨테이너에 대 한 모든 보호 컨테이너 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bdd9-111">Gets all protection container mappings for the specified protection container.</span></span>

## <span data-ttu-id="2bdd9-112">변수</span><span class="sxs-lookup"><span data-stu-id="2bdd9-112">PARAMETERS</span></span>

### <span data-ttu-id="2bdd9-113">-이름</span><span class="sxs-lookup"><span data-stu-id="2bdd9-113">-Name</span></span>
<span data-ttu-id="2bdd9-114">가져올 보호 컨테이너 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bdd9-114">Specifies the name of the protection container mapping to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2bdd9-115">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="2bdd9-115">-ProtectionContainer</span></span>
<span data-ttu-id="2bdd9-116">지정 된 ASR protection 컨테이너 개체에 해당 하는 보호 컨테이너 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2bdd9-116">Get protection container mappings corresponding to the specified ASR protection container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2bdd9-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bdd9-117">CommonParameters</span></span>
<span data-ttu-id="2bdd9-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2bdd9-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bdd9-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2bdd9-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bdd9-120">입력</span><span class="sxs-lookup"><span data-stu-id="2bdd9-120">INPUTS</span></span>

### <span data-ttu-id="2bdd9-121">SiteRecovery. ASRProtectionContainer에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="2bdd9-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="2bdd9-122">출력</span><span class="sxs-lookup"><span data-stu-id="2bdd9-122">OUTPUTS</span></span>

### <span data-ttu-id="2bdd9-123">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRProtectionContainerMapping, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="2bdd9-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainerMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="2bdd9-124">상속자</span><span class="sxs-lookup"><span data-stu-id="2bdd9-124">NOTES</span></span>

## <span data-ttu-id="2bdd9-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2bdd9-125">RELATED LINKS</span></span>

[<span data-ttu-id="2bdd9-126">새로운 AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2bdd9-126">New-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[<span data-ttu-id="2bdd9-127">제거-AzureRmRecoveryServicesAsrProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="2bdd9-127">Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
