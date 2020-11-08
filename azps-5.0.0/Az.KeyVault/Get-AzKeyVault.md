---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: cb1c4f901c598ec20af13e87707966704b285c64
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217732"
---
# <span data-ttu-id="a86ce-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a86ce-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="a86ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a86ce-102">SYNOPSIS</span></span>
<span data-ttu-id="a86ce-103">키 볼트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-103">Gets key vaults.</span></span>

## <span data-ttu-id="a86ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a86ce-104">SYNTAX</span></span>

### <span data-ttu-id="a86ce-105">GetVaultByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a86ce-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a86ce-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="a86ce-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a86ce-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="a86ce-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a86ce-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a86ce-108">DESCRIPTION</span></span>
<span data-ttu-id="a86ce-109">**AzKeyVault** cmdlet은 구독의 키 자격 증명 모음에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="a86ce-110">구독에서 모든 키 보관소 인스턴스를 보거나 리소스 그룹 또는 특정 키 보관소를 기준으로 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="a86ce-111">단일 키 자격 증명 모음을 가져올 때이 cmdlet에 리소스 그룹을 지정 하는 것은 선택 사항 이지만 성능이 더 나은 지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="a86ce-112">예제의</span><span class="sxs-lookup"><span data-stu-id="a86ce-112">EXAMPLES</span></span>

### <span data-ttu-id="a86ce-113">예제 1: 현재 구독의 모든 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="a86ce-113">Example 1: Get all key vaults in your current subscription</span></span>
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

<span data-ttu-id="a86ce-114">이 명령은 현재 구독의 모든 키 보관소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="a86ce-115">예제 2: 특정 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="a86ce-115">Example 2: Get a specific key vault</span></span>
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

<span data-ttu-id="a86ce-116">이 명령은 현재 구독에서 myvault 라는 키 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="a86ce-117">예제 3: 리소스 그룹의 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="a86ce-117">Example 3: Get key vaults in a resource group</span></span>
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

<span data-ttu-id="a86ce-118">이 명령은 ContosoPayRollResourceGroup 이라는 리소스 그룹의 모든 키 보관소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="a86ce-119">예제 4: 현재 구독에서 삭제 된 모든 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="a86ce-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
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

<span data-ttu-id="a86ce-120">이 명령은 현재 구독에서 삭제 된 모든 키 보관소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="a86ce-121">예제 5: 삭제 된 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="a86ce-121">Example 5: Get a deleted key vault</span></span>
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

<span data-ttu-id="a86ce-122">이 명령은 현재 구독과 westus 지역에서 myvault4 이라는 삭제 된 키 보관소 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="a86ce-123">예제 6: 필터링을 사용 하 여 키 자격 증명 모음 가져오기</span><span class="sxs-lookup"><span data-stu-id="a86ce-123">Example 6: Get key vaults using filtering</span></span>
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

<span data-ttu-id="a86ce-124">이 명령은 "myvault"로 시작 하는 구독의 모든 키 보관소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="a86ce-125">변수</span><span class="sxs-lookup"><span data-stu-id="a86ce-125">PARAMETERS</span></span>

### <span data-ttu-id="a86ce-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a86ce-126">-DefaultProfile</span></span>
<span data-ttu-id="a86ce-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a86ce-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a86ce-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="a86ce-128">-InRemovedState</span></span>
<span data-ttu-id="a86ce-129">이전에 삭제 된 자격 증명을 출력에 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="a86ce-130">-위치</span><span class="sxs-lookup"><span data-stu-id="a86ce-130">-Location</span></span>
<span data-ttu-id="a86ce-131">삭제 된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-131">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="a86ce-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a86ce-132">-ResourceGroupName</span></span>
<span data-ttu-id="a86ce-133">쿼리할 키 자격 증명 또는 키 보관소와 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a86ce-134">태그</span><span class="sxs-lookup"><span data-stu-id="a86ce-134">-Tag</span></span>
<span data-ttu-id="a86ce-135">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a86ce-136">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a86ce-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a86ce-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a86ce-137">-VaultName</span></span>
<span data-ttu-id="a86ce-138">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a86ce-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86ce-139">CommonParameters</span></span>
<span data-ttu-id="a86ce-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a86ce-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86ce-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a86ce-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86ce-142">입력</span><span class="sxs-lookup"><span data-stu-id="a86ce-142">INPUTS</span></span>

### <span data-ttu-id="a86ce-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a86ce-143">System.String</span></span>

### <span data-ttu-id="a86ce-144">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="a86ce-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a86ce-145">출력</span><span class="sxs-lookup"><span data-stu-id="a86ce-145">OUTPUTS</span></span>

### <span data-ttu-id="a86ce-146">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a86ce-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="a86ce-147">Microsoft. KeyVault. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="a86ce-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="a86ce-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="a86ce-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="a86ce-149">상속자</span><span class="sxs-lookup"><span data-stu-id="a86ce-149">NOTES</span></span>

## <span data-ttu-id="a86ce-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a86ce-150">RELATED LINKS</span></span>

[<span data-ttu-id="a86ce-151">새로운 AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a86ce-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="a86ce-152">제거-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="a86ce-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
