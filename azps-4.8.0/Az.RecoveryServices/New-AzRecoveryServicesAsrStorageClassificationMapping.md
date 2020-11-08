---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/new-azrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/New-AzRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 091f8892238d88554d0e0c3502ffbeb8e8d4c154
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214265"
---
# <span data-ttu-id="c5947-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c5947-101">New-AzRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="c5947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5947-102">SYNOPSIS</span></span>
<span data-ttu-id="c5947-103">복구 서비스 자격 증명 모음에 ASR 저장소 분류 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5947-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

## <span data-ttu-id="c5947-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c5947-104">SYNTAX</span></span>

```
New-AzRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5947-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c5947-105">DESCRIPTION</span></span>
<span data-ttu-id="c5947-106">**AzRecoveryServicesAsrStorageClassificationMapping** Cmdlet은 복구 서비스 자격 증명 모음을 저장소 분류 매핑으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c5947-106">The **New-AzRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="c5947-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c5947-107">EXAMPLES</span></span>

### <span data-ttu-id="c5947-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c5947-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzRecoveryServicesAsrStorageClassificationMapping -Name $StorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="c5947-109">지정 된 매개 변수를 사용 하 여 저장소 분류 매핑 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5947-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c5947-110">변수</span><span class="sxs-lookup"><span data-stu-id="c5947-110">PARAMETERS</span></span>

### <span data-ttu-id="c5947-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5947-111">-DefaultProfile</span></span>
<span data-ttu-id="c5947-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5947-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="c5947-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c5947-113">-Name</span></span>
<span data-ttu-id="c5947-114">ASR 저장소 분류 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5947-114">Specifies a name for the ASR storage classification mapping.</span></span>

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

### <span data-ttu-id="c5947-115">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c5947-115">-PrimaryStorageClassification</span></span>
<span data-ttu-id="c5947-116">매핑에 대 한 기본 ASR 저장소 분류 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5947-116">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="c5947-117">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c5947-117">-RecoveryStorageClassification</span></span>
<span data-ttu-id="c5947-118">매핑에 대 한 복구 ASR 저장소 분류 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5947-118">Specifies the recovery ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="c5947-119">-확인</span><span class="sxs-lookup"><span data-stu-id="c5947-119">-Confirm</span></span>
<span data-ttu-id="c5947-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5947-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5947-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5947-121">-WhatIf</span></span>
<span data-ttu-id="c5947-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5947-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5947-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5947-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5947-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5947-124">CommonParameters</span></span>
<span data-ttu-id="c5947-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c5947-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5947-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c5947-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5947-127">입력</span><span class="sxs-lookup"><span data-stu-id="c5947-127">INPUTS</span></span>

### <span data-ttu-id="c5947-128">SiteRecovery. ASRStorageClassification에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="c5947-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="c5947-129">출력</span><span class="sxs-lookup"><span data-stu-id="c5947-129">OUTPUTS</span></span>

### <span data-ttu-id="c5947-130">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="c5947-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c5947-131">상속자</span><span class="sxs-lookup"><span data-stu-id="c5947-131">NOTES</span></span>

## <span data-ttu-id="c5947-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5947-132">RELATED LINKS</span></span>

[<span data-ttu-id="c5947-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c5947-133">Get-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="c5947-134">제거-AzRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c5947-134">Remove-AzRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzRecoveryServicesAsrStorageClassificationMapping.md)
