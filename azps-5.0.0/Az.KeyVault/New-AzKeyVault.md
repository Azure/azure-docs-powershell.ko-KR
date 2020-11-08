---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 0da8ce1e7da509c140e5893240fadb37d7852ad8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226932"
---
# <span data-ttu-id="ce203-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ce203-101">New-AzKeyVault</span></span>

## <span data-ttu-id="ce203-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce203-102">SYNOPSIS</span></span>
<span data-ttu-id="ce203-103">키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-103">Creates a key vault.</span></span>

## <span data-ttu-id="ce203-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce203-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ce203-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ce203-105">DESCRIPTION</span></span>
<span data-ttu-id="ce203-106">**AzKeyVault** cmdlet은 지정 된 리소스 그룹에 키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="ce203-107">또한이 cmdlet은 현재 로그온 한 사용자에 게 키 자격 증명 모음에서 키와 비밀을 추가, 제거 또는 나열할 수 있는 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="ce203-108">참고: 새 키 자격 증명 모음을 만들려고 할 때 **구독이 ' microsoft. KeyVault '을 사용 하도록 등록 되어 있지 않은** 경우 **AzResourceProvider-Providernamespace "Microsoft. keyvault"** 을 실행 한 다음 **새-AzKeyVault** 명령을 다시 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce203-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="ce203-109">자세한 내용은 Register-AzResourceProvider를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce203-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="ce203-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ce203-110">EXAMPLES</span></span>

### <span data-ttu-id="ce203-111">예제 1: 표준 키 보관소 만들기</span><span class="sxs-lookup"><span data-stu-id="ce203-111">Example 1: Create a Standard key vault</span></span>
```powershell
PS C:\> New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
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

Tags                             :
```

<span data-ttu-id="ce203-112">이 명령은 Azure 지역 동부 US에 Contoso03Vault 이라는 키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="ce203-113">이 명령은 Group14 이라는 리소스 그룹에 키 보관소를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="ce203-114">명령이 *SKU* 매개 변수에 대 한 값을 지정 하지 않기 때문에 표준 키 자격 증명 모음이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="ce203-115">예제 2: Premium 키 자격 증명 모음 만들기</span><span class="sxs-lookup"><span data-stu-id="ce203-115">Example 2: Create a Premium key vault</span></span>
```powershell
PS C:\>New-AzKeyVault -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -Location 'East US' -Sku 'Premium'

Vault Name                       : contoso03vault
Resource Group Name              : group14
Location                         : East US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/group14/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Premium
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

Tags                             :
```

<span data-ttu-id="ce203-116">이 명령은 이전 예제와 마찬가지로 키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="ce203-117">그러나, Premium 키 자격 증명 모음을 만들기 위해 *SKU* 매개 변수에 premium 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="ce203-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="ce203-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="ce203-119">키 자격 증명 모음을 만들고 $myNetworkResId로 식별 되는 가상 네트워크에서 지정 된 IP 주소에 대 한 액세스를 허용 하는 네트워크 규칙을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="ce203-120">`New-AzKeyVaultNetworkRuleSetObject`자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce203-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="ce203-121">변수</span><span class="sxs-lookup"><span data-stu-id="ce203-121">PARAMETERS</span></span>

