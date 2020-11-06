---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dd17eef73ab07d662a10177ffb68776aa4ec6016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533900"
---
# <span data-ttu-id="e08c4-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="e08c4-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="e08c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e08c4-102">SYNOPSIS</span></span>
<span data-ttu-id="e08c4-103">지정 된 ASR 네트워크 매핑을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08c4-103">Updates the specified ASR network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e08c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e08c4-104">SYNTAX</span></span>

### <span data-ttu-id="e08c4-105">ByNetworkObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="e08c4-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e08c4-106">ById</span><span class="sxs-lookup"><span data-stu-id="e08c4-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e08c4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e08c4-107">DESCRIPTION</span></span>
<span data-ttu-id="e08c4-108">**업데이트 AzureRmRecoveryServicesAsrNetworkMapping** cmdlet은 지정 된 Azure Site Recovery 네트워크 매핑을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08c4-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="e08c4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e08c4-109">EXAMPLES</span></span>

### <span data-ttu-id="e08c4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e08c4-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="e08c4-111">지정 된 매개 변수를 사용 하 여 네트워크 매핑 업데이트 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08c4-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e08c4-112">변수</span><span class="sxs-lookup"><span data-stu-id="e08c4-112">PARAMETERS</span></span>

### <span data-ttu-id="e08c4-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e08c4-113">-InputObject</span></span>
<span data-ttu-id="e08c4-114">입력 개체: 업데이트 될 ASR 네트워크 매핑에 해당 하는 ASR 네트워크 매핑 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08c4-114">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated</span></span> 

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

### <span data-ttu-id="e08c4-115">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="e08c4-115">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="e08c4-116">네트워크 매핑의 복구 azure 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08c4-116">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08c4-117">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="e08c4-117">-RecoveryNetwork</span></span>
<span data-ttu-id="e08c4-118">네트워크 매핑에 대 한 복구 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08c4-118">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e08c4-119">-확인</span><span class="sxs-lookup"><span data-stu-id="e08c4-119">-Confirm</span></span>
<span data-ttu-id="e08c4-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08c4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e08c4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e08c4-121">-WhatIf</span></span>
<span data-ttu-id="e08c4-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e08c4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e08c4-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e08c4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e08c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e08c4-124">CommonParameters</span></span>
<span data-ttu-id="e08c4-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e08c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e08c4-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e08c4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e08c4-127">입력</span><span class="sxs-lookup"><span data-stu-id="e08c4-127">INPUTS</span></span>

### <span data-ttu-id="e08c4-128">않아야</span><span class="sxs-lookup"><span data-stu-id="e08c4-128">None</span></span>

## <span data-ttu-id="e08c4-129">출력</span><span class="sxs-lookup"><span data-stu-id="e08c4-129">OUTPUTS</span></span>

### <span data-ttu-id="e08c4-130">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="e08c4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e08c4-131">상속자</span><span class="sxs-lookup"><span data-stu-id="e08c4-131">NOTES</span></span>

## <span data-ttu-id="e08c4-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e08c4-132">RELATED LINKS</span></span>

