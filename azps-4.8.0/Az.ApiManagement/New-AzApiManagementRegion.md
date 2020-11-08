---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A4226BFB-AB3B-4883-9D52-5EB7F29D8A71
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementRegion.md
ms.openlocfilehash: 2259990c568dbf6fd5b7bc6f8bff34c464a082ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047992"
---
# <span data-ttu-id="96ad6-101">New-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="96ad6-101">New-AzApiManagementRegion</span></span>

## <span data-ttu-id="96ad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="96ad6-103">PsApiManagementRegion의 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96ad6-103">Creates an instance of PsApiManagementRegion.</span></span>

## <span data-ttu-id="96ad6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96ad6-104">SYNTAX</span></span>

```
New-AzApiManagementRegion -Location <String> [-Capacity <Int32>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96ad6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="96ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="96ad6-106">PsApiManagementRegion의 인스턴스를 만드는 도우미 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="96ad6-106">Helper command to create an instance of PsApiManagementRegion.</span></span>
<span data-ttu-id="96ad6-107">이 명령은 New-AzApiManagement 명령에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="96ad6-107">This command is to be used with New-AzApiManagement command.</span></span>

## <span data-ttu-id="96ad6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="96ad6-108">EXAMPLES</span></span>

### <span data-ttu-id="96ad6-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="96ad6-109">Example 1</span></span>
```
$apimRegion = New-AzApiManagementRegion -Location "Central US" 

$additionalRegions = @($apimRegion)

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -Sku "Premium"
```

### <span data-ttu-id="96ad6-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="96ad6-110">Example 2</span></span>
```
$apimRegionVirtualNetwork = New-AzApiManagementVirtualNetwork -Location "Central US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/centralusvirtualNetwork/subnets/backendSubnet"

$apimRegion = New-AzApiManagementRegion -Location "Central US" -VirtualNetwork $apimRegionVirtualNetwork 

$additionalRegions = @($apimRegion)

$virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc2-4174-a1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"

New-AzApiManagement -ResourceGroupName ContosoGroup -Location "West US" -Name ContosoApi -Organization Contoso -AdminEmail admin@contoso.com -AdditionalRegions $additionalRegions -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="96ad6-111">미국 지역에서 중앙 미국에 추가 지역을 사용 하 여 외부 VpnType의 ApiManagement 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96ad6-111">Creates an ApiManagement service of External VpnType in West US Region, with an Additional Region in Central US.</span></span>

## <span data-ttu-id="96ad6-112">변수</span><span class="sxs-lookup"><span data-stu-id="96ad6-112">PARAMETERS</span></span>

### <span data-ttu-id="96ad6-113">용량</span><span class="sxs-lookup"><span data-stu-id="96ad6-113">-Capacity</span></span>
<span data-ttu-id="96ad6-114">Azure API Management 서비스의 Sku 용량 추가 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="96ad6-114">Sku capacity of the Azure API Management service additional region.</span></span>
<span data-ttu-id="96ad6-115">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="96ad6-115">Default value is 1.</span></span>

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

### <span data-ttu-id="96ad6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96ad6-116">-DefaultProfile</span></span>
<span data-ttu-id="96ad6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96ad6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96ad6-118">-위치</span><span class="sxs-lookup"><span data-stu-id="96ad6-118">-Location</span></span>
<span data-ttu-id="96ad6-119">Api Management 서비스에 대해 지원 되는 지역에서 새 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ad6-119">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="96ad6-120">유효한 위치를 얻으려면 cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="96ad6-120">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="96ad6-121">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="96ad6-121">-VirtualNetwork</span></span>
<span data-ttu-id="96ad6-122">Azure API Management 배포 영역의 가상 네트워크 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="96ad6-122">Virtual Network Configuration of Azure API Management deployment region.</span></span>
<span data-ttu-id="96ad6-123">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="96ad6-123">Default value is $null.</span></span>

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

### <span data-ttu-id="96ad6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96ad6-124">CommonParameters</span></span>
<span data-ttu-id="96ad6-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96ad6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96ad6-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="96ad6-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96ad6-127">입력</span><span class="sxs-lookup"><span data-stu-id="96ad6-127">INPUTS</span></span>

### <span data-ttu-id="96ad6-128">ApiManagement. PsApiManagementVirtualNetwork/.</span><span class="sxs-lookup"><span data-stu-id="96ad6-128">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="96ad6-129">출력</span><span class="sxs-lookup"><span data-stu-id="96ad6-129">OUTPUTS</span></span>

### <span data-ttu-id="96ad6-130">ApiManagement. PsApiManagementRegion/.</span><span class="sxs-lookup"><span data-stu-id="96ad6-130">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion</span></span>

## <span data-ttu-id="96ad6-131">상속자</span><span class="sxs-lookup"><span data-stu-id="96ad6-131">NOTES</span></span>

## <span data-ttu-id="96ad6-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96ad6-132">RELATED LINKS</span></span>
