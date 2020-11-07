---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrServicesProvider.md
ms.openlocfilehash: 1d6199042cec106d81ba91ccb7ccb854741d319d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703660"
---
# <span data-ttu-id="59bbd-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="59bbd-101">Get-AzureRmRecoveryServicesAsrServicesProvider</span></span>

## <span data-ttu-id="59bbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59bbd-102">SYNOPSIS</span></span>
<span data-ttu-id="59bbd-103">복구 서비스 자격 증명 모음에 등록 된 ASR recovery services 공급자의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59bbd-103">Gets the details of the ASR recovery services providers registered to the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59bbd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59bbd-104">SYNTAX</span></span>

### <span data-ttu-id="59bbd-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="59bbd-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="59bbd-106">ByName</span><span class="sxs-lookup"><span data-stu-id="59bbd-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="59bbd-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="59bbd-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrServicesProvider -FriendlyName <String> -Fabric <ASRFabric> [<CommonParameters>]
```

## <span data-ttu-id="59bbd-108">설명은</span><span class="sxs-lookup"><span data-stu-id="59bbd-108">DESCRIPTION</span></span>
<span data-ttu-id="59bbd-109">**AzureRmRecoveryServicesAsrServicesProvider** cmdlet은 자격 증명 모음의 Azure Site Recovery 공급자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="59bbd-109">The **Get-AzureRmRecoveryServicesAsrServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="59bbd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="59bbd-110">EXAMPLES</span></span>

### <span data-ttu-id="59bbd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="59bbd-111">Example 1</span></span>
```
PS C:\> $RSPs = Get-AzureRmRecoveryServicesAsrFabric | Get-AzureRmRecoveryServicesAsrServicesProvider
```

<span data-ttu-id="59bbd-112">지정 된 패브릭에 해당 하는 복구 서비스 자격 증명 모음에 등록 된 모든 ASR 복제 서비스 공급자를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bbd-112">List all ASR replication services providers registered to the Recovery Services vault corresponding to the specified fabric.</span></span>

## <span data-ttu-id="59bbd-113">변수</span><span class="sxs-lookup"><span data-stu-id="59bbd-113">PARAMETERS</span></span>

### <span data-ttu-id="59bbd-114">-패브릭</span><span class="sxs-lookup"><span data-stu-id="59bbd-114">-Fabric</span></span>
<span data-ttu-id="59bbd-115">ASR fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bbd-115">Specifies the ASR fabric object.</span></span>

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

### <span data-ttu-id="59bbd-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="59bbd-116">-FriendlyName</span></span>
<span data-ttu-id="59bbd-117">세부 정보를 얻을 ASR recovery services 공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bbd-117">Specifies the friendly name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bbd-118">-이름</span><span class="sxs-lookup"><span data-stu-id="59bbd-118">-Name</span></span>
<span data-ttu-id="59bbd-119">세부 정보를 얻을 ASR recovery services 공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bbd-119">Specifies the name of the ASR recovery services provider to get details for.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bbd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bbd-120">CommonParameters</span></span>
<span data-ttu-id="59bbd-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59bbd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bbd-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59bbd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bbd-123">입력</span><span class="sxs-lookup"><span data-stu-id="59bbd-123">INPUTS</span></span>

### <span data-ttu-id="59bbd-124">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="59bbd-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="59bbd-125">출력</span><span class="sxs-lookup"><span data-stu-id="59bbd-125">OUTPUTS</span></span>

### <span data-ttu-id="59bbd-126">System.webserver. t e r ' 1 [[SiteRecovery Rrecovery서비스 공급자, Microsoft Azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]], "")</span><span class="sxs-lookup"><span data-stu-id="59bbd-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="59bbd-127">상속자</span><span class="sxs-lookup"><span data-stu-id="59bbd-127">NOTES</span></span>

## <span data-ttu-id="59bbd-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59bbd-128">RELATED LINKS</span></span>

[<span data-ttu-id="59bbd-129">제거-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="59bbd-129">Remove-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Remove-AzureRmRecoveryServicesAsrServicesProvider.md)

[<span data-ttu-id="59bbd-130">업데이트-AzureRmRecoveryServicesAsrServicesProvider</span><span class="sxs-lookup"><span data-stu-id="59bbd-130">Update-AzureRmRecoveryServicesAsrServicesProvider</span></span>](./Update-AzureRmRecoveryServicesAsrServicesProvider.md)
