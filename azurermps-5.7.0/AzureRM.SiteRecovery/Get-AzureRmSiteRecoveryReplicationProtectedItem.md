---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 99196F44-F1DB-4219-91C0-3056624ADE5B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryreplicationprotecteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 210b8ca6d8165049edc190e24e4a435046e1461e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703980"
---
# <span data-ttu-id="4cc0b-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4cc0b-101">Get-AzureRmSiteRecoveryReplicationProtectedItem</span></span>

## <span data-ttu-id="4cc0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cc0b-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc0b-103">Azure Site Recovery 보호 된 항목의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-103">Gets the properties of Azure Site Recovery Protected Items.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4cc0b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4cc0b-104">SYNTAX</span></span>

### <span data-ttu-id="4cc0b-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="4cc0b-105">ByObject (Default)</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cc0b-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="4cc0b-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -Name <String> -ProtectionContainer <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cc0b-107">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="4cc0b-107">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -FriendlyName <String>
 -ProtectionContainer <ASRProtectionContainer> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4cc0b-108">ByProtectableItemObject</span><span class="sxs-lookup"><span data-stu-id="4cc0b-108">ByProtectableItemObject</span></span>
```
Get-AzureRmSiteRecoveryReplicationProtectedItem -ProtectableItem <ASRProtectableItem>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4cc0b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="4cc0b-109">DESCRIPTION</span></span>
<span data-ttu-id="4cc0b-110">**AzureRmSiteRecoveryReplicationProtectedItem** Cmdlet은 Azure Site Recovery 보호 된 항목의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-110">The **Get-AzureRmSiteRecoveryReplicationProtectedItem** cmdlet gets the properties of Azure Site Recovery Protected Items.</span></span>

## <span data-ttu-id="4cc0b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4cc0b-111">EXAMPLES</span></span>

## <span data-ttu-id="4cc0b-112">변수</span><span class="sxs-lookup"><span data-stu-id="4cc0b-112">PARAMETERS</span></span>

### <span data-ttu-id="4cc0b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc0b-113">-DefaultProfile</span></span>
<span data-ttu-id="4cc0b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4cc0b-115">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="4cc0b-115">-FriendlyName</span></span>
<span data-ttu-id="4cc0b-116">이 cmdlet이 가져오는 복제 보호 항목의 식별 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-116">Specifies the friendly name of the Replication Protected Item that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cc0b-117">-이름</span><span class="sxs-lookup"><span data-stu-id="4cc0b-117">-Name</span></span>
<span data-ttu-id="4cc0b-118">이 cmdlet이 가져오는 복제 보호 항목의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-118">Specifies the name of the Replication Protected Item that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4cc0b-119">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4cc0b-119">-ProtectableItem</span></span>
<span data-ttu-id="4cc0b-120">복제 보호 항목에 해당 하는 보호 가능한 항목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-120">Specifies the Protectable Item corresponding to the Replication Protected Item.</span></span>

```yaml
Type: ASRProtectableItem
Parameter Sets: ByProtectableItemObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc0b-121">-ProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4cc0b-121">-ProtectionContainer</span></span>
<span data-ttu-id="4cc0b-122">Azure Site Recovery 보호 컨테이너 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-122">Specifies the Azure Site Recovery Protection Container object.</span></span>

```yaml
Type: ASRProtectionContainer
Parameter Sets: ByObject, ByObjectWithName, ByObjectWithFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4cc0b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc0b-123">CommonParameters</span></span>
<span data-ttu-id="4cc0b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc0b-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4cc0b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc0b-126">입력</span><span class="sxs-lookup"><span data-stu-id="4cc0b-126">INPUTS</span></span>

### <span data-ttu-id="4cc0b-127">ASRProtectableItem</span><span class="sxs-lookup"><span data-stu-id="4cc0b-127">ASRProtectableItem</span></span>
<span data-ttu-id="4cc0b-128">' ProtectableItem ' 매개 변수는 파이프라인에서 ' ASRProtectableItem ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-128">Parameter 'ProtectableItem' accepts value of type 'ASRProtectableItem' from the pipeline</span></span>

### <span data-ttu-id="4cc0b-129">ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4cc0b-129">ASRProtectionContainer</span></span>
<span data-ttu-id="4cc0b-130">' ProtectionContainer ' 매개 변수는 파이프라인에서 ' ASRProtectionContainer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4cc0b-130">Parameter 'ProtectionContainer' accepts value of type 'ASRProtectionContainer' from the pipeline</span></span>

## <span data-ttu-id="4cc0b-131">출력</span><span class="sxs-lookup"><span data-stu-id="4cc0b-131">OUTPUTS</span></span>

### <span data-ttu-id="4cc0b-132">ASRReplicationProtectedItem, SiteRecovery, Version = 2.0.1.0, Culture = 중립, PublicKeyToken = null]], system.webserver ' 1 [[Microsoft Azure.])</span><span class="sxs-lookup"><span data-stu-id="4cc0b-132">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="4cc0b-133">상속자</span><span class="sxs-lookup"><span data-stu-id="4cc0b-133">NOTES</span></span>

## <span data-ttu-id="4cc0b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4cc0b-134">RELATED LINKS</span></span>

[<span data-ttu-id="4cc0b-135">새로운 AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4cc0b-135">New-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="4cc0b-136">제거-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4cc0b-136">Remove-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)

[<span data-ttu-id="4cc0b-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="4cc0b-137">Set-AzureRmSiteRecoveryReplicationProtectedItem</span></span>](./Set-AzureRmSiteRecoveryReplicationProtectedItem.md)
