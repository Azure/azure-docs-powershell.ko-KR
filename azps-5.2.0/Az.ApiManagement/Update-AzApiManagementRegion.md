---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 5B7B285A-6418-44D7-BD78-E14AFFAA7765
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/update-azapimanagementregion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Update-AzApiManagementRegion.md
ms.openlocfilehash: 8552592acb45702c866c8d918121b8dd61d126a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346101"
---
# <span data-ttu-id="9e8aa-101">Update-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9e8aa-101">Update-AzApiManagementRegion</span></span>

## <span data-ttu-id="9e8aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e8aa-102">SYNOPSIS</span></span>
<span data-ttu-id="9e8aa-103">PsApiManagement 인스턴스의 기존 배포 지역을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-103">Updates existing deployment region in PsApiManagement instance.</span></span>

## <span data-ttu-id="9e8aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="9e8aa-104">SYNTAX</span></span>

```
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Location <String> -Sku <PsApiManagementSku>
 -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e8aa-105">설명</span><span class="sxs-lookup"><span data-stu-id="9e8aa-105">DESCRIPTION</span></span>
<span data-ttu-id="9e8aa-106">**Update-AzApiManagementRegion** cmdlet은 **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** 형식의 기존 인스턴스를 **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement** 형식의 제공된 인스턴스의 **AdditionalRegions** 개체 컬렉션에 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-106">The **Update-AzApiManagementRegion** cmdlet updates an existing instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion** in a collection of **AdditionalRegions** objects of a provided instance of type **Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement**.</span></span>
<span data-ttu-id="9e8aa-107">이 cmdlet은 메모리 내 **PsApiManagement** 인스턴스를 업데이트하는 것만 배포하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-107">This cmdlet does not deploy anything but updates an instance of **PsApiManagement** in-memory.</span></span>
<span data-ttu-id="9e8aa-108">API Management의 배포를 업데이트하기 위해 수정된 **PsApiManagementInstance를** Set-AzApiManagement cmdlet에 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-108">To update a deployment of an API Management use the modified **PsApiManagementInstance** to the Set-AzApiManagement cmdlet.</span></span>

## <span data-ttu-id="9e8aa-109">예제</span><span class="sxs-lookup"><span data-stu-id="9e8aa-109">EXAMPLES</span></span>

### <span data-ttu-id="9e8aa-110">예제 1: PsApiManagement 인스턴스에서 추가 지역의 용량 증가</span><span class="sxs-lookup"><span data-stu-id="9e8aa-110">Example 1: Increases capacity of Additional Region in a PsApiManagement instance</span></span>
```powershell
PS C:\>$apimService = Get-AzApiManagement -ResourceGroupName $resourceGroupName -Name $apiManagementName
PS C:\>$apimService = Update-AzApiManagementRegion -ApiManagement $apimService -Location "North Central US" -Capacity 2 -Sku Premium
PS C:\>$apimService = Set-AzApiManagement -InputObject $apimService -PassThru
```

<span data-ttu-id="9e8aa-111">이 명령은 미국 중남부 및 미국 중북부에 지역이 있는 API Management 프리미엄 SKU 서비스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-111">This command gets the API Management Premium SKU service, having regions in South Central US and North Central US.</span></span> <span data-ttu-id="9e8aa-112">그런 다음 **Set-AzApiManagement를** 사용하여 미국 중북부 지역의 용량을 2로 증가합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-112">It then increases the Capacity of the North Central US region to 2 using the **Set-AzApiManagement**.</span></span> <span data-ttu-id="9e8aa-113">다음 cmdlet **Set-AzApiManagement는** API Management 서비스에 구성 변경을 적용합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-113">The next cmdlet **Set-AzApiManagement** applies the configuration change to the Api Management service.</span></span>

### <span data-ttu-id="9e8aa-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9e8aa-114">Example 2</span></span>

<span data-ttu-id="9e8aa-115">PsApiManagement 인스턴스의 기존 배포 지역을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-115">Updates existing deployment region in PsApiManagement instance.</span></span> <span data-ttu-id="9e8aa-116">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="9e8aa-116">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzApiManagementRegion -ApiManagement <PsApiManagement> -Capacity 2 -Location 'North Central US' -Sku Developer -VirtualNetwork <PsApiManagementVirtualNetwork>
```

## <span data-ttu-id="9e8aa-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9e8aa-117">PARAMETERS</span></span>

