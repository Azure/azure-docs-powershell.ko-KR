---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 28EEB54B-C8C9-4C20-9454-5069C23583B9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 591cbcbc4663bde7b9d6e9bd4e35a1e91728cd85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529122"
---
# <span data-ttu-id="10ba8-101">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="10ba8-101">Get-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="10ba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="10ba8-103">Azure Site Recovery 패브릭의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10ba8-103">Get the properties of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10ba8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10ba8-104">SYNTAX</span></span>

### <span data-ttu-id="10ba8-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="10ba8-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoveryFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10ba8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="10ba8-106">ByName</span></span>
```
Get-AzureRmSiteRecoveryFabric -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10ba8-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="10ba8-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoveryFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10ba8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="10ba8-108">DESCRIPTION</span></span>
<span data-ttu-id="10ba8-109">**AzureRmSiteRecoveryFabric** cmdlet은 지정 된 Azure Site recovery 패브릭 또는 복구 서비스 자격 증명 모음의 모든 Azure Site recovery 패브릭에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="10ba8-109">The **Get-AzureRmSiteRecoveryFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="10ba8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="10ba8-110">EXAMPLES</span></span>

## <span data-ttu-id="10ba8-111">변수</span><span class="sxs-lookup"><span data-stu-id="10ba8-111">PARAMETERS</span></span>

### <span data-ttu-id="10ba8-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="10ba8-112">-FriendlyName</span></span>
<span data-ttu-id="10ba8-113">Azure Site Recovery 패브릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ba8-113">Specifies the friendly name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="10ba8-114">-이름</span><span class="sxs-lookup"><span data-stu-id="10ba8-114">-Name</span></span>
<span data-ttu-id="10ba8-115">Azure Site Recovery 패브릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ba8-115">Specifies the name of the Azure Site Recovery Fabric.</span></span>

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

### <span data-ttu-id="10ba8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10ba8-116">-DefaultProfile</span></span>
<span data-ttu-id="10ba8-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10ba8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10ba8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10ba8-118">CommonParameters</span></span>
<span data-ttu-id="10ba8-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10ba8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10ba8-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10ba8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10ba8-121">입력</span><span class="sxs-lookup"><span data-stu-id="10ba8-121">INPUTS</span></span>

## <span data-ttu-id="10ba8-122">출력</span><span class="sxs-lookup"><span data-stu-id="10ba8-122">OUTPUTS</span></span>

### <span data-ttu-id="10ba8-123">SiteRecovery ' 1 [[Microsoft Azure. SiteRecovery, Version = 2.0.1.0, Culture = 중립, PublicKeyToken = null]] 목록. List ' a '</span><span class="sxs-lookup"><span data-stu-id="10ba8-123">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.SiteRecovery, Version=2.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="10ba8-124">상속자</span><span class="sxs-lookup"><span data-stu-id="10ba8-124">NOTES</span></span>

## <span data-ttu-id="10ba8-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10ba8-125">RELATED LINKS</span></span>

[<span data-ttu-id="10ba8-126">새로운 AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="10ba8-126">New-AzureRmSiteRecoveryFabric</span></span>](./New-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="10ba8-127">제거-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="10ba8-127">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
