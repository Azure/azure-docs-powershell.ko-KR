---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 84a50782e9906271e3943c8cd545780457a1adfe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537024"
---
# <span data-ttu-id="ea2f9-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="ea2f9-101">Get-AzureRmRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="ea2f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea2f9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea2f9-103">복구 서비스 자격 증명 모음에서 ASR 보호 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-103">Gets ASR protection containers in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea2f9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea2f9-104">SYNTAX</span></span>

### <span data-ttu-id="ea2f9-105">ByFabricObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea2f9-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="ea2f9-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="ea2f9-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="ea2f9-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ea2f9-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="ea2f9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ea2f9-108">DESCRIPTION</span></span>
<span data-ttu-id="ea2f9-109">**AzureRmRecoveryServicesAsrProtectionContainer** Cmdlet은 Recovery Services 자격 증명 모음에서 Azure Site Recovery 보호 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-109">The **Get-AzureRmRecoveryServicesAsrProtectionContainer** cmdlet gets Azure Site Recovery protection containers in the Recovery Services vault.</span></span>
<span data-ttu-id="ea2f9-110">보호 컨테이너는 가상 컴퓨터와 같은 보호 되는 (검색 된) 개체를 위한 논리적 컨테이너 이며,</span><span class="sxs-lookup"><span data-stu-id="ea2f9-110">A protection container is a logical container for protectable(discovered) and protected objects such as virtual machines.</span></span>
<span data-ttu-id="ea2f9-111">복제 정책은 보호 된 항목에 대 한 복제 설정을 정의 하 고 보호 컨테이너에 연결 하 고 보호 가능한 항목에 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-111">Replication policies define replication settings for protected items and can be associated with a protection container and applied to a protectable item.</span></span>

## <span data-ttu-id="ea2f9-112">예제의</span><span class="sxs-lookup"><span data-stu-id="ea2f9-112">EXAMPLES</span></span>

### <span data-ttu-id="ea2f9-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="ea2f9-113">Example 1</span></span>
```
PS C:\> $ProtectionContainers = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrProtectionContainer
```

<span data-ttu-id="ea2f9-114">지정 된 ASR 패브릭의 모든 ASR 보호 컨테이너 (위의 예제에서 파이프라인 입력)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-114">Gets all the ASR protection containers in the specified ASR fabric (the pipeline input in the above example.)</span></span>

## <span data-ttu-id="ea2f9-115">변수</span><span class="sxs-lookup"><span data-stu-id="ea2f9-115">PARAMETERS</span></span>

### <span data-ttu-id="ea2f9-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="ea2f9-116">-Fabric</span></span>
<span data-ttu-id="ea2f9-117">지정 된 ASR 패브릭에서 보호 컨테이너를 찾습니다.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-117">Look for the protection container in the specified ASR fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea2f9-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ea2f9-118">-FriendlyName</span></span>
<span data-ttu-id="ea2f9-119">찾을 ASR 보호 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-119">Specifies the friendly name of the ASR protection container to look for.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea2f9-120">-이름</span><span class="sxs-lookup"><span data-stu-id="ea2f9-120">-Name</span></span>
<span data-ttu-id="ea2f9-121">찾을 ASR 보호 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-121">Specifies the name of the ASR protection container to look for.</span></span>

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

### <span data-ttu-id="ea2f9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea2f9-122">CommonParameters</span></span>
<span data-ttu-id="ea2f9-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea2f9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea2f9-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea2f9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea2f9-125">입력</span><span class="sxs-lookup"><span data-stu-id="ea2f9-125">INPUTS</span></span>

### <span data-ttu-id="ea2f9-126">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="ea2f9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ea2f9-127">출력</span><span class="sxs-lookup"><span data-stu-id="ea2f9-127">OUTPUTS</span></span>

### <span data-ttu-id="ea2f9-128">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRProtectionContainer, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="ea2f9-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="ea2f9-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ea2f9-129">NOTES</span></span>

## <span data-ttu-id="ea2f9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea2f9-130">RELATED LINKS</span></span>

