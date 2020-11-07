---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzStorageAccount.md
ms.openlocfilehash: 00665fbe6fc2cc0d78ebbfadded419a8b0157644
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876211"
---
# <span data-ttu-id="56ae2-101">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56ae2-101">Set-AzStorageAccount</span></span>

## <span data-ttu-id="56ae2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="56ae2-103">저장소 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-103">Modifies a Storage account.</span></span>

## <span data-ttu-id="56ae2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56ae2-104">SYNTAX</span></span>

### <span data-ttu-id="56ae2-105">StorageEncryption (기본값)</span><span class="sxs-lookup"><span data-stu-id="56ae2-105">StorageEncryption (Default)</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56ae2-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="56ae2-106">KeyvaultEncryption</span></span>
```
Set-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [-SkuName <String>]
 [-AccessTier <String>] [-CustomDomainName <String>] [-UseSubDomain <Boolean>] [-Tag <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>] [-UpgradeToStorageV2] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56ae2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="56ae2-107">DESCRIPTION</span></span>
<span data-ttu-id="56ae2-108">**AzStorageAccount** Cmdlet은 Azure 저장소 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-108">The **Set-AzStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="56ae2-109">이 cmdlet을 사용 하 여 계정 유형을 수정 하거나, 고객 도메인을 업데이트 하거나, 저장소 계정에서 태그를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="56ae2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="56ae2-110">EXAMPLES</span></span>

### <span data-ttu-id="56ae2-111">예제 1: 저장소 계정 유형 설정</span><span class="sxs-lookup"><span data-stu-id="56ae2-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="56ae2-112">이 명령은 저장소 계정 유형을 Standard_RAGRS 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="56ae2-113">예제 2: 저장소 계정의 사용자 지정 도메인 설정</span><span class="sxs-lookup"><span data-stu-id="56ae2-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="56ae2-114">이 명령은 저장소 계정에 대 한 사용자 지정 도메인을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="56ae2-115">예제 3: 액세스 계층 값 설정</span><span class="sxs-lookup"><span data-stu-id="56ae2-115">Example 3: Set the access tier value</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AccessTier Cool
```

<span data-ttu-id="56ae2-116">명령에서 액세스 계층 값이 멋진 것으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-116">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="56ae2-117">예제 4: 사용자 지정 도메인 및 태그 설정</span><span class="sxs-lookup"><span data-stu-id="56ae2-117">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="56ae2-118">이 명령은 저장소 계정의 사용자 지정 도메인 및 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-118">The command sets the custom domain and tags for a Storage account.</span></span>

### <span data-ttu-id="56ae2-119">예제 5: 암호화 KeySource를 Keysource로 설정</span><span class="sxs-lookup"><span data-stu-id="56ae2-119">Example 5: Set Encryption KeySource to Keyvault</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -AssignIdentity
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"

PS C:\>$keyVault = New-AzKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get

PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="56ae2-120">이 명령은 새로 만든 Keysource를 사용 하 여 암호화 KeySource를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-120">This command set Encryption KeySource with a new created Keyvault.</span></span>

