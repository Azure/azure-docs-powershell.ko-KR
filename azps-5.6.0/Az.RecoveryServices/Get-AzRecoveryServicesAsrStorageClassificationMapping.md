---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: c5dea86066fd2b7bc6bd3b2bd3eb7ac94f401895
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963808"
---
# <span data-ttu-id="f63dc-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f63dc-101">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="f63dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f63dc-102">SYNOPSIS</span></span>
<span data-ttu-id="f63dc-103">ASR 저장소 분류 매핑을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f63dc-103">Gets ASR storage classification mappings.</span></span>

## <span data-ttu-id="f63dc-104">구문</span><span class="sxs-lookup"><span data-stu-id="f63dc-104">SYNTAX</span></span>

### <span data-ttu-id="f63dc-105">ByObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="f63dc-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification <ASRStorageClassification>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f63dc-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="f63dc-106">ByObjectWithName</span></span>
```
Get-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -StorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f63dc-107">설명</span><span class="sxs-lookup"><span data-stu-id="f63dc-107">DESCRIPTION</span></span>
<span data-ttu-id="f63dc-108">**Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet은 ASR 저장소 분류 매핑에 대한 세부 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f63dc-108">The **Get-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet gets the details of an ASR storage classification mapping.</span></span>

## <span data-ttu-id="f63dc-109">예제</span><span class="sxs-lookup"><span data-stu-id="f63dc-109">EXAMPLES</span></span>

### <span data-ttu-id="f63dc-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f63dc-110">Example 1</span></span>
```
PS C:\> $StorageClassificationMappings = Get-AzRecoveryServicesAsrStorageClassificationMapping -StorageClassification $StorageClassification
```

<span data-ttu-id="f63dc-111">지정된 저장소 분류에 해당하는 모든 저장소 분류 매핑을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="f63dc-111">List all storage classification mappings corresponding to the specified storage classification.</span></span>

## <span data-ttu-id="f63dc-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f63dc-112">PARAMETERS</span></span>

### <span data-ttu-id="f63dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f63dc-113">-DefaultProfile</span></span>
<span data-ttu-id="f63dc-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f63dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f63dc-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f63dc-115">-Name</span></span>
<span data-ttu-id="f63dc-116">얻을 저장소 분류 매핑의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f63dc-116">Specifies the name of the storage classification mapping to get.</span></span>

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

### <span data-ttu-id="f63dc-117">-StorageClassification</span><span class="sxs-lookup"><span data-stu-id="f63dc-117">-StorageClassification</span></span>
<span data-ttu-id="f63dc-118">ASR 저장소 분류 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f63dc-118">Specifies an ASR storage classification object.</span></span> <span data-ttu-id="f63dc-119">cmdlet은 지정된 저장소 분류에 해당하는 ASR 저장소 분류 매핑을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f63dc-119">The cmdlet gets ASR storage classification mappings corresponding to the specified storage classification</span></span> 

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

### <span data-ttu-id="f63dc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f63dc-120">CommonParameters</span></span>
<span data-ttu-id="f63dc-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f63dc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f63dc-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f63dc-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f63dc-123">입력</span><span class="sxs-lookup"><span data-stu-id="f63dc-123">INPUTS</span></span>

### <span data-ttu-id="f63dc-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="f63dc-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="f63dc-125">출력</span><span class="sxs-lookup"><span data-stu-id="f63dc-125">OUTPUTS</span></span>

### <span data-ttu-id="f63dc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f63dc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="f63dc-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f63dc-127">NOTES</span></span>

## <span data-ttu-id="f63dc-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f63dc-128">RELATED LINKS</span></span>

[<span data-ttu-id="f63dc-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f63dc-129">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="f63dc-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="f63dc-130">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
