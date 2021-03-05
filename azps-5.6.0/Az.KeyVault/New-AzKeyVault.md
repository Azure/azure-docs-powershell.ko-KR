---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C40DAC9-5C0B-4AFD-9BDB-D407E0B9F701
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVault.md
ms.openlocfilehash: 6af82533540bd93b90847c51b9aaf0bd603dc727
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001376"
---
# <span data-ttu-id="827b8-101">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="827b8-101">New-AzKeyVault</span></span>

## <span data-ttu-id="827b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="827b8-102">SYNOPSIS</span></span>
<span data-ttu-id="827b8-103">키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-103">Creates a key vault.</span></span>

## <span data-ttu-id="827b8-104">구문</span><span class="sxs-lookup"><span data-stu-id="827b8-104">SYNTAX</span></span>

```
New-AzKeyVault [-Name] <String> [-ResourceGroupName] <String> [-Location] <String> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-EnablePurgeProtection]
 [-EnableRbacAuthorization] [-SoftDeleteRetentionInDays <Int32>] [-Sku <String>] [-Tag <Hashtable>]
 [-NetworkRuleSet <PSKeyVaultNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="827b8-105">설명</span><span class="sxs-lookup"><span data-stu-id="827b8-105">DESCRIPTION</span></span>
<span data-ttu-id="827b8-106">**New-AzKeyVault** cmdlet은 지정된 리소스 그룹에 키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-106">The **New-AzKeyVault** cmdlet creates a key vault in the specified resource group.</span></span> <span data-ttu-id="827b8-107">또한 이 cmdlet은 키 자격 증명 모음에 키와 비밀을 추가, 제거 또는 나열할 수 있는 현재 로그온된 사용자에게 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-107">This cmdlet also grants permissions to the currently logged on user to add, remove, or list keys and secrets in the key vault.</span></span>
<span data-ttu-id="827b8-108">참고: 새 키 자격 증명 모음을 만들려고 할 때 네임스페이스 **'Microsoft.KeyVault'를** 사용하기 위해 구독이 등록되지 않은 경우 **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"를** 실행한 다음 **New-AzKeyVault** 명령을 다시 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-108">Note: If you see the error **The subscription is not registered to use namespace 'Microsoft.KeyVault'** when you try to create your new key vault, run **Register-AzResourceProvider -ProviderNamespace "Microsoft.KeyVault"** and then rerun your **New-AzKeyVault** command.</span></span> <span data-ttu-id="827b8-109">자세한 내용은 Register-AzResourceProvider를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="827b8-109">For more information, see Register-AzResourceProvider.</span></span>

## <span data-ttu-id="827b8-110">예제</span><span class="sxs-lookup"><span data-stu-id="827b8-110">EXAMPLES</span></span>

### <span data-ttu-id="827b8-111">예제 1: 표준 키 자격 증명 모음 만들기</span><span class="sxs-lookup"><span data-stu-id="827b8-111">Example 1: Create a Standard key vault</span></span>
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

<span data-ttu-id="827b8-112">이 명령은 미국 동부 Azure 지역에 Contoso03Vault라는 키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-112">This command creates a key vault named Contoso03Vault, in the Azure region East US.</span></span> <span data-ttu-id="827b8-113">명령은 Group14라는 리소스 그룹에 키 자격 증명 모음을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-113">The command adds the key vault to the resource group named Group14.</span></span> <span data-ttu-id="827b8-114">명령은 *SKU* 매개 변수에 대한 값을 지정하지 않습니다. 따라서 표준 키 자격 증명 모음이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-114">Because the command does not specify a value for the *SKU* parameter, it creates a Standard key vault.</span></span>

### <span data-ttu-id="827b8-115">예제 2: Premium 키 자격 증명 모음 만들기</span><span class="sxs-lookup"><span data-stu-id="827b8-115">Example 2: Create a Premium key vault</span></span>
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

<span data-ttu-id="827b8-116">이 명령은 이전 예제와 마찬가지로 키 자격 증명 모음을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-116">This command creates a key vault, just like the previous example.</span></span> <span data-ttu-id="827b8-117">그러나 프리미엄 키 자격 증명 모음을 만들기 위해 *SKU* 매개 변수에 대한 Premium 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-117">However, it specifies a value of Premium for the *SKU* parameter to create a Premium key vault.</span></span>

### <span data-ttu-id="827b8-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="827b8-118">Example 3</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "110.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "110.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> $ruleSet = New-AzKeyVaultNetworkRuleSetObject -DefaultAction Allow -Bypass AzureServices -IpAddressRange "110.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId
PS C:\> New-AzKeyVault -ResourceGroupName "myRg" -VaultName "myVault" -NetworkRuleSet $ruleSet
```

