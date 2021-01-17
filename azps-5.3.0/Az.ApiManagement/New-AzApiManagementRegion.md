---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 2259990c568dbf6fd5b7bc6f8bff34c464a082ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382425"
---
# <span data-ttu-id="79ff8-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="79ff8-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="79ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="79ff8-103">PsApiManagementRegion의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79ff8-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="79ff8-104">구문</span><span class="sxs-lookup"><span data-stu-id="79ff8-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79ff8-105">설명</span><span class="sxs-lookup"><span data-stu-id="79ff8-105">DESCRIPTION</span></span>
<span data-ttu-id="79ff8-106">PsApiManagementRegion의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="79ff8-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="79ff8-107">이 명령은 New-AzApiManagement 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79ff8-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="79ff8-108">예제</span><span class="sxs-lookup"><span data-stu-id="79ff8-108">EXAMPLES</span></span>

### <span data-ttu-id="79ff8-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="79ff8-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="79ff8-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="79ff8-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="79ff8-111">미국 중부에 추가 지역을 사용하여 미국 서부 지역에 외부 VpnType의 ApiManagement 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79ff8-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="79ff8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79ff8-112">PARAMETERS</span></span>

### <span data-ttu-id="79ff8-113">-Capacity</span><span class="sxs-lookup"><span data-stu-id="79ff8-113">-Capacity</span></span>
<span data-ttu-id="79ff8-114">Azure API Management 서비스 추가 지역의 SKU 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="79ff8-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="79ff8-115">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="79ff8-115">Default value is 1.</span></span>

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

### <span data-ttu-id="79ff8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79ff8-116">-DefaultProfile</span></span>
<span data-ttu-id="79ff8-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79ff8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79ff8-118">-Location</span><span class="sxs-lookup"><span data-stu-id="79ff8-118">-Location</span></span>
<span data-ttu-id="79ff8-119">Api Management 서비스에 대해 지원되는 지역 중에서 새 배포 지역의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="79ff8-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="79ff8-120">유효한 위치를 얻습니다. -ProviderNamespace Get-AzResourceProvider "Microsoft.ApiManagement" cmdlet을 사용합니다. | where {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="79ff8-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="79ff8-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="79ff8-121">-VirtualNetwork</span></span>
<span data-ttu-id="79ff8-122">Azure API Management 배포 지역의 Virtual Network 구성</span><span class="sxs-lookup"><span data-stu-id="79ff8-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="79ff8-123">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="79ff8-123">Default value is $null.</span></span>

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

### <span data-ttu-id="79ff8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79ff8-124">CommonParameters</span></span>
<span data-ttu-id="79ff8-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="79ff8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79ff8-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79ff8-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79ff8-127">입력</span><span class="sxs-lookup"><span data-stu-id="79ff8-127">INPUTS</span></span>

### <span data-ttu-id="79ff8-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="79ff8-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="79ff8-129">출력</span><span class="sxs-lookup"><span data-stu-id="79ff8-129">OUTPUTS</span></span>

### <span data-ttu-id="79ff8-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="79ff8-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="79ff8-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="79ff8-131">NOTES</span></span>

## <span data-ttu-id="79ff8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79ff8-132">RELATED LINKS</span></span>
