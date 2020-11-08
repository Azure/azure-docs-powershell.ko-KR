---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: b1c0326be98efed91ce53c9cf04cdee6fce658f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041634"
---
# <span data-ttu-id="98f28-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="98f28-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="98f28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98f28-102">SYNOPSIS</span></span>
<span data-ttu-id="98f28-103">키 자격 증명 모음에서 네트워크 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="98f28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="98f28-104">SYNTAX</span></span>

### <span data-ttu-id="98f28-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="98f28-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98f28-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="98f28-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98f28-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="98f28-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98f28-108">설명은</span><span class="sxs-lookup"><span data-stu-id="98f28-108">DESCRIPTION</span></span>
<span data-ttu-id="98f28-109">키 자격 증명 모음에서 네트워크 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="98f28-110">예제의</span><span class="sxs-lookup"><span data-stu-id="98f28-110">EXAMPLES</span></span>

### <span data-ttu-id="98f28-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="98f28-111">Example 1</span></span>
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

<span data-ttu-id="98f28-112">이 명령은 지정 된 IP 주소와 가상 네트워크 리소스 식별자가 일치 하는 규칙이 있는 경우 지정 된 자격 증명 모음에서 네트워크 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="98f28-113">변수</span><span class="sxs-lookup"><span data-stu-id="98f28-113">PARAMETERS</span></span>

### <span data-ttu-id="98f28-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f28-114">-DefaultProfile</span></span>
<span data-ttu-id="98f28-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f28-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98f28-116">-InputObject</span></span>
<span data-ttu-id="98f28-117">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="98f28-117">KeyVault object</span></span>

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

### <span data-ttu-id="98f28-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="98f28-118">-IpAddressRange</span></span>
<span data-ttu-id="98f28-119">네트워크 규칙의 허용 된 네트워크 IP 주소 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="98f28-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98f28-120">-PassThru</span></span>
<span data-ttu-id="98f28-121">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="98f28-122">이 스위치가 지정 된 경우 업데이트 된 키 보관소 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="98f28-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f28-123">-ResourceGroupName</span></span>
<span data-ttu-id="98f28-124">네트워크 규칙이 수정 되 고 있는 키 자격 증명 모음과 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="98f28-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98f28-125">-ResourceId</span></span>
<span data-ttu-id="98f28-126">KeyVault 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="98f28-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="98f28-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="98f28-127">-VaultName</span></span>
<span data-ttu-id="98f28-128">네트워크 규칙이 수정 되 고 있는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="98f28-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="98f28-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="98f28-130">네트워크 규칙의 허용 되는 가상 네트워크 리소스 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="98f28-131">-확인</span><span class="sxs-lookup"><span data-stu-id="98f28-131">-Confirm</span></span>
<span data-ttu-id="98f28-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f28-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98f28-133">-WhatIf</span></span>
<span data-ttu-id="98f28-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f28-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98f28-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f28-136">CommonParameters</span></span>
<span data-ttu-id="98f28-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="98f28-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f28-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="98f28-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f28-139">입력</span><span class="sxs-lookup"><span data-stu-id="98f28-139">INPUTS</span></span>

### <span data-ttu-id="98f28-140">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="98f28-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="98f28-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="98f28-141">System.String</span></span>

## <span data-ttu-id="98f28-142">출력</span><span class="sxs-lookup"><span data-stu-id="98f28-142">OUTPUTS</span></span>

### <span data-ttu-id="98f28-143">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="98f28-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="98f28-144">상속자</span><span class="sxs-lookup"><span data-stu-id="98f28-144">NOTES</span></span>

## <span data-ttu-id="98f28-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98f28-145">RELATED LINKS</span></span>