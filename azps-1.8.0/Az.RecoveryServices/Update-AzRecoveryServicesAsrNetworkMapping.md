---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 32412127388e233af303cc29de8ecf66304a0bf3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699579"
---
# <span data-ttu-id="91faa-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="91faa-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="91faa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91faa-102">SYNOPSIS</span></span>
<span data-ttu-id="91faa-103">지정 된 azure site recovery 네트워크 매핑을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="91faa-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="91faa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91faa-104">SYNTAX</span></span>

### <span data-ttu-id="91faa-105">ByNetworkObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="91faa-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91faa-106">ById</span><span class="sxs-lookup"><span data-stu-id="91faa-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91faa-107">설명은</span><span class="sxs-lookup"><span data-stu-id="91faa-107">DESCRIPTION</span></span>
<span data-ttu-id="91faa-108">**업데이트 AzRecoveryServicesAsrNetworkMapping** cmdlet은 지정 된 Azure Site Recovery 네트워크 매핑을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="91faa-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="91faa-109">예제의</span><span class="sxs-lookup"><span data-stu-id="91faa-109">EXAMPLES</span></span>

### <span data-ttu-id="91faa-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="91faa-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="91faa-111">지정 된 매개 변수를 사용 하 여 네트워크 매핑 업데이트 작업을 시작 하 고 작업을 추적 하는 데 사용 되는 ASR 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="91faa-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="91faa-112">변수</span><span class="sxs-lookup"><span data-stu-id="91faa-112">PARAMETERS</span></span>

### <span data-ttu-id="91faa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91faa-113">-DefaultProfile</span></span>
<span data-ttu-id="91faa-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="91faa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="91faa-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="91faa-115">-InputObject</span></span>
<span data-ttu-id="91faa-116">입력 개체: 업데이트 될 ASR 네트워크 매핑에 해당 하는 ASR 네트워크 매핑 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91faa-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="91faa-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="91faa-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="91faa-118">네트워크 매핑의 복구 azure 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91faa-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91faa-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="91faa-119">-RecoveryNetwork</span></span>
<span data-ttu-id="91faa-120">네트워크 매핑에 대 한 복구 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91faa-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="91faa-121">-확인</span><span class="sxs-lookup"><span data-stu-id="91faa-121">-Confirm</span></span>
<span data-ttu-id="91faa-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="91faa-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91faa-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91faa-123">-WhatIf</span></span>
<span data-ttu-id="91faa-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="91faa-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="91faa-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="91faa-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91faa-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91faa-126">CommonParameters</span></span>
<span data-ttu-id="91faa-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91faa-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91faa-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91faa-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91faa-129">입력</span><span class="sxs-lookup"><span data-stu-id="91faa-129">INPUTS</span></span>

### <span data-ttu-id="91faa-130">SiteRecovery. r m g Networkmapping 매핑</span><span class="sxs-lookup"><span data-stu-id="91faa-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="91faa-131">출력</span><span class="sxs-lookup"><span data-stu-id="91faa-131">OUTPUTS</span></span>

### <span data-ttu-id="91faa-132">SiteRecovery. r i m m 작업</span><span class="sxs-lookup"><span data-stu-id="91faa-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="91faa-133">상속자</span><span class="sxs-lookup"><span data-stu-id="91faa-133">NOTES</span></span>

## <span data-ttu-id="91faa-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91faa-134">RELATED LINKS</span></span>
