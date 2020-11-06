---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ab2cca2fc0b517d8923d117978887c6dd0196ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533912"
---
# <span data-ttu-id="05dff-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="05dff-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="05dff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05dff-102">SYNOPSIS</span></span>
<span data-ttu-id="05dff-103">두 네트워크 간에 ASR 네트워크 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05dff-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05dff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05dff-104">SYNTAX</span></span>

### <span data-ttu-id="05dff-105">EnterpriseToEnterprise (기본값)</span><span class="sxs-lookup"><span data-stu-id="05dff-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05dff-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="05dff-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05dff-107">설명은</span><span class="sxs-lookup"><span data-stu-id="05dff-107">DESCRIPTION</span></span>
<span data-ttu-id="05dff-108">**AzureRmRecoveryServicesAsrNetworkMapping** cmdlet은 두 네트워크 간에 asr 네트워크 매핑을 만드는 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 asr 작업의 asr 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="05dff-108">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="05dff-109">예제의</span><span class="sxs-lookup"><span data-stu-id="05dff-109">EXAMPLES</span></span>

### <span data-ttu-id="05dff-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="05dff-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="05dff-111">지정 된 이름, 기본 및 복구 네트워크를 사용 하 여 네트워크 매핑 만들기 작업을 시작 하 고 작업을 추적 하는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="05dff-111">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

## <span data-ttu-id="05dff-112">변수</span><span class="sxs-lookup"><span data-stu-id="05dff-112">PARAMETERS</span></span>

### <span data-ttu-id="05dff-113">-이름</span><span class="sxs-lookup"><span data-stu-id="05dff-113">-Name</span></span>
<span data-ttu-id="05dff-114">만들 ASR 네트워크 매핑의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05dff-114">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="05dff-115">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="05dff-115">-PrimaryNetwork</span></span>
<span data-ttu-id="05dff-116">네트워크 매핑에 대 한 기본 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05dff-116">Specifies the primary network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05dff-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="05dff-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="05dff-118">네트워크 매핑의 복구 azure 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05dff-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05dff-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="05dff-119">-RecoveryNetwork</span></span>
<span data-ttu-id="05dff-120">네트워크 매핑에 대 한 복구 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05dff-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05dff-121">-확인</span><span class="sxs-lookup"><span data-stu-id="05dff-121">-Confirm</span></span>
<span data-ttu-id="05dff-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05dff-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05dff-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05dff-123">-WhatIf</span></span>
<span data-ttu-id="05dff-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05dff-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="05dff-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05dff-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05dff-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05dff-126">CommonParameters</span></span>
<span data-ttu-id="05dff-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05dff-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05dff-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05dff-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05dff-129">입력</span><span class="sxs-lookup"><span data-stu-id="05dff-129">INPUTS</span></span>

### <span data-ttu-id="05dff-130">SiteRecovery. r m/. m g 네트워크</span><span class="sxs-lookup"><span data-stu-id="05dff-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="05dff-131">출력</span><span class="sxs-lookup"><span data-stu-id="05dff-131">OUTPUTS</span></span>

### <span data-ttu-id="05dff-132">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="05dff-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="05dff-133">상속자</span><span class="sxs-lookup"><span data-stu-id="05dff-133">NOTES</span></span>

## <span data-ttu-id="05dff-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05dff-134">RELATED LINKS</span></span>

[<span data-ttu-id="05dff-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="05dff-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="05dff-136">제거-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="05dff-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
