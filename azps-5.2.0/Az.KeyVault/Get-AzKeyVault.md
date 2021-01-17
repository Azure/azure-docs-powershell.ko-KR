---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 37ed0c0cb29e69aa2e8018bb193fa4c82b0c3bcb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370329"
---
# <span data-ttu-id="9c3f1-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="9c3f1-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="9c3f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c3f1-102">SYNOPSIS</span></span>
<span data-ttu-id="9c3f1-103">키 자격 증명 모음을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-103">Gets key vaults.</span></span>

## <span data-ttu-id="9c3f1-104">구문</span><span class="sxs-lookup"><span data-stu-id="9c3f1-104">SYNTAX</span></span>

### <span data-ttu-id="9c3f1-105">GetVaultByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="9c3f1-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c3f1-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="9c3f1-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9c3f1-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="9c3f1-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9c3f1-108">설명</span><span class="sxs-lookup"><span data-stu-id="9c3f1-108">DESCRIPTION</span></span>
<span data-ttu-id="9c3f1-109">**Get-AzKeyVault** cmdlet은 구독의 키 자격 증명 모음에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="9c3f1-110">구독의 모든 키 자격 증명 모음 인스턴스를 보거나 리소스 그룹 또는 특정 키 자격 증명 모음을 통해 결과를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="9c3f1-111">단일 키 자격 증명 모음을 얻을 때 이 cmdlet에 대해 리소스 그룹을 지정하는 것은 선택 사항이지만 성능을 향상하기 위해 이 작업을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="9c3f1-112">예제</span><span class="sxs-lookup"><span data-stu-id="9c3f1-112">EXAMPLES</span></span>

### <span data-ttu-id="9c3f1-113">예제 1: 현재 구독의 모든 키 자격 증명 모음을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-113">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault

Vault Name          : myvault1
Resource Group Name : myrg
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.Ke
                      yVault/vaults/myvault1
Tags                :


Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="9c3f1-114">이 명령은 현재 구독의 모든 키 자격 증명 모음을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="9c3f1-115">예제 2: 특정 키 자격 증명 모음을 얻게</span><span class="sxs-lookup"><span data-stu-id="9c3f1-115">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault'

Vault Name                       : myvault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
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

Tags                             :
```

<span data-ttu-id="9c3f1-116">이 명령은 현재 구독에서 myvault라는 키 자격 증명 모음을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="9c3f1-117">예제 3: 리소스 그룹에서 키 자격 증명 모음을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-117">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVault -ResourceGroupName 'myrg1'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="9c3f1-118">이 명령은 ContosoPayRollResourceGroup이라는 리소스 그룹의 모든 키 자격 증명 모음을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="9c3f1-119">예제 4: 현재 구독에서 삭제된 모든 키 자격 증명 모음을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="9c3f1-120">이 명령은 현재 구독에서 삭제된 모든 키 자격 증명 모음을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="9c3f1-121">예제 5: 삭제된 키 자격 증명 모음을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-121">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="9c3f1-122">이 명령은 현재 구독 및 westus 지역에서 myvault4라는 삭제된 키 자격 증명 모음 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="9c3f1-123">예제 6: 필터링을 사용하여 키 자격 증명 모음을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-123">Example 6: Get key vaults using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault*'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="9c3f1-124">이 명령은 "myvault"로 시작하는 구독의 모든 키 자격 증명 모음을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="9c3f1-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c3f1-125">PARAMETERS</span></span>

### <span data-ttu-id="9c3f1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c3f1-126">-DefaultProfile</span></span>
<span data-ttu-id="9c3f1-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9c3f1-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c3f1-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="9c3f1-128">-InRemovedState</span></span>
<span data-ttu-id="9c3f1-129">이전에 삭제된 자격 증명 모음을 출력에 표시하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c3f1-130">-Location</span><span class="sxs-lookup"><span data-stu-id="9c3f1-130">-Location</span></span>
<span data-ttu-id="9c3f1-131">삭제된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-131">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3f1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c3f1-132">-ResourceGroupName</span></span>
<span data-ttu-id="9c3f1-133">키 자격 증명 모음 또는 키 자격 증명 모음과 연결된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9c3f1-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="9c3f1-134">-Tag</span></span>
<span data-ttu-id="9c3f1-135">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9c3f1-136">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9c3f1-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c3f1-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9c3f1-137">-VaultName</span></span>
<span data-ttu-id="9c3f1-138">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="9c3f1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c3f1-139">CommonParameters</span></span>
<span data-ttu-id="9c3f1-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c3f1-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9c3f1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c3f1-142">입력</span><span class="sxs-lookup"><span data-stu-id="9c3f1-142">INPUTS</span></span>

### <span data-ttu-id="9c3f1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="9c3f1-143">System.String</span></span>

### <span data-ttu-id="9c3f1-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="9c3f1-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9c3f1-145">출력</span><span class="sxs-lookup"><span data-stu-id="9c3f1-145">OUTPUTS</span></span>

### <span data-ttu-id="9c3f1-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9c3f1-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="9c3f1-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9c3f1-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="9c3f1-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="9c3f1-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="9c3f1-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9c3f1-149">NOTES</span></span>

## <span data-ttu-id="9c3f1-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c3f1-150">RELATED LINKS</span></span>

[<span data-ttu-id="9c3f1-151">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="9c3f1-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="9c3f1-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="9c3f1-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
