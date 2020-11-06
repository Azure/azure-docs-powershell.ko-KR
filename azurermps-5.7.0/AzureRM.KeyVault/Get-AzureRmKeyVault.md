---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537739"
---
# <span data-ttu-id="b6f79-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6f79-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="b6f79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6f79-102">SYNOPSIS</span></span>
<span data-ttu-id="b6f79-103">키 볼트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6f79-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6f79-104">SYNTAX</span></span>

### <span data-ttu-id="b6f79-105">ListAllVaultsInSubscription (기본값)</span><span class="sxs-lookup"><span data-stu-id="b6f79-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6f79-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="b6f79-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6f79-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="b6f79-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b6f79-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="b6f79-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b6f79-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b6f79-109">DESCRIPTION</span></span>
<span data-ttu-id="b6f79-110">**AzureRmKeyVault** cmdlet은 구독의 키 자격 증명 모음에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="b6f79-111">구독에서 모든 키 보관소 인스턴스를 보거나 리소스 그룹 또는 특정 키 보관소를 기준으로 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="b6f79-112">단일 키 자격 증명 모음을 가져올 때이 cmdlet에 리소스 그룹을 지정 하는 것은 선택 사항 이지만 성능이 더 나은 지 확인 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="b6f79-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b6f79-113">EXAMPLES</span></span>

### <span data-ttu-id="b6f79-114">예제 1: 현재 구독의 모든 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6f79-114">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="b6f79-115">이 명령은 현재 구독의 모든 키 보관소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="b6f79-116">예제 2: 특정 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6f79-116">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="b6f79-117">이 명령은 현재 구독에서 Contoso03Vault 이라는 키 보관소를 가져온 다음이를 $MyVault 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-117">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="b6f79-118">$MyVault의 속성을 검사 하 여 키 자격 증명 모음에 대 한 세부 정보를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-118">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="b6f79-119">예제 3: 리소스 그룹의 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6f79-119">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="b6f79-120">이 명령은 ContosoPayRollResourceGroup 이라는 리소스 그룹의 모든 키 보관소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-120">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="b6f79-121">예제 4: 현재 구독에서 삭제 된 모든 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6f79-121">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="b6f79-122">이 명령은 현재 구독에서 삭제 된 모든 키 보관소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-122">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="b6f79-123">예제 5: 삭제 된 키 보관소 가져오기</span><span class="sxs-lookup"><span data-stu-id="b6f79-123">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="b6f79-124">이 명령은 현재 구독과 eastus2 지역에서 Contoso03Vault 이라는 삭제 된 키 보관소 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-124">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="b6f79-125">변수</span><span class="sxs-lookup"><span data-stu-id="b6f79-125">PARAMETERS</span></span>

### <span data-ttu-id="b6f79-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6f79-126">-DefaultProfile</span></span>
<span data-ttu-id="b6f79-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b6f79-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b6f79-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="b6f79-128">-InRemovedState</span></span>
<span data-ttu-id="b6f79-129">이전에 삭제 된 자격 증명을 출력에 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6f79-130">-위치</span><span class="sxs-lookup"><span data-stu-id="b6f79-130">-Location</span></span>
<span data-ttu-id="b6f79-131">삭제 된 자격 증명 모음의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-131">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f79-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6f79-132">-ResourceGroupName</span></span>
<span data-ttu-id="b6f79-133">쿼리할 키 자격 증명 또는 키 보관소와 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f79-134">태그</span><span class="sxs-lookup"><span data-stu-id="b6f79-134">-Tag</span></span>
<span data-ttu-id="b6f79-135">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b6f79-136">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="b6f79-136">For example:</span></span>

<span data-ttu-id="b6f79-137">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b6f79-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f79-138">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b6f79-138">-VaultName</span></span>
<span data-ttu-id="b6f79-139">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-139">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6f79-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6f79-140">CommonParameters</span></span>
<span data-ttu-id="b6f79-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6f79-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6f79-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6f79-143">입력</span><span class="sxs-lookup"><span data-stu-id="b6f79-143">INPUTS</span></span>

### <span data-ttu-id="b6f79-144">않아야</span><span class="sxs-lookup"><span data-stu-id="b6f79-144">None</span></span>
<span data-ttu-id="b6f79-145">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6f79-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b6f79-146">출력</span><span class="sxs-lookup"><span data-stu-id="b6f79-146">OUTPUTS</span></span>

### <span data-ttu-id="b6f79-147">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6f79-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b6f79-148">PSKeyVaultIdentityItem의 ' 1 [Microsoft Azure.] 목록. List.</span><span class="sxs-lookup"><span data-stu-id="b6f79-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem]</span></span>

### <span data-ttu-id="b6f79-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6f79-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

### <span data-ttu-id="b6f79-150">EletedKeyVault의 List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSD]</span><span class="sxs-lookup"><span data-stu-id="b6f79-150">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span></span>

## <span data-ttu-id="b6f79-151">상속자</span><span class="sxs-lookup"><span data-stu-id="b6f79-151">NOTES</span></span>

## <span data-ttu-id="b6f79-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6f79-152">RELATED LINKS</span></span>

[<span data-ttu-id="b6f79-153">새로운 AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6f79-153">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="b6f79-154">제거-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="b6f79-154">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
