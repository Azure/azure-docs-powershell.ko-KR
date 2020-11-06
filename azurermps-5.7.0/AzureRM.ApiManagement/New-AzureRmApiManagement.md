---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: ebf95d8e809731bdca2f288bc09054fd14353686
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536140"
---
# <span data-ttu-id="8079f-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8079f-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="8079f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8079f-102">SYNOPSIS</span></span>
<span data-ttu-id="8079f-103">API Management 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8079f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8079f-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8079f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8079f-105">DESCRIPTION</span></span>
<span data-ttu-id="8079f-106">**AzureRmApiManagement** Cmdlet은 Azure api MANAGEMENT에서 API management 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="8079f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8079f-107">EXAMPLES</span></span>

### <span data-ttu-id="8079f-108">예제 1: 개발자 계층 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="8079f-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="8079f-109">이 명령은 개발자 계층 API 관리 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="8079f-110">명령은 조직과 관리자 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="8079f-111">명령에서 *SKU* 매개 변수를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="8079f-112">따라서 cmdlet은 기본 개발자 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="8079f-113">예제 2: 세 개의 단위가 있는 표준 계층 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="8079f-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="8079f-114">이 명령은 세 개의 단위가 있는 표준 계층 API 관리 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="8079f-115">예제 3: 외부 가상 네트워크에 대 한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="8079f-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="8079f-116">이 명령은 미국 내에서 마스터 영역이 있는 외부 연결 게이트웨이 끝점을 사용 하 여 Azure 가상 네트워크 서브넷에서 Premium 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="8079f-117">예제 4: 내부 가상 네트워크에 대 한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="8079f-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="8079f-118">이 명령은 미국 내에서 마스터 영역이 있는 내부 연결 게이트웨이 끝점을 사용 하는 Azure 가상 네트워크 서브넷에서 Premium 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="8079f-119">변수</span><span class="sxs-lookup"><span data-stu-id="8079f-119">PARAMETERS</span></span>

### <span data-ttu-id="8079f-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="8079f-120">-AdditionalRegions</span></span>
<span data-ttu-id="8079f-121">Azure API Management의 추가 배포 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: PsApiManagementRegion[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="8079f-122">-AdminEmail</span></span>
<span data-ttu-id="8079f-123">API Management 시스템에서 보내는 모든 알림에 대 한 원래 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-124">용량</span><span class="sxs-lookup"><span data-stu-id="8079f-124">-Capacity</span></span>
<span data-ttu-id="8079f-125">Azure API Management 서비스의 SKU 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="8079f-126">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-126">The default is one (1).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8079f-127">-DefaultProfile</span></span>
<span data-ttu-id="8079f-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-129">-위치</span><span class="sxs-lookup"><span data-stu-id="8079f-129">-Location</span></span>
<span data-ttu-id="8079f-130">Api Management 서비스를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-130">Specifies the location to create the Api Management service.</span></span>

<span data-ttu-id="8079f-131">유효한 위치를 얻으려면 cmdlet Get-AzureRmResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="8079f-131">To obtain valid locations, use the cmdlet Get-AzureRmResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-132">-이름</span><span class="sxs-lookup"><span data-stu-id="8079f-132">-Name</span></span>
<span data-ttu-id="8079f-133">API Management 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-133">Specifies a name for the API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-134">-조직</span><span class="sxs-lookup"><span data-stu-id="8079f-134">-Organization</span></span>
<span data-ttu-id="8079f-135">조직의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-135">Specifies the name of an organization.</span></span>
<span data-ttu-id="8079f-136">API Management는 전자 메일 알림에서 개발자 포털에서이 주소를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-136">API Management uses this address in the developer portal in email notifications.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8079f-137">-ResourceGroupName</span></span>
<span data-ttu-id="8079f-138">이 cmdlet이 API Management 배포를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-138">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-139">-Sku</span><span class="sxs-lookup"><span data-stu-id="8079f-139">-Sku</span></span>
<span data-ttu-id="8079f-140">API Management 서비스의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-140">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="8079f-141">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-141">Valid values are:</span></span> 

- <span data-ttu-id="8079f-142">디벨로퍼</span><span class="sxs-lookup"><span data-stu-id="8079f-142">Developer</span></span> 
- <span data-ttu-id="8079f-143">표준이</span><span class="sxs-lookup"><span data-stu-id="8079f-143">Standard</span></span> 
- <span data-ttu-id="8079f-144">Premium</span><span class="sxs-lookup"><span data-stu-id="8079f-144">Premium</span></span> 

<span data-ttu-id="8079f-145">기본값은 개발자입니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-145">The default is Developer.</span></span>

```yaml
Type: PsApiManagementSku
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-146">태그</span><span class="sxs-lookup"><span data-stu-id="8079f-146">-Tag</span></span>
<span data-ttu-id="8079f-147">태그 사전.</span><span class="sxs-lookup"><span data-stu-id="8079f-147">Tags dictionary.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-148">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8079f-148">-VirtualNetwork</span></span>
<span data-ttu-id="8079f-149">마스터 Azure API Management 배포 영역의 가상 네트워크 구성</span><span class="sxs-lookup"><span data-stu-id="8079f-149">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

```yaml
Type: PsApiManagementVirtualNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-150">-VpnType</span><span class="sxs-lookup"><span data-stu-id="8079f-150">-VpnType</span></span>
<span data-ttu-id="8079f-151">ApiManagement 배포의 가상 네트워크 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-151">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="8079f-152">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="8079f-152">Valid Values are</span></span> 
- <span data-ttu-id="8079f-153">"없음" (기본값)</span><span class="sxs-lookup"><span data-stu-id="8079f-153">"None" (Default Value.</span></span> <span data-ttu-id="8079f-154">ApiManagement는 가상 네트워크의 일부가 아닙니다. ")</span><span class="sxs-lookup"><span data-stu-id="8079f-154">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="8079f-155">"외부" (인터넷이 연결 된 끝점을 보유 한 가상 네트워크 내에서 ApiManagement 배포를 설정 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="8079f-155">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="8079f-156">"내부" (인트라넷이 연결 된 끝점을 보유 하 고 있는 가상 네트워크 내에서 ApiManagement 배포를 설정 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="8079f-156">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: PsApiManagementVpnType
Parameter Sets: (All)
Aliases:
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8079f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8079f-157">CommonParameters</span></span>
<span data-ttu-id="8079f-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8079f-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8079f-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8079f-160">입력</span><span class="sxs-lookup"><span data-stu-id="8079f-160">INPUTS</span></span>

### <span data-ttu-id="8079f-161">않아야</span><span class="sxs-lookup"><span data-stu-id="8079f-161">None</span></span>
<span data-ttu-id="8079f-162">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8079f-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8079f-163">출력</span><span class="sxs-lookup"><span data-stu-id="8079f-163">OUTPUTS</span></span>

### <span data-ttu-id="8079f-164">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="8079f-164">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="8079f-165">상속자</span><span class="sxs-lookup"><span data-stu-id="8079f-165">NOTES</span></span>

## <span data-ttu-id="8079f-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8079f-166">RELATED LINKS</span></span>

[<span data-ttu-id="8079f-167">백업-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8079f-167">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="8079f-168">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8079f-168">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="8079f-169">제거-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8079f-169">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="8079f-170">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="8079f-170">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


