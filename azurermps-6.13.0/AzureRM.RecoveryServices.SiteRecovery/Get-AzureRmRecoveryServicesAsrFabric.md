---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrFabric.md
ms.openlocfilehash: db93d022d2abd6d3c6cecfe32b1f82be4483e850
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531959"
---
# <span data-ttu-id="018fb-101">Get-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="018fb-101">Get-AzureRmRecoveryServicesAsrFabric</span></span>

## <span data-ttu-id="018fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="018fb-102">SYNOPSIS</span></span>
<span data-ttu-id="018fb-103">Azure Site Recovery 패브릭의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="018fb-103">Get the details of an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="018fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="018fb-104">SYNTAX</span></span>

### <span data-ttu-id="018fb-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="018fb-105">Default (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="018fb-106">ByName</span><span class="sxs-lookup"><span data-stu-id="018fb-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="018fb-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="018fb-107">ByFriendlyName</span></span>
```
Get-AzureRmRecoveryServicesAsrFabric -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="018fb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="018fb-108">DESCRIPTION</span></span>
<span data-ttu-id="018fb-109">**AzureRmRecoveryServicesAsrFabric** cmdlet은 지정 된 Azure Site recovery 패브릭 또는 복구 서비스 자격 증명 모음의 모든 Azure Site recovery 패브릭에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="018fb-109">The **Get-AzureRmRecoveryServicesAsrFabric** cmdlet gets the properties of a specified Azure Site Recovery Fabric or all Azure Site Recovery Fabrics in a Recovery Service vault.</span></span>

## <span data-ttu-id="018fb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="018fb-110">EXAMPLES</span></span>

### <span data-ttu-id="018fb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="018fb-111">Example 1</span></span>
```
PS C:\> $fabrics = Get-AzureRmRecoveryServicesAsrFabric
```

<span data-ttu-id="018fb-112">자격 증명 모음의 모든 Azure Site Recovery 패브릭을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="018fb-112">Returns all the Azure Site Recovery fabrics in the vault.</span></span>

### <span data-ttu-id="018fb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="018fb-113">Example 2</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -Name xxxx

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="018fb-114">이름 xxxx를 사용 하 여 azure site recovery fabric을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="018fb-114">Return azure site recovery fabric with name xxxx.</span></span>

### <span data-ttu-id="018fb-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="018fb-115">Example 3</span></span>
```
PS C:\> $fabric = Get-AzureRmRecoveryServicesAsrFabric -FriendlyName XXXXXXXXXX

Name                  : xxxx
FriendlyName          : XXXXXXXXXX
ID                    : /Subscriptions/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX/resourceGroups/canaryexproute/providers/Microsoft.RecoveryServices/vaults/XXXXXXXXXXXXX/replicationFabrics/XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
FabricType            : VMware
SiteIdentifier        : XXXXXXXXxxxxxxxxxxx
FabricSpecificDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVMWareSpecificDetails
```

<span data-ttu-id="018fb-116">이름 xxxx를 사용 하 여 azure site recovery fabric을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="018fb-116">Return azure site recovery fabric with friendly name xxxx.</span></span>

## <span data-ttu-id="018fb-117">변수</span><span class="sxs-lookup"><span data-stu-id="018fb-117">PARAMETERS</span></span>

### <span data-ttu-id="018fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="018fb-118">-DefaultProfile</span></span>
<span data-ttu-id="018fb-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="018fb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="018fb-120">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="018fb-120">-FriendlyName</span></span>
<span data-ttu-id="018fb-121">패브릭의 친근 한 이름으로 ASR 패브릭을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="018fb-121">Search for the ASR fabric by the friendly name of the fabric.</span></span>

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

### <span data-ttu-id="018fb-122">-이름</span><span class="sxs-lookup"><span data-stu-id="018fb-122">-Name</span></span>
<span data-ttu-id="018fb-123">패브릭 이름으로 ASR 패브릭을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="018fb-123">Search for the ASR fabric by the name of the fabric.</span></span>

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

### <span data-ttu-id="018fb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018fb-124">CommonParameters</span></span>
<span data-ttu-id="018fb-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="018fb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018fb-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="018fb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018fb-127">입력</span><span class="sxs-lookup"><span data-stu-id="018fb-127">INPUTS</span></span>

### <span data-ttu-id="018fb-128">않아야</span><span class="sxs-lookup"><span data-stu-id="018fb-128">None</span></span>

## <span data-ttu-id="018fb-129">출력</span><span class="sxs-lookup"><span data-stu-id="018fb-129">OUTPUTS</span></span>

### <span data-ttu-id="018fb-130">System.webserver. List ' 1 [[SiteRecovery. e r m, Microsoft azure. SiteRecovery, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = null]]을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="018fb-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="018fb-131">상속자</span><span class="sxs-lookup"><span data-stu-id="018fb-131">NOTES</span></span>

## <span data-ttu-id="018fb-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="018fb-132">RELATED LINKS</span></span>

[<span data-ttu-id="018fb-133">새로운 AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="018fb-133">New-AzureRmRecoveryServicesAsrFabric</span></span>](./New-AzureRmRecoveryServicesAsrFabric.md)

[<span data-ttu-id="018fb-134">제거-AzureRmRecoveryServicesAsrFabric</span><span class="sxs-lookup"><span data-stu-id="018fb-134">Remove-AzureRmRecoveryServicesAsrFabric</span></span>](./Remove-AzureRmRecoveryServicesAsrFabric.md)