### <span data-ttu-id="ce203-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce203-122">-DefaultProfile</span></span>
<span data-ttu-id="ce203-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ce203-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce203-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="ce203-124">-EnabledForDeployment</span></span>
<span data-ttu-id="ce203-125">이 키 자격 증명 모음이 리소스 만들기에서 참조 되는 경우 (예: 가상 컴퓨터를 만들 때)이 키 보관소에서 비밀을 검색 하도록 Microsoft. a 리소스 공급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce203-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="ce203-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="ce203-127">Azure 디스크 암호화 서비스에서이 키 자격 증명 모음의 비밀 및 래핑 키를 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce203-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="ce203-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="ce203-129">이 키 자격 증명 모음이 서식 파일 배포에서 참조 되는 경우 Azure 리소스 관리자가이 키 보관소에서 비밀을 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce203-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="ce203-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="ce203-131">지정 된 경우 즉시 삭제에 대 한 보호가이 자격 증명 모음에 대해 사용 하도록 설정 됩니다. 또한 소프트 삭제를 사용 하도록 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="ce203-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="ce203-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="ce203-133">지정 된 경우 RBAC (역할 기반 액세스 제어)에의 한 데이터 작업에 권한을 부여할 수 있으며, 자격 증명 정보에 지정 된 액세스 정책이 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="ce203-134">관리 작업은 항상 RBAC를 사용 하 여 승인 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="ce203-135">-위치</span><span class="sxs-lookup"><span data-stu-id="ce203-135">-Location</span></span>
<span data-ttu-id="ce203-136">키 자격 증명 모음을 만들 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="ce203-137">[AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) 명령을 사용 하 여 선택 항목을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce203-138">-이름</span><span class="sxs-lookup"><span data-stu-id="ce203-138">-Name</span></span>
<span data-ttu-id="ce203-139">만들려는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="ce203-140">이름은 문자, 숫자 또는 하이픈을 임의로 조합 하 여 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="ce203-141">이름은 문자 또는 숫자로 시작 하 고 끝나야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="ce203-142">이름은 범용으로 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-142">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VaultName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce203-143">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="ce203-143">-NetworkRuleSet</span></span>
<span data-ttu-id="ce203-144">자격 증명 모음의 네트워크 규칙 집합을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="ce203-145">특정 네트워크 위치에서 키 보관소의 접근성을 제어 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="ce203-146">만든 사람 `New-AzKeyVaultNetworkRuleSetObject` .</span><span class="sxs-lookup"><span data-stu-id="ce203-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce203-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce203-147">-ResourceGroupName</span></span>
<span data-ttu-id="ce203-148">키 자격 증명 모음을 만들 기존 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce203-149">-Sku</span><span class="sxs-lookup"><span data-stu-id="ce203-149">-Sku</span></span>
<span data-ttu-id="ce203-150">키 보관소 인스턴스의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="ce203-151">각 SKU에 대해 사용할 수 있는 기능에 대 한 자세한 내용은 Azure 키 보관소 가격 웹 사이트 ()를 참조 하세요 https://go.microsoft.com/fwlink/?linkid=512521) .</span><span class="sxs-lookup"><span data-stu-id="ce203-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce203-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="ce203-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="ce203-153">삭제 된 리소스의 보존 기간 및 삭제 됨 상태의 개체를 제거할 수 있을 때까지 걸리는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="ce203-154">기본값은 90 일입니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-154">The default is 90 days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce203-155">태그</span><span class="sxs-lookup"><span data-stu-id="ce203-155">-Tag</span></span>
<span data-ttu-id="ce203-156">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ce203-157">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ce203-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce203-158">-확인</span><span class="sxs-lookup"><span data-stu-id="ce203-158">-Confirm</span></span>
<span data-ttu-id="ce203-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce203-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce203-160">-WhatIf</span></span>
<span data-ttu-id="ce203-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce203-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce203-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce203-163">CommonParameters</span></span>
<span data-ttu-id="ce203-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce203-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce203-165">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ce203-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce203-166">입력</span><span class="sxs-lookup"><span data-stu-id="ce203-166">INPUTS</span></span>

### <span data-ttu-id="ce203-167">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ce203-167">System.String</span></span>

### <span data-ttu-id="ce203-168">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ce203-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ce203-169">Microsoft Azure. KeyVault. 모델.</span><span class="sxs-lookup"><span data-stu-id="ce203-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="ce203-170">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ce203-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ce203-171">출력</span><span class="sxs-lookup"><span data-stu-id="ce203-171">OUTPUTS</span></span>

### <span data-ttu-id="ce203-172">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ce203-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="ce203-173">상속자</span><span class="sxs-lookup"><span data-stu-id="ce203-173">NOTES</span></span>

## <span data-ttu-id="ce203-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce203-174">RELATED LINKS</span></span>

[<span data-ttu-id="ce203-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ce203-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="ce203-176">제거-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="ce203-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
