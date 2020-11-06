---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: ec5ba90fd0c3dbdbf96ddf2370948de090306611
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535688"
---
# <span data-ttu-id="294d5-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="294d5-101">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="294d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="294d5-102">SYNOPSIS</span></span>
<span data-ttu-id="294d5-103">ASR 저장소 분류 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="294d5-103">Gets ASR storage classification mappings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="294d5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="294d5-104">SYNTAX</span></span>

### <span data-ttu-id="294d5-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="294d5-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="294d5-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="294d5-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="294d5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="294d5-107">DESCRIPTION</span></span>
<span data-ttu-id="294d5-108">**AzureRmRecoveryServicesAsrStorageClassificationMapping** CMDLET은 ASR 저장소 분류 매핑의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="294d5-108">The **Get-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="294d5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="294d5-109">EXAMPLES</span></span>

### <span data-ttu-id="294d5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="294d5-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="294d5-111">지정 된 저장소 분류에 해당 하는 모든 저장소 분류 매핑을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="294d5-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="294d5-112">변수</span><span class="sxs-lookup"><span data-stu-id="294d5-112">PARAMETERS</span></span>

### <span data-ttu-id="294d5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="294d5-113">-DefaultProfile</span></span>
<span data-ttu-id="294d5-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="294d5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="294d5-115">-이름</span><span class="sxs-lookup"><span data-stu-id="294d5-115">-Name</span></span>
<span data-ttu-id="294d5-116">가져올 저장소 분류 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="294d5-116">Specifies the name of the storage classification mapping to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="294d5-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="294d5-117">-StorageClassification</span></span>
<span data-ttu-id="294d5-118">ASR 저장소 분류 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="294d5-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="294d5-119">Cmdlet은 지정 된 저장소 분류에 해당 하는 ASR 저장소 분류 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="294d5-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="294d5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="294d5-120">CommonParameters</span></span>
<span data-ttu-id="294d5-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="294d5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="294d5-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="294d5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="294d5-123">입력</span><span class="sxs-lookup"><span data-stu-id="294d5-123">INPUTS</span></span>

### <span data-ttu-id="294d5-124">않아야</span><span class="sxs-lookup"><span data-stu-id="294d5-124">None</span></span>

## <span data-ttu-id="294d5-125">출력</span><span class="sxs-lookup"><span data-stu-id="294d5-125">OUTPUTS</span></span>

### <span data-ttu-id="294d5-126">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASRStorageClassificationMapping, SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="294d5-126">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="294d5-127">상속자</span><span class="sxs-lookup"><span data-stu-id="294d5-127">NOTES</span></span>

## <span data-ttu-id="294d5-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="294d5-128">RELATED LINKS</span></span>

[<span data-ttu-id="294d5-129">새로운 AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="294d5-129">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="294d5-130">제거-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="294d5-130">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
