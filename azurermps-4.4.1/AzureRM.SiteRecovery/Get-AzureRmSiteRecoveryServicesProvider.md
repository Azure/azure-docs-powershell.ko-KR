---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: EB68FC6B-310F-41DB-B870-B907147F8513
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: e61136122873f7837120065194252aba145ea733
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535408"
---
# <span data-ttu-id="45d67-101">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="45d67-101">Get-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="45d67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45d67-102">SYNOPSIS</span></span>
<span data-ttu-id="45d67-103">자격 증명 모음의 Azure Site Recovery 제공자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45d67-103">Gets information on the Azure Site Recovery providers in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45d67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45d67-104">SYNTAX</span></span>

### <span data-ttu-id="45d67-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="45d67-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Fabric <ASRFabric> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45d67-106">ByName</span><span class="sxs-lookup"><span data-stu-id="45d67-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -Name <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45d67-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="45d67-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryServicesProvider -FriendlyName <String> -Fabric <ASRFabric>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45d67-108">설명은</span><span class="sxs-lookup"><span data-stu-id="45d67-108">DESCRIPTION</span></span>
<span data-ttu-id="45d67-109">**AzureRmSiteRecoveryServicesProvider** cmdlet은 자격 증명 모음의 Azure Site Recovery 공급자에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45d67-109">The **Get-AzureRmSiteRecoveryServicesProvider** cmdlet gets information on the Azure Site Recovery providers in the vault.</span></span>

## <span data-ttu-id="45d67-110">예제의</span><span class="sxs-lookup"><span data-stu-id="45d67-110">EXAMPLES</span></span>

## <span data-ttu-id="45d67-111">변수</span><span class="sxs-lookup"><span data-stu-id="45d67-111">PARAMETERS</span></span>

### <span data-ttu-id="45d67-112">-패브릭</span><span class="sxs-lookup"><span data-stu-id="45d67-112">-Fabric</span></span>
<span data-ttu-id="45d67-113">Azure Site Recovery Fabric 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d67-113">Specifies the Azure Site Recovery Fabric object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRFabric
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="45d67-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="45d67-114">-FriendlyName</span></span>
<span data-ttu-id="45d67-115">이 cmdlet이 가져오는 Azure Site Recovery 공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d67-115">Specifies the friendly name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d67-116">-이름</span><span class="sxs-lookup"><span data-stu-id="45d67-116">-Name</span></span>
<span data-ttu-id="45d67-117">이 cmdlet이 가져오는 Azure Site Recovery 공급자의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d67-117">Specifies the name of the Azure Site Recovery Provider that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45d67-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45d67-118">-DefaultProfile</span></span>
<span data-ttu-id="45d67-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45d67-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45d67-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45d67-120">CommonParameters</span></span>
<span data-ttu-id="45d67-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d67-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45d67-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45d67-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45d67-123">입력</span><span class="sxs-lookup"><span data-stu-id="45d67-123">INPUTS</span></span>

### <span data-ttu-id="45d67-124">ASRFabric</span><span class="sxs-lookup"><span data-stu-id="45d67-124">ASRFabric</span></span>
<span data-ttu-id="45d67-125">' Fabric ' 매개 변수는 파이프라인에서 ' ASRFabric ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="45d67-125">Parameter 'Fabric' accepts value of type 'ASRFabric' from the pipeline</span></span>

## <span data-ttu-id="45d67-126">출력</span><span class="sxs-lookup"><span data-stu-id="45d67-126">OUTPUTS</span></span>

### <span data-ttu-id="45d67-127">System.webserver. t e r ' 1 [[SiteRecovery Rrecovery서비스 공급자, Microsoft Azure. SiteRecovery, Version = 2.0.1.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="45d67-127">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="45d67-128">상속자</span><span class="sxs-lookup"><span data-stu-id="45d67-128">NOTES</span></span>

## <span data-ttu-id="45d67-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45d67-129">RELATED LINKS</span></span>

[<span data-ttu-id="45d67-130">제거-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="45d67-130">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="45d67-131">업데이트-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="45d67-131">Update-AzureRmSiteRecoveryServicesProvider</span></span>](./Update-AzureRmSiteRecoveryServicesProvider.md)
