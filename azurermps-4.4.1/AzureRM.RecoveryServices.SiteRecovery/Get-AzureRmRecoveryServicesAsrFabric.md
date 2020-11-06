---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: dde3873c7fe7ee18ee4745af967eb222833029d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527347"
---
# <span data-ttu-id="de985-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="de985-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="de985-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de985-102">SYNOPSIS</span></span>
<span data-ttu-id="de985-103">Azure Site Recovery 패브릭의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="de985-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de985-104">구문과</span><span class="sxs-lookup"><span data-stu-id="de985-104">SYNTAX</span></span>

### <span data-ttu-id="de985-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="de985-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [<CommonParameters>]
```

### <span data-ttu-id="de985-106">ByName</span><span class="sxs-lookup"><span data-stu-id="de985-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="de985-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="de985-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [<CommonParameters>]
```

## <span data-ttu-id="de985-108">설명은</span><span class="sxs-lookup"><span data-stu-id="de985-108">DESCRIPTION</span></span>
<span data-ttu-id="de985-109">**AzureRmRecoveryServicesAsrFabric** cmdlet은 지정 된 Azure Site recovery 패브릭 또는 복구 서비스 자격 증명 모음의 모든 Azure Site recovery 패브릭에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="de985-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="de985-110">예제의</span><span class="sxs-lookup"><span data-stu-id="de985-110">EXAMPLES</span></span>

### <span data-ttu-id="de985-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="de985-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="de985-112">자격 증명 모음의 모든 Azure Site Recovery 패브릭을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="de985-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

## <span data-ttu-id="de985-113">변수</span><span class="sxs-lookup"><span data-stu-id="de985-113">PARAMETERS</span></span>

### <span data-ttu-id="de985-114">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="de985-114">-FriendlyName</span></span>
<span data-ttu-id="de985-115">패브릭의 친근 한 이름으로 ASR 패브릭을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="de985-115">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="de985-116">-이름</span><span class="sxs-lookup"><span data-stu-id="de985-116">-Name</span></span>
<span data-ttu-id="de985-117">패브릭 이름으로 ASR 패브릭을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="de985-117">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="de985-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de985-118">CommonParameters</span></span>
<span data-ttu-id="de985-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="de985-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de985-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de985-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de985-121">입력</span><span class="sxs-lookup"><span data-stu-id="de985-121">INPUTS</span></span>

### <span data-ttu-id="de985-122">않아야</span><span class="sxs-lookup"><span data-stu-id="de985-122">None</span></span>

## <span data-ttu-id="de985-123">출력</span><span class="sxs-lookup"><span data-stu-id="de985-123">OUTPUTS</span></span>

### <span data-ttu-id="de985-124">System.webserver. List ' 1 [[SiteRecovery. e r m, Microsoft azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]]을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="de985-124">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="de985-125">상속자</span><span class="sxs-lookup"><span data-stu-id="de985-125">NOTES</span></span>

## <span data-ttu-id="de985-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="de985-126">RELATED LINKS</span></span>

[<span data-ttu-id="de985-127">새로운 AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="de985-127">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="de985-128">제거-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="de985-128">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
