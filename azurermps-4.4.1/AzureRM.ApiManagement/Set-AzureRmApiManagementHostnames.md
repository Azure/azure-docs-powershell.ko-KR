---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: F9CE8705-F7B1-45AB-98BC-FC6DC023D38D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementHostnames.md
ms.openlocfilehash: 3e3fea3e43f2370347ae819604d6caf1e830ebd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531881"
---
# <span data-ttu-id="e71fb-101">Set-AzureRmApiManagementHostnames</span><span class="sxs-lookup"><span data-stu-id="e71fb-101">Set-AzureRmApiManagementHostnames</span></span>

## <span data-ttu-id="e71fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e71fb-102">SYNOPSIS</span></span>
<span data-ttu-id="e71fb-103">API Management 서비스 프록시 또는 포털에 대 한 사용자 지정 호스트 이름 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-103">Sets a custom hostname configuration for an API Management service proxy or portal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e71fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e71fb-104">SYNTAX</span></span>

### <span data-ttu-id="e71fb-105">특정 API Management 서비스 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e71fb-105">Specific API Management service (Default)</span></span>
```
Set-AzureRmApiManagementHostnames -ResourceGroupName <String> -Name <String>
 [-PortalHostnameConfiguration <PsApiManagementHostnameConfiguration>]
 [-ProxyHostnameConfiguration <PsApiManagementHostnameConfiguration>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e71fb-106">제공 된 PsApiManagement 인스턴스에서 설정</span><span class="sxs-lookup"><span data-stu-id="e71fb-106">Set from provided PsApiManagement instance</span></span>
```
Set-AzureRmApiManagementHostnames -ApiManagement <PsApiManagement> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e71fb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e71fb-107">DESCRIPTION</span></span>
<span data-ttu-id="e71fb-108">**AzureRmApiManagementHostnames** CMDLET은 API Management 서비스 프록시 또는 포털에 대 한 사용자 지정 호스트 이름 구성을 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-108">The **Set-AzureRmApiManagementHostnames** cmdlet applies a custom hostname configuration for an API Management service proxy or portal.</span></span>

## <span data-ttu-id="e71fb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e71fb-109">EXAMPLES</span></span>

### <span data-ttu-id="e71fb-110">예제 1: 프록시와 포털에 대 한 사용자 지정 호스트 이름 구성 설정</span><span class="sxs-lookup"><span data-stu-id="e71fb-110">Example 1: Set the custom hostname configuration for a proxy and portal</span></span>
```
PS C:\>Set-AzureRmApiManagementHostnames -Name ContosoApi -ResourceGroupName Contoso -PortalHostnameConfiguration $portalHostnameConf -ProxyHostnameConfiguration $proxyHostnameConf
```

<span data-ttu-id="e71fb-111">이 명령은 프록시와 포털에 대 한 사용자 지정 호스트 이름 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-111">This command sets the custom hostname configuration for proxy and portal.</span></span>

### <span data-ttu-id="e71fb-112">예제 2: 프록시와 포털에 대 한 사용자 지정 호스트 이름 구성</span><span class="sxs-lookup"><span data-stu-id="e71fb-112">Example 2: Configure a custom hostname for a proxy and portal</span></span>
```
PS C:\>Import-AzureRmApiManagementHostnameCertificate -Name ContosoApi -ResourceGroupName "Contoso" -HostnameType "Proxy" -PfxPath "C:\proxycert.pfx" -PfxPassword "CertSecret"
PS C:\> Import-AzureRmApiManagementHostnameCertificate -Name "ContosoApi" -ResourceGroupName "Contoso" -HostnameType "Portal" -PfxPath "C:\portalcert.pfx" -PfxPassword "CertSecret"
PS C:\> $PortalHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "portal.contoso.com" -CertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C"
PS C:\> $ProxyHostnameConf = New-AzureRmApiManagementHostnameConfiguration -Hostname "proxy.contoso.com" -CertificateThumbprint "5DD7CCF6A1E74E0987DD2873406B7264"
PS C:\> Set-AzureRmApiManagementHostnames -Name "ContosoApi" -ResourceGroupName "Contoso" -PortalHostnameConfiguration $PortalHostnameConf -ProxyHostnameConfiguration $ProxyHostnameConf
```