<span data-ttu-id="827b8-119">키 자격 증명 모음을 만들고 네트워크 규칙을 지정하여 네트워크에서 식별된 가상 네트워크에서 지정된 IP 주소에 액세스할 수 $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="827b8-119">Creating a key vault and specifies network rules to allow access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span> <span data-ttu-id="827b8-120">자세한 `New-AzKeyVaultNetworkRuleSetObject` 내용은 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="827b8-120">See `New-AzKeyVaultNetworkRuleSetObject` for more information.</span></span>

## <span data-ttu-id="827b8-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="827b8-121">PARAMETERS</span></span>

### <span data-ttu-id="827b8-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="827b8-122">-DefaultProfile</span></span>
<span data-ttu-id="827b8-123">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="827b8-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="827b8-124">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="827b8-124">-EnabledForDeployment</span></span>
<span data-ttu-id="827b8-125">가상 머신을 만들 때와 같은 리소스 만들기에서 이 키 자격 증명 모음을 참조할 때 Microsoft.Compute 리소스 공급자가 이 키 자격 증명 모음에서 비밀을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-125">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="827b8-126">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="827b8-126">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="827b8-127">Azure 디스크 암호화 서비스를 사용하여 이 키 자격 증명 모음에서 비밀을 얻고 키를 래프 래프할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-127">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="827b8-128">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="827b8-128">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="827b8-129">이 키 자격 증명 모음이 템플릿 배포에서 참조될 때 Azure Resource Manager가 이 키 자격 증명 모음에서 비밀을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-129">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="827b8-130">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="827b8-130">-EnablePurgeProtection</span></span>
<span data-ttu-id="827b8-131">지정한 경우 이 자격 증명 모음에 대해 즉각적인 지우기 방지가 활성화됩니다. 소프트 삭제도 사용하도록 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-131">If specified, protection against immediate deletion is enabled for this vault; requires soft delete to be enabled as well.</span></span>

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

### <span data-ttu-id="827b8-132">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="827b8-132">-EnableRbacAuthorization</span></span>
<span data-ttu-id="827b8-133">지정한 경우 RBAC(역할 기반 액세스 제어)에 의해 데이터 작업을 권한을 부여할 수 있으며 자격 증명 모음 속성에 지정된 액세스 정책은 무시됩니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-133">If specified, enables to authorize data actions by Role Based Access Control (RBAC), and then the access policies specified in vault properties will be ignored.</span></span> <span data-ttu-id="827b8-134">관리 작업은 항상 RBAC를 통해 권한이 부여됩니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-134">Note that management actions are always authorized with RBAC.</span></span>

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

