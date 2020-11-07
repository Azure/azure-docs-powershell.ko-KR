---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 9601a3a9a64e52938ebad2024bbc9fd1301b920a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711229"
---
# <span data-ttu-id="850ca-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="850ca-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="850ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="850ca-102">SYNOPSIS</span></span>
<span data-ttu-id="850ca-103">Azure Site Recovery 패브릭을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="850ca-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="850ca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="850ca-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="850ca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="850ca-105">DESCRIPTION</span></span>
<span data-ttu-id="850ca-106">**AzureRmSiteRecoveryFabric** cmdlet은 지정 된 형식의 Azure Site Recovery Fabric을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="850ca-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="850ca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="850ca-107">EXAMPLES</span></span>

## <span data-ttu-id="850ca-108">변수</span><span class="sxs-lookup"><span data-stu-id="850ca-108">PARAMETERS</span></span>

### <span data-ttu-id="850ca-109">-이름</span><span class="sxs-lookup"><span data-stu-id="850ca-109">-Name</span></span>
<span data-ttu-id="850ca-110">Azure Site Recovery 패브릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="850ca-110">Specifies the name of the Azure Site Recovery Fabric</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850ca-111">-Type</span><span class="sxs-lookup"><span data-stu-id="850ca-111">-Type</span></span>
<span data-ttu-id="850ca-112">Azure Site Recovery 패브릭 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="850ca-112">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="850ca-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="850ca-113">-DefaultProfile</span></span>
<span data-ttu-id="850ca-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="850ca-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="850ca-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="850ca-115">CommonParameters</span></span>
<span data-ttu-id="850ca-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="850ca-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="850ca-117">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="850ca-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="850ca-118">입력</span><span class="sxs-lookup"><span data-stu-id="850ca-118">INPUTS</span></span>

## <span data-ttu-id="850ca-119">출력</span><span class="sxs-lookup"><span data-stu-id="850ca-119">OUTPUTS</span></span>

### <span data-ttu-id="850ca-120">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="850ca-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="850ca-121">상속자</span><span class="sxs-lookup"><span data-stu-id="850ca-121">NOTES</span></span>

## <span data-ttu-id="850ca-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="850ca-122">RELATED LINKS</span></span>

[<span data-ttu-id="850ca-123">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="850ca-123">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="850ca-124">제거-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="850ca-124">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
