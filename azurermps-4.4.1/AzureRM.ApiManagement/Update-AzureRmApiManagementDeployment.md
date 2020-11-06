---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 56604912-53A0-496D-9BDC-472BCE45A6A2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Update-AzureRmApiManagementDeployment.md
ms.openlocfilehash: e4170dbe2a1ac4ed8ad39bdb7a5db6d7174555e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525740"
---
# <span data-ttu-id="fc987-101">Update-AzureRmApiManagementDeployment</span><span class="sxs-lookup"><span data-stu-id="fc987-101">Update-AzureRmApiManagementDeployment</span></span>

## <span data-ttu-id="fc987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc987-102">SYNOPSIS</span></span>
<span data-ttu-id="fc987-103">API Management 서비스의 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-103">Updates deployment of an API Management Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc987-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fc987-104">SYNTAX</span></span>

### <span data-ttu-id="fc987-105">특정 API Management 서비스 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fc987-105">Specific API Management service (Default)</span></span>
```
Update-AzureRmApiManagementDeployment -ResourceGroupName <String> -Name <String> -Location <String>
 -Sku <PsApiManagementSku> -Capacity <Int32> [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-VpnType <PsApiManagementVpnType>]
 [-AdditionalRegions <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fc987-106">PsApiManagement 인스턴스에서 업데이트</span><span class="sxs-lookup"><span data-stu-id="fc987-106">Update from PsApiManagement instance</span></span>
```
Update-AzureRmApiManagementDeployment -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc987-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fc987-107">DESCRIPTION</span></span>
<span data-ttu-id="fc987-108">**업데이트 AzureRmApiManagementDeployment** CMDLET은 API Management 서비스의 현재 배포를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-108">The **Update-AzureRmApiManagementDeployment** cmdlet updates current deployments of an API Management service.</span></span>

## <span data-ttu-id="fc987-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fc987-109">EXAMPLES</span></span>

### <span data-ttu-id="fc987-110">예제 1: ApiManagement 인스턴스의 배포 업데이트</span><span class="sxs-lookup"><span data-stu-id="fc987-110">Example 1: Update a deployment of an ApiManagement instance</span></span>
```
PS C:\>Update-AzureRmApiManagementDeployment -ResourceGroupName "Contoso" -Name "ContosoApi" -Sku "Standard" -Capacity 3
```

<span data-ttu-id="fc987-111">이 명령은 API Management 인스턴스의 배포를 세 가지 단위 용량 표준으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-111">This command updates deployment of an API Management instance to a three unit capacity standard.</span></span>

### <span data-ttu-id="fc987-112">예제 2: ApiManagement 인스턴스 가져오기 및 크기 조정</span><span class="sxs-lookup"><span data-stu-id="fc987-112">Example 2: Get an ApiManagement instance and rescale it</span></span>
```
PS C:\>$ApiManagement = Get-AzureRmApiManagement -ResourceGroupName "Contoso" -Name "ContosoApi"
PS C:\> $ApiManagement.Sku = "Premium"
PS C:\> $ApiManagement.Capacity = 5
PS C:\> $ApiManagement.AddRegion("Central US", "Premium", 3)
PS C:\> Update-AzureRmApiManagementDeployment -ApiManagement $ApiManagement
```

<span data-ttu-id="fc987-113">이 예제에서는 Api Management 인스턴스를 가져오고, 5 개의 premium 단위로 크기를 조정 하 고, 프리미엄 영역에 3 단위를 추가로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-113">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="fc987-114">예제 3: 업데이트 배포 (외부 VNET)</span><span class="sxs-lookup"><span data-stu-id="fc987-114">Example 3: Update deployment (external VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "External"
```

<span data-ttu-id="fc987-115">이 명령은 기존 API Management 배포를 업데이트 하 고 외부 *VpnType* 에 참가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-115">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="fc987-116">예제 4: 업데이트 배포 (내부 VNET)</span><span class="sxs-lookup"><span data-stu-id="fc987-116">Example 4: Update deployment (internal VNET)</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-West-US/providers/Microsoft.ClassicNetwork/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> Update-AzureRmApiManagementDeployment -ResourceGroupName "ContosoGroup" -Name "ContosoApi" -VirtualNetwork $virtualNetwork -VpnType "Internal"
```

