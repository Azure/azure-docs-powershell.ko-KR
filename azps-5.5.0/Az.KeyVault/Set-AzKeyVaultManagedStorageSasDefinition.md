---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185484"
---
# <span data-ttu-id="3ab88-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="3ab88-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="3ab88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ab88-102">SYNOPSIS</span></span>
<span data-ttu-id="3ab88-103">주어진 Key Vault 관리 Azure Storage 계정에 대한 Key Vault를 사용하여 SAS(공유 액세스 서명) 정의를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="3ab88-104">구문</span><span class="sxs-lookup"><span data-stu-id="3ab88-104">SYNTAX</span></span>

### <span data-ttu-id="3ab88-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="3ab88-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ab88-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3ab88-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ab88-107">설명</span><span class="sxs-lookup"><span data-stu-id="3ab88-107">DESCRIPTION</span></span>
<span data-ttu-id="3ab88-108">주어진 Key Vault 관리 Azure Storage 계정으로 SAS(공유 액세스 서명) 정의를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="3ab88-109">또한 이 SAS 정의에 따라 SAS 토큰을 사용하는 데 사용할 수 있는 비밀을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="3ab88-110">SAS 토큰은 이러한 매개 변수 및 Key Vault 관리 Azure Storage 계정의 활성 키를 사용하여 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="3ab88-111">예제</span><span class="sxs-lookup"><span data-stu-id="3ab88-111">EXAMPLES</span></span>

### <span data-ttu-id="3ab88-112">예제 1: 계정 유형 SAS 정의를 설정하고 이를 기반으로 현재 SAS 토큰을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
```powershell
PS C:\> $sa = Get-AzStorageAccount -Name mysa -ResourceGroupName myrg
PS C:\> $kv = Get-AzKeyVault -VaultName mykv
PS C:\> Add-AzKeyVaultManagedStorageAccount -VaultName $kv.VaultName -AccountName $sa.StorageAccountName -AccountResourceId $sa.Id -ActiveKeyName key1 -RegenerationPeriod ([System.Timespan]::FromDays(180))
PS C:\> $sctx = New-AzStorageContext -StorageAccountName $sa.StorageAccountName -Protocol Https -StorageAccountKey Key1
PS C:\> $start = [System.DateTime]::Now.AddDays(-1)
PS C:\> $end = [System.DateTime]::Now.AddMonths(1)
PS C:\> $at = New-AzStorageAccountSasToken -Service blob,file,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -StartTime $start -ExpiryTime $end -Context $sctx
PS C:\> $sas = Set-AzKeyVaultManagedStorageSasDefinition -AccountName $sa.StorageAccountName -VaultName $kv.VaultName -Name accountsas -TemplateUri $at -SasType 'account' -ValidityPeriod ([System.Timespan]::FromDays(30))
PS C:\> Get-AzKeyVaultSecret -VaultName $kv.VaultName -Name $sas.Sid.Substring($sas.Sid.LastIndexOf('/')+1)
```

<span data-ttu-id="3ab88-113">자격 증명 모음 'mykv'의 KeyVault 관리 저장소 계정 'mysa'에서 계정 SAS 정의 'accountsas'를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="3ab88-114">특히 위의 시퀀스는 다음을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="3ab88-115">(기존) 저장소 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="3ab88-116">(기존) 키 자격 증명 모음을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="3ab88-117">KeyVault 관리 저장소 계정을 자격 증명 모음에 추가하고 Key1을 활성 키로 설정하고 다시 재생성 기간은 180일입니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="3ab88-118">Key1을 통해 지정된 저장소 계정에 대한 저장소 컨텍스트를 설정</span><span class="sxs-lookup"><span data-stu-id="3ab88-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="3ab88-119">서비스, 컨테이너 및 개체에 대한 서비스 Blob, 파일, 테이블 및 큐에 대한 계정 SAS 토큰을 만들고 https를 통해, 지정된 시작 및 종료 날짜를 사용하여 모든 권한을 사용하여 서비스, 컨테이너 및 개체에 대한 계정 SAS 토큰을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="3ab88-120">자격 증명 모음에서 KeyVault 관리 저장소 SAS 정의를 설정하고 템플릿 URI를 위에서 만든 SAS 토큰으로 설정하고 SAS 형식 '계정'으로 설정하고 30일 동안 유효합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="3ab88-121">SAS 정의에 해당하는 KeyVault 비밀에서 실제 액세스 토큰을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="3ab88-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ab88-122">PARAMETERS</span></span>

### <span data-ttu-id="3ab88-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3ab88-123">-AccountName</span></span>
<span data-ttu-id="3ab88-124">Key Vault 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="3ab88-125">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 관리되는 저장소 계정 이름에서 관리되는 저장소 계정 이름의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab88-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ab88-126">-DefaultProfile</span></span>
<span data-ttu-id="3ab88-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3ab88-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3ab88-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="3ab88-128">-Disable</span></span>
<span data-ttu-id="3ab88-129">sas 토큰 생성에 sas 정의 사용을 비활성화합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="3ab88-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3ab88-130">-InputObject</span></span>
<span data-ttu-id="3ab88-131">ManagedStorageAccount 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-131">ManagedStorageAccount object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ab88-132">-Name</span><span class="sxs-lookup"><span data-stu-id="3ab88-132">-Name</span></span>
<span data-ttu-id="3ab88-133">저장소 sas 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-133">Storage sas definition name.</span></span> <span data-ttu-id="3ab88-134">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경, 저장소 계정 이름 및 sas 정의 이름에서 저장소 sas 정의의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab88-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="3ab88-135">-SasType</span></span>
<span data-ttu-id="3ab88-136">저장소 SAS 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-136">Storage SAS type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab88-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="3ab88-137">-Tag</span></span>
<span data-ttu-id="3ab88-138">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3ab88-139">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="3ab88-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab88-140">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="3ab88-140">-TemplateUri</span></span>
<span data-ttu-id="3ab88-141">저장소 SAS 정의 템플릿 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-141">Storage SAS definition template uri.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab88-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="3ab88-142">-ValidityPeriod</span></span>
<span data-ttu-id="3ab88-143">생성되는 시간부터 sas 토큰의 만료 시간을 설정하는 데 사용되는 유효 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab88-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3ab88-144">-VaultName</span></span>
<span data-ttu-id="3ab88-145">자격 증명 모음 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-145">Vault name.</span></span>
<span data-ttu-id="3ab88-146">Cmdlet은 이름 및 현재 선택한 환경을 기반으로 자격 증명 모음의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ab88-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3ab88-147">-Confirm</span></span>
<span data-ttu-id="3ab88-148">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ab88-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ab88-149">-WhatIf</span></span>
<span data-ttu-id="3ab88-150">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3ab88-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ab88-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ab88-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ab88-152">CommonParameters</span></span>
<span data-ttu-id="3ab88-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3ab88-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ab88-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3ab88-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ab88-155">입력</span><span class="sxs-lookup"><span data-stu-id="3ab88-155">INPUTS</span></span>

### <span data-ttu-id="3ab88-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="3ab88-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="3ab88-157">출력</span><span class="sxs-lookup"><span data-stu-id="3ab88-157">OUTPUTS</span></span>

### <span data-ttu-id="3ab88-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="3ab88-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="3ab88-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3ab88-159">NOTES</span></span>

## <span data-ttu-id="3ab88-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ab88-160">RELATED LINKS</span></span>

[<span data-ttu-id="3ab88-161">Azureâ€'RM.â€'€Keyâ€€Vault</span><span class="sxs-lookup"><span data-stu-id="3ab88-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
