---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 4D7EEDD7-89D4-4B1E-A9A1-B301E759CE72
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmStorageAccount.md
ms.openlocfilehash: 5ca65c09746f6bb9a050c14fe10987702465b484
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530635"
---
# <span data-ttu-id="04d69-101">Set-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04d69-101">Set-AzureRmStorageAccount</span></span>

## <span data-ttu-id="04d69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04d69-102">SYNOPSIS</span></span>
<span data-ttu-id="04d69-103">저장소 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-103">Modifies a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04d69-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04d69-104">SYNTAX</span></span>

### <span data-ttu-id="04d69-105">StorageEncryption (기본값)</span><span class="sxs-lookup"><span data-stu-id="04d69-105">StorageEncryption (Default)</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-StorageEncryption] [-AssignIdentity]
 [-NetworkRuleSet <PSNetworkRuleSet>] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="04d69-106">KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="04d69-106">KeyvaultEncryption</span></span>
```
Set-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String> [-Force] [[-SkuName] <String>]
 [[-AccessTier] <String>] [[-CustomDomainName] <String>] [[-UseSubDomain] <Boolean>]
 [[-EnableEncryptionService] <EncryptionSupportServiceEnum>]
 [[-DisableEncryptionService] <EncryptionSupportServiceEnum>] [[-Tag] <Hashtable>]
 [-EnableHttpsTrafficOnly <Boolean>] [-KeyvaultEncryption] -KeyName <String> -KeyVersion <String>
 -KeyVaultUri <String> [-AssignIdentity] [-NetworkRuleSet <PSNetworkRuleSet>]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04d69-107">설명은</span><span class="sxs-lookup"><span data-stu-id="04d69-107">DESCRIPTION</span></span>
<span data-ttu-id="04d69-108">**AzureRmStorageAccount** Cmdlet은 Azure 저장소 계정을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-108">The **Set-AzureRmStorageAccount** cmdlet modifies an Azure Storage account.</span></span>
<span data-ttu-id="04d69-109">이 cmdlet을 사용 하 여 계정 유형을 수정 하거나, 고객 도메인을 업데이트 하거나, 저장소 계정에서 태그를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-109">You can use this cmdlet to modify the account type, update a customer domain, or set tags on a Storage account.</span></span>

## <span data-ttu-id="04d69-110">예제의</span><span class="sxs-lookup"><span data-stu-id="04d69-110">EXAMPLES</span></span>

### <span data-ttu-id="04d69-111">예제 1: 저장소 계정 유형 설정</span><span class="sxs-lookup"><span data-stu-id="04d69-111">Example 1: Set the Storage account type</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -Type "Standard_RAGRS"
```

<span data-ttu-id="04d69-112">이 명령은 저장소 계정 유형을 Standard_RAGRS 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-112">This command sets the Storage account type to Standard_RAGRS.</span></span>

### <span data-ttu-id="04d69-113">예제 2: 저장소 계정의 사용자 지정 도메인 설정</span><span class="sxs-lookup"><span data-stu-id="04d69-113">Example 2: Set a custom domain for a Storage account</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.contoso.com" -UseSubDomain $True
```

<span data-ttu-id="04d69-114">이 명령은 저장소 계정에 대 한 사용자 지정 도메인을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-114">This command sets a custom domain for a Storage account.</span></span>

### <span data-ttu-id="04d69-115">예제 3: Blob 및 파일 서비스에서 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="04d69-115">Example 3: Enable encryption on Blob and File Services</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob,File"
```

<span data-ttu-id="04d69-116">이 명령은 저장소 계정의 Blob 및 파일에서 저장소 서비스 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-116">This command enables Storage Service encryption on Blob and File for a Storage account.</span></span>

### <span data-ttu-id="04d69-117">예제 4: 액세스 계층 값 설정</span><span class="sxs-lookup"><span data-stu-id="04d69-117">Example 4: Set the access tier value</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AccessTier Cool
```

<span data-ttu-id="04d69-118">명령에서 액세스 계층 값이 멋진 것으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-118">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="04d69-119">예제 4: 사용자 지정 도메인 및 태그 설정</span><span class="sxs-lookup"><span data-stu-id="04d69-119">Example 4: Set the custom domain and tags</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -CustomDomainName "www.domainname.com" -UseSubDomain $true -Tag @{tag0="value0";tag1="value1";tag2="value2"}
```

<span data-ttu-id="04d69-120">명령에서 액세스 계층 값이 멋진 것으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-120">The command sets the Access Tier value to be cool.</span></span>

### <span data-ttu-id="04d69-121">예제 5: Keyvault를 사용 하 여 Blob 서비스에서 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="04d69-121">Example 5: Enable encryption on Blob Services with Keyvault</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -AssignIdentity
PS C:\>$account = Get-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount"

