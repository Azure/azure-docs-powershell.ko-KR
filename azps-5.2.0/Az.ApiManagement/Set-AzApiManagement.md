---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: c00e8e8d33ef0f7b7b2591287e9bda9bc876e3c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337665"
---
# <span data-ttu-id="82365-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="82365-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="82365-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82365-102">SYNOPSIS</span></span>
<span data-ttu-id="82365-103">Azure Api Management 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="82365-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="82365-104">구문</span><span class="sxs-lookup"><span data-stu-id="82365-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82365-105">설명</span><span class="sxs-lookup"><span data-stu-id="82365-105">DESCRIPTION</span></span>

<span data-ttu-id="82365-106">**Set-AzApiManagement** cmdlet은 Azure API Management 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="82365-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="82365-107">예제</span><span class="sxs-lookup"><span data-stu-id="82365-107">EXAMPLES</span></span>

### <span data-ttu-id="82365-108">예제 1: API Management 서비스를 시작하고 프리미엄으로 확장하고 지역 추가</span><span class="sxs-lookup"><span data-stu-id="82365-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="82365-109">이 예제에서는 Api Management 인스턴스를 5개의 프리미엄 단위로 확장한 다음 프리미엄 지역에 3단위를 더 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="82365-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="82365-110">예제 2: 업데이트 배포(외부 VNET)</span><span class="sxs-lookup"><span data-stu-id="82365-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="82365-111">이 명령은 기존 API Management 배포를 업데이트하고 외부 *VpnType에 조인합니다.*</span><span class="sxs-lookup"><span data-stu-id="82365-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="82365-112">예제 3: KeyVault 리소스의 비밀을 사용하여 PsApiManagementCustomHostNameConfiguration 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="82365-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzApiManagement -InputObject $apim -SystemAssignedIdentity
```

### <span data-ttu-id="82365-113">예제 4: 게시자 전자 메일, NotificationSender 전자 메일 및 조직 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="82365-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="82365-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82365-114">PARAMETERS</span></span>

### <span data-ttu-id="82365-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82365-115">-AsJob</span></span>
<span data-ttu-id="82365-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="82365-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82365-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82365-117">-DefaultProfile</span></span>
<span data-ttu-id="82365-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82365-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82365-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82365-119">-InputObject</span></span>
<span data-ttu-id="82365-120">ApiManagement 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="82365-120">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="82365-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82365-121">-PassThru</span></span>
<span data-ttu-id="82365-122">작업이 성공하면 업데이트된 PsApiManagement를 파이프라인에 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="82365-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="82365-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="82365-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="82365-124">Azure KeyVault와 같은 키 관리 서비스에서 사용할 이 서버에 대한 Azure Active Directory ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="82365-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="82365-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="82365-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="82365-126">Azure KeyVault와 같은 키 관리 서비스에서 사용할 사용자 ID를 이 서버에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="82365-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="82365-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82365-127">-Confirm</span></span>
<span data-ttu-id="82365-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="82365-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82365-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82365-129">-WhatIf</span></span>
<span data-ttu-id="82365-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="82365-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="82365-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82365-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82365-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82365-132">CommonParameters</span></span>
<span data-ttu-id="82365-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="82365-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82365-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="82365-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82365-135">입력</span><span class="sxs-lookup"><span data-stu-id="82365-135">INPUTS</span></span>

### <span data-ttu-id="82365-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="82365-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="82365-137">출력</span><span class="sxs-lookup"><span data-stu-id="82365-137">OUTPUTS</span></span>

### <span data-ttu-id="82365-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span><span class="sxs-lookup"><span data-stu-id="82365-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="82365-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="82365-139">NOTES</span></span>

## <span data-ttu-id="82365-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82365-140">RELATED LINKS</span></span>

[<span data-ttu-id="82365-141">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="82365-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="82365-142">New-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="82365-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="82365-143">Remove-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="82365-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