<span data-ttu-id="e71fb-113">이 예제에서는 프록시와 포털에 대 한 사용자 지정 호스트 이름을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-113">This example configures a custom hostname for proxy and portal.</span></span>
<span data-ttu-id="e71fb-114">해당 인증서를 가져온 다음 사용자 지정 호스트 이름을 적용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-114">You need to import corresponding certificates and then apply the custom hostnames.</span></span>

## <span data-ttu-id="e71fb-115">변수</span><span class="sxs-lookup"><span data-stu-id="e71fb-115">PARAMETERS</span></span>

### <span data-ttu-id="e71fb-116">-ApiManagement</span><span class="sxs-lookup"><span data-stu-id="e71fb-116">-ApiManagement</span></span>
<span data-ttu-id="e71fb-117">이 cmdlet이 *PortalHostnameConfiguration* 및 *ProxyHostnameConfiguration* 매개 변수를 가져오는 **PsApiManagement** 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-117">Specifies the **PsApiManagement** instance that this cmdlet gets the *PortalHostnameConfiguration* and *ProxyHostnameConfiguration* parameters from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement
Parameter Sets: Set from provided PsApiManagement instance
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e71fb-118">-이름</span><span class="sxs-lookup"><span data-stu-id="e71fb-118">-Name</span></span>
<span data-ttu-id="e71fb-119">API Management 인스턴스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-119">Specifies the name of the API Management instance.</span></span>

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

### <span data-ttu-id="e71fb-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e71fb-120">-PassThru</span></span>
<span data-ttu-id="e71fb-121">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-121">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e71fb-122">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e71fb-123">-PortalHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e71fb-123">-PortalHostnameConfiguration</span></span>
<span data-ttu-id="e71fb-124">사용자 지정 포털 호스트 이름 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-124">Specifies the custom portal hostname configuration.</span></span>
<span data-ttu-id="e71fb-125">Cmdlet에 $null를 전달 하면 기본 호스트 이름이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-125">Passing $null to the cmdlet sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e71fb-126">-ProxyHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e71fb-126">-ProxyHostnameConfiguration</span></span>
<span data-ttu-id="e71fb-127">사용자 지정 프록시 호스트 이름 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-127">Specifies the custom proxy hostname configuration.</span></span>
<span data-ttu-id="e71fb-128">$Null를 전달 하면 기본 호스트 이름이 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-128">Passing $null sets the default hostname.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagementHostnameConfiguration
Parameter Sets: Specific API Management service
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e71fb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e71fb-129">-ResourceGroupName</span></span>
<span data-ttu-id="e71fb-130">API Management 인스턴스가 있는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-130">Specifies the name of the resource group under which the API Management instance exists.</span></span>

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

### <span data-ttu-id="e71fb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e71fb-131">-DefaultProfile</span></span>
<span data-ttu-id="e71fb-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e71fb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e71fb-133">CommonParameters</span></span>
<span data-ttu-id="e71fb-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e71fb-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e71fb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e71fb-136">입력</span><span class="sxs-lookup"><span data-stu-id="e71fb-136">INPUTS</span></span>

### <span data-ttu-id="e71fb-137">PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="e71fb-137">PsApiManagement</span></span>
<span data-ttu-id="e71fb-138">' ApiManagement ' 매개 변수는 파이프라인에서 ' PsApiManagement ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e71fb-138">Parameter 'ApiManagement' accepts value of type 'PsApiManagement' from the pipeline</span></span>

## <span data-ttu-id="e71fb-139">출력</span><span class="sxs-lookup"><span data-stu-id="e71fb-139">OUTPUTS</span></span>

### <span data-ttu-id="e71fb-140">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="e71fb-140">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="e71fb-141">상속자</span><span class="sxs-lookup"><span data-stu-id="e71fb-141">NOTES</span></span>

## <span data-ttu-id="e71fb-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e71fb-142">RELATED LINKS</span></span>

[<span data-ttu-id="e71fb-143">가져오기-AzureRmApiManagementHostnameCertificate</span><span class="sxs-lookup"><span data-stu-id="e71fb-143">Import-AzureRmApiManagementHostnameCertificate</span></span>](./Import-AzureRmApiManagementHostnameCertificate.md)

[<span data-ttu-id="e71fb-144">새로운 AzureRmApiManagementHostnameConfiguration</span><span class="sxs-lookup"><span data-stu-id="e71fb-144">New-AzureRmApiManagementHostnameConfiguration</span></span>](./New-AzureRmApiManagementHostnameConfiguration.md)


