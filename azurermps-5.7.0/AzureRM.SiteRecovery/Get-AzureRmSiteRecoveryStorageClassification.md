---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F62A993-18BF-4189-A7C0-BB877F550AA5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoverystorageclassification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryStorageClassification.md
ms.openlocfilehash: 4ca96961aa99a15161e9abbbc01174f97a27968e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534627"
---
# <span data-ttu-id="e67b2-101">Get-AzureRmSiteRecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="e67b2-101">Get-AzureRmSiteRecoveryStorageClassification</span></span>

## <span data-ttu-id="e67b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e67b2-102">SYNOPSIS</span></span>
<span data-ttu-id="e67b2-103">사이트 복구의 저장소 분류를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e67b2-103">Gets storage classifications in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e67b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e67b2-104">SYNTAX</span></span>

### <span data-ttu-id="e67b2-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e67b2-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e67b2-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e67b2-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e67b2-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="e67b2-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e67b2-108">ByFabricObject</span><span class="sxs-lookup"><span data-stu-id="e67b2-108">ByFabricObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e67b2-109">ByServerObject</span><span class="sxs-lookup"><span data-stu-id="e67b2-109">ByServerObject</span></span>
```
Get-AzureRmSiteRecoveryStorageClassification -Server <ASRServer> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e67b2-110">설명은</span><span class="sxs-lookup"><span data-stu-id="e67b2-110">DESCRIPTION</span></span>
<span data-ttu-id="e67b2-111">**AzureRmSiteRecoveryStorageClassification** Cmdlet은 Azure Site Recovery의 저장소 분류를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e67b2-111">The **Get-AzureRmSiteRecoveryStorageClassification** cmdlet gets storage classifications in Azure Site Recovery.</span></span>

## <span data-ttu-id="e67b2-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e67b2-112">EXAMPLES</span></span>

## <span data-ttu-id="e67b2-113">변수</span><span class="sxs-lookup"><span data-stu-id="e67b2-113">PARAMETERS</span></span>

### <span data-ttu-id="e67b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e67b2-114">-DefaultProfile</span></span>
<span data-ttu-id="e67b2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e67b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e67b2-116">-패브릭</span><span class="sxs-lookup"><span data-stu-id="e67b2-116">-Fabric</span></span>
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

### <span data-ttu-id="e67b2-117">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e67b2-117">-FriendlyName</span></span>
<span data-ttu-id="e67b2-118">이 cmdlet이 가져오는 저장소 분류의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e67b2-118">Specifies the friendly name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67b2-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e67b2-119">-Name</span></span>
<span data-ttu-id="e67b2-120">이 cmdlet이 가져오는 저장소 분류의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e67b2-120">Specifies the name of the storage classification that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e67b2-121">-서버</span><span class="sxs-lookup"><span data-stu-id="e67b2-121">-Server</span></span>
```yaml
Type: ASRServer
Parameter Sets: ByServerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e67b2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e67b2-122">CommonParameters</span></span>
<span data-ttu-id="e67b2-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e67b2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e67b2-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e67b2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e67b2-125">입력</span><span class="sxs-lookup"><span data-stu-id="e67b2-125">INPUTS</span></span>

### <span data-ttu-id="e67b2-126">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="e67b2-126">ASRFabric</span></span>
<span data-ttu-id="e67b2-127">' Fabric ' 매개 변수는 파이프라인에서 ' ASRFabric ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e67b2-127">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

### <span data-ttu-id="e67b2-128">ASRServer</span><span class="sxs-lookup"><span data-stu-id="e67b2-128">ASRServer</span></span>
<span data-ttu-id="e67b2-129">' Server ' 매개 변수는 파이프라인에서 ' ASRServer ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e67b2-129">Parameter 'Server' accepts value of type 'ASRServer' from the pipeline</span></span>

## <span data-ttu-id="e67b2-130">출력</span><span class="sxs-lookup"><span data-stu-id="e67b2-130">OUTPUTS</span></span>

### <span data-ttu-id="e67b2-131">System.webserver. t e 1.aspx ' 1 [Microsoft SiteRecovery. ASRStorageClassification]</span><span class="sxs-lookup"><span data-stu-id="e67b2-131">System.Collections.Generic.IEnumerable\`1[Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification]</span></span>

## <span data-ttu-id="e67b2-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e67b2-132">NOTES</span></span>

## <span data-ttu-id="e67b2-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e67b2-133">RELATED LINKS</span></span>

