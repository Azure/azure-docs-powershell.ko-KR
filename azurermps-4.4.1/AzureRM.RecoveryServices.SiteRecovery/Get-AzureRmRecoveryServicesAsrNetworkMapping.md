---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 510e38e201c84ad6158c959d4d56fe9872ad83df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711515"
---
# <span data-ttu-id="67869-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="67869-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="67869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67869-102">SYNOPSIS</span></span>
<span data-ttu-id="67869-103">현재 자격 증명 모음에 대 한 사이트 복구 네트워크 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67869-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67869-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67869-104">SYNTAX</span></span>

### <span data-ttu-id="67869-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="67869-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Network <ASRNetwork> [<CommonParameters>]
```

### <span data-ttu-id="67869-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="67869-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -Network <ASRNetwork> [<CommonParameters>]
```

## <span data-ttu-id="67869-107">설명은</span><span class="sxs-lookup"><span data-stu-id="67869-107">DESCRIPTION</span></span>
<span data-ttu-id="67869-108">**AzureRmRecoveryServicesAsrNetworkMapping** Cmdlet은 복구 서비스 자격 증명 모음에 대 한 Azure Site Recovery 네트워크 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67869-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="67869-109">예제의</span><span class="sxs-lookup"><span data-stu-id="67869-109">EXAMPLES</span></span>

### <span data-ttu-id="67869-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="67869-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="67869-111">전달 된 네트워크에 대 한 모든 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67869-111">Gets all networks mappings for the passed Network.</span></span>

## <span data-ttu-id="67869-112">변수</span><span class="sxs-lookup"><span data-stu-id="67869-112">PARAMETERS</span></span>

### <span data-ttu-id="67869-113">-이름</span><span class="sxs-lookup"><span data-stu-id="67869-113">-Name</span></span>
<span data-ttu-id="67869-114">가져올 ASR 네트워크 매핑 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67869-114">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67869-115">-네트워크</span><span class="sxs-lookup"><span data-stu-id="67869-115">-Network</span></span>
<span data-ttu-id="67869-116">지정 된 네트워크 ASR 개체에 해당 하는 ASR 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="67869-116">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

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

### <span data-ttu-id="67869-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67869-117">CommonParameters</span></span>
<span data-ttu-id="67869-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67869-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67869-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67869-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67869-120">입력</span><span class="sxs-lookup"><span data-stu-id="67869-120">INPUTS</span></span>

### <span data-ttu-id="67869-121">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="67869-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="67869-122">출력</span><span class="sxs-lookup"><span data-stu-id="67869-122">OUTPUTS</span></span>

### <span data-ttu-id="67869-123">SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null] 인 컬렉션인 SiteRecovery ' 1 [[모든 Microsoft Azure. r e t] 매핑, Microsoft Azure. 명령에 대 한 일반 서비스.</span><span class="sxs-lookup"><span data-stu-id="67869-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="67869-124">상속자</span><span class="sxs-lookup"><span data-stu-id="67869-124">NOTES</span></span>

## <span data-ttu-id="67869-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67869-125">RELATED LINKS</span></span>

[<span data-ttu-id="67869-126">새로운 AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="67869-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="67869-127">제거-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="67869-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
