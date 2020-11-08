---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 1478a6fbe28e1d014767a829144138d7ada3dcfd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034275"
---
# <span data-ttu-id="ac1a9-101">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ac1a9-101">Get-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="ac1a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac1a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ac1a9-103">현재 자격 증명 모음에 대 한 사이트 복구 네트워크 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

## <span data-ttu-id="ac1a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac1a9-104">SYNTAX</span></span>

### <span data-ttu-id="ac1a9-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="ac1a9-105">ByObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac1a9-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="ac1a9-106">ByFabricObject</span></span>
```
Get-AzRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac1a9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ac1a9-107">DESCRIPTION</span></span>
<span data-ttu-id="ac1a9-108">**AzRecoveryServicesAsrNetworkMapping** Cmdlet은 복구 서비스 자격 증명 모음에 대 한 Azure Site Recovery 네트워크 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-108">The **Get-AzRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="ac1a9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ac1a9-109">EXAMPLES</span></span>

### <span data-ttu-id="ac1a9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="ac1a9-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="ac1a9-111">전달 된 네트워크에 대 한 모든 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="ac1a9-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="ac1a9-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="ac1a9-113">지정 된 azure site recovery 패브릭에 있는 이름이 제공 되는 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="ac1a9-114">변수</span><span class="sxs-lookup"><span data-stu-id="ac1a9-114">PARAMETERS</span></span>

### <span data-ttu-id="ac1a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac1a9-115">-DefaultProfile</span></span>
<span data-ttu-id="ac1a9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ac1a9-117">-이름</span><span class="sxs-lookup"><span data-stu-id="ac1a9-117">-Name</span></span>
<span data-ttu-id="ac1a9-118">가져올 ASR 네트워크 매핑 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-118">The name of the ASR network mapping object to get.</span></span>

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

### <span data-ttu-id="ac1a9-119">-네트워크</span><span class="sxs-lookup"><span data-stu-id="ac1a9-119">-Network</span></span>
<span data-ttu-id="ac1a9-120">지정 된 네트워크 ASR 개체에 해당 하는 ASR 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="ac1a9-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="ac1a9-121">-PrimaryFabric</span></span>
<span data-ttu-id="ac1a9-122">지정 된 기본 패브릭 개체에 해당 하는 ASR 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

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

### <span data-ttu-id="ac1a9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac1a9-123">CommonParameters</span></span>
<span data-ttu-id="ac1a9-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac1a9-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ac1a9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac1a9-126">입력</span><span class="sxs-lookup"><span data-stu-id="ac1a9-126">INPUTS</span></span>

### <span data-ttu-id="ac1a9-127">SiteRecovery. r m/. m g 네트워크</span><span class="sxs-lookup"><span data-stu-id="ac1a9-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

### <span data-ttu-id="ac1a9-128">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="ac1a9-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ac1a9-129">출력</span><span class="sxs-lookup"><span data-stu-id="ac1a9-129">OUTPUTS</span></span>

### <span data-ttu-id="ac1a9-130">SiteRecovery. r m g Networkmapping 매핑</span><span class="sxs-lookup"><span data-stu-id="ac1a9-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="ac1a9-131">상속자</span><span class="sxs-lookup"><span data-stu-id="ac1a9-131">NOTES</span></span>

## <span data-ttu-id="ac1a9-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac1a9-132">RELATED LINKS</span></span>

[<span data-ttu-id="ac1a9-133">새로운 AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ac1a9-133">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="ac1a9-134">제거-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="ac1a9-134">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzRecoveryServicesAsrNetworkMapping.md)
