---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 54c90e4dac97084ed371e0f5f9011bbcef0a254e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003259"
---
# <span data-ttu-id="ce9a3-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="ce9a3-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="ce9a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9a3-103">현재 자격 증명 모음에 대한 Site Recovery에서 관리되는 네트워크에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="ce9a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce9a3-104">SYNTAX</span></span>

### <span data-ttu-id="ce9a3-105">ByFabricObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="ce9a3-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce9a3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ce9a3-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ce9a3-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="ce9a3-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce9a3-108">설명</span><span class="sxs-lookup"><span data-stu-id="ce9a3-108">DESCRIPTION</span></span>
<span data-ttu-id="ce9a3-109">**Get-AzRecoveryServicesAsrNetwork** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에 대한 Azure Site Recovery 네트워크에 대한 정보를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="ce9a3-110">예제</span><span class="sxs-lookup"><span data-stu-id="ce9a3-110">EXAMPLES</span></span>

### <span data-ttu-id="ce9a3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ce9a3-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="ce9a3-112">지정된 패브릭에서 알려진 모든 네트워크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="ce9a3-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce9a3-113">PARAMETERS</span></span>

### <span data-ttu-id="ce9a3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce9a3-114">-DefaultProfile</span></span>
<span data-ttu-id="ce9a3-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ce9a3-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="ce9a3-116">-Fabric</span></span>
<span data-ttu-id="ce9a3-117">ASR 패브릭 개체</span><span class="sxs-lookup"><span data-stu-id="ce9a3-117">ASR fabric object</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce9a3-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ce9a3-118">-FriendlyName</span></span>
<span data-ttu-id="ce9a3-119">네트워크 ASR 개체의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-119">Friendly name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9a3-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ce9a3-120">-Name</span></span>
<span data-ttu-id="ce9a3-121">네트워크 ASR 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-121">Name of network ASR object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9a3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9a3-122">CommonParameters</span></span>
<span data-ttu-id="ce9a3-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9a3-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ce9a3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9a3-125">입력</span><span class="sxs-lookup"><span data-stu-id="ce9a3-125">INPUTS</span></span>

### <span data-ttu-id="ce9a3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="ce9a3-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="ce9a3-127">출력</span><span class="sxs-lookup"><span data-stu-id="ce9a3-127">OUTPUTS</span></span>

### <span data-ttu-id="ce9a3-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="ce9a3-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="ce9a3-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce9a3-129">NOTES</span></span>

## <span data-ttu-id="ce9a3-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce9a3-130">RELATED LINKS</span></span>
