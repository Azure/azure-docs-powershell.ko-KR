---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 0f7a05cd0cd711388973c3f823b1aee6aa9f6902
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490484"
---
# <span data-ttu-id="edf7a-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="edf7a-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="edf7a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edf7a-102">SYNOPSIS</span></span>
<span data-ttu-id="edf7a-103">리소스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-103">Gets a resource provider.</span></span>

## <span data-ttu-id="edf7a-104">구문</span><span class="sxs-lookup"><span data-stu-id="edf7a-104">SYNTAX</span></span>

### <span data-ttu-id="edf7a-105">ListAvailable(기본값)</span><span class="sxs-lookup"><span data-stu-id="edf7a-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="edf7a-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="edf7a-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edf7a-107">설명</span><span class="sxs-lookup"><span data-stu-id="edf7a-107">DESCRIPTION</span></span>
<span data-ttu-id="edf7a-108">**Get-AzResourceProvider** cmdlet은 Azure 리소스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="edf7a-109">예제</span><span class="sxs-lookup"><span data-stu-id="edf7a-109">EXAMPLES</span></span>

### <span data-ttu-id="edf7a-110">예제 1: 현재 구독에 등록된 모든 리소스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-110">Example 1: Get all resource providers registered with the current subscription</span></span>

```powershell
PS C:\>Get-AzResourceProvider

ProviderNamespace : Microsoft.AppConfiguration
RegistrationState : Registered
ResourceTypes     : {configurationStores, configurationStores/eventGridFilters, checkNameAvailability, locations…}
Locations         : {West Central US, Central US, West US, East US…}

ProviderNamespace : Microsoft.KeyVault
RegistrationState : Registered
ResourceTypes     : {vaults, vaults/secrets, vaults/accessPolicies, operations…}
Locations         : {North Central US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks, publicIPAddresses, networkInterfaces, privateEndpoints…}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets, virtualMachines, virtualMachines/extensions, virtualMachineScaleSets…}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Security
RegistrationState : Registered
ResourceTypes     : {operations, securityStatuses, tasks, regulatoryComplianceStandards…}
Locations         : {Central US, East US, West Europe, West Central US…}

ProviderNamespace : Microsoft.ResourceHealth
RegistrationState : Registered
ResourceTypes     : {availabilityStatuses, childAvailabilityStatuses, childResources, events…}
Locations         : {Australia Southeast}

ProviderNamespace : Microsoft.PolicyInsights
RegistrationState : Registered
ResourceTypes     : {policyEvents, policyStates, operations, asyncOperationResults…}
Locations         : {}

ProviderNamespace : Microsoft.Storage
RegistrationState : Registered
ResourceTypes     : {storageAccounts, operations, locations/asyncoperations, storageAccounts/listAccountSas…}
Locations         : {East US, East US 2, West US, West Europe…}

ProviderNamespace : Microsoft.Web
RegistrationState : Registered
ResourceTypes     : {publishingUsers, ishostnameavailable, validate, isusernameavailable…}
Locations         : {Central US, North Europe, West Europe, Southeast Asia…}

ProviderNamespace : Sendgrid.Email
RegistrationState : Registered
ResourceTypes     : {accounts, operations}
Locations         : {Australia East, Australia Southeast, Brazil South, Canada Central…}

ProviderNamespace : Microsoft.Authorization
RegistrationState : Registered
ResourceTypes     : {roleAssignments, roleDefinitions, classicAdministrators, permissions…}
Locations         : {}
...
```

<span data-ttu-id="edf7a-111">이 명령은 구독에서 모든 리소스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-111">This command gets all the resource providers from the subscription.</span></span>

### <span data-ttu-id="edf7a-112">예제 2: 주어진 ProviderNamespace에서 모든 리소스 공급자 세부 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="edf7a-112">Example 2: Get all resource provider details from the given ProviderNamespace</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/networkInterfaces}
Locations         : {East US, East US 2, West US, Central US…}
...
```

<span data-ttu-id="edf7a-113">이 명령은 "Microsoft.Compute" 아래에 있는 모든 리소스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-113">This command Gets all the resource providers under "Microsoft.Compute".</span></span>

### <span data-ttu-id="edf7a-114">예제 3: 제공된 ProviderNamespace 배열에서 모든 리소스 공급자 세부 정보 얻기</span><span class="sxs-lookup"><span data-stu-id="edf7a-114">Example 3: Get all resource provider details from the given ProviderNamespace array</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute,Microsoft.Network
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}
...

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {publicIPAddresses}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkInterfaces}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpoints}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpointRedirectMaps}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {loadBalancers}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkSecurityGroups}
Locations         : {West US, East US, North Europe, West Europe…}
...
```

<span data-ttu-id="edf7a-115">이 명령은 "Microsoft.Compute" 및 "Microsoft.Network" 아래에 있는 모든 리소스 공급자를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-115">This command Gets all the resource providers under "Microsoft.Compute" and "Microsoft.Network".</span></span>

## <span data-ttu-id="edf7a-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edf7a-116">PARAMETERS</span></span>

### <span data-ttu-id="edf7a-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="edf7a-117">-ApiVersion</span></span>
<span data-ttu-id="edf7a-118">리소스 공급자가 지원하는 API 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="edf7a-119">기본 버전과 다른 버전을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-119">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf7a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edf7a-120">-DefaultProfile</span></span>
<span data-ttu-id="edf7a-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="edf7a-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="edf7a-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="edf7a-122">-ListAvailable</span></span>
<span data-ttu-id="edf7a-123">이 작업이 사용 가능한 모든 리소스 공급자를 얻게 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-123">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf7a-124">-Location</span><span class="sxs-lookup"><span data-stu-id="edf7a-124">-Location</span></span>
<span data-ttu-id="edf7a-125">리소스 공급자의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-125">Specifies the location of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="edf7a-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="edf7a-126">-Pre</span></span>
<span data-ttu-id="edf7a-127">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="edf7a-128">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="edf7a-128">-ProviderNamespace</span></span>
<span data-ttu-id="edf7a-129">리소스 공급자의 네임스페이스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-129">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="edf7a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edf7a-130">CommonParameters</span></span>
<span data-ttu-id="edf7a-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="edf7a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edf7a-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="edf7a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edf7a-133">입력</span><span class="sxs-lookup"><span data-stu-id="edf7a-133">INPUTS</span></span>

### <span data-ttu-id="edf7a-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="edf7a-134">System.String[]</span></span>

## <span data-ttu-id="edf7a-135">출력</span><span class="sxs-lookup"><span data-stu-id="edf7a-135">OUTPUTS</span></span>

### <span data-ttu-id="edf7a-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="edf7a-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="edf7a-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="edf7a-137">NOTES</span></span>

## <span data-ttu-id="edf7a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edf7a-138">RELATED LINKS</span></span>

[<span data-ttu-id="edf7a-139">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="edf7a-139">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="edf7a-140">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="edf7a-140">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


