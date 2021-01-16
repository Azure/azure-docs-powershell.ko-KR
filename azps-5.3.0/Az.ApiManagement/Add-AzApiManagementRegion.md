---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: 172bd1490b105b942dc706afe9440030d39d5c49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494495"
---
# <span data-ttu-id="115af-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="115af-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="115af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="115af-102">SYNOPSIS</span></span>
<span data-ttu-id="115af-103">PsApiManagement 인스턴스에 새 배포 지역을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="115af-104">구문</span><span class="sxs-lookup"><span data-stu-id="115af-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="115af-105">설명</span><span class="sxs-lookup"><span data-stu-id="115af-105">DESCRIPTION</span></span>
<span data-ttu-id="115af-106">**Add-AzApiManagementRegion** cmdlet은 **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement** 형식의 **제공된 인스턴스의 AdditionalRegions** 컬렉션에 **PsApiManagementRegion** 유형의 새 인스턴스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="115af-107">이 cmdlet은 자체적으로 배포하지는 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="115af-108">API Management의 배포를 업데이트하기 위해 수정된 **PsApiManagement** 인스턴스를 Set-AzApiManagement에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="115af-109">예제</span><span class="sxs-lookup"><span data-stu-id="115af-109">EXAMPLES</span></span>

### <span data-ttu-id="115af-110">예제 1: PsApiManagement 인스턴스에 새 배포 지역 추가</span><span class="sxs-lookup"><span data-stu-id="115af-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="115af-111">이 명령은 **PsApiManagement** 인스턴스에 두 개의 프리미엄 SKU 단위와 미국 동부라는 지역을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="115af-112">예제 2: PsApiManagement 인스턴스에 새 배포 지역 추가 및 배포 업데이트</span><span class="sxs-lookup"><span data-stu-id="115af-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="115af-113">이 명령은 **PsApiManagement** 개체를, 미국 동부라는 지역에 대해 두 개의 프리미엄 SKU 단위를 추가한 다음, 배포를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="115af-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="115af-114">PARAMETERS</span></span>

### <span data-ttu-id="115af-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="115af-115">-ApiManagement</span></span>
<span data-ttu-id="115af-116">이 cmdlet이 추가 배포 지역을 추가하는 **PsApiManagement** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="115af-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="115af-117">-Capacity</span></span>
<span data-ttu-id="115af-118">배포 지역의 SKU 용량을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="115af-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="115af-119">-DefaultProfile</span></span>
<span data-ttu-id="115af-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="115af-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="115af-121">-Location</span><span class="sxs-lookup"><span data-stu-id="115af-121">-Location</span></span>
<span data-ttu-id="115af-122">Api Management 서비스에 대해 지원되는 지역 중에서 새 배포 지역의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="115af-123">유효한 위치를 얻습니다. -ProviderNamespace Get-AzResourceProvider "Microsoft.ApiManagement" cmdlet을 사용합니다. | where {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="115af-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="115af-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="115af-124">-Sku</span></span>
<span data-ttu-id="115af-125">배포 지역의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="115af-126">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="115af-126">Valid values are:</span></span> 
- <span data-ttu-id="115af-127">개발자</span><span class="sxs-lookup"><span data-stu-id="115af-127">Developer</span></span>
- <span data-ttu-id="115af-128">표준</span><span class="sxs-lookup"><span data-stu-id="115af-128">Standard</span></span>
- <span data-ttu-id="115af-129">프리미엄</span><span class="sxs-lookup"><span data-stu-id="115af-129">Premium</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115af-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="115af-130">-VirtualNetwork</span></span>
<span data-ttu-id="115af-131">가상 네트워크 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-131">Specifies a virtual network configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="115af-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="115af-132">CommonParameters</span></span>
<span data-ttu-id="115af-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="115af-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="115af-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="115af-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="115af-135">입력</span><span class="sxs-lookup"><span data-stu-id="115af-135">INPUTS</span></span>

### <span data-ttu-id="115af-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="115af-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="115af-137">출력</span><span class="sxs-lookup"><span data-stu-id="115af-137">OUTPUTS</span></span>

### <span data-ttu-id="115af-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="115af-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="115af-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="115af-139">NOTES</span></span>
* <span data-ttu-id="115af-140">cmdlet은 업데이트된 **PsApiManagement 인스턴스를 파이프라인에** 쓴다.</span><span class="sxs-lookup"><span data-stu-id="115af-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="115af-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="115af-141">RELATED LINKS</span></span>

[<span data-ttu-id="115af-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="115af-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="115af-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="115af-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="115af-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="115af-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


