---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4BF1E20A-46EA-48E2-8C7A-F121AE6815AF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 1b01fef6563fef97f78913f916a6481acd6f6ed3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711226"
---
# <span data-ttu-id="fa6ee-101">New-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fa6ee-101">New-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="fa6ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="fa6ee-103">가상 네트워크 간에 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fa6ee-103">Creates a mapping between virtual networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa6ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fa6ee-104">SYNTAX</span></span>

### <span data-ttu-id="fa6ee-105">Enterprise엔터프라이즈</span><span class="sxs-lookup"><span data-stu-id="fa6ee-105">EnterpriseToEnterprise</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fa6ee-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="fa6ee-106">EnterpriseToAzure</span></span>
```
New-AzureRmSiteRecoveryNetworkMapping [-Name <String>] -PrimaryNetwork <ASRNetwork> -AzureVMNetworkId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa6ee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fa6ee-107">DESCRIPTION</span></span>
<span data-ttu-id="fa6ee-108">**AzureRMSiteRecoveryNetworkMapping** cmdlet은 두 가상 네트워크 간의 매핑을 만들고 Azure Site Recovery 작업을 추적 하기 위해 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa6ee-108">The **New-AzureRMSiteRecoveryNetworkMapping** cmdlet creates a mapping between two virtual networks and returns an Azure Site Recovery job to track it.</span></span>

## <span data-ttu-id="fa6ee-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fa6ee-109">EXAMPLES</span></span>

## <span data-ttu-id="fa6ee-110">변수</span><span class="sxs-lookup"><span data-stu-id="fa6ee-110">PARAMETERS</span></span>

### <span data-ttu-id="fa6ee-111">-AzureVMNetworkId</span><span class="sxs-lookup"><span data-stu-id="fa6ee-111">-AzureVMNetworkId</span></span>
<span data-ttu-id="fa6ee-112">Azure 가상 네트워크 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa6ee-112">Specifies the Azure virtual network ID.</span></span>

```yaml
Type: System.String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa6ee-113">-이름</span><span class="sxs-lookup"><span data-stu-id="fa6ee-113">-Name</span></span>
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

### <span data-ttu-id="fa6ee-114">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="fa6ee-114">-PrimaryNetwork</span></span>
<span data-ttu-id="fa6ee-115">주 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa6ee-115">Specifies the primary network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fa6ee-116">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="fa6ee-116">-RecoveryNetwork</span></span>
<span data-ttu-id="fa6ee-117">복구 네트워크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa6ee-117">Specifies the recovery network object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fa6ee-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa6ee-118">-DefaultProfile</span></span>
<span data-ttu-id="fa6ee-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fa6ee-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa6ee-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa6ee-120">CommonParameters</span></span>
<span data-ttu-id="fa6ee-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa6ee-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa6ee-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa6ee-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa6ee-123">입력</span><span class="sxs-lookup"><span data-stu-id="fa6ee-123">INPUTS</span></span>

### <span data-ttu-id="fa6ee-124">ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="fa6ee-124">ASRNetwork</span></span>
<span data-ttu-id="fa6ee-125">' PrimaryNetwork ' 매개 변수는 파이프라인에서 ' ASRNetwork ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fa6ee-125">Parameter 'PrimaryNetwork' accepts value of type 'ASRNetwork' from the pipeline</span></span>

## <span data-ttu-id="fa6ee-126">출력</span><span class="sxs-lookup"><span data-stu-id="fa6ee-126">OUTPUTS</span></span>

### <span data-ttu-id="fa6ee-127">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="fa6ee-127">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="fa6ee-128">상속자</span><span class="sxs-lookup"><span data-stu-id="fa6ee-128">NOTES</span></span>

## <span data-ttu-id="fa6ee-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa6ee-129">RELATED LINKS</span></span>

[<span data-ttu-id="fa6ee-130">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fa6ee-130">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="fa6ee-131">제거-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="fa6ee-131">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>](./Remove-AzureRmSiteRecoveryNetworkMapping.md)
