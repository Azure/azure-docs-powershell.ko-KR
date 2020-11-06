---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementhostnames
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: 7093b51ffee3f0ad635da7a6c0b63d26e93e5f2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528677"
---
# <span data-ttu-id="f58ac-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="f58ac-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="f58ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f58ac-102">SYNOPSIS</span></span>
<span data-ttu-id="f58ac-103">API Management 서비스 프록시 또는 포털에 대 한 사용자 지정 호스트 이름 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f58ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f58ac-104">SYNTAX</span></span>

### <span data-ttu-id="f58ac-105">SetSpecificService (기본값)</span><span class="sxs-lookup"><span data-stu-id="f58ac-105">SetSpecificService (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f58ac-106">SetFromPsApiManagementInstance</span><span class="sxs-lookup"><span data-stu-id="f58ac-106">SetFromPsApiManagementInstance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f58ac-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f58ac-107">DESCRIPTION</span></span>
<span data-ttu-id="f58ac-108">**AzureRmApiManagementHostnames** CMDLET은 API Management 서비스 프록시 또는 포털에 대 한 사용자 지정 호스트 이름 구성을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="f58ac-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f58ac-109">EXAMPLES</span></span>

### <span data-ttu-id="f58ac-110">예제 1: 프록시와 포털에 대 한 사용자 지정 호스트 이름 구성 설정</span><span class="sxs-lookup"><span data-stu-id="f58ac-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="f58ac-111">이 명령은 프록시와 포털에 대 한 사용자 지정 호스트 이름 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="f58ac-112">예제 2: 프록시와 포털에 대 한 사용자 지정 호스트 이름 구성</span><span class="sxs-lookup"><span data-stu-id="f58ac-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="f58ac-113">이 예제에서는 프록시와 포털에 대 한 사용자 지정 호스트 이름을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="f58ac-114">해당 인증서를 가져온 다음 사용자 지정 호스트 이름을 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="f58ac-115">변수</span><span class="sxs-lookup"><span data-stu-id="f58ac-115">PARAMETERS</span></span>

### <span data-ttu-id="f58ac-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="f58ac-116">-ApiManagement</span></span>
<span data-ttu-id="f58ac-117">이 cmdlet이 *PortalHostnameConfiguration* 및 *ProxyHostnameConfiguration* 매개 변수를 가져오는 **PsApiManagement** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: SetFromPsApiManagementInstance
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f58ac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f58ac-118">-DefaultProfile</span></span>
<span data-ttu-id="f58ac-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f58ac-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f58ac-120">-Name</span></span>
<span data-ttu-id="f58ac-121">API Management 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-121">Specifies the name of the API Management instance.</span></span>

```yaml
Type: System.String
Parameter Sets: SetSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f58ac-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f58ac-122">-PassThru</span></span>
<span data-ttu-id="f58ac-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f58ac-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f58ac-125">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f58ac-125">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="f58ac-126">사용자 지정 포털 호스트 이름 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-126">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="f58ac-127">Cmdlet에 $null를 전달 하면 기본 호스트 이름이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-127">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f58ac-128">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f58ac-128">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="f58ac-129">사용자 지정 프록시 호스트 이름 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-129">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="f58ac-130">$Null를 전달 하면 기본 호스트 이름이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-130">Passing $null sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: SetSpecificService
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f58ac-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f58ac-131">-ResourceGroupName</span></span>
<span data-ttu-id="f58ac-132">API Management 인스턴스가 있는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-132">Specifies the name of the resource group under which the API Management instance exists.</span></span>

```yaml
Type: System.String
Parameter Sets: SetSpecificService
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f58ac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f58ac-133">CommonParameters</span></span>
<span data-ttu-id="f58ac-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f58ac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f58ac-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f58ac-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f58ac-136">입력</span><span class="sxs-lookup"><span data-stu-id="f58ac-136">INPUTS</span></span>

### <span data-ttu-id="f58ac-137">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="f58ac-137">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="f58ac-138">매개 변수: ApiManagement (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f58ac-138">Parameters: ApiManagement (ByValue)</span></span>

### <span data-ttu-id="f58ac-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f58ac-139">System.String</span></span>

### <span data-ttu-id="f58ac-140">ApiManagement. PsApiManagementHostnameConfiguration/.</span><span class="sxs-lookup"><span data-stu-id="f58ac-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration</span></span>

## <span data-ttu-id="f58ac-141">출력</span><span class="sxs-lookup"><span data-stu-id="f58ac-141">OUTPUTS</span></span>

### <span data-ttu-id="f58ac-142">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="f58ac-142">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="f58ac-143">상속자</span><span class="sxs-lookup"><span data-stu-id="f58ac-143">NOTES</span></span>

## <span data-ttu-id="f58ac-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f58ac-144">RELATED LINKS</span></span>

[<span data-ttu-id="f58ac-145">가져오기-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="f58ac-145">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="f58ac-146">새로운 AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="f58ac-146">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)


