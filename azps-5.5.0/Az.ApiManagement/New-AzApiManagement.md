---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 164C5205-01BA-47BB-B780-D0B9AE614A4B
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagement.md
ms.openlocfilehash: 32e3bc6419ef94b177a06735654844d09ea04f3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192497"
---
# <span data-ttu-id="4c732-101">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4c732-101">New-AzApiManagement</span></span>

## <span data-ttu-id="4c732-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c732-102">SYNOPSIS</span></span>
<span data-ttu-id="4c732-103">API Management 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-103">Creates an API Management deployment.</span></span>

## <span data-ttu-id="4c732-104">구문</span><span class="sxs-lookup"><span data-stu-id="4c732-104">SYNTAX</span></span>

```
New-AzApiManagement -ResourceGroupName <String> -Name <String> -Location <String> -Organization <String>
 -AdminEmail <String> [-Sku <PsApiManagementSku>] [-Capacity <Int32>] [-VpnType <PsApiManagementVpnType>]
 [-VirtualNetwork <PsApiManagementVirtualNetwork>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-AdditionalRegions <PsApiManagementRegion[]>]
 [-CustomHostnameConfiguration <PsApiManagementCustomHostNameConfiguration[]>]
 [-SystemCertificateConfiguration <PsApiManagementSystemCertificate[]>]
 [-SslSetting <PsApiManagementSslSetting>] [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-EnableClientCertificate] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c732-105">설명</span><span class="sxs-lookup"><span data-stu-id="4c732-105">DESCRIPTION</span></span>
<span data-ttu-id="4c732-106">**New-AzApiManagement** cmdlet은 Azure API Management에서 API Management 배포를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-106">The **New-AzApiManagement** cmdlet creates an API Management deployment in Azure API Management.</span></span>

## <span data-ttu-id="4c732-107">예제</span><span class="sxs-lookup"><span data-stu-id="4c732-107">EXAMPLES</span></span>

### <span data-ttu-id="4c732-108">예제 1: 개발자 계층 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="4c732-108">Example 1: Create a Developer tier API Management service</span></span>
```powershell
PS D:\> New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi2" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com"