### <span data-ttu-id="827b8-135">-Location</span><span class="sxs-lookup"><span data-stu-id="827b8-135">-Location</span></span>
<span data-ttu-id="827b8-136">키 자격 증명 모음을 만들 Azure 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-136">Specifies the Azure region in which to create the key vault.</span></span> <span data-ttu-id="827b8-137">[Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) 명령을 사용하여 선택을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-137">Use the command [Get-AzLocation](https://docs.microsoft.com/powershell/module/Azure/Get-AzLocation) to see your choices.</span></span>

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

### <span data-ttu-id="827b8-138">-Name</span><span class="sxs-lookup"><span data-stu-id="827b8-138">-Name</span></span>
<span data-ttu-id="827b8-139">만들 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-139">Specifies a name of the key vault to create.</span></span> <span data-ttu-id="827b8-140">이름은 문자, 숫자 또는 하이픈의 조합일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-140">The name can be any combination of letters, digits, or hyphens.</span></span> <span data-ttu-id="827b8-141">이름은 문자 또는 숫자로 시작하고 끝내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-141">The name must start and end with a letter or digit.</span></span> <span data-ttu-id="827b8-142">이름은 보편적으로 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-142">The name must be universally unique.</span></span>

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

### <span data-ttu-id="827b8-143">-NetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="827b8-143">-NetworkRuleSet</span></span>
<span data-ttu-id="827b8-144">자격 증명 모음의 네트워크 규칙 집합을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-144">Specifies the network rule set of the vault.</span></span> <span data-ttu-id="827b8-145">특정 네트워크 위치에서 키 자격 증명 모음의 접근성을 제어합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-145">It governs the accessibility of the key vault from specific network locations.</span></span> <span data-ttu-id="827b8-146">에 의해 `New-AzKeyVaultNetworkRuleSetObject` 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-146">Created by `New-AzKeyVaultNetworkRuleSetObject`.</span></span>

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

### <span data-ttu-id="827b8-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="827b8-147">-ResourceGroupName</span></span>
<span data-ttu-id="827b8-148">키 자격 증명 모음을 만들 기존 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-148">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="827b8-149">-Sku</span><span class="sxs-lookup"><span data-stu-id="827b8-149">-Sku</span></span>
<span data-ttu-id="827b8-150">키 자격 증명 모음 인스턴스의 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-150">Specifies the SKU of the key vault instance.</span></span> <span data-ttu-id="827b8-151">각 SKU에 사용할 수 있는 기능에 대한 자세한 내용은 Azure Key Vault 가격 책정 웹 https://go.microsoft.com/fwlink/?linkid=512521) 사이트(를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="827b8-151">For information about which features are available for each SKU, see the Azure Key Vault Pricing website (https://go.microsoft.com/fwlink/?linkid=512521).</span></span>

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

### <span data-ttu-id="827b8-152">-SoftDeleteRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="827b8-152">-SoftDeleteRetentionInDays</span></span>
<span data-ttu-id="827b8-153">삭제된 리소스가 보존되는 기간과 삭제된 상태의 자격 증명 모음 또는 개체를 제거할 수 있는 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-153">Specifies how long deleted resources are retained, and how long until a vault or an object in the deleted state can be purged.</span></span> <span data-ttu-id="827b8-154">기본값은 90일입니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-154">The default is 90 days.</span></span>

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

### <span data-ttu-id="827b8-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="827b8-155">-Tag</span></span>
<span data-ttu-id="827b8-156">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-156">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="827b8-157">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="827b8-157">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="827b8-158">-확인</span><span class="sxs-lookup"><span data-stu-id="827b8-158">-Confirm</span></span>
<span data-ttu-id="827b8-159">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="827b8-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="827b8-160">-WhatIf</span></span>
<span data-ttu-id="827b8-161">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="827b8-162">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="827b8-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="827b8-163">CommonParameters</span></span>
<span data-ttu-id="827b8-164">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="827b8-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="827b8-165">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="827b8-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="827b8-166">입력</span><span class="sxs-lookup"><span data-stu-id="827b8-166">INPUTS</span></span>

### <span data-ttu-id="827b8-167">System.String</span><span class="sxs-lookup"><span data-stu-id="827b8-167">System.String</span></span>

### <span data-ttu-id="827b8-168">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="827b8-168">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="827b8-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span><span class="sxs-lookup"><span data-stu-id="827b8-169">Microsoft.Azure.Management.KeyVault.Models.SkuName</span></span>

### <span data-ttu-id="827b8-170">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="827b8-170">System.Collections.Hashtable</span></span>

## <span data-ttu-id="827b8-171">출력</span><span class="sxs-lookup"><span data-stu-id="827b8-171">OUTPUTS</span></span>

### <span data-ttu-id="827b8-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="827b8-172">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="827b8-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="827b8-173">NOTES</span></span>

## <span data-ttu-id="827b8-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="827b8-174">RELATED LINKS</span></span>

[<span data-ttu-id="827b8-175">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="827b8-175">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="827b8-176">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="827b8-176">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
