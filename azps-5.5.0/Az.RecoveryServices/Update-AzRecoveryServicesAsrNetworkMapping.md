---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 09e6cbbbae30d1a2e43d8292573f4bf45d9db461
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189249"
---
# <span data-ttu-id="bbb67-101">Update-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bbb67-101">Update-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="bbb67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbb67-102">SYNOPSIS</span></span>
<span data-ttu-id="bbb67-103">지정된 Azure Site Recovery 네트워크 매핑을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bbb67-103">Updates the specified azure site recovery network mapping.</span></span>

## <span data-ttu-id="bbb67-104">구문</span><span class="sxs-lookup"><span data-stu-id="bbb67-104">SYNTAX</span></span>

### <span data-ttu-id="bbb67-105">ByNetworkObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="bbb67-105">ByNetworkObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbb67-106">ById</span><span class="sxs-lookup"><span data-stu-id="bbb67-106">ById</span></span>
```
Update-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryAzureNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbb67-107">설명</span><span class="sxs-lookup"><span data-stu-id="bbb67-107">DESCRIPTION</span></span>
<span data-ttu-id="bbb67-108">**Update-AzRecoveryServicesAsrNetworkMapping** cmdlet은 지정된 Azure Site Recovery 네트워크 매핑을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bbb67-108">The **Update-AzRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="bbb67-109">예제</span><span class="sxs-lookup"><span data-stu-id="bbb67-109">EXAMPLES</span></span>

### <span data-ttu-id="bbb67-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="bbb67-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="bbb67-111">지정된 매개 변수를 사용하여 네트워크 매핑 업데이트 작업을 시작하고 작업을 추적하는 데 사용되는 ASR 작업을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="bbb67-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bbb67-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bbb67-112">PARAMETERS</span></span>

### <span data-ttu-id="bbb67-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbb67-113">-DefaultProfile</span></span>
<span data-ttu-id="bbb67-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bbb67-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bbb67-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbb67-115">-InputObject</span></span>
<span data-ttu-id="bbb67-116">입력 개체: 업데이트할 ASR 네트워크 매핑에 해당하는 ASR 네트워크 매핑 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbb67-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

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

### <span data-ttu-id="bbb67-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="bbb67-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="bbb67-118">네트워크 매핑에 대한 복구 Azure 네트워크 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbb67-118">Specifies the recovery azure network ID for the network mapping.</span></span>

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

### <span data-ttu-id="bbb67-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="bbb67-119">-RecoveryNetwork</span></span>
<span data-ttu-id="bbb67-120">네트워크 매핑에 대한 복구 네트워크 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bbb67-120">Specifies the recovery network object for the network mapping.</span></span>

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

### <span data-ttu-id="bbb67-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bbb67-121">-Confirm</span></span>
<span data-ttu-id="bbb67-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bbb67-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbb67-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbb67-123">-WhatIf</span></span>
<span data-ttu-id="bbb67-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bbb67-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bbb67-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bbb67-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbb67-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbb67-126">CommonParameters</span></span>
<span data-ttu-id="bbb67-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bbb67-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbb67-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bbb67-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbb67-129">입력</span><span class="sxs-lookup"><span data-stu-id="bbb67-129">INPUTS</span></span>

### <span data-ttu-id="bbb67-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="bbb67-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="bbb67-131">출력</span><span class="sxs-lookup"><span data-stu-id="bbb67-131">OUTPUTS</span></span>

### <span data-ttu-id="bbb67-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="bbb67-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bbb67-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bbb67-133">NOTES</span></span>

## <span data-ttu-id="bbb67-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bbb67-134">RELATED LINKS</span></span>
