---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurermkeyvaultnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureRmKeyVaultNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureRmKeyVaultNetworkRuleSet.md
ms.openlocfilehash: b1a0081f24932cf25026bdea4e9064e9dbb5a0cb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529555"
---
# <span data-ttu-id="3887d-101">Update-AzureRmKeyVaultNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="3887d-101">Update-AzureRmKeyVaultNetworkRuleSet</span></span>

## <span data-ttu-id="3887d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3887d-102">SYNOPSIS</span></span>
<span data-ttu-id="3887d-103">키 자격 증명 모음의 네트워크 규칙 집합을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-103">Updates the network rule set on a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3887d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3887d-104">SYNTAX</span></span>

### <span data-ttu-id="3887d-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="3887d-105">ByVaultName (Default)</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3887d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3887d-106">ByInputObject</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-InputObject] <PSKeyVault>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3887d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3887d-107">ByResourceId</span></span>
```
Update-AzureRmKeyVaultNetworkRuleSet [-ResourceId] <String>
 [-DefaultAction <PSKeyVaultNetworkRuleDefaultActionEnum>] [-Bypass <PSKeyVaultNetworkRuleBypassEnum>]
 [-IpAddressRange <String[]>] [-VirtualNetworkResourceId <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3887d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3887d-108">DESCRIPTION</span></span>
<span data-ttu-id="3887d-109">**AzureRmKeyVaultNetworkRuleSet** 명령은 지정 된 키 보관소에 적용 되는 네트워크 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-109">The **Update-AzureRmKeyVaultNetworkRuleSet** command updates the network rules in effect on the specified key vault.</span></span> 

## <span data-ttu-id="3887d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3887d-110">EXAMPLES</span></span>

### <span data-ttu-id="3887d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="3887d-111">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzureRmVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Update-AzureRmKeyVaultNetworkRuleSet -VaultName 'myVault' -ResourceGroupName myRG -Bypass AzureServices -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

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

<span data-ttu-id="3887d-112">이 명령은 지정 된 IP 범위와 가상 네트워크에 대 한 ' myVault ' 이라는 자격 증명 모음의 네트워크 규칙 집합을 업데이트 하 여 Azure 서비스에 대 한 network rule을 무시할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-112">This command updates the network ruleset on the vault named 'myVault' for the specified IP range and the virtual network, allowing bypassing of the network rule for Azure services.</span></span>

## <span data-ttu-id="3887d-113">변수</span><span class="sxs-lookup"><span data-stu-id="3887d-113">PARAMETERS</span></span>

### <span data-ttu-id="3887d-114">-바이패스</span><span class="sxs-lookup"><span data-stu-id="3887d-114">-Bypass</span></span>
<span data-ttu-id="3887d-115">네트워크 규칙의 우회를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-115">Specifies bypass of network rule.</span></span>

```yaml
Type: PSKeyVaultNetworkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-116">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="3887d-116">-DefaultAction</span></span>
<span data-ttu-id="3887d-117">네트워크 규칙의 기본 동작을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-117">Specifies default action of network rule.</span></span>

```yaml
Type: PSKeyVaultNetworkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3887d-118">-DefaultProfile</span></span>
<span data-ttu-id="3887d-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3887d-120">-InputObject</span></span>
<span data-ttu-id="3887d-121">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="3887d-121">KeyVault object</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-122">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="3887d-122">-IpAddressRange</span></span>
<span data-ttu-id="3887d-123">네트워크 규칙의 허용 된 네트워크 IP 주소 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-123">Specifies allowed network IP address range of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3887d-124">-PassThru</span></span>
<span data-ttu-id="3887d-125">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-125">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="3887d-126">이 스위치가 지정 된 경우 업데이트 된 키 보관소 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-126">If this switch is specified, it returns the updated key vault object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3887d-127">-ResourceGroupName</span></span>
<span data-ttu-id="3887d-128">네트워크 규칙이 수정 되 고 있는 키 자격 증명 모음과 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-128">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3887d-129">-ResourceId</span></span>
<span data-ttu-id="3887d-130">KeyVault 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="3887d-130">KeyVault Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3887d-131">-VaultName</span></span>
<span data-ttu-id="3887d-132">네트워크 규칙이 수정 되 고 있는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-132">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3887d-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3887d-134">네트워크 규칙의 허용 되는 가상 네트워크 리소스 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-134">Specifies allowed virtual network resource identifier of network rule.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-135">-확인</span><span class="sxs-lookup"><span data-stu-id="3887d-135">-Confirm</span></span>
<span data-ttu-id="3887d-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3887d-137">-WhatIf</span></span>
<span data-ttu-id="3887d-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3887d-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-139">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3887d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3887d-140">CommonParameters</span></span>
<span data-ttu-id="3887d-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3887d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3887d-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3887d-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3887d-143">입력</span><span class="sxs-lookup"><span data-stu-id="3887d-143">INPUTS</span></span>

### <span data-ttu-id="3887d-144">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3887d-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="3887d-145">출력</span><span class="sxs-lookup"><span data-stu-id="3887d-145">OUTPUTS</span></span>

### <span data-ttu-id="3887d-146">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3887d-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="3887d-147">상속자</span><span class="sxs-lookup"><span data-stu-id="3887d-147">NOTES</span></span>

## <span data-ttu-id="3887d-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3887d-148">RELATED LINKS</span></span>
