---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/update-azurermapimanagementdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: f8f0273ab624cd81488734f9b84debc045f6fed2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526360"
---
# <span data-ttu-id="5286f-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="5286f-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="5286f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5286f-102">SYNOPSIS</span></span>
<span data-ttu-id="5286f-103">API Management 서비스의 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5286f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5286f-104">SYNTAX</span></span>

### <span data-ttu-id="5286f-105">UpdateSpecificService (기본값)</span><span class="sxs-lookup"><span data-stu-id="5286f-105">UpdateSpecificService (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5286f-106">UpdateFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="5286f-106">UpdateFromPsApiManagementInstance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5286f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5286f-107">DESCRIPTION</span></span>
<span data-ttu-id="5286f-108">**업데이트 AzureRmApiManagementDeployment** CMDLET은 API Management 서비스의 현재 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="5286f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5286f-109">EXAMPLES</span></span>

### <span data-ttu-id="5286f-110">예제 1: ApiManagement 인스턴스의 배포 업데이트</span><span class="sxs-lookup"><span data-stu-id="5286f-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```powershell
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="5286f-111">이 명령은 API Management 인스턴스의 배포를 세 가지 단위 용량 표준으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="5286f-112">예제 2: ApiManagement 인스턴스 가져오기 및 크기 조정</span><span class="sxs-lookup"><span data-stu-id="5286f-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```powershell
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="5286f-113">이 예제에서는 Api Management 인스턴스를 가져오고, 5 개의 premium 단위로 크기를 조정 하 고, 프리미엄 영역에 3 단위를 추가로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="5286f-114">예제 3: 업데이트 배포 (외부 VNET)</span><span class="sxs-lookup"><span data-stu-id="5286f-114">Example 3: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="5286f-115">이 명령은 기존 API Management 배포를 업데이트 하 고 외부 *VpnType* 에 참가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="5286f-116">예제 4: 업데이트 배포 (내부 VNET)</span><span class="sxs-lookup"><span data-stu-id="5286f-116">Example 4: Update deployment (internal VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="5286f-117">이 명령은 기존 API Management 배포를 업데이트 하 고 내부 *VpnType* 에 참가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="5286f-118">변수</span><span class="sxs-lookup"><span data-stu-id="5286f-118">PARAMETERS</span></span>

### <span data-ttu-id="5286f-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="5286f-119">-AdditionalRegions</span></span>
<span data-ttu-id="5286f-120">Azure API Management의 추가 배포 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5286f-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="5286f-121">-ApiManagement</span></span>
<span data-ttu-id="5286f-122">배포 구성을 가져올 **PsApiManagement** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="5286f-123">인스턴스에 필요한 모든 변경 내용이 이미 있는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: UpdateFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5286f-124">용량</span><span class="sxs-lookup"><span data-stu-id="5286f-124">-Capacity</span></span>
<span data-ttu-id="5286f-125">마스터 Azure API 관리 배포 영역의 SKU 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5286f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5286f-126">-DefaultProfile</span></span>
<span data-ttu-id="5286f-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5286f-128">-위치</span><span class="sxs-lookup"><span data-stu-id="5286f-128">-Location</span></span>
<span data-ttu-id="5286f-129">마스터 API 관리 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-129">Specifies the location of the master API Management deployment region.</span></span>
<span data-ttu-id="5286f-130">유효한 위치를 얻으려면 cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="5286f-130">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5286f-131">-이름</span><span class="sxs-lookup"><span data-stu-id="5286f-131">-Name</span></span>
<span data-ttu-id="5286f-132">이 cmdlet이 업데이트 하는 API 관리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-132">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5286f-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5286f-133">-PassThru</span></span>
<span data-ttu-id="5286f-134">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-134">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5286f-135">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-135">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5286f-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5286f-136">-ResourceGroupName</span></span>
<span data-ttu-id="5286f-137">API Management가 존재 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-137">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5286f-138">-Sku</span><span class="sxs-lookup"><span data-stu-id="5286f-138">-Sku</span></span>
<span data-ttu-id="5286f-139">마스터 Azure API 관리 배포 영역의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-139">Specifies the tier of the master Azure API Management deployment region.</span></span>
<span data-ttu-id="5286f-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5286f-141">디벨로퍼</span><span class="sxs-lookup"><span data-stu-id="5286f-141">Developer</span></span>
- <span data-ttu-id="5286f-142">표준이</span><span class="sxs-lookup"><span data-stu-id="5286f-142">Standard</span></span>
- <span data-ttu-id="5286f-143">Premium</span><span class="sxs-lookup"><span data-stu-id="5286f-143">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: Developer, Standard, Premium, Basic

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5286f-144">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5286f-144">-VirtualNetwork</span></span>
<span data-ttu-id="5286f-145">마스터 Azure API 관리 배포 영역의 가상 네트워크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-145">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: UpdateSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5286f-146">-VpnType</span><span class="sxs-lookup"><span data-stu-id="5286f-146">-VpnType</span></span>
<span data-ttu-id="5286f-147">API Management 배포의 가상 네트워크 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-147">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="5286f-148">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-148">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="5286f-149">않아야.</span><span class="sxs-lookup"><span data-stu-id="5286f-149">None.</span></span>
<span data-ttu-id="5286f-150">API Management 구축은 가상 네트워크의 일부가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-150">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="5286f-151">이 값이 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-151">This is the default value.</span></span> 
- <span data-ttu-id="5286f-152">내부.</span><span class="sxs-lookup"><span data-stu-id="5286f-152">External.</span></span>
<span data-ttu-id="5286f-153">API Management 배포에 외부 연결 가상 주소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-153">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="5286f-154">내부용.</span><span class="sxs-lookup"><span data-stu-id="5286f-154">Internal.</span></span>
<span data-ttu-id="5286f-155">API Management 배포에 인트라넷 연결 가상 주소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-155">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: UpdateSpecificService
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5286f-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5286f-156">CommonParameters</span></span>
<span data-ttu-id="5286f-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5286f-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5286f-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5286f-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5286f-159">입력</span><span class="sxs-lookup"><span data-stu-id="5286f-159">INPUTS</span></span>

### <span data-ttu-id="5286f-160">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="5286f-160">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="5286f-161">매개 변수: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5286f-161">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="5286f-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5286f-162">System.String</span></span>

### <span data-ttu-id="5286f-163">ApiManagement. PsApiManagementSku/.</span><span class="sxs-lookup"><span data-stu-id="5286f-163">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku</span></span>

### <span data-ttu-id="5286f-164">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="5286f-164">System.Int32</span></span>

### <span data-ttu-id="5286f-165">ApiManagement. PsApiManagementVirtualNetwork/.</span><span class="sxs-lookup"><span data-stu-id="5286f-165">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="5286f-166">ApiManagement. PsApiManagementVpnType/.</span><span class="sxs-lookup"><span data-stu-id="5286f-166">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType</span></span>

### <span data-ttu-id="5286f-167">System.webserver. IList ' 1 [[ApiManagement. PsApiManagementRegion, Microsoft azure. ApiManagement, Version = 6.1.2.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5286f-167">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion, Microsoft.Azure.Commands.ApiManagement, Version=6.1.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="5286f-168">출력</span><span class="sxs-lookup"><span data-stu-id="5286f-168">OUTPUTS</span></span>

### <span data-ttu-id="5286f-169">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="5286f-169">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="5286f-170">상속자</span><span class="sxs-lookup"><span data-stu-id="5286f-170">NOTES</span></span>

## <span data-ttu-id="5286f-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5286f-171">RELATED LINKS</span></span>

[<span data-ttu-id="5286f-172">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="5286f-172">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