### <span data-ttu-id="56ae2-121">예제 6: 암호화 KeySource를 "Microsoft. 저장소"로 설정</span><span class="sxs-lookup"><span data-stu-id="56ae2-121">Example 6: Set Encryption KeySource to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -StorageEncryption
```

<span data-ttu-id="56ae2-122">이 명령은 암호화 KeySource를 "Microsoft. 저장소"로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-122">This command set Encryption KeySource to "Microsoft.Storage"</span></span>

### <span data-ttu-id="56ae2-123">예제 7: JSON을 사용 하 여 저장소 계정의 NetworkRuleSet 규칙 집합 속성 설정</span><span class="sxs-lookup"><span data-stu-id="56ae2-123">Example 7: Set NetworkRuleSet property of a Storage account with JSON</span></span>
```
PS C:\>Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -NetworkRuleSet (@{bypass="Logging,Metrics";
    ipRules=(@{IPAddressOrRange="20.11.0.0/16";Action="allow"},
            @{IPAddressOrRange="10.0.0.0/7";Action="allow"});
    virtualNetworkRules=(@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},
                        @{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2";Action="allow"});
    defaultAction="allow"})
```

<span data-ttu-id="56ae2-124">이 명령은 JSON으로 저장소 계정의 네트워크 규칙 집합 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-124">This command sets NetworkRuleSet property of a Storage account with JSON</span></span>

### <span data-ttu-id="56ae2-125">예제 8: 저장소 계정에서 NetworkRuleSet 속성 가져오기 및 다른 저장소 계정으로 설정</span><span class="sxs-lookup"><span data-stu-id="56ae2-125">Example 8: Get NetworkRuleSet property from a Storage account, and set it to another Storage account</span></span>
```
PS C:\> $networkRuleSet = (Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount").NetworkRuleSet 
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount2" -NetworkRuleSet $networkRuleSet
```

<span data-ttu-id="56ae2-126">첫 번째 명령은 저장소 계정에서 NetworkRuleSet 집합 속성을 가져오며, 두 번째 명령은 다른 저장소 계정으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-126">This first command gets NetworkRuleSet property from a Storage account, and the second command sets it to another Storage account</span></span> 

### <span data-ttu-id="56ae2-127">예제 9: 유형 "저장소" 또는 "BlobStorage"를 "StorageV2" kind 저장소 계정으로 사용 하 여 저장소 계정 업그레이드</span><span class="sxs-lookup"><span data-stu-id="56ae2-127">Example 9: Upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account</span></span>
```
PS C:\> Set-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -UpgradeToStorageV2
```

<span data-ttu-id="56ae2-128">"저장소" 또는 "BlobStorage" 종류가 "StorageV2" kind 저장소 계정으로 저장 된 저장소 계정을 명령으로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-128">The command upgrade a Storage account with Kind "Storage" or "BlobStorage" to "StorageV2" kind Storage account.</span></span>

## <span data-ttu-id="56ae2-129">변수</span><span class="sxs-lookup"><span data-stu-id="56ae2-129">PARAMETERS</span></span>

### <span data-ttu-id="56ae2-130">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="56ae2-130">-AccessTier</span></span>
<span data-ttu-id="56ae2-131">이 cmdlet이 수정 하는 저장소 계정의 액세스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-131">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="56ae2-132">이 매개 변수에 허용 되는 값은 Hot 및 멋지게입니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-132">The acceptable values for this parameter are: Hot and Cool.</span></span>
<span data-ttu-id="56ae2-133">액세스 계층을 변경 하면 추가 요금이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-133">If you change the access tier, it may result in additional charges.</span></span> <span data-ttu-id="56ae2-134">자세한 내용은 [Azure Blob Storage: 핫 및 유용한 저장소 계층](http://go.microsoft.com/fwlink/?LinkId=786482)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="56ae2-134">For more information, see [Azure Blob Storage: Hot and cool storage tiers](http://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="56ae2-135">저장소 계정의 종류가 StorageV2 또는 BlobStorage 인 경우 *AccessTier* 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-135">If the Storage account has Kind as StorageV2 or BlobStorage, you can specify the *AccessTier* parameter.</span></span> <span data-ttu-id="56ae2-136">저장소 계정에 저장소 유형이 있는 경우 *AccessTier* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="56ae2-136">If the Storage account has Kind as Storage, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-137">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56ae2-137">-AsJob</span></span>
<span data-ttu-id="56ae2-138">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="56ae2-138">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56ae2-139">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="56ae2-139">-AssignIdentity</span></span>
<span data-ttu-id="56ae2-140">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 저장소 계정 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-140">Generate and assign a new Storage account Identity for this Storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="56ae2-141">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="56ae2-141">-CustomDomainName</span></span>
<span data-ttu-id="56ae2-142">사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-142">Specifies the name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ae2-143">-DefaultProfile</span></span>
<span data-ttu-id="56ae2-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56ae2-145">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="56ae2-145">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="56ae2-146">저장소 계정이 HTTPS 트래픽만 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-146">Indicates whether or not the Storage account only enables HTTPS traffic.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-147">-Force</span><span class="sxs-lookup"><span data-stu-id="56ae2-147">-Force</span></span>
<span data-ttu-id="56ae2-148">변경 내용이 저장소 계정에 기록 되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-148">Forces the change to be written to the Storage account.</span></span>

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

### <span data-ttu-id="56ae2-149">-KeyName</span><span class="sxs-lookup"><span data-stu-id="56ae2-149">-KeyName</span></span>
<span data-ttu-id="56ae2-150">-KeyvaultEncryption를 사용 하 여 키 자격 증명 모음으로 암호화를 사용 하는 경우이 옵션을 사용 하 여 Keyname 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-150">If using -KeyvaultEncryption to enable encryption with Key Vault, specify the Keyname property with this option.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-151">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="56ae2-151">-KeyvaultEncryption</span></span>
<span data-ttu-id="56ae2-152">저장소 서비스 암호화를 사용 하는 경우 암호화 키에 Microsoft KeyVault를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-152">Indicates whether or not to use Microsoft KeyVault for the encryption keys when using Storage Service Encryption.</span></span> <span data-ttu-id="56ae2-153">KeyName, KeyVersion, KeyVaultUri이 모두 설정 된 경우 Keyversion는이 매개 변수 설정 여부에 관계 없이 Microsoft. Keyversion에 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-153">If KeyName, KeyVersion, and KeyVaultUri are all set, KeySource will be set to Microsoft.Keyvault whether this parameter is set or not.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: KeyvaultEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-154">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="56ae2-154">-KeyVaultUri</span></span>
<span data-ttu-id="56ae2-155">-KeyvaultEncryption 매개 변수를 지정 하 여 키 보관소 암호화를 사용 하는 경우이 옵션을 사용 하 여 키 보관소에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-155">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-156">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="56ae2-156">-KeyVersion</span></span>
<span data-ttu-id="56ae2-157">-KeyvaultEncryption 매개 변수를 지정 하 여 키 보관소 암호화를 사용 하는 경우이 옵션을 사용 하 여 키 버전에 대 한 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-157">When using Key Vault Encryption by specifying the -KeyvaultEncryption parameter, use this option to specify the URI to the Key Version.</span></span>

```yaml
Type: System.String
Parameter Sets: KeyvaultEncryption
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-158">-이름</span><span class="sxs-lookup"><span data-stu-id="56ae2-158">-Name</span></span>
<span data-ttu-id="56ae2-159">수정할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-159">Specifies the name of the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-160">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="56ae2-160">-NetworkRuleSet</span></span>
<span data-ttu-id="56ae2-161">NetworkRuleSet는 방화벽과 가상 네트워크에 대 한 구성 규칙 집합을 정의 하 고 규칙을 우회 하도록 허용 된 서비스 같은 네트워크 속성에 대 한 값을 설정 하 고 정의 된 규칙과 일치 하지 않는 요청을 처리 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-161">NetworkRuleSet is used to define a set of configuration rules for firewalls and virtual networks, as well as to set values for network properties such as services allowed to bypass the rules and how to handle requests that don't match any of the defined rules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-162">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56ae2-162">-ResourceGroupName</span></span>
<span data-ttu-id="56ae2-163">저장소 계정을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-163">Specifies the name of the resource group in which to modify the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-164">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="56ae2-164">-SkuName</span></span>
<span data-ttu-id="56ae2-165">저장소 계정의 SKU 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-165">Specifies the SKU name of the Storage account.</span></span>
<span data-ttu-id="56ae2-166">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-166">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56ae2-167">Standard_LRS 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="56ae2-167">Standard_LRS - Locally-redundant storage.</span></span>
- <span data-ttu-id="56ae2-168">Standard_ZRS 영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="56ae2-168">Standard_ZRS - Zone-redundant storage.</span></span>
- <span data-ttu-id="56ae2-169">Standard_GRS 지역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="56ae2-169">Standard_GRS - Geo-redundant storage.</span></span>
- <span data-ttu-id="56ae2-170">Standard_RAGRS-액세스 지리적 중복 저장소를 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-170">Standard_RAGRS - Read access geo-redundant storage.</span></span>
- <span data-ttu-id="56ae2-171">Premium_LRS-Premium 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="56ae2-171">Premium_LRS - Premium locally-redundant storage.</span></span>
<span data-ttu-id="56ae2-172">Standard_ZRS 및 Premium_LRS 형식을 다른 계정 형식으로 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-172">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="56ae2-173">다른 계정 유형은 Standard_ZRS 하거나 Premium_LRS 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-173">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type
Accepted values: Standard_LRS, Standard_ZRS, Standard_GRS, Standard_RAGRS, Premium_LRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-174">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="56ae2-174">-StorageEncryption</span></span>
<span data-ttu-id="56ae2-175">Microsoft 관리 키를 사용 하도록 저장소 계정 암호화를 설정할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-175">Indicates whether or not to set the Storage account encryption to use Microsoft-managed keys.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StorageEncryption
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-176">태그</span><span class="sxs-lookup"><span data-stu-id="56ae2-176">-Tag</span></span>
<span data-ttu-id="56ae2-177">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-177">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="56ae2-178">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="56ae2-178">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="56ae2-179">-UpgradeToStorageV2</span><span class="sxs-lookup"><span data-stu-id="56ae2-179">-UpgradeToStorageV2</span></span>
<span data-ttu-id="56ae2-180">저장소 또는 BlobStorage에서 저장소 계정 종류를 StorageV2로 업그레이드 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-180">Upgrade Storage account Kind from  Storage or BlobStorage to StorageV2.</span></span>

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

### <span data-ttu-id="56ae2-181">-(도메인)</span><span class="sxs-lookup"><span data-stu-id="56ae2-181">-UseSubDomain</span></span>
<span data-ttu-id="56ae2-182">간접 CName 유효성 검사를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-182">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-183">-확인</span><span class="sxs-lookup"><span data-stu-id="56ae2-183">-Confirm</span></span>
<span data-ttu-id="56ae2-184">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-184">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-185">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56ae2-185">-WhatIf</span></span>
<span data-ttu-id="56ae2-186">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-186">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56ae2-187">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-187">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ae2-188">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ae2-188">CommonParameters</span></span>
<span data-ttu-id="56ae2-189">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56ae2-189">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ae2-190">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56ae2-190">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ae2-191">입력</span><span class="sxs-lookup"><span data-stu-id="56ae2-191">INPUTS</span></span>

### <span data-ttu-id="56ae2-192">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56ae2-192">System.String</span></span>

### <span data-ttu-id="56ae2-193">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="56ae2-193">System.Collections.Hashtable</span></span>

### <span data-ttu-id="56ae2-194">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="56ae2-194">System.Boolean</span></span>

## <span data-ttu-id="56ae2-195">출력</span><span class="sxs-lookup"><span data-stu-id="56ae2-195">OUTPUTS</span></span>

### <span data-ttu-id="56ae2-196">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56ae2-196">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="56ae2-197">상속자</span><span class="sxs-lookup"><span data-stu-id="56ae2-197">NOTES</span></span>

## <span data-ttu-id="56ae2-198">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56ae2-198">RELATED LINKS</span></span>

[<span data-ttu-id="56ae2-199">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56ae2-199">Get-AzStorageAccount</span></span>](./Get-AzStorageAccount.md)

[<span data-ttu-id="56ae2-200">새로운 AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56ae2-200">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="56ae2-201">제거-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="56ae2-201">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)