PublicIPAddresses                     : {104.43.240.65}
PrivateIPAddresses                    :
Id                                    : /subscriptions/a200340d-6b82-494d-9dbf-687ba6e33f9e/resourceGroups/ContosoGroup02/providers/Microsoft.ApiManagement/service/ContosoApi2
Name                                  : ContosoApi2
Location                              : Central US
Sku                                   : Developer
Capacity                              : 1
CreatedTimeUtc                        : 2/24/2020 10:34:12 PM
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://contosoapi2.azure-api.net
RuntimeRegionalUrl                    : https://contosoapi2-centralus-01.regional.azure-api.net
PortalUrl                             : https://contosoapi2.portal.azure-api.net
DeveloperPortalUrl                    : https://contosoapi2.developer.azure-api.net
ManagementApiUrl                      : https://contosoapi2.management.azure-api.net
ScmUrl                                : https://contosoapi2.scm.azure-api.net
PublisherEmail                        : admin@contoso.com
OrganizationName                      : Contoso
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {contosoapi2.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : ContosoGroup02
```

<span data-ttu-id="4c732-109">이 명령은 개발자 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-109">This command creates a Developer tier API Management service.</span></span>
<span data-ttu-id="4c732-110">이 명령은 조직 및 관리자 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-110">The command specifies the organization and the administrator address.</span></span>
<span data-ttu-id="4c732-111">이 명령은 SKU 매개 *변수를 지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-111">The command does not specify the *SKU* parameter.</span></span>
<span data-ttu-id="4c732-112">따라서 cmdlet은 Developer의 기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-112">Therefore, the cmdlet uses the default value of Developer.</span></span>

### <span data-ttu-id="4c732-113">예제 2: 3단위가 있는 표준 계층 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="4c732-113">Example 2: Create a Standard tier service that has three units</span></span>
```powershell
PS C:\>New-AzApiManagement -ResourceGroupName "ContosoGroup02" -Name "ContosoApi" -Location "Central US" -Organization "Contoso" -AdminEmail "admin@contoso.com" -Sku Standard -Capacity 3
```

<span data-ttu-id="4c732-114">이 명령은 세 단위가 있는 표준 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-114">This command creates a Standard tier API Management service that has three units.</span></span>

### <span data-ttu-id="4c732-115">예제 3: 소비 계층 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="4c732-115">Example 3: Create a Consumption tier service</span></span>
```powershell
PS D:\github\azure-powershell> New-AzApiManagement -ResourceGroupName Api-Default-North-Europe -Name consumptionskuservice -Location 'West Europe' -Sku Consumption -Organization microsoft -AdminEmail contoso@contoso.com -SystemAssignedIdentity -EnableClientCertificate

PublicIPAddresses                     :
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-North-Europe/providers/Microsoft.ApiManagement/service/consumptionskuservice
Name                                  : consumptionskuservice
Location                              : West Europe
Sku                                   : Consumption
Capacity                              : 0
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://consumptionskuservice.azure-api.net
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {consumptionskuservice.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementServiceIdentity
EnableClientCertificate               : True
ResourceGroupName                     : Api-Default-North-Europe
```

<span data-ttu-id="4c732-116">이 명령은 유럽 서부에서 사용하도록 설정된 클라이언트 인증서를 사용하여 소비 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-116">This command creates a consumption tier API Management service with Client Certificate enabled in west Europe.</span></span>

### <span data-ttu-id="4c732-117">예제 4: 외부 가상 네트워크에 대한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="4c732-117">Example 4: Create an API Management service for an external virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization Contoso -AdminEmail admin@contoso.com -VirtualNetwork $virtualNetwork -VpnType "External" -Sku "Premium"
```

<span data-ttu-id="4c732-118">이 명령은 Azure 가상 네트워크 서브넷에 미국 서부의 마스터 지역이 있는 외부 연결 게이트웨이 엔드포인트가 있는 프리미엄 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-118">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an external-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="4c732-119">예제 5: 내부 가상 네트워크에 대한 API Management 서비스 만들기</span><span class="sxs-lookup"><span data-stu-id="4c732-119">Example 5: Create an API Management service for an internal virtual network</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "West US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-b1e8-3726ab15d0e2/resourceGroups/ContosoGroup/providers/Microsoft.Network/virtualNetworks/westUsVirtualNetwork/subnets/backendSubnet"
PS C:\> New-AzApiManagement -ResourceGroupName "ContosoGroup" -Location "West US" -Name "ContosoApi" -Organization "Contoso" -AdminEmail "admin@contoso.com" -VirtualNetwork $virtualNetwork -VpnType "Internal" -Sku "Premium"
```

<span data-ttu-id="4c732-120">이 명령은 Azure 가상 네트워크 서브넷에 미국 서부의 마스터 지역이 있는 내부 연결 게이트웨이 엔드포인트가 있는 프리미엄 계층 API Management 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-120">This command creates a Premium-tier API Management service in an Azure virtual network subnet having an internal-facing gateway endpoint with a master region in the West US.</span></span>

### <span data-ttu-id="4c732-121">예제 6: API Management 서비스 만들기 및 TLS 1.0 프로토콜 사용</span><span class="sxs-lookup"><span data-stu-id="4c732-121">Example 6: Create an API Management service and Enable TLS 1.0 protocol</span></span>
```powershell
PS C:\> $enableTls=@{"Tls10" = "True"}
PS C:\> $sslSetting = New-AzApiManagementSslSetting -FrontendProtocol $enableTls -BackendProtocol $enableTls
PS C:\> New-AzApiManagement -ResourceGroupName Api-Default-CentralUS -Name "testtlspowershell" -Sku Standard -Location "CentralUS" -Organization "Microsoft" -AdminEmail "bar@contoso.com" -SslSetting $sslSetting

PublicIPAddresses                     : {23.99.140.18}
PrivateIPAddresses                    :
Id                                    : /subscriptions/subid/resourceGroups/Api-Default-CentralUS/providers/Microsoft.ApiManagement/service/testtlspowershell
Name                                  : testtlspowershell
Location                              : Central US
Sku                                   : Standard
Capacity                              : 1
ProvisioningState                     : Succeeded
RuntimeUrl                            : https://testtlspowershell.azure-api.net
RuntimeRegionalUrl                    : https://testtlspowershell-centralus-01.regional.azure-api.net
PortalUrl                             : https://testtlspowershell.portal.azure-api.net
ManagementApiUrl                      : https://testtlspowershell.management.azure-api.net
ScmUrl                                : https://testtlspowershell.scm.azure-api.net
PublisherEmail                        : bar@contoso.com
OrganizationName                      : Microsoft
NotificationSenderEmail               : apimgmt-noreply@mail.windowsazure.com
VirtualNetwork                        :
VpnType                               : None
PortalCustomHostnameConfiguration     :
ProxyCustomHostnameConfiguration      : {testtlspowershell.azure-api.net}
ManagementCustomHostnameConfiguration :
ScmCustomHostnameConfiguration        :
DeveloperPortalHostnameConfiguration  :
SystemCertificates                    :
Tags                                  : {}
AdditionalRegions                     : {}
SslSetting                            : Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Identity                              :
EnableClientCertificate               :
ResourceGroupName                     : Api-Default-CentralUS
```

<span data-ttu-id="4c732-122">이 명령은 표준 SKU Api Management 서비스를 만들고, ApiManagement 게이트웨이와 백 엔드 간에 프런트 엔드 클라이언트에서 TLS 1.0을 사용하도록 설정하고 ApiManagement 게이트웨이와 백 엔드 클라이언트를 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-122">This command creates a Standard SKU Api Management service and Enable TLS 1.0 on Frontend client to ApiManagement Gateway and Backend client between ApiManagement Gateway and Backend.</span></span>

## <span data-ttu-id="4c732-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c732-123">PARAMETERS</span></span>

### <span data-ttu-id="4c732-124">-AdditionalRegions</span><span class="sxs-lookup"><span data-stu-id="4c732-124">-AdditionalRegions</span></span>
<span data-ttu-id="4c732-125">Azure API Management의 추가 배포 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-125">Additional deployment regions of Azure API Management.</span></span>

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

### <span data-ttu-id="4c732-126">-AdminEmail</span><span class="sxs-lookup"><span data-stu-id="4c732-126">-AdminEmail</span></span>
<span data-ttu-id="4c732-127">API Management 시스템에서 보내는 모든 알림에 대해 원래 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-127">Specifies the originating email address for all notifications that the API Management system sends.</span></span>

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

### <span data-ttu-id="4c732-128">-Capacity</span><span class="sxs-lookup"><span data-stu-id="4c732-128">-Capacity</span></span>
<span data-ttu-id="4c732-129">Azure API Management 서비스의 SKU 용량을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-129">Specifies the SKU capacity of the Azure API Management service.</span></span>
<span data-ttu-id="4c732-130">기본값은 1(1)입니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-130">The default is one (1).</span></span>

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

### <span data-ttu-id="4c732-131">-CustomHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c732-131">-CustomHostnameConfiguration</span></span>
<span data-ttu-id="4c732-132">사용자 지정 호스트 이름 구성.</span><span class="sxs-lookup"><span data-stu-id="4c732-132">Custom hostname configurations.</span></span> <span data-ttu-id="4c732-133">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="4c732-133">Default value is $null.</span></span> <span data-ttu-id="4c732-134">이 $null 기본 호스트 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-134">Passing $null will set the default hostname.</span></span>

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

### <span data-ttu-id="4c732-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c732-135">-DefaultProfile</span></span>
<span data-ttu-id="4c732-136">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c732-137">-EnableClientCertificate</span><span class="sxs-lookup"><span data-stu-id="4c732-137">-EnableClientCertificate</span></span>
<span data-ttu-id="4c732-138">소비 SKU ApiManagement 서비스에만 사용되는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-138">Flag only meant to be used for Consumption SKU ApiManagement Service.</span></span> <span data-ttu-id="4c732-139">그러면 게이트웨이에 대한 각 요청에 클라이언트 인증서가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-139">This enforces a client certificate to be presented on each request to the gateway.</span></span> <span data-ttu-id="4c732-140">이렇게 하면 게이트웨이의 정책에서 인증서를 인증할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-140">This also enables the ability to authenticate the certificate in the policy on the gateway.</span></span>

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

### <span data-ttu-id="4c732-141">-Location</span><span class="sxs-lookup"><span data-stu-id="4c732-141">-Location</span></span>
<span data-ttu-id="4c732-142">Api Management 서비스를 만들 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-142">Specifies the location to create the Api Management service.</span></span>
<span data-ttu-id="4c732-143">유효한 위치를 얻게 Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" cmdlet을 | where {$_. ResourceTypes[0]. ResourceTypeName -eq "service"} | Select-Object 위치</span><span class="sxs-lookup"><span data-stu-id="4c732-143">To obtain valid locations, use the cmdlet Get-AzResourceProvider -ProviderNamespace "Microsoft.ApiManagement" | where {$_.ResourceTypes[0].ResourceTypeName -eq "service"} | Select-Object Locations</span></span>

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

### <span data-ttu-id="4c732-144">-Name</span><span class="sxs-lookup"><span data-stu-id="4c732-144">-Name</span></span>
<span data-ttu-id="4c732-145">API Management 배포의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-145">Specifies a name for the API Management deployment.</span></span>

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

### <span data-ttu-id="4c732-146">-Organization</span><span class="sxs-lookup"><span data-stu-id="4c732-146">-Organization</span></span>
<span data-ttu-id="4c732-147">조직의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-147">Specifies the name of an organization.</span></span>
<span data-ttu-id="4c732-148">API Management는 개발자 포털의 전자 메일 알림에서 이 주소를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-148">API Management uses this address in the developer portal in email notifications.</span></span>

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

### <span data-ttu-id="4c732-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c732-149">-ResourceGroupName</span></span>
<span data-ttu-id="4c732-150">이 cmdlet에서 API Management 배포를 만드는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-150">Specifies the name of the of resource group under which this cmdlet creates an API Management deployment.</span></span>

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

### <span data-ttu-id="4c732-151">-Sku</span><span class="sxs-lookup"><span data-stu-id="4c732-151">-Sku</span></span>
<span data-ttu-id="4c732-152">API Management 서비스의 계층을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-152">Specifies the tier of the API Management service.</span></span>
<span data-ttu-id="4c732-153">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="4c732-153">Valid values are:</span></span> 
- <span data-ttu-id="4c732-154">개발자</span><span class="sxs-lookup"><span data-stu-id="4c732-154">Developer</span></span> 
- <span data-ttu-id="4c732-155">표준</span><span class="sxs-lookup"><span data-stu-id="4c732-155">Standard</span></span> 
- <span data-ttu-id="4c732-156">Premium 기본값은 Developer입니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-156">Premium The default is Developer.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku]
Parameter Sets: (All)
Aliases:
Accepted values: Developer, Basic, Standard, Premium, Consumption

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c732-157">-SslSetting</span><span class="sxs-lookup"><span data-stu-id="4c732-157">-SslSetting</span></span>
<span data-ttu-id="4c732-158">ApiManagement 서비스의 Ssl 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-158">The Ssl Setting of the ApiManagement Service.</span></span> <span data-ttu-id="4c732-159">기본값은 $null</span><span class="sxs-lookup"><span data-stu-id="4c732-159">Default value is $null</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSslSetting
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c732-160">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4c732-160">-SystemAssignedIdentity</span></span>
<span data-ttu-id="4c732-161">Azure KeyVault와 같은 키 관리 서비스에서 사용할 이 서버에 대한 Azure Active Directory ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-161">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="4c732-162">-SystemCertificateConfiguration</span><span class="sxs-lookup"><span data-stu-id="4c732-162">-SystemCertificateConfiguration</span></span>
<span data-ttu-id="4c732-163">서비스에 설치하기 위해 내부 CA에서 발급한 인증서입니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-163">Certificates issued by Internal CA to be installed on the service.</span></span> <span data-ttu-id="4c732-164">기본값은 $null.</span><span class="sxs-lookup"><span data-stu-id="4c732-164">Default value is $null.</span></span>

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

### <span data-ttu-id="4c732-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="4c732-165">-Tag</span></span>
<span data-ttu-id="4c732-166">태그 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-166">Tags dictionary.</span></span>

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

### <span data-ttu-id="4c732-167">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="4c732-167">-UserAssignedIdentity</span></span>
<span data-ttu-id="4c732-168">Azure KeyVault와 같은 키 관리 서비스에서 사용할 사용자 ID를 이 서버에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-168">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c732-169">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4c732-169">-VirtualNetwork</span></span>
<span data-ttu-id="4c732-170">마스터 Azure API Management 배포 지역의 Virtual Network 구성</span><span class="sxs-lookup"><span data-stu-id="4c732-170">Virtual Network Configuration of master Azure API Management deployment region.</span></span>

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

### <span data-ttu-id="4c732-171">-VpnType</span><span class="sxs-lookup"><span data-stu-id="4c732-171">-VpnType</span></span>
<span data-ttu-id="4c732-172">ApiManagement 배포의 가상 네트워크 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-172">Virtual Network Type of the ApiManagement Deployment.</span></span> <span data-ttu-id="4c732-173">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="4c732-173">Valid Values are</span></span> 
- <span data-ttu-id="4c732-174">"None"(기본값).</span><span class="sxs-lookup"><span data-stu-id="4c732-174">"None" (Default Value.</span></span> <span data-ttu-id="4c732-175">ApiManagement는 Virtual Network에 참여하지 않습니다.")</span><span class="sxs-lookup"><span data-stu-id="4c732-175">ApiManagement is not part of any Virtual Network")</span></span>
- <span data-ttu-id="4c732-176">"외부"(ApiManagement 배포는 인터넷 연결 엔드포인트가 있는 Virtual Network 내에서 설정됩니다.)</span><span class="sxs-lookup"><span data-stu-id="4c732-176">"External" (ApiManagement Deployment is setup inside a Virtual Network having an Internet Facing Endpoint)</span></span>
- <span data-ttu-id="4c732-177">"내부"(인트라넷 연결 엔드포인트가 있는 Virtual Network 내에서 ApiManagement 배포가 설정됩니다.)</span><span class="sxs-lookup"><span data-stu-id="4c732-177">"Internal" (ApiManagement Deployment is setup inside a Virtual Network having an Intranet Facing Endpoint)</span></span>

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

### <span data-ttu-id="4c732-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c732-178">CommonParameters</span></span>
<span data-ttu-id="4c732-179">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4c732-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c732-180">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4c732-180">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c732-181">입력</span><span class="sxs-lookup"><span data-stu-id="4c732-181">INPUTS</span></span>

### <span data-ttu-id="4c732-182">System.String</span><span class="sxs-lookup"><span data-stu-id="4c732-182">System.String</span></span>

### <span data-ttu-id="4c732-183">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4c732-183">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSku, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4c732-184">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4c732-184">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4c732-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4c732-185">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementVirtualNetwork</span></span>

### <span data-ttu-id="4c732-186">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4c732-186">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4c732-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span><span class="sxs-lookup"><span data-stu-id="4c732-187">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementRegion[]</span></span>

### <span data-ttu-id="4c732-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span><span class="sxs-lookup"><span data-stu-id="4c732-188">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementCustomHostNameConfiguration[]</span></span>

### <span data-ttu-id="4c732-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span><span class="sxs-lookup"><span data-stu-id="4c732-189">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementSystemCertificate[]</span></span>

## <span data-ttu-id="4c732-190">출력</span><span class="sxs-lookup"><span data-stu-id="4c732-190">OUTPUTS</span></span>

### <span data-ttu-id="4c732-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="4c732-191">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="4c732-192">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4c732-192">NOTES</span></span>

## <span data-ttu-id="4c732-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c732-193">RELATED LINKS</span></span>

[<span data-ttu-id="4c732-194">Backup-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4c732-194">Backup-AzApiManagement</span></span>](./Backup-AzApiManagement.md)

[<span data-ttu-id="4c732-195">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4c732-195">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="4c732-196">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4c732-196">Set-AzApiManagement</span></span>](./Set-AzApiManagement.md)

[<span data-ttu-id="4c732-197">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4c732-197">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)

[<span data-ttu-id="4c732-198">Restore-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="4c732-198">Restore-AzApiManagement</span></span>](./Restore-AzApiManagement.md)