PS C:\>$keyVault = New-AzureRmKeyVault -VaultName "MyKeyVault" -ResourceGroupName "MyResourceGroup" -Location "EastUS2"
PS C:\>$key = Add-AzureKeyVaultKey -VaultName "MyKeyVault" -Name "MyKey" -Destination 'Software'
PS C:\>Set-AzureRmKeyVaultAccessPolicy -VaultName "MyKeyVault" -ObjectId $account.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey

PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -EnableEncryptionService "Blob" -KeyvaultEncryption -KeyName $key.Name -KeyVersion $key.Version -KeyVaultUri $keyVault.VaultUri
```

<span data-ttu-id="04d69-122">이 명령은 새로 만든 Keyvault를 사용 하 여 Blob에서 저장소 서비스 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-122">This command enables Storage Service encryption on Blob with a new created Keyvault.</span></span>

### <span data-ttu-id="04d69-123">예제 6: KeySource를 "Microsoft. 저장소"로 설정한 파일 서비스에서 암호화 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="04d69-123">Example 6: Disable encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>
```
PS C:\>Set-AzureRmStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "MyStorageAccount" -DisableEncryptionService File  -StorageEncryption
```

<span data-ttu-id="04d69-124">이 명령은 KeySource가 "Microsoft. 저장소"로 설정 되어 있는 파일 서비스에서 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-124">This command disables encryption on File Services with KeySource set to "Microsoft.Storage"</span></span>

## <span data-ttu-id="04d69-125">변수</span><span class="sxs-lookup"><span data-stu-id="04d69-125">PARAMETERS</span></span>

### <span data-ttu-id="04d69-126">-AccessTier</span><span class="sxs-lookup"><span data-stu-id="04d69-126">-AccessTier</span></span>
<span data-ttu-id="04d69-127">이 cmdlet이 수정 하는 저장소 계정의 액세스 계층을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-127">Specifies the access tier of the Storage account that this cmdlet modifies.</span></span>
<span data-ttu-id="04d69-128">이 매개 변수에 허용 되는 값은 Hot 및 멋지게입니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-128">The acceptable values for this parameter are: Hot and Cool.</span></span>

<span data-ttu-id="04d69-129">액세스 계층을 변경 하면 추가 요금이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-129">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="04d69-130">자세한 내용은 Azure Blob Storage: Hot 저장소 계층 ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=786482 https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="04d69-130">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="04d69-131">저장소 계정의 종류가 저장소 인 경우에는이 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="04d69-131">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d69-132">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="04d69-132">-AssignIdentity</span></span>
<span data-ttu-id="04d69-133">Azure KeyVault 같은 키 관리 서비스에 사용 하기 위해이 저장소 계정에 대 한 새 저장소 계정 Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-133">Generate and assign a new Storage Account Identity for this storage account for use with key management services like Azure KeyVault.</span></span>

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

### <span data-ttu-id="04d69-134">-CustomDomainName</span><span class="sxs-lookup"><span data-stu-id="04d69-134">-CustomDomainName</span></span>
<span data-ttu-id="04d69-135">사용자 지정 도메인의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-135">Specifies the name of the custom domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d69-136">-Disable\ 서비스</span><span class="sxs-lookup"><span data-stu-id="04d69-136">-DisableEncryptionService</span></span>
<span data-ttu-id="04d69-137">이 cmdlet이 저장소 서비스에서 저장소 서비스 암호화를 사용 하지 않도록 설정할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-137">Indicates whether this cmdlet disables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="04d69-138">Azure Blob 및 Azure 파일 서비스가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-138">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d69-139">-Enable\ \ 서비스</span><span class="sxs-lookup"><span data-stu-id="04d69-139">-EnableEncryptionService</span></span>
<span data-ttu-id="04d69-140">이 cmdlet이 저장소 서비스에서 저장소 서비스 암호화를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-140">Indicates whether this cmdlet enables Storage Service encryption on the Storage Service.</span></span>
<span data-ttu-id="04d69-141">Azure Blob 및 Azure 파일 서비스가 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-141">Azure Blob and Azure File Services are supported.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Storage.StorageAccountBaseCmdlet+EncryptionSupportServiceEnum]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d69-142">-EnableHttpsTrafficOnly</span><span class="sxs-lookup"><span data-stu-id="04d69-142">-EnableHttpsTrafficOnly</span></span>
<span data-ttu-id="04d69-143">저장소 계정이 https 트래픽만 사용 하도록 설정 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-143">Indicates whether or not the Storage Account only enable https traffic.</span></span>

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

### <span data-ttu-id="04d69-144">-Force</span><span class="sxs-lookup"><span data-stu-id="04d69-144">-Force</span></span>
<span data-ttu-id="04d69-145">액세스 계층을 변경 하면 추가 요금이 발생할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-145">If you change the access tier, it may result in additional charges.</span></span>
<span data-ttu-id="04d69-146">자세한 내용은 Azure Blob Storage: Hot 저장소 계층 ()을 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=786482 https://go.microsoft.com/fwlink/?LinkId=786482) .</span><span class="sxs-lookup"><span data-stu-id="04d69-146">For more information, see Azure Blob Storage: Hot and cool storage tiershttps://go.microsoft.com/fwlink/?LinkId=786482 (https://go.microsoft.com/fwlink/?LinkId=786482).</span></span>
<span data-ttu-id="04d69-147">저장소 계정의 종류가 저장소 인 경우에는이 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="04d69-147">If the kind of Storage account is Storage, do not specify this parameter.</span></span>

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

### <span data-ttu-id="04d69-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="04d69-148">-InformationAction</span></span>
<span data-ttu-id="04d69-149">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="04d69-150">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04d69-151">하기로</span><span class="sxs-lookup"><span data-stu-id="04d69-151">Continue</span></span>
- <span data-ttu-id="04d69-152">숨기기</span><span class="sxs-lookup"><span data-stu-id="04d69-152">Ignore</span></span>
- <span data-ttu-id="04d69-153">Inquire</span><span class="sxs-lookup"><span data-stu-id="04d69-153">Inquire</span></span>
- <span data-ttu-id="04d69-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="04d69-154">SilentlyContinue</span></span>
- <span data-ttu-id="04d69-155">중지가</span><span class="sxs-lookup"><span data-stu-id="04d69-155">Stop</span></span>
- <span data-ttu-id="04d69-156">대기</span><span class="sxs-lookup"><span data-stu-id="04d69-156">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d69-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="04d69-157">-InformationVariable</span></span>
<span data-ttu-id="04d69-158">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-158">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d69-159">-KeyName</span><span class="sxs-lookup"><span data-stu-id="04d69-159">-KeyName</span></span>
<span data-ttu-id="04d69-160">저장소 계정 암호화 keySource Keysource KeyName</span><span class="sxs-lookup"><span data-stu-id="04d69-160">Storage Account encryption keySource KeyVault KeyName</span></span>

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

### <span data-ttu-id="04d69-161">-KeyvaultEncryption</span><span class="sxs-lookup"><span data-stu-id="04d69-161">-KeyvaultEncryption</span></span>
<span data-ttu-id="04d69-162">저장소 계정 암호화 KeySource를 Microsoft. Keysource로 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-162">Whether to set Storage Account Encryption KeySource to Microsoft.Keyvault or not.</span></span> <span data-ttu-id="04d69-163">KeyName, KeyVersion 및 KeyvaultUri를 지정 하면 저장소 계정 암호화 키 원본도 Microsoft로 설정 됩니다. Keyversion 날씨이 매개 변수는 설정 되거나 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-163">If you specify KeyName, KeyVersion and KeyvaultUri, Storage Account encryption keySource will also be set to Microsoft.Keyvault weather this parameter is set or not.</span></span>
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

### <span data-ttu-id="04d69-164">-KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="04d69-164">-KeyVaultUri</span></span>
<span data-ttu-id="04d69-165">저장소 계정 암호화 keySource Keysource KeyVaultUri</span><span class="sxs-lookup"><span data-stu-id="04d69-165">Storage Account encryption keySource KeyVault KeyVaultUri</span></span>

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

### <span data-ttu-id="04d69-166">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="04d69-166">-KeyVersion</span></span>
<span data-ttu-id="04d69-167">저장소 계정 암호화 keySource Keysource Keysource</span><span class="sxs-lookup"><span data-stu-id="04d69-167">Storage Account encryption keySource KeyVault KeyVersion</span></span>

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

### <span data-ttu-id="04d69-168">-이름</span><span class="sxs-lookup"><span data-stu-id="04d69-168">-Name</span></span>
<span data-ttu-id="04d69-169">수정할 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-169">Specifies the name of the Storage account to Modify.</span></span>

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

### <span data-ttu-id="04d69-170">-NetworkRuleSet 집합</span><span class="sxs-lookup"><span data-stu-id="04d69-170">-NetworkRuleSet</span></span>
<span data-ttu-id="04d69-171">저장소 계정 네트워크 규칙 집합</span><span class="sxs-lookup"><span data-stu-id="04d69-171">Storage Account NetworkRuleSet</span></span>

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

### <span data-ttu-id="04d69-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04d69-172">-ResourceGroupName</span></span>
<span data-ttu-id="04d69-173">저장소 계정을 수정할 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-173">Specifies the name of the resource group in which to modify the Storage account.</span></span>

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

### <span data-ttu-id="04d69-174">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="04d69-174">-SkuName</span></span>
<span data-ttu-id="04d69-175">저장소 계정의 SKU 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-175">Specifies the SKU name of the storage account.</span></span>
<span data-ttu-id="04d69-176">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-176">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="04d69-177">Standard_LRS.</span><span class="sxs-lookup"><span data-stu-id="04d69-177">Standard_LRS.</span></span>
<span data-ttu-id="04d69-178">로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="04d69-178">Locally-redundant storage.</span></span> 
- <span data-ttu-id="04d69-179">Standard_ZRS.</span><span class="sxs-lookup"><span data-stu-id="04d69-179">Standard_ZRS.</span></span>
<span data-ttu-id="04d69-180">영역 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="04d69-180">Zone-redundant storage.</span></span>
- <span data-ttu-id="04d69-181">Standard_GRS.</span><span class="sxs-lookup"><span data-stu-id="04d69-181">Standard_GRS.</span></span>
<span data-ttu-id="04d69-182">지리적 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="04d69-182">Geo-redundant storage.</span></span> 
- <span data-ttu-id="04d69-183">Standard_RAGRS.</span><span class="sxs-lookup"><span data-stu-id="04d69-183">Standard_RAGRS.</span></span>
<span data-ttu-id="04d69-184">액세스 지리적 중복 저장소 읽기</span><span class="sxs-lookup"><span data-stu-id="04d69-184">Read access geo-redundant storage.</span></span> 
- <span data-ttu-id="04d69-185">Premium_LRS.</span><span class="sxs-lookup"><span data-stu-id="04d69-185">Premium_LRS.</span></span>
<span data-ttu-id="04d69-186">프리미엄 로컬 중복 저장소.</span><span class="sxs-lookup"><span data-stu-id="04d69-186">Premium locally-redundant storage.</span></span>

<span data-ttu-id="04d69-187">Standard_ZRS 및 Premium_LRS 형식을 다른 계정 형식으로 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-187">You cannot change Standard_ZRS and Premium_LRS types to other account types.</span></span>
<span data-ttu-id="04d69-188">다른 계정 유형은 Standard_ZRS 하거나 Premium_LRS 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-188">You cannot change other account types to Standard_ZRS or Premium_LRS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountType, AccountType, Type

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04d69-189">-StorageEncryption</span><span class="sxs-lookup"><span data-stu-id="04d69-189">-StorageEncryption</span></span>
<span data-ttu-id="04d69-190">저장소 계정 암호화 KeySource를 Microsoft. 저장소로 설정할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-190">Whether to set Storage Account Encryption KeySource to Microsoft.Storage or not.</span></span>

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

### <span data-ttu-id="04d69-191">태그</span><span class="sxs-lookup"><span data-stu-id="04d69-191">-Tag</span></span>
<span data-ttu-id="04d69-192">New-AzureRmStorageAccount cmdlet의 *Kind* 매개 변수에 blobstorage 값을 지정 하는 경우 *AccessTier* 매개 변수에 대 한 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-192">If you specify a value of BlobStorage for the *Kind* parameter of the New-AzureRmStorageAccount cmdlet, you must specify a value for the *AccessTier* parameter.</span></span>

<span data-ttu-id="04d69-193">이 *Kind* 매개 변수에 대 한 저장소 값을 지정 하는 경우 *AccessTier* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="04d69-193">If you specify a value of Storage for this *Kind* parameter, do not specify the *AccessTier* parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04d69-194">-(도메인)</span><span class="sxs-lookup"><span data-stu-id="04d69-194">-UseSubDomain</span></span>
<span data-ttu-id="04d69-195">간접 CName 유효성 검사를 사용할지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-195">Indicates whether to enable indirect CName validation.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04d69-196">-확인</span><span class="sxs-lookup"><span data-stu-id="04d69-196">-Confirm</span></span>
<span data-ttu-id="04d69-197">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04d69-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04d69-198">-WhatIf</span></span>
<span data-ttu-id="04d69-199">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04d69-200">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04d69-201">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04d69-201">-DefaultProfile</span></span>
<span data-ttu-id="04d69-202">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-202">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04d69-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04d69-203">CommonParameters</span></span>
<span data-ttu-id="04d69-204">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04d69-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04d69-205">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04d69-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04d69-206">입력</span><span class="sxs-lookup"><span data-stu-id="04d69-206">INPUTS</span></span>

## <span data-ttu-id="04d69-207">출력</span><span class="sxs-lookup"><span data-stu-id="04d69-207">OUTPUTS</span></span>

## <span data-ttu-id="04d69-208">상속자</span><span class="sxs-lookup"><span data-stu-id="04d69-208">NOTES</span></span>

## <span data-ttu-id="04d69-209">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04d69-209">RELATED LINKS</span></span>

[<span data-ttu-id="04d69-210">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04d69-210">Get-AzureRmStorageAccount</span></span>](./Get-AzureRmStorageAccount.md)

[<span data-ttu-id="04d69-211">새로운 AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04d69-211">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="04d69-212">제거-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04d69-212">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

