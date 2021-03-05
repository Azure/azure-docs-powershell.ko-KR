---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/update-azkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultNetworkRuleSet.md
ms.openlocfilehash: d71712067b546e4147dff49b15dcf6466550131c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976880"
---
# <span data-ttu-id="1d140-101">Update-AzKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1d140-101">Update-AzKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="1d140-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d140-102">SYNOPSIS</span></span>
<span data-ttu-id="1d140-103">키 자격 증명 모음에 설정된 네트워크 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-103">Updates the network rule set on a key vault.</span></span>

## <span data-ttu-id="1d140-104">구문</span><span class="sxs-lookup"><span data-stu-id="1d140-104">SYNTAX</span></span>

### <span data-ttu-id="1d140-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="1d140-105">ByVaultName (Default)</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d140-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1d140-106">ByInputObject</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d140-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1d140-107">ByResourceId</span></span>
```
Update-AzKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d140-108">설명</span><span class="sxs-lookup"><span data-stu-id="1d140-108">DESCRIPTION</span></span>
<span data-ttu-id="1d140-109">**Update-AzKeyVaultNetworkRuleSet** 명령은 지정된 키 자격 증명 모음에 적용된 네트워크 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-109">The **Update-AzKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="1d140-110">예제</span><span class="sxs-lookup"><span data-stu-id="1d140-110">EXAMPLES</span></span>

### <span data-ttu-id="1d140-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1d140-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myRG
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
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
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myrg/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="1d140-112">이 명령은 지정된 IP 범위 및 가상 네트워크에 대해 'myVault'라는 자격 증명 모음의 네트워크 규칙 모음을 업데이트하여 Azure 서비스에 대한 네트워크 규칙을 우회할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

### <span data-ttu-id="1d140-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="1d140-113">Example 2</span></span>

<span data-ttu-id="1d140-114">키 자격 증명 모음에 설정된 네트워크 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-114">Updates the network rule set on a key vault.</span></span> <span data-ttu-id="1d140-115">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="1d140-115">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Update-AzKeyVaultNetworkRuleSet -DefaultAction Allow -VaultName 'myVault'
```

## <span data-ttu-id="1d140-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1d140-116">PARAMETERS</span></span>

### <span data-ttu-id="1d140-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="1d140-117">-Bypass</span></span>
<span data-ttu-id="1d140-118">네트워크 규칙의 우회를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-118">Specifies bypass of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum]
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d140-119">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="1d140-119">-DefaultAction</span></span>
<span data-ttu-id="1d140-120">네트워크 규칙의 기본 작업을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-120">Specifies default action of network rule.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum]
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d140-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d140-121">-DefaultProfile</span></span>
<span data-ttu-id="1d140-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d140-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d140-123">-InputObject</span></span>
<span data-ttu-id="1d140-124">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="1d140-124">KeyVault object</span></span>

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

### <span data-ttu-id="1d140-125">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="1d140-125">-IpAddressRange</span></span>
<span data-ttu-id="1d140-126">허용되는 네트워크 IP 주소 범위의 네트워크 규칙을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-126">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="1d140-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d140-127">-PassThru</span></span>
<span data-ttu-id="1d140-128">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-128">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="1d140-129">이 스위치가 지정되어 있는 경우 업데이트된 키 자격 증명 모음 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-129">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="1d140-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d140-130">-ResourceGroupName</span></span>
<span data-ttu-id="1d140-131">네트워크 규칙이 수정되는 키 자격 증명 모음과 연결된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-131">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="1d140-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d140-132">-ResourceId</span></span>
<span data-ttu-id="1d140-133">KeyVault 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="1d140-133">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="1d140-134">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1d140-134">-VaultName</span></span>
<span data-ttu-id="1d140-135">네트워크 규칙을 수정하는 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-135">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="1d140-136">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="1d140-136">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="1d140-137">네트워크 규칙의 허용된 가상 네트워크 리소스 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-137">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="1d140-138">-확인</span><span class="sxs-lookup"><span data-stu-id="1d140-138">-Confirm</span></span>
<span data-ttu-id="1d140-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d140-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d140-140">-WhatIf</span></span>
<span data-ttu-id="1d140-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d140-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d140-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d140-143">CommonParameters</span></span>
<span data-ttu-id="1d140-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1d140-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d140-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1d140-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d140-146">입력</span><span class="sxs-lookup"><span data-stu-id="1d140-146">INPUTS</span></span>

### <span data-ttu-id="1d140-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1d140-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="1d140-148">System.String</span><span class="sxs-lookup"><span data-stu-id="1d140-148">System.String</span></span>

### <span data-ttu-id="1d140-149">System.Nullable'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="1d140-149">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleDefaultActionEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="1d140-150">System.Nullable'1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="1d140-150">System.Nullable\`1[[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleBypassEnum, Microsoft.Azure.PowerShell.Cmdlets.KeyVault, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1d140-151">출력</span><span class="sxs-lookup"><span data-stu-id="1d140-151">OUTPUTS</span></span>

### <span data-ttu-id="1d140-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="1d140-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="1d140-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1d140-153">NOTES</span></span>

## <span data-ttu-id="1d140-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d140-154">RELATED LINKS</span></span>
