---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetwork
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetwork.md
ms.openlocfilehash: 4eac63104f9e75643119c371d2a4d0e882945966
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530119"
---
# <span data-ttu-id="4d78e-101">Get-AzureRmRecoveryServicesAsrNetwork</span><span class="sxs-lookup"><span data-stu-id="4d78e-101">Get-AzureRmRecoveryServicesAsrNetwork</span></span>

## <span data-ttu-id="4d78e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d78e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d78e-103">현재 자격 증명 모음의 사이트 복구에서 관리 되는 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d78e-103">Gets information about the networks managed by Site Recovery for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d78e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d78e-104">SYNTAX</span></span>

### <span data-ttu-id="4d78e-105">ByFabricObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d78e-105">ByFabricObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d78e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="4d78e-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d78e-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4d78e-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetwork -Fabric <ASRFabric> -FriendlyName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d78e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4d78e-108">DESCRIPTION</span></span>
<span data-ttu-id="4d78e-109">**AzureRmRecoveryServicesAsrNetwork** cmdlet은 현재 Azure site recovery 자격 증명 모음에 대 한 Azure site recovery 네트워크에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d78e-109">The **Get-AzureRmRecoveryServicesAsrNetwork** cmdlet gets information about Azure Site Recovery networks for the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="4d78e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4d78e-110">EXAMPLES</span></span>

### <span data-ttu-id="4d78e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d78e-111">Example 1</span></span>
```
PS C:\> $Networks = Get-AzureRmRecoveryServicesAsrNetwork -Fabric $Fabric
```

<span data-ttu-id="4d78e-112">지정 된 패브릭의 알려진 모든 네트워크를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4d78e-112">Gets all known networks in the specified fabric.</span></span>

## <span data-ttu-id="4d78e-113">변수</span><span class="sxs-lookup"><span data-stu-id="4d78e-113">PARAMETERS</span></span>

### <span data-ttu-id="4d78e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d78e-114">-DefaultProfile</span></span>
<span data-ttu-id="4d78e-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d78e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d78e-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="4d78e-116">-Fabric</span></span>
<span data-ttu-id="4d78e-117">ASR fabric 개체</span><span class="sxs-lookup"><span data-stu-id="4d78e-117">ASR fabric object</span></span>

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

### <span data-ttu-id="4d78e-118">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4d78e-118">-FriendlyName</span></span>
<span data-ttu-id="4d78e-119">네트워크 ASR 개체의 식별 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d78e-119">Friendly name of network ASR object.</span></span>

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

### <span data-ttu-id="4d78e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="4d78e-120">-Name</span></span>
<span data-ttu-id="4d78e-121">네트워크 ASR 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d78e-121">Name of network ASR object.</span></span>

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

### <span data-ttu-id="4d78e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d78e-122">CommonParameters</span></span>
<span data-ttu-id="4d78e-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d78e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d78e-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d78e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d78e-125">입력</span><span class="sxs-lookup"><span data-stu-id="4d78e-125">INPUTS</span></span>

### <span data-ttu-id="4d78e-126">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="4d78e-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="4d78e-127">출력</span><span class="sxs-lookup"><span data-stu-id="4d78e-127">OUTPUTS</span></span>

### <span data-ttu-id="4d78e-128">System.webserver. t e r ' 1 [[SiteRecovery], [[Microsoft Azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]],,.</span><span class="sxs-lookup"><span data-stu-id="4d78e-128">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4d78e-129">상속자</span><span class="sxs-lookup"><span data-stu-id="4d78e-129">NOTES</span></span>

## <span data-ttu-id="4d78e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d78e-130">RELATED LINKS</span></span>
