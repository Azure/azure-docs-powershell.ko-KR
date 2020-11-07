---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: d79c28b09c9f6ca36ae163566574555bb3c50459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703844"
---
# <span data-ttu-id="88b7d-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="88b7d-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="88b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="88b7d-103">키 볼트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88b7d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88b7d-104">SYNTAX</span></span>

### <span data-ttu-id="88b7d-105">ListAllVaultsInSubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="88b7d-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88b7d-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="88b7d-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88b7d-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="88b7d-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88b7d-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="88b7d-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88b7d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="88b7d-109">DESCRIPTION</span></span>
<span data-ttu-id="88b7d-110">**AzureRmKeyVault** cmdlet은 구독의 키 자격 증명 모음에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="88b7d-111">구독에서 모든 키 보관소 인스턴스를 보거나 리소스 그룹 또는 특정 키 보관소를 기준으로 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="88b7d-112">단일 키 자격 증명 모음을 가져올 때이 cmdlet에 리소스 그룹을 지정 하는 것은 선택 사항 이지만 성능이 더 나은 지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="88b7d-113">예제의</span><span class="sxs-lookup"><span data-stu-id="88b7d-113">EXAMPLES</span></span>

### <span data-ttu-id="88b7d-114">예제 1: 현재 구독의 모든 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="88b7d-114">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault

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

<span data-ttu-id="88b7d-115">이 명령은 현재 구독의 모든 키 보관소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="88b7d-116">예제 2: 특정 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="88b7d-116">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault -VaultName 'myvault'

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

<span data-ttu-id="88b7d-117">이 명령은 현재 구독에서 myvault 라는 키 자격 증명 모음을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-117">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="88b7d-118">예제 3: 리소스 그룹의 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="88b7d-118">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzureRmKeyVault -ResourceGroupName 'myrg1'

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

<span data-ttu-id="88b7d-119">이 명령은 ContosoPayRollResourceGroup 이라는 리소스 그룹의 모든 키 보관소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-119">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="88b7d-120">예제 4: 현재 구독에서 삭제 된 모든 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="88b7d-120">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzureRmKeyVault -InRemovedState

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

<span data-ttu-id="88b7d-121">이 명령은 현재 구독에서 삭제 된 모든 키 보관소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-121">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="88b7d-122">예제 5: 삭제 된 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="88b7d-122">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

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

<span data-ttu-id="88b7d-123">이 명령은 현재 구독과 westus 지역에서 myvault4 이라는 삭제 된 키 보관소 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-123">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

## <span data-ttu-id="88b7d-124">변수</span><span class="sxs-lookup"><span data-stu-id="88b7d-124">PARAMETERS</span></span>

### <span data-ttu-id="88b7d-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b7d-125">-DefaultProfile</span></span>
<span data-ttu-id="88b7d-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="88b7d-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b7d-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="88b7d-127">-InRemovedState</span></span>
<span data-ttu-id="88b7d-128">이전에 삭제 된 자격 증명을 출력에 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="88b7d-129">-위치</span><span class="sxs-lookup"><span data-stu-id="88b7d-129">-Location</span></span>
<span data-ttu-id="88b7d-130">삭제 된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-130">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="88b7d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b7d-131">-ResourceGroupName</span></span>
<span data-ttu-id="88b7d-132">쿼리할 키 자격 증명 또는 키 보관소와 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

### <span data-ttu-id="88b7d-133">태그</span><span class="sxs-lookup"><span data-stu-id="88b7d-133">-Tag</span></span>
<span data-ttu-id="88b7d-134">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="88b7d-135">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="88b7d-135">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88b7d-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="88b7d-136">-VaultName</span></span>
<span data-ttu-id="88b7d-137">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-137">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="88b7d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b7d-138">CommonParameters</span></span>
<span data-ttu-id="88b7d-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88b7d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b7d-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88b7d-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b7d-141">입력</span><span class="sxs-lookup"><span data-stu-id="88b7d-141">INPUTS</span></span>

### <span data-ttu-id="88b7d-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88b7d-142">System.String</span></span>

### <span data-ttu-id="88b7d-143">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="88b7d-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="88b7d-144">출력</span><span class="sxs-lookup"><span data-stu-id="88b7d-144">OUTPUTS</span></span>

### <span data-ttu-id="88b7d-145">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="88b7d-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="88b7d-146">Microsoft. KeyVault. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="88b7d-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="88b7d-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="88b7d-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="88b7d-148">상속자</span><span class="sxs-lookup"><span data-stu-id="88b7d-148">NOTES</span></span>

## <span data-ttu-id="88b7d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88b7d-149">RELATED LINKS</span></span>

[<span data-ttu-id="88b7d-150">새로운 AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="88b7d-150">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="88b7d-151">제거-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="88b7d-151">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
