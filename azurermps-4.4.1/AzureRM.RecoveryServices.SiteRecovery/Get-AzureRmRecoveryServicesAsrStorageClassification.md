---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassification.md
ms.openlocfilehash: d79a717fcf5d2422f86df4184d9c0344ebc32d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536215"
---
# <span data-ttu-id="a1498-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span><span class="sxs-lookup"><span data-stu-id="a1498-101">Get-AzureRmRecoveryServicesAsrStorageClassification</span></span>

## <span data-ttu-id="a1498-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1498-102">SYNOPSIS</span></span>
<span data-ttu-id="a1498-103">복구 서비스 자격 증명 모음에서 사용 가능한 (검색 된) ASR 저장소 분류를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1498-103">Gets the available(discovered) ASR storage classifications in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1498-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1498-104">SYNTAX</span></span>

### <span data-ttu-id="a1498-105">ByFabricObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="a1498-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="a1498-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a1498-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -Name <String> -Fabric <ASRFabric> [<CommonParameters>]
```

### <span data-ttu-id="a1498-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a1498-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassification -FriendlyName <String> -Fabric <ASRFabric>
 [<CommonParameters>]
```

## <span data-ttu-id="a1498-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a1498-108">DESCRIPTION</span></span>
<span data-ttu-id="a1498-109">**AzureRmRecoveryServicesAsrStorageClassification** Cmdlet은 복구 서비스 자격 증명 모음에 있는 검색 된 ASR 저장소 분류의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1498-109">The **Get-AzureRmRecoveryServicesAsrStorageClassification** cmdlet gets details of the discovered ASR storage classifications in the Recovery Services vault.</span></span>

## <span data-ttu-id="a1498-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a1498-110">EXAMPLES</span></span>

### <span data-ttu-id="a1498-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a1498-111">Example 1</span></span>
```
PS C:\> $StorageClassifications = Get-AzureRmRecoveryServicesAsrStorageClassification -Fabric $Fabric
```

<span data-ttu-id="a1498-112">지정 된 ASR 패브릭에 해당 하는 검색 된 저장소 분류를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1498-112">List the discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

## <span data-ttu-id="a1498-113">변수</span><span class="sxs-lookup"><span data-stu-id="a1498-113">PARAMETERS</span></span>

### <span data-ttu-id="a1498-114">-패브릭</span><span class="sxs-lookup"><span data-stu-id="a1498-114">-Fabric</span></span>
<span data-ttu-id="a1498-115">ASR fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1498-115">Specifies an ASR fabric object.</span></span> <span data-ttu-id="a1498-116">Cmdlet은 지정 된 ASR 패브릭에 해당 하는 검색 된 저장소 분류의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a1498-116">The cmdlet gets the details of discovered storage classifications corresponding to the specified ASR fabric.</span></span> 

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

### <span data-ttu-id="a1498-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a1498-117">-FriendlyName</span></span>
<span data-ttu-id="a1498-118">가져올 저장소 분류 개체의 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1498-118">Specifies the friendly name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="a1498-119">-이름</span><span class="sxs-lookup"><span data-stu-id="a1498-119">-Name</span></span>
<span data-ttu-id="a1498-120">가져올 저장소 분류 개체의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1498-120">Specifies the name of the storage classification object to get.</span></span>

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

### <span data-ttu-id="a1498-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1498-121">CommonParameters</span></span>
<span data-ttu-id="a1498-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1498-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1498-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1498-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1498-124">입력</span><span class="sxs-lookup"><span data-stu-id="a1498-124">INPUTS</span></span>

### <span data-ttu-id="a1498-125">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="a1498-125">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="a1498-126">출력</span><span class="sxs-lookup"><span data-stu-id="a1498-126">OUTPUTS</span></span>

### <span data-ttu-id="a1498-127">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRStorageClassification, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="a1498-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a1498-128">상속자</span><span class="sxs-lookup"><span data-stu-id="a1498-128">NOTES</span></span>

## <span data-ttu-id="a1498-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1498-129">RELATED LINKS</span></span>

