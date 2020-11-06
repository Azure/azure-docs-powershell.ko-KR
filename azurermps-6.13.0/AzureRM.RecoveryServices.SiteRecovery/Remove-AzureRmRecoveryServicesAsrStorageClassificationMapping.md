---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: bafa671431c617807fa28e2d4fbfed57236fc6a7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530117"
---
# <span data-ttu-id="e5f9d-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e5f9d-101">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="e5f9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="e5f9d-103">지정 된 ASR 저장소 분류 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f9d-103">Deletes the specified ASR storage classification mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5f9d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5f9d-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -InputObject <ASRStorageClassificationMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5f9d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e5f9d-105">DESCRIPTION</span></span>
<span data-ttu-id="e5f9d-106">**AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet은 지정 된 Azure Site Recovery 저장소 분류 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f9d-106">The **Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet deletes the specified Azure Site Recovery storage classification mapping.</span></span>

## <span data-ttu-id="e5f9d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e5f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="e5f9d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5f9d-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping -StorageClassificationMapping $StorageClassificationMapping
```

<span data-ttu-id="e5f9d-109">지정 된 저장소 분류 매핑의 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f9d-109">Starts the deletion of specified storage classification mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e5f9d-110">변수</span><span class="sxs-lookup"><span data-stu-id="e5f9d-110">PARAMETERS</span></span>

### <span data-ttu-id="e5f9d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5f9d-111">-DefaultProfile</span></span>
<span data-ttu-id="e5f9d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f9d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="e5f9d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e5f9d-113">-InputObject</span></span>
<span data-ttu-id="e5f9d-114">Cmdlet에 대 한 입력 개체: 삭제 될 ASR 저장소 분류 매핑에 해당 하는 ASR 저장소 분류 매핑 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e5f9d-114">The input object to the cmdlet: The ASR storage classification mapping object corresponding to the ASR storage classification mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: StorageClassificationMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e5f9d-115">-확인</span><span class="sxs-lookup"><span data-stu-id="e5f9d-115">-Confirm</span></span>
<span data-ttu-id="e5f9d-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f9d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f9d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5f9d-117">-WhatIf</span></span>
<span data-ttu-id="e5f9d-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5f9d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5f9d-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5f9d-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5f9d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5f9d-120">CommonParameters</span></span>
<span data-ttu-id="e5f9d-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5f9d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5f9d-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5f9d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5f9d-123">입력</span><span class="sxs-lookup"><span data-stu-id="e5f9d-123">INPUTS</span></span>

### <span data-ttu-id="e5f9d-124">SiteRecovery. ASRStorageClassificationMapping에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="e5f9d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassificationMapping</span></span>

## <span data-ttu-id="e5f9d-125">출력</span><span class="sxs-lookup"><span data-stu-id="e5f9d-125">OUTPUTS</span></span>

### <span data-ttu-id="e5f9d-126">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="e5f9d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e5f9d-127">상속자</span><span class="sxs-lookup"><span data-stu-id="e5f9d-127">NOTES</span></span>

## <span data-ttu-id="e5f9d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5f9d-128">RELATED LINKS</span></span>

[<span data-ttu-id="e5f9d-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e5f9d-129">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="e5f9d-130">새로운 AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="e5f9d-130">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)