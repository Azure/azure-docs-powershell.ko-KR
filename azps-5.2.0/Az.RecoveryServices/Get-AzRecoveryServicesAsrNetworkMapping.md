---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364764"
---
# <span data-ttu-id="3883d-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3883d-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="3883d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3883d-102">SYNOPSIS</span></span>
<span data-ttu-id="3883d-103">현재 자격 증명 모음에 대한 Site Recovery 네트워크 매핑에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3883d-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="3883d-104">구문</span><span class="sxs-lookup"><span data-stu-id="3883d-104">SYNTAX</span></span>

### <span data-ttu-id="3883d-105">ByObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="3883d-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3883d-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="3883d-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3883d-107">설명</span><span class="sxs-lookup"><span data-stu-id="3883d-107">DESCRIPTION</span></span>
<span data-ttu-id="3883d-108">**Get-AzRecoveryServicesAsrNetworkMapping** cmdlet은 Recovery Services 자격 증명 모음에 대한 Azure Site Recovery 네트워크 매핑에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3883d-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="3883d-109">예제</span><span class="sxs-lookup"><span data-stu-id="3883d-109">EXAMPLES</span></span>

### <span data-ttu-id="3883d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3883d-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="3883d-111">전달된 네트워크에 대한 모든 네트워크 매핑을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3883d-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="3883d-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="3883d-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="3883d-113">지정된 Azure Site Recovery 패브릭에서 제공된 이름으로 네트워크 매핑을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3883d-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="3883d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3883d-114">PARAMETERS</span></span>

### <span data-ttu-id="3883d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3883d-115">-DefaultProfile</span></span>
<span data-ttu-id="3883d-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3883d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="3883d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3883d-117">-Name</span></span>
<span data-ttu-id="3883d-118">얻을 ASR 네트워크 매핑 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3883d-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3883d-119">-Network</span><span class="sxs-lookup"><span data-stu-id="3883d-119">-Network</span></span>
<span data-ttu-id="3883d-120">지정된 네트워크 ASR 개체에 해당하는 ASR 네트워크 매핑을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3883d-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3883d-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="3883d-121">-PrimaryFabric</span></span>
<span data-ttu-id="3883d-122">지정된 주 패브릭 개체에 해당하는 ASR 네트워크 매핑을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3883d-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3883d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3883d-123">CommonParameters</span></span>
<span data-ttu-id="3883d-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3883d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3883d-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3883d-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3883d-126">입력</span><span class="sxs-lookup"><span data-stu-id="3883d-126">INPUTS</span></span>

### <span data-ttu-id="3883d-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="3883d-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="3883d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="3883d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="3883d-129">출력</span><span class="sxs-lookup"><span data-stu-id="3883d-129">OUTPUTS</span></span>

### <span data-ttu-id="3883d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3883d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="3883d-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3883d-131">NOTES</span></span>

## <span data-ttu-id="3883d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3883d-132">RELATED LINKS</span></span>

[<span data-ttu-id="3883d-133">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3883d-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="3883d-134">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="3883d-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
