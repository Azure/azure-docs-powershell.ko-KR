---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 8aba9281fa402cc9063cb5a42f79c7da74fb1103
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493358"
---
# <span data-ttu-id="6b277-101">Get-AzRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="6b277-101">Get-AzRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="6b277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b277-102">SYNOPSIS</span></span>
<span data-ttu-id="6b277-103">현재 자격 증명 모음에 대한 Site Recovery에서 관리하는 네트워크에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b277-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

## <span data-ttu-id="6b277-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b277-104">SYNTAX</span></span>

### <span data-ttu-id="6b277-105">ByFabricObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="6b277-105">ByFabricObject (Default)</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b277-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6b277-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6b277-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b277-107">ByFriendlyName</span></span>
```
Get-AzRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b277-108">설명</span><span class="sxs-lookup"><span data-stu-id="6b277-108">DESCRIPTION</span></span>
<span data-ttu-id="6b277-109">**Get-AzRecoveryServicesAsrNetwork** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에 대한 Azure Site Recovery 네트워크에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b277-109">The **Get-AzRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="6b277-110">예제</span><span class="sxs-lookup"><span data-stu-id="6b277-110">EXAMPLES</span></span>

### <span data-ttu-id="6b277-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b277-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="6b277-112">지정된 패브릭에서 알려진 모든 네트워크를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6b277-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="6b277-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6b277-113">PARAMETERS</span></span>

### <span data-ttu-id="6b277-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b277-114">-DefaultProfile</span></span>
<span data-ttu-id="6b277-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b277-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="6b277-116">-Fabric</span><span class="sxs-lookup"><span data-stu-id="6b277-116">-Fabric</span></span>
<span data-ttu-id="6b277-117">ASR 패브릭 개체</span><span class="sxs-lookup"><span data-stu-id="6b277-117">ASR fabric object</span></span>

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

### <span data-ttu-id="6b277-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="6b277-118">-FriendlyName</span></span>
<span data-ttu-id="6b277-119">네트워크 ASR 개체의 친숙한 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b277-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="6b277-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6b277-120">-Name</span></span>
<span data-ttu-id="6b277-121">네트워크 ASR 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b277-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="6b277-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b277-122">CommonParameters</span></span>
<span data-ttu-id="6b277-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b277-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b277-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6b277-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b277-125">입력</span><span class="sxs-lookup"><span data-stu-id="6b277-125">INPUTS</span></span>

### <span data-ttu-id="6b277-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span><span class="sxs-lookup"><span data-stu-id="6b277-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="6b277-127">출력</span><span class="sxs-lookup"><span data-stu-id="6b277-127">OUTPUTS</span></span>

### <span data-ttu-id="6b277-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="6b277-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="6b277-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b277-129">NOTES</span></span>

## <span data-ttu-id="6b277-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b277-130">RELATED LINKS</span></span>
