---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: ee7b9672869bba13b72ddd7b5a1d0b26325e9f62
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879273"
---
# <span data-ttu-id="756ac-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="756ac-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="756ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="756ac-102">SYNOPSIS</span></span>
<span data-ttu-id="756ac-103">클라이언트의 인터넷 주소에 따라 키 보관소에 대 한 액세스를 제한 하기 위한 규칙을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="756ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="756ac-104">SYNTAX</span></span>

### <span data-ttu-id="756ac-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="756ac-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="756ac-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="756ac-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="756ac-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="756ac-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="756ac-108">설명은</span><span class="sxs-lookup"><span data-stu-id="756ac-108">DESCRIPTION</span></span>
<span data-ttu-id="756ac-109">**AzKeyVaultNetworkRule** cmdlet은 해당 IP 주소 또는 자신이 속한 가상 네트워크에 의해 지정 된 호출자 집합에 대 한 키 자격 증명에 대 한 액세스 권한을 부여 하거나 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="756ac-110">이 규칙은 액세스 정책을 통해 사용 권한을 부여 받은 다른 사용자, 응용 프로그램 또는 보안 그룹에 대 한 액세스를 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

## <span data-ttu-id="756ac-111">예제의</span><span class="sxs-lookup"><span data-stu-id="756ac-111">EXAMPLES</span></span>

### <span data-ttu-id="756ac-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="756ac-112">Example 1</span></span>
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

<span data-ttu-id="756ac-113">이 명령은 지정 된 자격 증명 모음에 네트워크 규칙을 추가 하 여 $myNetworkResId으로 식별 되는 가상 네트워크에서 지정 된 IP 주소에 액세스할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-113">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="756ac-114">변수</span><span class="sxs-lookup"><span data-stu-id="756ac-114">PARAMETERS</span></span>

### <span data-ttu-id="756ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="756ac-115">-DefaultProfile</span></span>
<span data-ttu-id="756ac-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="756ac-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="756ac-117">-InputObject</span></span>
<span data-ttu-id="756ac-118">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="756ac-118">KeyVault object</span></span>

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

### <span data-ttu-id="756ac-119">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="756ac-119">-IpAddressRange</span></span>
<span data-ttu-id="756ac-120">네트워크 규칙의 허용 된 네트워크 IP 주소 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-120">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="756ac-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="756ac-121">-PassThru</span></span>
<span data-ttu-id="756ac-122">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-122">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="756ac-123">이 스위치가 지정 된 경우 업데이트 된 키 보관소 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-123">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="756ac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="756ac-124">-ResourceGroupName</span></span>
<span data-ttu-id="756ac-125">네트워크 규칙이 수정 되 고 있는 키 자격 증명 모음과 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-125">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="756ac-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="756ac-126">-ResourceId</span></span>
<span data-ttu-id="756ac-127">KeyVault 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="756ac-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="756ac-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="756ac-128">-VaultName</span></span>
<span data-ttu-id="756ac-129">네트워크 규칙이 수정 되 고 있는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-129">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="756ac-130">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="756ac-130">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="756ac-131">네트워크 규칙의 허용 되는 가상 네트워크 리소스 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-131">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="756ac-132">-확인</span><span class="sxs-lookup"><span data-stu-id="756ac-132">-Confirm</span></span>
<span data-ttu-id="756ac-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="756ac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="756ac-134">-WhatIf</span></span>
<span data-ttu-id="756ac-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="756ac-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="756ac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="756ac-137">CommonParameters</span></span>
<span data-ttu-id="756ac-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="756ac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="756ac-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="756ac-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="756ac-140">입력</span><span class="sxs-lookup"><span data-stu-id="756ac-140">INPUTS</span></span>

### <span data-ttu-id="756ac-141">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="756ac-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="756ac-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="756ac-142">System.String</span></span>

## <span data-ttu-id="756ac-143">출력</span><span class="sxs-lookup"><span data-stu-id="756ac-143">OUTPUTS</span></span>

### <span data-ttu-id="756ac-144">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="756ac-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="756ac-145">상속자</span><span class="sxs-lookup"><span data-stu-id="756ac-145">NOTES</span></span>

## <span data-ttu-id="756ac-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="756ac-146">RELATED LINKS</span></span>