<span data-ttu-id="fc987-117">이 명령은 기존 API Management 배포를 업데이트 하 고 내부 *VpnType* 에 참가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-117">This command updates an existing API Management deployment and joins to an internal *VpnType*.</span></span>

## <span data-ttu-id="fc987-118">변수</span><span class="sxs-lookup"><span data-stu-id="fc987-118">PARAMETERS</span></span>

### <span data-ttu-id="fc987-119">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="fc987-119">-AdditionalRegions</span></span>
<span data-ttu-id="fc987-120">Azure API Management의 추가 배포 영역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-120">Specifies additional deployment regions of Azure API Management.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion]
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc987-121">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="fc987-121">-ApiManagement</span></span>
<span data-ttu-id="fc987-122">배포 구성을 가져올 **PsApiManagement** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-122">Specifies the **PsApiManagement** instance to get deployment configuration from.</span></span>
<span data-ttu-id="fc987-123">인스턴스에 필요한 모든 변경 내용이 이미 있는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-123">Use this parameter if the instance already has all the required changes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Update from PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc987-124">용량</span><span class="sxs-lookup"><span data-stu-id="fc987-124">-Capacity</span></span>
<span data-ttu-id="fc987-125">마스터 Azure API 관리 배포 영역의 SKU 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-125">Specifies the SKU capacity of the master Azure API Management deployment region.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc987-126">-위치</span><span class="sxs-lookup"><span data-stu-id="fc987-126">-Location</span></span>
<span data-ttu-id="fc987-127">마스터 API 관리 배포 영역의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-127">Specifies the location of the master API Management deployment region.</span></span>

<span data-ttu-id="fc987-128">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fc987-129">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="fc987-129">North Central US</span></span>
- <span data-ttu-id="fc987-130">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="fc987-130">South Central US</span></span>
- <span data-ttu-id="fc987-131">중부 US</span><span class="sxs-lookup"><span data-stu-id="fc987-131">Central US</span></span>
- <span data-ttu-id="fc987-132">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="fc987-132">West Europe</span></span>
- <span data-ttu-id="fc987-133">동유럽</span><span class="sxs-lookup"><span data-stu-id="fc987-133">North Europe</span></span>
- <span data-ttu-id="fc987-134">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="fc987-134">West US</span></span>
- <span data-ttu-id="fc987-135">미국 동부</span><span class="sxs-lookup"><span data-stu-id="fc987-135">East US</span></span>
- <span data-ttu-id="fc987-136">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="fc987-136">East US 2</span></span>
- <span data-ttu-id="fc987-137">일본 동부</span><span class="sxs-lookup"><span data-stu-id="fc987-137">Japan East</span></span>
- <span data-ttu-id="fc987-138">일본 서쪽</span><span class="sxs-lookup"><span data-stu-id="fc987-138">Japan West</span></span>
- <span data-ttu-id="fc987-139">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="fc987-139">Brazil South</span></span>
- <span data-ttu-id="fc987-140">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="fc987-140">Southeast Asia</span></span>
- <span data-ttu-id="fc987-141">동아시아</span><span class="sxs-lookup"><span data-stu-id="fc987-141">East Asia</span></span>
- <span data-ttu-id="fc987-142">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="fc987-142">Australia East</span></span>
- <span data-ttu-id="fc987-143">오스트레일리아 남동쪽</span><span class="sxs-lookup"><span data-stu-id="fc987-143">Australia Southeast</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc987-144">-이름</span><span class="sxs-lookup"><span data-stu-id="fc987-144">-Name</span></span>
<span data-ttu-id="fc987-145">이 cmdlet이 업데이트 하는 API 관리의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-145">Specifies the name of API Management that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc987-146">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc987-146">-PassThru</span></span>
<span data-ttu-id="fc987-147">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-147">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fc987-148">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-148">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fc987-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc987-149">-ResourceGroupName</span></span>
<span data-ttu-id="fc987-150">API Management가 존재 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-150">Specifies the name of resource group under which API Management exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific API Management service
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc987-151">-Sku</span><span class="sxs-lookup"><span data-stu-id="fc987-151">-Sku</span></span>
<span data-ttu-id="fc987-152">마스터 Azure API 관리 배포 영역의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-152">Specifies the tier of the master Azure API Management deployment region.</span></span>

