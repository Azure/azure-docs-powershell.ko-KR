---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 43393995fcc370e2b3ff2b20586ab696c39d059b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689118"
---
# <span data-ttu-id="4ae0e-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ae0e-101">New-AzApiManagement</span></span>

## <span data-ttu-id="4ae0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ae0e-102">SYNOPSIS</span></span>
<span data-ttu-id="4ae0e-103">API Management 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="4ae0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4ae0e-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>] [-AssignIdentity]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ae0e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4ae0e-105">DESCRIPTION</span></span>
<span data-ttu-id="4ae0e-106">**AzApiManagement** Cmdlet은 Azure api MANAGEMENT에서 API management 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="4ae0e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4ae0e-107">EXAMPLES</span></span>

### <span data-ttu-id="4ae0e-108">예제 1: 개발자 계층 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="4ae0e-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"
```

<span data-ttu-id="4ae0e-109">이 명령은 개발자 계층 API 관리 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="4ae0e-110">명령은 조직과 관리자 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="4ae0e-111">명령에서 *SKU* 매개 변수를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="4ae0e-112">따라서 cmdlet은 기본 개발자 값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="4ae0e-113">예제 2: 세 개의 단위가 있는 표준 계층 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="4ae0e-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02 -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="4ae0e-114">이 명령은 세 개의 단위가 있는 표준 계층 API 관리 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="4ae0e-115">예제 3: 외부 가상 네트워크에 대 한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="4ae0e-115">Example 3: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="4ae0e-116">이 명령은 미국 내에서 마스터 영역이 있는 외부 연결 게이트웨이 끝점을 사용 하 여 Azure 가상 네트워크 서브넷에서 Premium 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-116">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="4ae0e-117">예제 4: 내부 가상 네트워크에 대 한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="4ae0e-117">Example 4: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="4ae0e-118">이 명령은 미국 내에서 마스터 영역이 있는 내부 연결 게이트웨이 끝점을 사용 하는 Azure 가상 네트워크 서브넷에서 Premium 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

## <span data-ttu-id="4ae0e-119">변수</span><span class="sxs-lookup"><span data-stu-id="4ae0e-119">PARAMETERS</span></span>

### <span data-ttu-id="4ae0e-120">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="4ae0e-120">-AdditionalRegions</span></span>
<span data-ttu-id="4ae0e-121">Azure API Management의 추가 배포 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-121">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="4ae0e-122">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="4ae0e-122">-AdminEmail</span></span>
<span data-ttu-id="4ae0e-123">API Management 시스템에서 보내는 모든 알림에 대 한 원래 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-123">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="4ae0e-124">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="4ae0e-124">-AssignIdentity</span></span>
<span data-ttu-id="4ae0e-125">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-125">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="4ae0e-126">용량</span><span class="sxs-lookup"><span data-stu-id="4ae0e-126">-Capacity</span></span>
<span data-ttu-id="4ae0e-127">Azure API Management 서비스의 SKU 용량을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-127">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="4ae0e-128">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-128">The default is one (1).</span></span>

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

### <span data-ttu-id="4ae0e-129">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ae0e-129">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="4ae0e-130">사용자 지정 호스트 이름 구성</span><span class="sxs-lookup"><span data-stu-id="4ae0e-130">Custom hostname configurations.</span></span> <span data-ttu-id="4ae0e-131">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-131">Default value is $null.</span></span> <span data-ttu-id="4ae0e-132">$Null를 전달 하면 기본 호스트 이름이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-132">Passing $null will set the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae0e-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ae0e-133">-DefaultProfile</span></span>
<span data-ttu-id="4ae0e-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ae0e-135">-위치</span><span class="sxs-lookup"><span data-stu-id="4ae0e-135">-Location</span></span>
<span data-ttu-id="4ae0e-136">Api Management 서비스를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-136">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="4ae0e-137">유효한 위치를 얻으려면 cmdlet Get-AzResourceProvider ProviderNamespace "ApiManagement" |을 (를) 사용 하세요. 여기서 {$ _. ResourceTypes [0]. ResourceTypeName-eq "서비스"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="4ae0e-137">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="4ae0e-138">-이름</span><span class="sxs-lookup"><span data-stu-id="4ae0e-138">-Name</span></span>
<span data-ttu-id="4ae0e-139">API Management 배포의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-139">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="4ae0e-140">-조직</span><span class="sxs-lookup"><span data-stu-id="4ae0e-140">-Organization</span></span>
<span data-ttu-id="4ae0e-141">조직의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-141">Specifies the name of an organization.</span></span>
<span data-ttu-id="4ae0e-142">API Management는 전자 메일 알림에서 개발자 포털에서이 주소를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-142">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="4ae0e-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ae0e-143">-ResourceGroupName</span></span>
<span data-ttu-id="4ae0e-144">이 cmdlet이 API Management 배포를 만드는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-144">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="4ae0e-145">-Sku</span><span class="sxs-lookup"><span data-stu-id="4ae0e-145">-Sku</span></span>
<span data-ttu-id="4ae0e-146">API Management 서비스의 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-146">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="4ae0e-147">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-147">Valid values are:</span></span> 
- <span data-ttu-id="4ae0e-148">디벨로퍼</span><span class="sxs-lookup"><span data-stu-id="4ae0e-148">Developer</span></span> 
- <span data-ttu-id="4ae0e-149">표준이</span><span class="sxs-lookup"><span data-stu-id="4ae0e-149">Standard</span></span> 
- <span data-ttu-id="4ae0e-150">Premium 기본값은 개발자입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-150">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae0e-151">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="4ae0e-151">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="4ae0e-152">서비스에 설치 되도록 내부 CA에서 발급 한 인증서입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-152">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="4ae0e-153">기본값은 $null입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-153">Default value is $null.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ae0e-154">태그</span><span class="sxs-lookup"><span data-stu-id="4ae0e-154">-Tag</span></span>
<span data-ttu-id="4ae0e-155">태그 사전.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-155">Tags dictionary.</span></span>

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

### <span data-ttu-id="4ae0e-156">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4ae0e-156">-VirtualNetwork</span></span>
<span data-ttu-id="4ae0e-157">마스터 Azure API Management 배포 영역의 가상 네트워크 구성</span><span class="sxs-lookup"><span data-stu-id="4ae0e-157">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="4ae0e-158">-VpnType</span><span class="sxs-lookup"><span data-stu-id="4ae0e-158">-VpnType</span></span>
<span data-ttu-id="4ae0e-159">ApiManagement 배포의 가상 네트워크 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-159">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="4ae0e-160">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="4ae0e-160">Valid Values are</span></span> 
- <span data-ttu-id="4ae0e-161">"없음" (기본값)</span><span class="sxs-lookup"><span data-stu-id="4ae0e-161">"None" (Default Value.</span></span> <span data-ttu-id="4ae0e-162">ApiManagement는 가상 네트워크의 일부가 아닙니다. ")</span><span class="sxs-lookup"><span data-stu-id="4ae0e-162">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="4ae0e-163">"외부" (인터넷이 연결 된 끝점을 보유 한 가상 네트워크 내에서 ApiManagement 배포를 설정 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="4ae0e-163">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="4ae0e-164">"내부" (인트라넷이 연결 된 끝점을 보유 하 고 있는 가상 네트워크 내에서 ApiManagement 배포를 설정 하는 경우)</span><span class="sxs-lookup"><span data-stu-id="4ae0e-164">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="4ae0e-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ae0e-165">CommonParameters</span></span>
<span data-ttu-id="4ae0e-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ae0e-167">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ae0e-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ae0e-168">입력</span><span class="sxs-lookup"><span data-stu-id="4ae0e-168">INPUTS</span></span>

### <span data-ttu-id="4ae0e-169">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4ae0e-169">System.String</span></span>

### <span data-ttu-id="4ae0e-170">시스템 Null 허용 ' 1 [[ApiManagement. PsApiManagementSku, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="4ae0e-170">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4ae0e-171">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="4ae0e-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ae0e-172">ApiManagement. PsApiManagementVirtualNetwork/.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-172">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="4ae0e-173">System.webserver. Dictionary ' 2 [[4.0.0.0], CoreLib, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e], [System.webserver,, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4ae0e-173">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4ae0e-174">ApiManagement [] PsApiManagementRegion []</span><span class="sxs-lookup"><span data-stu-id="4ae0e-174">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="4ae0e-175">ApiManagement [] PsApiManagementCustomHostNameConfiguration []</span><span class="sxs-lookup"><span data-stu-id="4ae0e-175">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="4ae0e-176">ApiManagement [] PsApiManagementSystemCertificate []</span><span class="sxs-lookup"><span data-stu-id="4ae0e-176">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="4ae0e-177">출력</span><span class="sxs-lookup"><span data-stu-id="4ae0e-177">OUTPUTS</span></span>

### <span data-ttu-id="4ae0e-178">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="4ae0e-178">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="4ae0e-179">상속자</span><span class="sxs-lookup"><span data-stu-id="4ae0e-179">NOTES</span></span>

## <span data-ttu-id="4ae0e-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ae0e-180">RELATED LINKS</span></span>

[<span data-ttu-id="4ae0e-181">백업-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ae0e-181">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="4ae0e-182">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ae0e-182">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="4ae0e-183">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ae0e-183">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="4ae0e-184">제거-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ae0e-184">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="4ae0e-185">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4ae0e-185">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


