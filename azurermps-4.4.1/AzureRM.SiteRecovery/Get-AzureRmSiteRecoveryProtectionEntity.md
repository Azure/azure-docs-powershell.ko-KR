---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 511D2401-5415-4EC6-AA75-E9D2D4D6D19C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionEntity.md
ms.openlocfilehash: 706b1ba37d7ac31215e5ecb07f3941e7e89ede5b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536956"
---
# <span data-ttu-id="7824d-101">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7824d-101">Get-AzureRmSiteRecoveryProtectionEntity</span></span>

## <span data-ttu-id="7824d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7824d-102">SYNOPSIS</span></span>
<span data-ttu-id="7824d-103">현재 사이트 복구 자격 증명 모음에 있는 보호 되는 엔터티 또는 보호 된 엔터티의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7824d-103">Gets a list of protectable or protected entities in the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7824d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7824d-104">SYNTAX</span></span>

### <span data-ttu-id="7824d-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="7824d-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7824d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="7824d-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7824d-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="7824d-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionEntity -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7824d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7824d-108">DESCRIPTION</span></span>
<span data-ttu-id="7824d-109">**AzureRmSiteRecoveryProtectionEntity** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에 있는 가상 컴퓨터와 같은 보호 되는 항목의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7824d-109">The **Get-AzureRmSiteRecoveryProtectionEntity** cmdlet gets a list of protectable or protected entities, such as virtual machines, in the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="7824d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7824d-110">EXAMPLES</span></span>

## <span data-ttu-id="7824d-111">변수</span><span class="sxs-lookup"><span data-stu-id="7824d-111">PARAMETERS</span></span>

### <span data-ttu-id="7824d-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="7824d-112">-FriendlyName</span></span>
<span data-ttu-id="7824d-113">보호 엔터티의 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7824d-113">Specifies the friendly name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7824d-114">-이름</span><span class="sxs-lookup"><span data-stu-id="7824d-114">-Name</span></span>
<span data-ttu-id="7824d-115">보호 엔터티의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7824d-115">Specifies the name of the protection entity.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7824d-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7824d-116">-ProtectionContainer</span></span>
<span data-ttu-id="7824d-117">보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7824d-117">Specifies the protection container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7824d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7824d-118">-DefaultProfile</span></span>
<span data-ttu-id="7824d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7824d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7824d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7824d-120">CommonParameters</span></span>
<span data-ttu-id="7824d-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7824d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7824d-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7824d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7824d-123">입력</span><span class="sxs-lookup"><span data-stu-id="7824d-123">INPUTS</span></span>

### <span data-ttu-id="7824d-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7824d-124">ASRProtectionContainer</span></span>
<span data-ttu-id="7824d-125">' ProtectionContainer ' 매개 변수는 파이프라인에서 ' ASRProtectionContainer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7824d-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="7824d-126">출력</span><span class="sxs-lookup"><span data-stu-id="7824d-126">OUTPUTS</span></span>

### <span data-ttu-id="7824d-127">System.webserver. t e 1.aspx ' 1 [Microsoft SiteRecovery. ASRProtectionEntity]</span><span class="sxs-lookup"><span data-stu-id="7824d-127">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity]</span></span>

## <span data-ttu-id="7824d-128">상속자</span><span class="sxs-lookup"><span data-stu-id="7824d-128">NOTES</span></span>

## <span data-ttu-id="7824d-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7824d-129">RELATED LINKS</span></span>

[<span data-ttu-id="7824d-130">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7824d-130">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
