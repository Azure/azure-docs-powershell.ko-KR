---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e38a7b30622b8bb5dcbcf6912db7212465026687
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034067"
---
# <span data-ttu-id="a4f2d-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="a4f2d-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="a4f2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4f2d-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f2d-103">ASR 저장소 분류 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="a4f2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4f2d-104">SYNTAX</span></span>

### <span data-ttu-id="a4f2d-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="a4f2d-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4f2d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a4f2d-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4f2d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a4f2d-107">DESCRIPTION</span></span>
<span data-ttu-id="a4f2d-108">**AzRecoveryServicesAsrStorageClassificationMapping** CMDLET은 ASR 저장소 분류 매핑의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="a4f2d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a4f2d-109">EXAMPLES</span></span>

### <span data-ttu-id="a4f2d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="a4f2d-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="a4f2d-111">지정 된 저장소 분류에 해당 하는 모든 저장소 분류 매핑을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="a4f2d-112">변수</span><span class="sxs-lookup"><span data-stu-id="a4f2d-112">PARAMETERS</span></span>

### <span data-ttu-id="a4f2d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f2d-113">-DefaultProfile</span></span>
<span data-ttu-id="a4f2d-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="a4f2d-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a4f2d-115">-Name</span></span>
<span data-ttu-id="a4f2d-116">가져올 저장소 분류 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="a4f2d-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="a4f2d-117">-StorageClassification</span></span>
<span data-ttu-id="a4f2d-118">ASR 저장소 분류 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="a4f2d-119">Cmdlet은 지정 된 저장소 분류에 해당 하는 ASR 저장소 분류 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="a4f2d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f2d-120">CommonParameters</span></span>
<span data-ttu-id="a4f2d-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f2d-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a4f2d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f2d-123">입력</span><span class="sxs-lookup"><span data-stu-id="a4f2d-123">INPUTS</span></span>

### <span data-ttu-id="a4f2d-124">SiteRecovery. ASRStorageClassification에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="a4f2d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="a4f2d-125">출력</span><span class="sxs-lookup"><span data-stu-id="a4f2d-125">OUTPUTS</span></span>

### <span data-ttu-id="a4f2d-126">SiteRecovery. ASRStorageClassificationMapping에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="a4f2d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="a4f2d-127">상속자</span><span class="sxs-lookup"><span data-stu-id="a4f2d-127">NOTES</span></span>

## <span data-ttu-id="a4f2d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4f2d-128">RELATED LINKS</span></span>

[<span data-ttu-id="a4f2d-129">새로운 AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="a4f2d-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="a4f2d-130">제거-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="a4f2d-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
