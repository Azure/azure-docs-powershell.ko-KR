---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: 6949de15168043e9ede9e8a023f6f5fcec333557
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952507"
---
# <span data-ttu-id="83f32-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="83f32-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="83f32-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83f32-102">SYNOPSIS</span></span>
<span data-ttu-id="83f32-103">키 자격 증명 모음에서 네트워크 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="83f32-104">구문</span><span class="sxs-lookup"><span data-stu-id="83f32-104">SYNTAX</span></span>

### <span data-ttu-id="83f32-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="83f32-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f32-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="83f32-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="83f32-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="83f32-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="83f32-108">설명</span><span class="sxs-lookup"><span data-stu-id="83f32-108">DESCRIPTION</span></span>
<span data-ttu-id="83f32-109">키 자격 증명 모음에서 네트워크 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="83f32-110">예제</span><span class="sxs-lookup"><span data-stu-id="83f32-110">EXAMPLES</span></span>

### <span data-ttu-id="83f32-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="83f32-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myrg
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
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="83f32-112">이 명령은 지정된 IP 주소 및 가상 네트워크 리소스 식별자와 일치하는 규칙이 발견된 경우 지정된 자격 증명 모음에서 네트워크 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="83f32-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="83f32-113">PARAMETERS</span></span>

### <span data-ttu-id="83f32-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83f32-114">-DefaultProfile</span></span>
<span data-ttu-id="83f32-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83f32-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83f32-116">-InputObject</span></span>
<span data-ttu-id="83f32-117">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="83f32-117">KeyVault object</span></span>

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

### <span data-ttu-id="83f32-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="83f32-118">-IpAddressRange</span></span>
<span data-ttu-id="83f32-119">허용되는 네트워크 IP 주소 범위의 네트워크 규칙을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="83f32-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="83f32-120">-PassThru</span></span>
<span data-ttu-id="83f32-121">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="83f32-122">이 스위치가 지정되어 있는 경우 업데이트된 키 자격 증명 모음 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="83f32-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83f32-123">-ResourceGroupName</span></span>
<span data-ttu-id="83f32-124">네트워크 규칙이 수정되는 키 자격 증명 모음과 연결된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="83f32-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="83f32-125">-ResourceId</span></span>
<span data-ttu-id="83f32-126">KeyVault 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="83f32-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="83f32-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="83f32-127">-VaultName</span></span>
<span data-ttu-id="83f32-128">네트워크 규칙을 수정하는 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="83f32-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="83f32-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="83f32-130">네트워크 규칙의 허용된 가상 네트워크 리소스 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="83f32-131">-확인</span><span class="sxs-lookup"><span data-stu-id="83f32-131">-Confirm</span></span>
<span data-ttu-id="83f32-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83f32-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83f32-133">-WhatIf</span></span>
<span data-ttu-id="83f32-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83f32-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83f32-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83f32-136">CommonParameters</span></span>
<span data-ttu-id="83f32-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83f32-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83f32-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83f32-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83f32-139">입력</span><span class="sxs-lookup"><span data-stu-id="83f32-139">INPUTS</span></span>

### <span data-ttu-id="83f32-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="83f32-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="83f32-141">System.String</span><span class="sxs-lookup"><span data-stu-id="83f32-141">System.String</span></span>

## <span data-ttu-id="83f32-142">출력</span><span class="sxs-lookup"><span data-stu-id="83f32-142">OUTPUTS</span></span>

### <span data-ttu-id="83f32-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="83f32-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="83f32-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83f32-144">NOTES</span></span>

## <span data-ttu-id="83f32-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83f32-145">RELATED LINKS</span></span>
