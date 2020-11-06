---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 99196F44-F1DB-4219-91C0-3056624ADE5B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 0e94a46b8d6433ddd96530dc011234050398bf37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535411"
---
# <span data-ttu-id="a0c7d-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a0c7d-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="a0c7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0c7d-102">SYNOPSIS</span></span>
<span data-ttu-id="a0c7d-103">Azure Site Recovery 보호 된 항목의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7d-103">Gets the properties of Azure Site Recovery Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0c7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0c7d-104">SYNTAX</span></span>

### <span data-ttu-id="a0c7d-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="a0c7d-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c7d-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="a0c7d-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c7d-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a0c7d-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0c7d-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="a0c7d-108">ByProtectableItemObject</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0c7d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a0c7d-109">DESCRIPTION</span></span>
<span data-ttu-id="a0c7d-110">**AzureRmSiteRecoveryReplicationProtectedItem** Cmdlet은 Azure Site Recovery 보호 된 항목의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7d-110">The **Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet gets the properties of Azure Site Recovery Protected Items.</span></span>

## <span data-ttu-id="a0c7d-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a0c7d-111">EXAMPLES</span></span>

## <span data-ttu-id="a0c7d-112">변수</span><span class="sxs-lookup"><span data-stu-id="a0c7d-112">PARAMETERS</span></span>

### <span data-ttu-id="a0c7d-113">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a0c7d-113">-FriendlyName</span></span>
<span data-ttu-id="a0c7d-114">이 cmdlet이 가져오는 복제 보호 항목의 식별 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7d-114">Specifies the friendly name of the Replication Protected Item that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a0c7d-115">-이름</span><span class="sxs-lookup"><span data-stu-id="a0c7d-115">-Name</span></span>
<span data-ttu-id="a0c7d-116">이 cmdlet이 가져오는 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7d-116">Specifies the name of the Replication Protected Item that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a0c7d-117">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a0c7d-117">-ProtectableItem</span></span>
<span data-ttu-id="a0c7d-118">복제 보호 항목에 해당 하는 보호 가능한 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7d-118">Specifies the Protectable Item corresponding to the Replication Protected Item.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0c7d-119">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a0c7d-119">-ProtectionContainer</span></span>
<span data-ttu-id="a0c7d-120">Azure Site Recovery 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7d-120">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0c7d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0c7d-121">-DefaultProfile</span></span>
<span data-ttu-id="a0c7d-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0c7d-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0c7d-123">CommonParameters</span></span>
<span data-ttu-id="a0c7d-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7d-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0c7d-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0c7d-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0c7d-126">입력</span><span class="sxs-lookup"><span data-stu-id="a0c7d-126">INPUTS</span></span>

### <span data-ttu-id="a0c7d-127">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="a0c7d-127">ASRProtectableItem</span></span>
<span data-ttu-id="a0c7d-128">' ProtectableItem ' 매개 변수는 파이프라인에서 ' ASRProtectableItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7d-128">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

### <span data-ttu-id="a0c7d-129">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="a0c7d-129">ASRProtectionContainer</span></span>
<span data-ttu-id="a0c7d-130">' ProtectionContainer ' 매개 변수는 파이프라인에서 ' ASRProtectionContainer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0c7d-130">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="a0c7d-131">출력</span><span class="sxs-lookup"><span data-stu-id="a0c7d-131">OUTPUTS</span></span>

### <span data-ttu-id="a0c7d-132">ASRReplicationProtectedItem, SiteRecovery, Version = 2.0.1.0, Culture = 중립, PublicKeyToken = null]], system.webserver ' 1 [[Microsoft Azure.])</span><span class="sxs-lookup"><span data-stu-id="a0c7d-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a0c7d-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a0c7d-133">NOTES</span></span>

## <span data-ttu-id="a0c7d-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0c7d-134">RELATED LINKS</span></span>

[<span data-ttu-id="a0c7d-135">새로운 AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a0c7d-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="a0c7d-136">제거-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a0c7d-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="a0c7d-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a0c7d-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