<span data-ttu-id="fc987-153">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-153">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fc987-154">디벨로퍼</span><span class="sxs-lookup"><span data-stu-id="fc987-154">Developer</span></span>
- <span data-ttu-id="fc987-155">표준이</span><span class="sxs-lookup"><span data-stu-id="fc987-155">Standard</span></span>
- <span data-ttu-id="fc987-156">Premium</span><span class="sxs-lookup"><span data-stu-id="fc987-156">Premium</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: Developer, Standard, Premium

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc987-157">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc987-157">-VirtualNetwork</span></span>
<span data-ttu-id="fc987-158">마스터 Azure API 관리 배포 영역의 가상 네트워크 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-158">Specifies the Virtual Network configuration of the master Azure API Management deployment region.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc987-159">-VpnType</span><span class="sxs-lookup"><span data-stu-id="fc987-159">-VpnType</span></span>
<span data-ttu-id="fc987-160">API Management 배포의 가상 네트워크 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-160">Specifies the virtual network Type of the API Management deployment.</span></span>
<span data-ttu-id="fc987-161">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="fc987-162">않아야.</span><span class="sxs-lookup"><span data-stu-id="fc987-162">None.</span></span>
<span data-ttu-id="fc987-163">API Management 구축은 가상 네트워크의 일부가 아닙니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-163">The API Management deployment is not part of any Virtual Network.</span></span>
<span data-ttu-id="fc987-164">이 값이 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-164">This is the default value.</span></span> 
- <span data-ttu-id="fc987-165">내부.</span><span class="sxs-lookup"><span data-stu-id="fc987-165">External.</span></span>
<span data-ttu-id="fc987-166">API Management 배포에 외부 연결 가상 주소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-166">The API Management deployment has an external facing virtual address.</span></span> 
- <span data-ttu-id="fc987-167">내부용.</span><span class="sxs-lookup"><span data-stu-id="fc987-167">Internal.</span></span>
<span data-ttu-id="fc987-168">API Management 배포에 인트라넷 연결 가상 주소가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-168">The API Management deployment has an intranet facing virtual address.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: Specific API Management service
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc987-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc987-169">-DefaultProfile</span></span>
<span data-ttu-id="fc987-170">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc987-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc987-171">CommonParameters</span></span>
<span data-ttu-id="fc987-172">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc987-173">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc987-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc987-174">입력</span><span class="sxs-lookup"><span data-stu-id="fc987-174">INPUTS</span></span>

### <span data-ttu-id="fc987-175">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="fc987-175">PsApiManagement</span></span>
<span data-ttu-id="fc987-176">' ApiManagement ' 매개 변수는 파이프라인에서 ' PsApiManagement ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fc987-176">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="fc987-177">출력</span><span class="sxs-lookup"><span data-stu-id="fc987-177">OUTPUTS</span></span>

### <span data-ttu-id="fc987-178">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="fc987-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="fc987-179">상속자</span><span class="sxs-lookup"><span data-stu-id="fc987-179">NOTES</span></span>

## <span data-ttu-id="fc987-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc987-180">RELATED LINKS</span></span>

[<span data-ttu-id="fc987-181">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="fc987-181">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)


