---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/get-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 4e65636c732ede20487df0b80973172977c6c832
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534632"
---
# <span data-ttu-id="a22bb-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a22bb-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="a22bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a22bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a22bb-103">자격 증명 모음의 Azure Site Recovery 제공자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a22bb-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a22bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a22bb-104">SYNTAX</span></span>

### <span data-ttu-id="a22bb-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a22bb-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a22bb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a22bb-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a22bb-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="a22bb-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a22bb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a22bb-108">DESCRIPTION</span></span>
<span data-ttu-id="a22bb-109">**AzureRmSiteRecoveryServicesProvider** cmdlet은 자격 증명 모음의 Azure Site Recovery 공급자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a22bb-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="a22bb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a22bb-110">EXAMPLES</span></span>

## <span data-ttu-id="a22bb-111">변수</span><span class="sxs-lookup"><span data-stu-id="a22bb-111">PARAMETERS</span></span>

### <span data-ttu-id="a22bb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a22bb-112">-DefaultProfile</span></span>
<span data-ttu-id="a22bb-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a22bb-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a22bb-114">-패브릭</span><span class="sxs-lookup"><span data-stu-id="a22bb-114">-Fabric</span></span>
<span data-ttu-id="a22bb-115">Azure Site Recovery Fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22bb-115">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a22bb-116">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="a22bb-116">-FriendlyName</span></span>
<span data-ttu-id="a22bb-117">이 cmdlet이 가져오는 Azure Site Recovery 공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22bb-117">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a22bb-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a22bb-118">-Name</span></span>
<span data-ttu-id="a22bb-119">이 cmdlet이 가져오는 Azure Site Recovery 공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22bb-119">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

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

### <span data-ttu-id="a22bb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a22bb-120">CommonParameters</span></span>
<span data-ttu-id="a22bb-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22bb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a22bb-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a22bb-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a22bb-123">입력</span><span class="sxs-lookup"><span data-stu-id="a22bb-123">INPUTS</span></span>

### <span data-ttu-id="a22bb-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="a22bb-124">ASRFabric</span></span>
<span data-ttu-id="a22bb-125">' Fabric ' 매개 변수는 파이프라인에서 ' ASRFabric ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a22bb-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="a22bb-126">출력</span><span class="sxs-lookup"><span data-stu-id="a22bb-126">OUTPUTS</span></span>

### <span data-ttu-id="a22bb-127">System.webserver. t e r ' 1 [[SiteRecovery Rrecovery서비스 공급자, Microsoft Azure. SiteRecovery, Version = 2.0.1.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a22bb-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a22bb-128">상속자</span><span class="sxs-lookup"><span data-stu-id="a22bb-128">NOTES</span></span>

## <span data-ttu-id="a22bb-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a22bb-129">RELATED LINKS</span></span>

[<span data-ttu-id="a22bb-130">제거-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a22bb-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="a22bb-131">업데이트-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="a22bb-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
