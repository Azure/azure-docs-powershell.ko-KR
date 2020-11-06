---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagement.md
ms.openlocfilehash: 82e09e146999ce0bd320ba398ab2f196f1115688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531283"
---
# <span data-ttu-id="1dfdb-101">New-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1dfdb-101">New-AzureRmApiManagement</span></span>

## <span data-ttu-id="1dfdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1dfdb-102">SYNOPSIS</span></span>
<span data-ttu-id="1dfdb-103">API Management 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-103">Creates an API Management deployment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dfdb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1dfdb-104">SYNTAX</span></span>

```
New-AzureRmApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tags <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1dfdb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1dfdb-105">DESCRIPTION</span></span>
<span data-ttu-id="1dfdb-106">**AzureRmApiManagement** Cmdlet은 Azure api MANAGEMENT에서 API management 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-106">The **New-AzureRmApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="1dfdb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1dfdb-107">EXAMPLES</span></span>

### <span data-ttu-id="1dfdb-108">예제 1: 개발자 계층 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="1dfdb-108">Example 1: Create a Developer tier API Management service</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="1dfdb-109">이 명령은 개발자 계층 API 관리 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="1dfdb-110">명령은 조직과 관리자 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="1dfdb-111">명령에서 *SKU* 매개 변수를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="1dfdb-112">따라서 cmdlet은 기본 개발자 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="1dfdb-113">예제 2: 세 개의 단위가 있는 표준 계층 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="1dfdb-113">Example 2: Create a Standard tier service that has three units</span></span>
```
PS C:\>New-AzureRmApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="1dfdb-114">이 명령은 세 개의 단위가 있는 표준 계층 API 관리 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="1dfdb-115">예제 3: 외부 가상 네트워크에 대 한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="1dfdb-115">Example 3: Create an API Management service for an external virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="1dfdb-116">이 명령은 미국 내에서 마스터 영역이 있는 외부 연결 게이트웨이 끝점을 사용 하 여 Azure 가상 네트워크 서브넷에서 Premium 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="1dfdb-117">예제 4: 내부 가상 네트워크에 대 한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="1dfdb-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="1dfdb-118">이 명령은 미국 내에서 마스터 영역이 있는 내부 연결 게이트웨이 끝점을 사용 하는 Azure 가상 네트워크 서브넷에서 Premium 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="1dfdb-119">변수</span><span class="sxs-lookup"><span data-stu-id="1dfdb-119">PARAMETERS</span></span>

### <span data-ttu-id="1dfdb-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="1dfdb-120">-AdditionalRegions</span></span>
<span data-ttu-id="1dfdb-121">Azure API Management의 추가 배포 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-121">Additional deployment regions of Azure API Management.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dfdb-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="1dfdb-122">-AdminEmail</span></span>
<span data-ttu-id="1dfdb-123">API Management 시스템에서 보내는 모든 알림에 대 한 원래 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="1dfdb-124">용량</span><span class="sxs-lookup"><span data-stu-id="1dfdb-124">-Capacity</span></span>
<span data-ttu-id="1dfdb-125">Azure API Management 서비스의 SKU 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-125">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="1dfdb-126">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-126">The default is one (1).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dfdb-127">-위치</span><span class="sxs-lookup"><span data-stu-id="1dfdb-127">-Location</span></span>
<span data-ttu-id="1dfdb-128">이 cmdlet이 API Management 배포를 만드는 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-128">Specifies the location in which this cmdlet creates an API Management deployment.</span></span>
<span data-ttu-id="1dfdb-129">유효한 위치를 얻으려면 Get-AzureLocation cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-129">To obtain valid locations, use the Get-AzureLocation cmdlets.</span></span>

<span data-ttu-id="1dfdb-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-130">Valid values are:</span></span> 

- <span data-ttu-id="1dfdb-131">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="1dfdb-131">North Central US</span></span>
- <span data-ttu-id="1dfdb-132">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="1dfdb-132">South Central US</span></span>
- <span data-ttu-id="1dfdb-133">중부 US</span><span class="sxs-lookup"><span data-stu-id="1dfdb-133">Central US</span></span>
- <span data-ttu-id="1dfdb-134">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="1dfdb-134">West Europe</span></span>
- <span data-ttu-id="1dfdb-135">동유럽</span><span class="sxs-lookup"><span data-stu-id="1dfdb-135">North Europe</span></span>
- <span data-ttu-id="1dfdb-136">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="1dfdb-136">West US</span></span>
- <span data-ttu-id="1dfdb-137">미국 동부</span><span class="sxs-lookup"><span data-stu-id="1dfdb-137">East US</span></span>
- <span data-ttu-id="1dfdb-138">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="1dfdb-138">East US 2</span></span>
- <span data-ttu-id="1dfdb-139">일본 동부</span><span class="sxs-lookup"><span data-stu-id="1dfdb-139">Japan East</span></span>
- <span data-ttu-id="1dfdb-140">일본 서쪽</span><span class="sxs-lookup"><span data-stu-id="1dfdb-140">Japan West</span></span>
- <span data-ttu-id="1dfdb-141">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="1dfdb-141">Brazil South</span></span>
- <span data-ttu-id="1dfdb-142">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="1dfdb-142">Southeast Asia</span></span>
- <span data-ttu-id="1dfdb-143">동아시아</span><span class="sxs-lookup"><span data-stu-id="1dfdb-143">East Asia</span></span>
- <span data-ttu-id="1dfdb-144">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="1dfdb-144">Australia East</span></span>
- <span data-ttu-id="1dfdb-145">오스트레일리아 남동쪽</span><span class="sxs-lookup"><span data-stu-id="1dfdb-145">Australia Southeast</span></span>

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

