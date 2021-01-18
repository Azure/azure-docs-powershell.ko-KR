---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: c437611603bab6b2c4b9fff5cd0696e306182afa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495343"
---
# <span data-ttu-id="b93da-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b93da-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="b93da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b93da-102">SYNOPSIS</span></span>
<span data-ttu-id="b93da-103">클라이언트의 인터넷 주소에 따라 키 자격 증명 모음에 대한 액세스를 제한하는 규칙을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="b93da-104">구문</span><span class="sxs-lookup"><span data-stu-id="b93da-104">SYNTAX</span></span>

### <span data-ttu-id="b93da-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="b93da-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b93da-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="b93da-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b93da-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b93da-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b93da-108">설명</span><span class="sxs-lookup"><span data-stu-id="b93da-108">DESCRIPTION</span></span>
<span data-ttu-id="b93da-109">**Add-AzKeyVaultNetworkRule** cmdlet은 키 자격 증명 모음에 대한 액세스를 해당 IP 주소 또는 해당 IP 주소가 지정한 호출자 집합 또는 키 자격 증명 모음이 속한 가상 네트워크로 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="b93da-110">규칙에는 액세스 정책을 통해 사용 권한이 부여된 다른 사용자, 애플리케이션 또는 보안 그룹에 대한 액세스를 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

<span data-ttu-id="b93da-111">네트워크 규칙을 추가하는 데(개인 `10.0.0.0-10.255.255.255` IP 주소) 내부의 IP 범위를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-111">Please note that any IP range inside `10.0.0.0-10.255.255.255` (private IP addresses) cannot be used to add network rules.</span></span>

## <span data-ttu-id="b93da-112">예제</span><span class="sxs-lookup"><span data-stu-id="b93da-112">EXAMPLES</span></span>

### <span data-ttu-id="b93da-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="b93da-113">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myvault
Resource Group Name              : myRG
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myRG/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myRG/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="b93da-114">이 명령은 지정된 자격 증명 모음에 네트워크 규칙을 추가하여 지정된 자격 증명 모음으로 식별된 가상 네트워크에서 지정된 IP 주소에 액세스할 $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="b93da-114">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="b93da-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b93da-115">PARAMETERS</span></span>

### <span data-ttu-id="b93da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93da-116">-DefaultProfile</span></span>
<span data-ttu-id="b93da-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b93da-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b93da-118">-InputObject</span></span>
<span data-ttu-id="b93da-119">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="b93da-119">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b93da-120">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="b93da-120">-IpAddressRange</span></span>
<span data-ttu-id="b93da-121">네트워크 규칙의 허용되는 네트워크 IP 주소 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-121">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93da-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b93da-122">-PassThru</span></span>
<span data-ttu-id="b93da-123">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b93da-124">이 스위치를 지정하면 업데이트된 키 자격 증명 모음 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-124">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="b93da-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b93da-125">-ResourceGroupName</span></span>
<span data-ttu-id="b93da-126">네트워크 규칙을 수정하는 키 자격 증명 모음과 연결된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-126">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93da-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b93da-127">-ResourceId</span></span>
<span data-ttu-id="b93da-128">KeyVault 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b93da-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b93da-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b93da-129">-VaultName</span></span>
<span data-ttu-id="b93da-130">네트워크 규칙을 수정하는 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-130">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93da-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="b93da-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="b93da-132">네트워크 규칙의 허용되는 가상 네트워크 리소스 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-132">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93da-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b93da-133">-Confirm</span></span>
<span data-ttu-id="b93da-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b93da-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b93da-135">-WhatIf</span></span>
<span data-ttu-id="b93da-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b93da-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b93da-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b93da-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93da-138">CommonParameters</span></span>
<span data-ttu-id="b93da-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b93da-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93da-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b93da-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93da-141">입력</span><span class="sxs-lookup"><span data-stu-id="b93da-141">INPUTS</span></span>

### <span data-ttu-id="b93da-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b93da-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b93da-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b93da-143">System.String</span></span>

## <span data-ttu-id="b93da-144">출력</span><span class="sxs-lookup"><span data-stu-id="b93da-144">OUTPUTS</span></span>

### <span data-ttu-id="b93da-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b93da-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="b93da-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b93da-146">NOTES</span></span>

## <span data-ttu-id="b93da-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b93da-147">RELATED LINKS</span></span>