### <span data-ttu-id="9e8aa-118">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e8aa-118">-ApiManagement</span></span>
<span data-ttu-id="9e8aa-119">기존 배포 지역을 업데이트할 **PsApiManagement** 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-119">Specifies the **PsApiManagement** instance to update an existing deployment region in.</span></span>

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

### <span data-ttu-id="9e8aa-120">-Capacity</span><span class="sxs-lookup"><span data-stu-id="9e8aa-120">-Capacity</span></span>
<span data-ttu-id="9e8aa-121">배포 지역에 대한 새 SKU 용량 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-121">Specifies the new SKU capacity value for the deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e8aa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e8aa-122">-DefaultProfile</span></span>
<span data-ttu-id="9e8aa-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e8aa-124">-Location</span><span class="sxs-lookup"><span data-stu-id="9e8aa-124">-Location</span></span>
<span data-ttu-id="9e8aa-125">업데이트할 배포 지역의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-125">Specifies the location of the deployment region to update.</span></span>
<span data-ttu-id="9e8aa-126">Api Management 서비스에 대해 지원되는 지역 중에서 새 배포 지역의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-126">Specifies the location of the new deployment region amongst the supported region for Api Management service.</span></span>
<span data-ttu-id="9e8aa-127">유효한 위치를 얻습니다. -ProviderNamespace Get-AzResourceProvider "Microsoft.ApiManagement" cmdlet을 사용합니다. | where {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="9e8aa-127">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e8aa-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="9e8aa-128">-Sku</span></span>
<span data-ttu-id="9e8aa-129">배포 지역에 대한 새 계층 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-129">Specifies the new tier value for the deployment region.</span></span>
<span data-ttu-id="9e8aa-130">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="9e8aa-130">Valid values are:</span></span>
- <span data-ttu-id="9e8aa-131">개발자</span><span class="sxs-lookup"><span data-stu-id="9e8aa-131">Developer</span></span>
- <span data-ttu-id="9e8aa-132">표준</span><span class="sxs-lookup"><span data-stu-id="9e8aa-132">Standard</span></span>
- <span data-ttu-id="9e8aa-133">프리미엄</span><span class="sxs-lookup"><span data-stu-id="9e8aa-133">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium, Basic, Consumption

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e8aa-134">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e8aa-134">-VirtualNetwork</span></span>
<span data-ttu-id="9e8aa-135">배포 지역에 대한 가상 네트워크 구성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-135">Specifies a virtual network configuration for the deployment region.</span></span>
<span data-ttu-id="9e8aa-136">이 $null 전달하면 지역에 대한 가상 네트워크 구성이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-136">Passing $null will remove virtual network configuration for the region.</span></span>

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

### <span data-ttu-id="9e8aa-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e8aa-137">CommonParameters</span></span>
<span data-ttu-id="9e8aa-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e8aa-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9e8aa-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e8aa-140">입력</span><span class="sxs-lookup"><span data-stu-id="9e8aa-140">INPUTS</span></span>

### <span data-ttu-id="9e8aa-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e8aa-141">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

### <span data-ttu-id="9e8aa-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9e8aa-142">System.String</span></span>

### <span data-ttu-id="9e8aa-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span><span class="sxs-lookup"><span data-stu-id="9e8aa-143">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="9e8aa-144">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9e8aa-144">System.Int32</span></span>

### <span data-ttu-id="9e8aa-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="9e8aa-145">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

## <span data-ttu-id="9e8aa-146">출력</span><span class="sxs-lookup"><span data-stu-id="9e8aa-146">OUTPUTS</span></span>

### <span data-ttu-id="9e8aa-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e8aa-147">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="9e8aa-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9e8aa-148">NOTES</span></span>

## <span data-ttu-id="9e8aa-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e8aa-149">RELATED LINKS</span></span>

[<span data-ttu-id="9e8aa-150">Add-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9e8aa-150">Add-AzApiManagementRegion</span></span>](./Add-AzApiManagementRegion.md)

[<span data-ttu-id="9e8aa-151">Remove-AzApiManagementRegion</span><span class="sxs-lookup"><span data-stu-id="9e8aa-151">Remove-AzApiManagementRegion</span></span>](./Remove-AzApiManagementRegion.md)

[<span data-ttu-id="9e8aa-152">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="9e8aa-152">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)