### <span data-ttu-id="1dfdb-146">-이름</span><span class="sxs-lookup"><span data-stu-id="1dfdb-146">-Name</span></span>
<span data-ttu-id="1dfdb-147">API Management 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-147">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="1dfdb-148">-조직</span><span class="sxs-lookup"><span data-stu-id="1dfdb-148">-Organization</span></span>
<span data-ttu-id="1dfdb-149">조직의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-149">Specifies the name of an organization.</span></span>
<span data-ttu-id="1dfdb-150">API Management는 전자 메일 알림에서 개발자 포털에서이 주소를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-150">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="1dfdb-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dfdb-151">-ResourceGroupName</span></span>
<span data-ttu-id="1dfdb-152">이 cmdlet이 API Management 배포를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-152">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="1dfdb-153">-Sku</span><span class="sxs-lookup"><span data-stu-id="1dfdb-153">-Sku</span></span>
<span data-ttu-id="1dfdb-154">API Management 서비스의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-154">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="1dfdb-155">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-155">Valid values are:</span></span> 

- <span data-ttu-id="1dfdb-156">디벨로퍼</span><span class="sxs-lookup"><span data-stu-id="1dfdb-156">Developer</span></span> 
- <span data-ttu-id="1dfdb-157">표준이</span><span class="sxs-lookup"><span data-stu-id="1dfdb-157">Standard</span></span> 
- <span data-ttu-id="1dfdb-158">Premium</span><span class="sxs-lookup"><span data-stu-id="1dfdb-158">Premium</span></span> 

<span data-ttu-id="1dfdb-159">기본값은 개발자입니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-159">The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases: 
Accepted values: Developer, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dfdb-160">태그</span><span class="sxs-lookup"><span data-stu-id="1dfdb-160">-Tags</span></span>
<span data-ttu-id="1dfdb-161">태그 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-161">Specifies a dictionary of tags.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dfdb-162">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="1dfdb-162">-VirtualNetwork</span></span>
<span data-ttu-id="1dfdb-163">마스터 Azure API Management 배포 영역의 가상 네트워크 구성</span><span class="sxs-lookup"><span data-stu-id="1dfdb-163">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="1dfdb-164">-VpnType</span><span class="sxs-lookup"><span data-stu-id="1dfdb-164">-VpnType</span></span>
<span data-ttu-id="1dfdb-165">ApiManagement 배포의 가상 네트워크 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-165">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="1dfdb-166">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="1dfdb-166">Valid Values are</span></span> 
- <span data-ttu-id="1dfdb-167">"없음" (기본값)</span><span class="sxs-lookup"><span data-stu-id="1dfdb-167">"None" (Default Value.</span></span> <span data-ttu-id="1dfdb-168">ApiManagement는 가상 네트워크의 일부가 아닙니다. ")</span><span class="sxs-lookup"><span data-stu-id="1dfdb-168">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="1dfdb-169">"외부" (인터넷이 연결 된 끝점을 보유 한 가상 네트워크 내에서 ApiManagement 배포를 설정 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="1dfdb-169">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="1dfdb-170">"내부" (인트라넷이 연결 된 끝점을 보유 하 고 있는 가상 네트워크 내에서 ApiManagement 배포를 설정 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="1dfdb-170">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVpnType
Parameter Sets: (All)
Aliases: 
Accepted values: None, External, Internal

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dfdb-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dfdb-171">-DefaultProfile</span></span>
<span data-ttu-id="1dfdb-172">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1dfdb-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dfdb-173">CommonParameters</span></span>
<span data-ttu-id="1dfdb-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dfdb-175">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dfdb-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dfdb-176">입력</span><span class="sxs-lookup"><span data-stu-id="1dfdb-176">INPUTS</span></span>

## <span data-ttu-id="1dfdb-177">출력</span><span class="sxs-lookup"><span data-stu-id="1dfdb-177">OUTPUTS</span></span>

### <span data-ttu-id="1dfdb-178">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="1dfdb-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="1dfdb-179">상속자</span><span class="sxs-lookup"><span data-stu-id="1dfdb-179">NOTES</span></span>

## <span data-ttu-id="1dfdb-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1dfdb-180">RELATED LINKS</span></span>

[<span data-ttu-id="1dfdb-181">백업-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1dfdb-181">Backup-AzureRmApiManagement</span></span>](./Backup-AzureRmApiManagement.md)

[<span data-ttu-id="1dfdb-182">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1dfdb-182">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="1dfdb-183">제거-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1dfdb-183">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)

[<span data-ttu-id="1dfdb-184">Restore-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="1dfdb-184">Restore-AzureRmApiManagement</span></span>](./Restore-AzureRmApiManagement.md)


