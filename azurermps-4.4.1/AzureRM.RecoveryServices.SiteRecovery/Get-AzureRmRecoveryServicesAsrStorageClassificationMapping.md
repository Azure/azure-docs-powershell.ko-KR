---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 5b15fdea68cc57d6f389fe43e81fb3f710736953
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703659"
---
# <span data-ttu-id="0e96f-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0e96f-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="0e96f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e96f-102">SYNOPSIS</span></span>
<span data-ttu-id="0e96f-103">ASR 저장소 분류 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e96f-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e96f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e96f-104">SYNTAX</span></span>

### <span data-ttu-id="0e96f-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e96f-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [<CommonParameters>]
```

### <span data-ttu-id="0e96f-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="0e96f-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [<CommonParameters>]
```

## <span data-ttu-id="0e96f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0e96f-107">DESCRIPTION</span></span>
<span data-ttu-id="0e96f-108">**AzureRmRecoveryServicesAsrStorageClassificationMapping** CMDLET은 ASR 저장소 분류 매핑의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e96f-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="0e96f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0e96f-109">EXAMPLES</span></span>

### <span data-ttu-id="0e96f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="0e96f-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="0e96f-111">지정 된 저장소 분류에 해당 하는 모든 저장소 분류 매핑을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e96f-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="0e96f-112">변수</span><span class="sxs-lookup"><span data-stu-id="0e96f-112">PARAMETERS</span></span>

### <span data-ttu-id="0e96f-113">-이름</span><span class="sxs-lookup"><span data-stu-id="0e96f-113">-Name</span></span>
<span data-ttu-id="0e96f-114">가져올 저장소 분류 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e96f-114">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="0e96f-115">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="0e96f-115">-StorageClassification</span></span>
<span data-ttu-id="0e96f-116">ASR 저장소 분류 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e96f-116">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="0e96f-117">Cmdlet은 지정 된 저장소 분류에 해당 하는 ASR 저장소 분류 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e96f-117">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0e96f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e96f-118">CommonParameters</span></span>
<span data-ttu-id="0e96f-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e96f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e96f-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e96f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e96f-121">입력</span><span class="sxs-lookup"><span data-stu-id="0e96f-121">INPUTS</span></span>

### <span data-ttu-id="0e96f-122">않아야</span><span class="sxs-lookup"><span data-stu-id="0e96f-122">None</span></span>

## <span data-ttu-id="0e96f-123">출력</span><span class="sxs-lookup"><span data-stu-id="0e96f-123">OUTPUTS</span></span>

### <span data-ttu-id="0e96f-124">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRStorageClassificationMapping, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="0e96f-124">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0e96f-125">상속자</span><span class="sxs-lookup"><span data-stu-id="0e96f-125">NOTES</span></span>

## <span data-ttu-id="0e96f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e96f-126">RELATED LINKS</span></span>

[<span data-ttu-id="0e96f-127">새로운 AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0e96f-127">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="0e96f-128">제거-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="0e96f-128">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
