---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 77F1556C-323D-49CA-BD6C-75B2D4E0F894
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryProtectionContainer.md
ms.openlocfilehash: d5c2032828c5d34b94af8d448155c18b6d8b06c6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703984"
---
# <span data-ttu-id="d79cf-101">Get-AzureRmSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d79cf-101">Get-AzureRmSiteRecoveryProtectionContainer</span></span>

## <span data-ttu-id="d79cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d79cf-102">SYNOPSIS</span></span>
<span data-ttu-id="d79cf-103">현재 사이트 복구 자격 증명 모음에 대 한 보호 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d79cf-103">Gets protection containers for the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d79cf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d79cf-104">SYNTAX</span></span>

### <span data-ttu-id="d79cf-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d79cf-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d79cf-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="d79cf-106">ByObjectWithName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d79cf-107">ByObjectWithNameLegacy</span><span class="sxs-lookup"><span data-stu-id="d79cf-107">ByObjectWithNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d79cf-108">ByObjectWithFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d79cf-108">ByObjectWithFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d79cf-109">ByObjectWithFriendlyNameLegacy</span><span class="sxs-lookup"><span data-stu-id="d79cf-109">ByObjectWithFriendlyNameLegacy</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d79cf-110">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="d79cf-110">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryProtectionContainer -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d79cf-111">설명은</span><span class="sxs-lookup"><span data-stu-id="d79cf-111">DESCRIPTION</span></span>
<span data-ttu-id="d79cf-112">**AzureRmSiteRecoveryProtectionContainer** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에 대 한 보호 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d79cf-112">The **Get-AzureRmSiteRecoveryProtectionContainer** cmdlet gets protection containers for the current Azure Site Recovery vault.</span></span>
<span data-ttu-id="d79cf-113">보호 컨테이너는 가상 컴퓨터와 같은 보호 된 개체에 대 한 논리적 컨테이너입니다.</span><span class="sxs-lookup"><span data-stu-id="d79cf-113">A protection container is a logical container for protected objects such as virtual machines.</span></span>
<span data-ttu-id="d79cf-114">보호 정책은 보호 된 항목에 대 한 복제 설정을 정의 하 고 보호 컨테이너와 연결 되어 보호 된 엔터티에 적용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d79cf-114">Protection policies define replication settings for protected items and can be associated with a protection container and applied to a protected entity.</span></span>

## <span data-ttu-id="d79cf-115">예제의</span><span class="sxs-lookup"><span data-stu-id="d79cf-115">EXAMPLES</span></span>

## <span data-ttu-id="d79cf-116">변수</span><span class="sxs-lookup"><span data-stu-id="d79cf-116">PARAMETERS</span></span>

### <span data-ttu-id="d79cf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79cf-117">-DefaultProfile</span></span>
<span data-ttu-id="d79cf-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d79cf-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d79cf-119">-패브릭</span><span class="sxs-lookup"><span data-stu-id="d79cf-119">-Fabric</span></span>
```yaml
Type: ASRFabric
Parameter Sets: ByObjectWithName, ByObjectWithFriendlyName, ByFabricObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d79cf-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="d79cf-120">-FriendlyName</span></span>
<span data-ttu-id="d79cf-121">보호 컨테이너의 친근 한 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d79cf-121">Specifies the friendly name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithFriendlyName, ByObjectWithFriendlyNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79cf-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d79cf-122">-Name</span></span>
<span data-ttu-id="d79cf-123">보호 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d79cf-123">Specifies the name of the protection container.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName, ByObjectWithNameLegacy
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79cf-124">CommonParameters</span></span>
<span data-ttu-id="d79cf-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d79cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79cf-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d79cf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79cf-127">입력</span><span class="sxs-lookup"><span data-stu-id="d79cf-127">INPUTS</span></span>

### <span data-ttu-id="d79cf-128">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="d79cf-128">ASRFabric</span></span>
<span data-ttu-id="d79cf-129">' Fabric ' 매개 변수는 파이프라인에서 ' ASRFabric ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d79cf-129">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="d79cf-130">출력</span><span class="sxs-lookup"><span data-stu-id="d79cf-130">OUTPUTS</span></span>

### <span data-ttu-id="d79cf-131">System.webserver. t e 1.aspx ' 1 [Microsoft SiteRecovery. ASRProtectionContainer]</span><span class="sxs-lookup"><span data-stu-id="d79cf-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRProtectionContainer]</span></span>

## <span data-ttu-id="d79cf-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d79cf-132">NOTES</span></span>

## <span data-ttu-id="d79cf-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d79cf-133">RELATED LINKS</span></span>

