---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagement.md
ms.openlocfilehash: c00e8e8d33ef0f7b7b2591287e9bda9bc876e3c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308642"
---
# <span data-ttu-id="185ed-101">Set-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="185ed-101">Set-AzApiManagement</span></span>

## <span data-ttu-id="185ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="185ed-102">SYNOPSIS</span></span>
<span data-ttu-id="185ed-103">Azure Api Management 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="185ed-103">Updates an Azure Api Management service</span></span>

## <span data-ttu-id="185ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="185ed-104">SYNTAX</span></span>

```
Set-AzApiManagement -InputObject <PsApiManagement> [-SystemAssignedIdentity] [-UserAssignedIdentity <String[]>]
 [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="185ed-105">설명은</span><span class="sxs-lookup"><span data-stu-id="185ed-105">DESCRIPTION</span></span>

<span data-ttu-id="185ed-106">**AzApiManagement** Cmdlet은 Azure API Management 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-106">The **Set-AzApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="185ed-107">예제의</span><span class="sxs-lookup"><span data-stu-id="185ed-107">EXAMPLES</span></span>

### <span data-ttu-id="185ed-108">예제 1: API Management 서비스를 받고 Premium으로 확장 하 고 영역을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-108">Example 1: Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="185ed-109">이 예제에서는 Api Management 인스턴스를 가져오고, 5 개의 premium 단위로 크기를 조정 하 고, 프리미엄 영역에 3 단위를 추가로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="185ed-110">예제 2: 업데이트 배포 (외부 VNET)</span><span class="sxs-lookup"><span data-stu-id="185ed-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzApiManagement -InputObject $apim
```

<span data-ttu-id="185ed-111">이 명령은 기존 API Management 배포를 업데이트 하 고 외부 *VpnType* 에 참가 합니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="185ed-112">예제 3: KeyVault 리소스의 비밀을 사용 하 여 PsApiManagementCustomHostNameConfiguration 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="185ed-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
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

### <span data-ttu-id="185ed-113">예제 4: Publisher 전자 메일 업데이트, NotificationSender 전자 메일 및 조직 이름</span><span class="sxs-lookup"><span data-stu-id="185ed-113">Example 4: Update Publisher Email, NotificationSender Email and Organization Name</span></span>
```powershell
PS C:\> $apim = Get-AzApiManagement -ResourceGroupName "api-Default-West-US" -Name "Contoso"
PS C:\> $apim.PublisherEmail = "foobar@contoso.com"
PS C:\> $apim.NotificationSenderEmail = "notification@contoso.com"
PS C:\> $apim.OrganizationName = "Contoso"
PS C:\> Set-AzApiManagement -InputObject $apim -PassThru
```

## <span data-ttu-id="185ed-114">변수</span><span class="sxs-lookup"><span data-stu-id="185ed-114">PARAMETERS</span></span>

### <span data-ttu-id="185ed-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="185ed-115">-AsJob</span></span>
<span data-ttu-id="185ed-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="185ed-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="185ed-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="185ed-117">-DefaultProfile</span></span>
<span data-ttu-id="185ed-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="185ed-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="185ed-119">-InputObject</span></span>
<span data-ttu-id="185ed-120">ApiManagement 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-120">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="185ed-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="185ed-121">-PassThru</span></span>
<span data-ttu-id="185ed-122">작업이 성공한 경우 업데이트 된 PsApiManagement 파이프라인으로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-122">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="185ed-123">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="185ed-123">-SystemAssignedIdentity</span></span>
<span data-ttu-id="185ed-124">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-124">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="185ed-125">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="185ed-125">-UserAssignedIdentity</span></span>
<span data-ttu-id="185ed-126">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 사용자 Id를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-126">Assign User Identities to this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="185ed-127">-확인</span><span class="sxs-lookup"><span data-stu-id="185ed-127">-Confirm</span></span>
<span data-ttu-id="185ed-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="185ed-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="185ed-129">-WhatIf</span></span>
<span data-ttu-id="185ed-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="185ed-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="185ed-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="185ed-132">CommonParameters</span></span>
<span data-ttu-id="185ed-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="185ed-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="185ed-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="185ed-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="185ed-135">입력</span><span class="sxs-lookup"><span data-stu-id="185ed-135">INPUTS</span></span>

### <span data-ttu-id="185ed-136">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="185ed-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="185ed-137">출력</span><span class="sxs-lookup"><span data-stu-id="185ed-137">OUTPUTS</span></span>

### <span data-ttu-id="185ed-138">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="185ed-138">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="185ed-139">상속자</span><span class="sxs-lookup"><span data-stu-id="185ed-139">NOTES</span></span>

## <span data-ttu-id="185ed-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="185ed-140">RELATED LINKS</span></span>

[<span data-ttu-id="185ed-141">Get-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="185ed-141">Get-AzApiManagement</span></span>](./Get-AzApiManagement.md)

[<span data-ttu-id="185ed-142">새로운 AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="185ed-142">New-AzApiManagement</span></span>](./New-AzApiManagement.md)

[<span data-ttu-id="185ed-143">제거-AzApiManagement</span><span class="sxs-lookup"><span data-stu-id="185ed-143">Remove-AzApiManagement</span></span>](./Remove-AzApiManagement.md)
