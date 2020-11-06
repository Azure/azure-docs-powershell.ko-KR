---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 13c2f20f6d8ef7823244c62cfbe97e4b3a25eb73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529194"
---
# <span data-ttu-id="31a13-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="31a13-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="31a13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31a13-102">SYNOPSIS</span></span>
<span data-ttu-id="31a13-103">복구 서비스 자격 증명 모음에서 지정 된 ASR 네트워크 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="31a13-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31a13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31a13-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="31a13-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31a13-105">DESCRIPTION</span></span>
<span data-ttu-id="31a13-106">**AzureRmRecoveryServicesAsrNetworkMapping** cmdlet은 지정 된 ASR 네트워크 매핑을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="31a13-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="31a13-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31a13-107">EXAMPLES</span></span>

### <span data-ttu-id="31a13-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="31a13-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="31a13-109">지정 된 ASR 네트워크 매핑 삭제를 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="31a13-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="31a13-110">변수</span><span class="sxs-lookup"><span data-stu-id="31a13-110">PARAMETERS</span></span>

### <span data-ttu-id="31a13-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31a13-111">-InputObject</span></span>
<span data-ttu-id="31a13-112">Cmdlet에 대 한 입력 개체: 삭제할 ASR 네트워크 매핑에 해당 하는 ASR 네트워크 매핑 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="31a13-112">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31a13-113">-확인</span><span class="sxs-lookup"><span data-stu-id="31a13-113">-Confirm</span></span>
<span data-ttu-id="31a13-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="31a13-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31a13-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31a13-115">-WhatIf</span></span>
<span data-ttu-id="31a13-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="31a13-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="31a13-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="31a13-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31a13-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31a13-118">CommonParameters</span></span>
<span data-ttu-id="31a13-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31a13-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31a13-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31a13-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31a13-121">입력</span><span class="sxs-lookup"><span data-stu-id="31a13-121">INPUTS</span></span>

### <span data-ttu-id="31a13-122">SiteRecovery. r m g Networkmapping 매핑</span><span class="sxs-lookup"><span data-stu-id="31a13-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="31a13-123">출력</span><span class="sxs-lookup"><span data-stu-id="31a13-123">OUTPUTS</span></span>

### <span data-ttu-id="31a13-124">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="31a13-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="31a13-125">상속자</span><span class="sxs-lookup"><span data-stu-id="31a13-125">NOTES</span></span>

## <span data-ttu-id="31a13-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31a13-126">RELATED LINKS</span></span>

[<span data-ttu-id="31a13-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="31a13-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="31a13-128">새로운 AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="31a13-128">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
