---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementRegion.md
ms.openlocfilehash: 8d292f6e03661ae55a63686a0282ce65292087f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526399"
---
# <span data-ttu-id="79a1b-101">New-AzureRmApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="79a1b-101">New-AzureRmApiManagementRegion</span></span>

## <span data-ttu-id="79a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="79a1b-103">PsApiManagementRegion의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79a1b-103">Creates an instance of PsApiManagementRegion.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79a1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79a1b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79a1b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="79a1b-106">PsApiManagementRegion의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="79a1b-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="79a1b-107">이 명령은 New-AzureRmApiManagement 명령에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="79a1b-107">This command is to be used with New-AzureRmApiManagement command.</span></span>

## <span data-ttu-id="79a1b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="79a1b-108">EXAMPLES</span></span>

### <span data-ttu-id="79a1b-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="79a1b-109">Example 1</span></span>
```
$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="79a1b-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="79a1b-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzureRmApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzureRmApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="79a1b-111">미국 지역에서 중앙 미국에 추가 지역을 사용 하 여 외부 VpnType의 ApiManagement 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79a1b-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="79a1b-112">변수</span><span class="sxs-lookup"><span data-stu-id="79a1b-112">PARAMETERS</span></span>

### <span data-ttu-id="79a1b-113">용량</span><span class="sxs-lookup"><span data-stu-id="79a1b-113">-Capacity</span></span>
<span data-ttu-id="79a1b-114">Azure API Management 서비스의 Sku 용량 추가 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="79a1b-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="79a1b-115">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="79a1b-115">Default value is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79a1b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79a1b-116">-DefaultProfile</span></span>
<span data-ttu-id="79a1b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79a1b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79a1b-118">-위치</span><span class="sxs-lookup"><span data-stu-id="79a1b-118">-Location</span></span>
<span data-ttu-id="79a1b-119">Api Management 서비스에 대해 지원 되는 지역에서 새 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79a1b-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="79a1b-120">유효한 위치를 얻으려면 cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="79a1b-120">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="79a1b-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="79a1b-121">-VirtualNetwork</span></span>
<span data-ttu-id="79a1b-122">Azure API Management 배포 영역의 가상 네트워크 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="79a1b-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="79a1b-123">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="79a1b-123">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79a1b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79a1b-124">CommonParameters</span></span>
<span data-ttu-id="79a1b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79a1b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79a1b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79a1b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79a1b-127">입력</span><span class="sxs-lookup"><span data-stu-id="79a1b-127">INPUTS</span></span>

### <span data-ttu-id="79a1b-128">ApiManagement. PsApiManagementVirtualNetwork/.</span><span class="sxs-lookup"><span data-stu-id="79a1b-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="79a1b-129">출력</span><span class="sxs-lookup"><span data-stu-id="79a1b-129">OUTPUTS</span></span>

### <span data-ttu-id="79a1b-130">ApiManagement. PsApiManagementRegion/.</span><span class="sxs-lookup"><span data-stu-id="79a1b-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="79a1b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="79a1b-131">NOTES</span></span>

## <span data-ttu-id="79a1b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79a1b-132">RELATED LINKS</span></span>
