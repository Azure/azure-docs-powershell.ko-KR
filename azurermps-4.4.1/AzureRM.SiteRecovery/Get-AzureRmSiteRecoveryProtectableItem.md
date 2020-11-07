---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BE2D05F5-70CE-4EAA-9363-6CA89A312DDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectableItem.md
ms.openlocfilehash: 0b2fe8f500e17bc21407870a712ad4b9f00fd544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702400"
---
# <span data-ttu-id="27b8c-101">Get-AzureRmSiteRecoveryProtectableItem</span><span class="sxs-lookup"><span data-stu-id="27b8c-101">Get-AzureRmSiteRecoveryProtectableItem</span></span>

## <span data-ttu-id="27b8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b8c-102">SYNOPSIS</span></span>
<span data-ttu-id="27b8c-103">보호 컨테이너에서 보호할 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27b8c-103">Get the protectable items in a Protection Container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27b8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27b8c-104">SYNTAX</span></span>

### <span data-ttu-id="27b8c-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="27b8c-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27b8c-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="27b8c-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="27b8c-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="27b8c-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectableItem -FriendlyName <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="27b8c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="27b8c-108">DESCRIPTION</span></span>
<span data-ttu-id="27b8c-109">**AzureRmSiteRecoveryProtectableItem** Cmdlet은 Azure Site Recovery 보호 컨테이너에서 보호 가능한 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="27b8c-109">The **Get-AzureRmSiteRecoveryProtectableItem** cmdlet gets the protectable items in an Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="27b8c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="27b8c-110">EXAMPLES</span></span>

## <span data-ttu-id="27b8c-111">변수</span><span class="sxs-lookup"><span data-stu-id="27b8c-111">PARAMETERS</span></span>

### <span data-ttu-id="27b8c-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="27b8c-112">-FriendlyName</span></span>
<span data-ttu-id="27b8c-113">Azure Site Recovery 보호 가능한 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b8c-113">Specifies the friendly name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="27b8c-114">-이름</span><span class="sxs-lookup"><span data-stu-id="27b8c-114">-Name</span></span>
<span data-ttu-id="27b8c-115">Azure Site Recovery 보호 가능한 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b8c-115">Specifies the name of the Azure Site Recovery protectable item.</span></span>

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

### <span data-ttu-id="27b8c-116">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="27b8c-116">-ProtectionContainer</span></span>
<span data-ttu-id="27b8c-117">Azure Site Recovery 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b8c-117">Specifies the Azure Site Recovery Protection Container object.</span></span>

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

### <span data-ttu-id="27b8c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b8c-118">-DefaultProfile</span></span>
<span data-ttu-id="27b8c-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27b8c-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="27b8c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b8c-120">CommonParameters</span></span>
<span data-ttu-id="27b8c-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b8c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b8c-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27b8c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b8c-123">입력</span><span class="sxs-lookup"><span data-stu-id="27b8c-123">INPUTS</span></span>

### <span data-ttu-id="27b8c-124">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="27b8c-124">ASRProtectionContainer</span></span>
<span data-ttu-id="27b8c-125">' ProtectionContainer ' 매개 변수는 파이프라인에서 ' ASRProtectionContainer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="27b8c-125">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="27b8c-126">출력</span><span class="sxs-lookup"><span data-stu-id="27b8c-126">OUTPUTS</span></span>

### <span data-ttu-id="27b8c-127">ASRProtectableItem, SiteRecovery, Version = 2.0.1.0, Culture = 중립, PublicKeyToken = null]], system.webserver ' 1 [[Microsoft Azure.])</span><span class="sxs-lookup"><span data-stu-id="27b8c-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="27b8c-128">상속자</span><span class="sxs-lookup"><span data-stu-id="27b8c-128">NOTES</span></span>

## <span data-ttu-id="27b8c-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27b8c-129">RELATED LINKS</span></span>

[<span data-ttu-id="27b8c-130">Get-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="27b8c-130">Get-AzureRmSiteRecoveryProtectionEntity</span></span>](./Get-AzureRmSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="27b8c-131">Set-AzureRmSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="27b8c-131">Set-AzureRmSiteRecoveryProtectionEntity</span></span>](./Set-AzureRmSiteRecoveryProtectionEntity.md)
