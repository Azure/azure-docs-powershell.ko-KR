---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: e313b3dd9df76185c1eeaf289e918e1d47ace58d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702014"
---
# <span data-ttu-id="c6422-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c6422-101">New-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>

## <span data-ttu-id="c6422-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6422-102">SYNOPSIS</span></span>
<span data-ttu-id="c6422-103">복구 서비스 자격 증명 모음에 ASR 저장소 분류 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6422-103">Creates an ASR storage classification mapping in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6422-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6422-104">SYNTAX</span></span>

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6422-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c6422-105">DESCRIPTION</span></span>
<span data-ttu-id="c6422-106">**AzureRmRecoveryServicesAsrStorageClassificationMapping** Cmdlet은 복구 서비스 자격 증명 모음을 저장소 분류 매핑으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c6422-106">The **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** cmdlet creates a storage classification mapping the Recovery Services vault.</span></span>

## <span data-ttu-id="c6422-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c6422-107">EXAMPLES</span></span>

### <span data-ttu-id="c6422-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c6422-108">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

<span data-ttu-id="c6422-109">지정 된 매개 변수를 사용 하 여 저장소 분류 매핑 만들기 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6422-109">Starts the storage classification mapping creation operation with the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="c6422-110">변수</span><span class="sxs-lookup"><span data-stu-id="c6422-110">PARAMETERS</span></span>

### <span data-ttu-id="c6422-111">-확인</span><span class="sxs-lookup"><span data-stu-id="c6422-111">-Confirm</span></span>
<span data-ttu-id="c6422-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6422-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6422-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6422-113">-DefaultProfile</span></span>
<span data-ttu-id="c6422-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6422-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6422-115">-이름</span><span class="sxs-lookup"><span data-stu-id="c6422-115">-Name</span></span>
<span data-ttu-id="c6422-116">ASR 저장소 분류 매핑의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6422-116">Specifies a name for the ASR storage classification mapping.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6422-117">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c6422-117">-PrimaryStorageClassification</span></span>
<span data-ttu-id="c6422-118">매핑에 대 한 기본 ASR 저장소 분류 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6422-118">Specifies the primary ASR storage classification object for the mapping.</span></span>

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

### <span data-ttu-id="c6422-119">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="c6422-119">-RecoveryStorageClassification</span></span>
<span data-ttu-id="c6422-120">매핑에 대 한 복구 ASR 저장소 분류 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6422-120">Specifies the recovery ASR storage classification object for the mapping.</span></span>

```yaml
Type: ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6422-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6422-121">-WhatIf</span></span>
<span data-ttu-id="c6422-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c6422-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6422-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6422-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6422-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6422-124">CommonParameters</span></span>
<span data-ttu-id="c6422-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6422-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6422-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6422-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6422-127">입력</span><span class="sxs-lookup"><span data-stu-id="c6422-127">INPUTS</span></span>

### <span data-ttu-id="c6422-128">SiteRecovery. ASRStorageClassification에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="c6422-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification</span></span>

## <span data-ttu-id="c6422-129">출력</span><span class="sxs-lookup"><span data-stu-id="c6422-129">OUTPUTS</span></span>

### <span data-ttu-id="c6422-130">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="c6422-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c6422-131">상속자</span><span class="sxs-lookup"><span data-stu-id="c6422-131">NOTES</span></span>

## <span data-ttu-id="c6422-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6422-132">RELATED LINKS</span></span>

[<span data-ttu-id="c6422-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c6422-133">Get-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[<span data-ttu-id="c6422-134">제거-AzureRmRecoveryServicesAsrStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="c6422-134">Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
