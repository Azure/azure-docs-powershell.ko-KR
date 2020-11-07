---
external help file: Microsoft.Azure.Commands.ApiManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagement.md
ms.openlocfilehash: 3831be3072f6922ad986cbde5a0a800764d1656a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703499"
---
# <span data-ttu-id="03bbc-101">Set-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="03bbc-101">Set-AzureRmApiManagement</span></span>

## <span data-ttu-id="03bbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03bbc-102">SYNOPSIS</span></span>
<span data-ttu-id="03bbc-103">Azure Api Management 서비스 업데이트</span><span class="sxs-lookup"><span data-stu-id="03bbc-103">Updates an Azure Api Management service</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="03bbc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03bbc-104">SYNTAX</span></span>

```
Set-AzureRmApiManagement -InputObject <PsApiManagement> [-AssignIdentity] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03bbc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03bbc-105">DESCRIPTION</span></span>

<span data-ttu-id="03bbc-106">**AzureRmApiManagement** Cmdlet은 Azure API Management 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-106">The **Set-AzureRmApiManagement** cmdlet updates an Azure API Management service.</span></span>

## <span data-ttu-id="03bbc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="03bbc-107">EXAMPLES</span></span>

### <span data-ttu-id="03bbc-108">예제 1 API Management 서비스를 다운로드 하 고 Premium으로 확장 하 고 지역을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-108">Example 1 Get an API Management service and scale it to Premium and Add a region</span></span>
```powershell
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.Sku = "Premium"
PS C:\> $apim.Capacity = 5
PS C:\> $apim.AddRegion("Central US", "Premium", 3)
PS C:\>Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="03bbc-109">이 예제에서는 Api Management 인스턴스를 가져오고, 5 개의 premium 단위로 크기를 조정 하 고, 프리미엄 영역에 3 단위를 추가로 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-109">This example gets an Api Management instance, scales it to five premium units and then adds an additional three units to the premium region.</span></span>

### <span data-ttu-id="03bbc-110">예제 2: 업데이트 배포 (외부 VNET)</span><span class="sxs-lookup"><span data-stu-id="03bbc-110">Example 2: Update deployment (external VNET)</span></span>
```powershell
PS C:\> $virtualNetwork = New-AzureRmApiManagementVirtualNetwork -Location "East US" -SubnetResourceId "/subscriptions/a8ff56dc-3bc7-4174-a1e8-3726ab15d0e2/resourceGroups/Api-Default-WestUS/providers/Microsoft.Network/virtualNetworks/dfVirtualNetwork/subnets/backendSubnet"
PS C:\> $apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\> $apim.VpnType = "External"
PS C:\> $apim.VirtualNetwork = $virtualNetwork
PS C:\> Set-AzureRmApiManagement -ApiManagement $apim
```

<span data-ttu-id="03bbc-111">이 명령은 기존 API Management 배포를 업데이트 하 고 외부 *VpnType* 에 참가 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-111">This command updates an existing API Management deployment and joins to an external *VpnType*.</span></span>

### <span data-ttu-id="03bbc-112">예제 3: KeyVault 리소스의 비밀을 사용 하 여 PsApiManagementCustomHostNameConfiguration 인스턴스 만들기 및 초기화</span><span class="sxs-lookup"><span data-stu-id="03bbc-112">Example 3: Create and initialize an instance of PsApiManagementCustomHostNameConfiguration using an Secret from KeyVault Resource</span></span>
```powershell
PS C:\>$portal = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "portal.contoso.com" -HostnameType Portal -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/api-portal-custom-ssl.pfx"
PS C:\>$proxy1 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.contoso.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/contoso-proxy-custom-ssl.pfx"
PS C:\>$proxy2 = New-AzureRmApiManagementCustomHostnameConfiguration -Hostname "gatewayl.foobar.com" -HostnameType Proxy -KeyVaultId "https://apim-test-keyvault.vault.azure.net/secrets/foobar-proxy-custom-ssl.pfx"
PS C:\>$proxyCustomConfig = @($proxy1,$proxy2)
PS C:\>$apim = Get-AzureRmApiManagement -ResourceGroupName "ContosoGroup" -Name "ContosoApi"
PS C:\>$apim.PortalCustomHostnameConfiguration = $portal
PS C:\>$apim.ProxyCustomHostnameConfiguration = $proxyCustomConfig 
PS C:\>Set-AzureRmApiManagement -InputObject $apim -AssignIdentity
```

## <span data-ttu-id="03bbc-113">변수</span><span class="sxs-lookup"><span data-stu-id="03bbc-113">PARAMETERS</span></span>

### <span data-ttu-id="03bbc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="03bbc-114">-AsJob</span></span>
<span data-ttu-id="03bbc-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="03bbc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="03bbc-116">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="03bbc-116">-AssignIdentity</span></span>
<span data-ttu-id="03bbc-117">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 서버에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-117">Generate and assign an Azure Active Directory Identity for this server for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="03bbc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03bbc-118">-DefaultProfile</span></span>
<span data-ttu-id="03bbc-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03bbc-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="03bbc-120">-InputObject</span></span>
<span data-ttu-id="03bbc-121">ApiManagement 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-121">The ApiManagement instance.</span></span>

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

### <span data-ttu-id="03bbc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="03bbc-122">-PassThru</span></span>
<span data-ttu-id="03bbc-123">작업이 성공한 경우 업데이트 된 PsApiManagement 파이프라인으로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-123">Sends updated PsApiManagement to pipeline if operation succeeds.</span></span>

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

### <span data-ttu-id="03bbc-124">-확인</span><span class="sxs-lookup"><span data-stu-id="03bbc-124">-Confirm</span></span>
<span data-ttu-id="03bbc-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03bbc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03bbc-126">-WhatIf</span></span>
<span data-ttu-id="03bbc-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03bbc-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03bbc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03bbc-129">CommonParameters</span></span>
<span data-ttu-id="03bbc-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03bbc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03bbc-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03bbc-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03bbc-132">입력</span><span class="sxs-lookup"><span data-stu-id="03bbc-132">INPUTS</span></span>

### <span data-ttu-id="03bbc-133">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="03bbc-133">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>
<span data-ttu-id="03bbc-134">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="03bbc-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="03bbc-135">출력</span><span class="sxs-lookup"><span data-stu-id="03bbc-135">OUTPUTS</span></span>

### <span data-ttu-id="03bbc-136">ApiManagement. PsApiManagement/.</span><span class="sxs-lookup"><span data-stu-id="03bbc-136">Microsoft.Azure.Commands.ApiManagement.Models.PsApiManagement</span></span>

## <span data-ttu-id="03bbc-137">상속자</span><span class="sxs-lookup"><span data-stu-id="03bbc-137">NOTES</span></span>

## <span data-ttu-id="03bbc-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03bbc-138">RELATED LINKS</span></span>

[<span data-ttu-id="03bbc-139">Get-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="03bbc-139">Get-AzureRmApiManagement</span></span>](./Get-AzureRmApiManagement.md)

[<span data-ttu-id="03bbc-140">새로운 AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="03bbc-140">New-AzureRmApiManagement</span></span>](./New-AzureRmApiManagement.md)

[<span data-ttu-id="03bbc-141">제거-AzureRmApiManagement</span><span class="sxs-lookup"><span data-stu-id="03bbc-141">Remove-AzureRmApiManagement</span></span>](./Remove-AzureRmApiManagement.md)
