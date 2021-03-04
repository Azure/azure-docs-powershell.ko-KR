---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9D4A68A8-0A39-4C9A-8EA6-391A5E7A0E25
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementRegion.md
ms.openlocfilehash: ce1183588458dc0213bff77493caf41a9b1d2766
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994639"
---
# <span data-ttu-id="a5ac2-101">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a5ac2-101">Add-AzApiManagementRegion</span></span>

## <span data-ttu-id="a5ac2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ac2-103">PsApiManagement 인스턴스에 새 배포 지역을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-103">Adds new deployment regions to a PsApiManagement instance.</span></span>

## <span data-ttu-id="a5ac2-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5ac2-104">SYNTAX</span></span>

```
Add-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> [-Sku <PsApiManagementSku>]
 [-Capacity <Int32>] [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a5ac2-105">설명</span><span class="sxs-lookup"><span data-stu-id="a5ac2-105">DESCRIPTION</span></span>
<span data-ttu-id="a5ac2-106">**Add-AzApiManagementRegion** cmdlet은 **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement의** 제공된 인스턴스의 추가Regions 컬렉션에 **PsApiManagementRegion** 형식의 새 인스턴스를 추가합니다. </span><span class="sxs-lookup"><span data-stu-id="a5ac2-106">The **Add-AzApiManagementRegion** cmdlet adds new instance of type **PsApiManagementRegion** to the collection of **AdditionalRegions** of provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="a5ac2-107">이 cmdlet은 자체적으로 배포하지 않지만 메모리 내 **PsApiManagement** 인스턴스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-107">This cmdlet does not deploy anything by itself but updates instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="a5ac2-108">API Management의 배포를 업데이트하기 위해 수정된 **PsApiManagement** 인스턴스를 Set-AzApiManagement로 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-108">To update a deployment of an API Management pass the modified **PsApiManagement** Instance to Set-AzApiManagement.</span></span>

## <span data-ttu-id="a5ac2-109">예제</span><span class="sxs-lookup"><span data-stu-id="a5ac2-109">EXAMPLES</span></span>

### <span data-ttu-id="a5ac2-110">예제 1: PsApiManagement 인스턴스에 새 배포 지역 추가</span><span class="sxs-lookup"><span data-stu-id="a5ac2-110">Example 1: Add new deployment regions to a PsApiManagement instance</span></span>
```
PS C:\>Add-AzApiManagementRegion -ApiManagement $ApiManagement -Location "East US" -Sku "Premium" -Capacity 2
```

<span data-ttu-id="a5ac2-111">이 명령은 두 개의 프리미엄 SKU 단위와 미국 동부라는 지역을 **PsApiManagement 인스턴스에 추가합니다.**</span><span class="sxs-lookup"><span data-stu-id="a5ac2-111">This command adds two premium SKU units and the region named East US to the **PsApiManagement** instance.</span></span>

### <span data-ttu-id="a5ac2-112">예제 2: PsApiManagement 인스턴스에 새 배포 지역 추가 및 배포 업데이트</span><span class="sxs-lookup"><span data-stu-id="a5ac2-112">Example 2: Add new deployment regions to a PsApiManagement instance and then update deployment</span></span>
```powershell
PS C:\>$service = Get-AzApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\>$service = Add-AzApiManagementRegion -ApiManagement $service -Location $secondarylocation -VirtualNetwork $additionalRegionVirtualNetwork
PS C:\>$service = Set-AzApiManagement -InputObject $service -PassThru
```

<span data-ttu-id="a5ac2-113">이 명령은 **PsApiManagement** 개체를, 미국 동부라는 지역에 대해 두 개의 프리미엄 SKU 단위를 추가한 다음 배포를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-113">This command gets a **PsApiManagement** object, adds two premium SKU units for the region named East US, and then updates deployment.</span></span>

## <span data-ttu-id="a5ac2-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a5ac2-114">PARAMETERS</span></span>

### <span data-ttu-id="a5ac2-115">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5ac2-115">-ApiManagement</span></span>
<span data-ttu-id="a5ac2-116">이 cmdlet에서 추가 배포 지역을 추가하는 **PsApiManagement** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-116">Specifies the **PsApiManagement** instance that this cmdlet adds additional deployment regions to.</span></span>

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

### <span data-ttu-id="a5ac2-117">-Capacity</span><span class="sxs-lookup"><span data-stu-id="a5ac2-117">-Capacity</span></span>
<span data-ttu-id="a5ac2-118">배포 지역의 SKU 용량을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-118">Specifies the SKU capacity of the deployment region.</span></span>

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

### <span data-ttu-id="a5ac2-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ac2-119">-DefaultProfile</span></span>
<span data-ttu-id="a5ac2-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5ac2-121">-Location</span><span class="sxs-lookup"><span data-stu-id="a5ac2-121">-Location</span></span>
<span data-ttu-id="a5ac2-122">Api Management 서비스에 대해 지원되는 지역 사이에 새 배포 지역의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-122">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="a5ac2-123">유효한 위치를 얻게 Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | 여기서 {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="a5ac2-123">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="a5ac2-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="a5ac2-124">-Sku</span></span>
<span data-ttu-id="a5ac2-125">배포 지역의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-125">Specifies the tier of the deployment region.</span></span>
<span data-ttu-id="a5ac2-126">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="a5ac2-126">Valid values are:</span></span> 
- <span data-ttu-id="a5ac2-127">개발자</span><span class="sxs-lookup"><span data-stu-id="a5ac2-127">Developer</span></span>
- <span data-ttu-id="a5ac2-128">표준</span><span class="sxs-lookup"><span data-stu-id="a5ac2-128">Standard</span></span>
- <span data-ttu-id="a5ac2-129">프리미엄</span><span class="sxs-lookup"><span data-stu-id="a5ac2-129">Premium</span></span>

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

### <span data-ttu-id="a5ac2-130">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="a5ac2-130">-VirtualNetwork</span></span>
<span data-ttu-id="a5ac2-131">가상 네트워크 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-131">Specifies a virtual network configuration.</span></span>

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

### <span data-ttu-id="a5ac2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ac2-132">CommonParameters</span></span>
<span data-ttu-id="a5ac2-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ac2-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5ac2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ac2-135">입력</span><span class="sxs-lookup"><span data-stu-id="a5ac2-135">INPUTS</span></span>

### <span data-ttu-id="a5ac2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5ac2-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="a5ac2-137">출력</span><span class="sxs-lookup"><span data-stu-id="a5ac2-137">OUTPUTS</span></span>

### <span data-ttu-id="a5ac2-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5ac2-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="a5ac2-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5ac2-139">NOTES</span></span>
* <span data-ttu-id="a5ac2-140">cmdlet은 파이프라인에 **업데이트된 PsApiManagement 인스턴스를** 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ac2-140">The cmdlet writes updated **PsApiManagement** instance to pipeline.</span></span>

## <span data-ttu-id="a5ac2-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5ac2-141">RELATED LINKS</span></span>

[<span data-ttu-id="a5ac2-142">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a5ac2-142">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="a5ac2-143">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="a5ac2-143">Update-AzApiManagementRegion</span></span>](./Update-AzApiManagementRegion.md)

[<span data-ttu-id="a5ac2-144">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="a5ac2-144">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)


