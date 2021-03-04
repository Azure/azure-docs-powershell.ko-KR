---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 8ad9ca87687acfdeb526dc33cdcb5a6ec70c65bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953419"
---
# <span data-ttu-id="1c9d8-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="1c9d8-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="1c9d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="1c9d8-103">Recovery Services 자격 증명 모음에서 ASR 저장소 분류 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="1c9d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="1c9d8-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c9d8-105">설명</span><span class="sxs-lookup"><span data-stu-id="1c9d8-105">DESCRIPTION</span></span>
<span data-ttu-id="1c9d8-106">**New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet은 Recovery Services 자격 증명 모음을 매핑하는 저장소 분류를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="1c9d8-107">예제</span><span class="sxs-lookup"><span data-stu-id="1c9d8-107">EXAMPLES</span></span>

### <span data-ttu-id="1c9d8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1c9d8-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="1c9d8-109">지정된 매개 변수로 저장소 분류 매핑 만들기 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1c9d8-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1c9d8-110">PARAMETERS</span></span>

### <span data-ttu-id="1c9d8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c9d8-111">-DefaultProfile</span></span>
<span data-ttu-id="1c9d8-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1c9d8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="1c9d8-113">-Name</span></span>
<span data-ttu-id="1c9d8-114">ASR 저장소 분류 매핑의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-114">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9d8-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="1c9d8-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="1c9d8-116">매핑에 대한 기본 ASR 저장소 분류 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="1c9d8-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="1c9d8-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="1c9d8-118">매핑에 대한 복구 ASR 저장소 분류 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c9d8-119">-확인</span><span class="sxs-lookup"><span data-stu-id="1c9d8-119">-Confirm</span></span>
<span data-ttu-id="1c9d8-120">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c9d8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c9d8-121">-WhatIf</span></span>
<span data-ttu-id="1c9d8-122">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1c9d8-123">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c9d8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c9d8-124">CommonParameters</span></span>
<span data-ttu-id="1c9d8-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1c9d8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c9d8-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1c9d8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c9d8-127">입력</span><span class="sxs-lookup"><span data-stu-id="1c9d8-127">INPUTS</span></span>

### <span data-ttu-id="1c9d8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="1c9d8-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="1c9d8-129">출력</span><span class="sxs-lookup"><span data-stu-id="1c9d8-129">OUTPUTS</span></span>

### <span data-ttu-id="1c9d8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="1c9d8-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1c9d8-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1c9d8-131">NOTES</span></span>

## <span data-ttu-id="1c9d8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1c9d8-132">RELATED LINKS</span></span>

[<span data-ttu-id="1c9d8-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="1c9d8-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="1c9d8-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="1c9d8-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
