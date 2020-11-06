---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 442fd62393b33cc69e8f5a38f726bb8816c5bc64
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528880"
---
# <span data-ttu-id="89078-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="89078-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="89078-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89078-102">SYNOPSIS</span></span>
<span data-ttu-id="89078-103">현재 자격 증명 모음에 대 한 사이트 복구 네트워크 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89078-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89078-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89078-104">SYNTAX</span></span>

### <span data-ttu-id="89078-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="89078-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -Network <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89078-106">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="89078-106">ByFabricObject</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping [-Name <String>] -PrimaryFabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89078-107">설명은</span><span class="sxs-lookup"><span data-stu-id="89078-107">DESCRIPTION</span></span>
<span data-ttu-id="89078-108">**AzureRmRecoveryServicesAsrNetworkMapping** Cmdlet은 복구 서비스 자격 증명 모음에 대 한 Azure Site Recovery 네트워크 매핑에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89078-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="89078-109">예제의</span><span class="sxs-lookup"><span data-stu-id="89078-109">EXAMPLES</span></span>

### <span data-ttu-id="89078-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="89078-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="89078-111">전달 된 네트워크에 대 한 모든 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89078-111">Gets all networks mappings for the passed Network.</span></span>

### <span data-ttu-id="89078-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="89078-112">Example 2</span></span>
```
PS C:\> $primaryFabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Name $networkMappingName -PrimaryFabric $primaryFabric
```

<span data-ttu-id="89078-113">지정 된 azure site recovery 패브릭에 있는 이름이 제공 되는 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89078-113">Gets networks mapping with provided name in specified azure site recovery fabric.</span></span>

## <span data-ttu-id="89078-114">변수</span><span class="sxs-lookup"><span data-stu-id="89078-114">PARAMETERS</span></span>

### <span data-ttu-id="89078-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89078-115">-DefaultProfile</span></span>
<span data-ttu-id="89078-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89078-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89078-117">-이름</span><span class="sxs-lookup"><span data-stu-id="89078-117">-Name</span></span>
<span data-ttu-id="89078-118">가져올 ASR 네트워크 매핑 개체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89078-118">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89078-119">-네트워크</span><span class="sxs-lookup"><span data-stu-id="89078-119">-Network</span></span>
<span data-ttu-id="89078-120">지정 된 네트워크 ASR 개체에 해당 하는 ASR 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89078-120">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89078-121">-PrimaryFabric</span><span class="sxs-lookup"><span data-stu-id="89078-121">-PrimaryFabric</span></span>
<span data-ttu-id="89078-122">지정 된 기본 패브릭 개체에 해당 하는 ASR 네트워크 매핑을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89078-122">Get the ASR network mappings corresponding to the specified primary fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByFabricObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89078-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89078-123">CommonParameters</span></span>
<span data-ttu-id="89078-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89078-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89078-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89078-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89078-126">입력</span><span class="sxs-lookup"><span data-stu-id="89078-126">INPUTS</span></span>

### <span data-ttu-id="89078-127">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="89078-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="89078-128">출력</span><span class="sxs-lookup"><span data-stu-id="89078-128">OUTPUTS</span></span>

### <span data-ttu-id="89078-129">SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null] 인 컬렉션인 SiteRecovery ' 1 [[모든 Microsoft Azure. r e t] 매핑, Microsoft Azure. 명령에 대 한 일반 서비스.</span><span class="sxs-lookup"><span data-stu-id="89078-129">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="89078-130">상속자</span><span class="sxs-lookup"><span data-stu-id="89078-130">NOTES</span></span>

## <span data-ttu-id="89078-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89078-131">RELATED LINKS</span></span>

[<span data-ttu-id="89078-132">새로운 AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="89078-132">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="89078-133">제거-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="89078-133">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
