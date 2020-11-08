---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultmanagedstoragesasdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultManagedStorageSasDefinition.md
ms.openlocfilehash: ff73d5db0b16d7176b9c49aa6e70bc13fc9f3fba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215283"
---
# <span data-ttu-id="f5014-101">Set-AzKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f5014-101">Set-AzKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f5014-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5014-102">SYNOPSIS</span></span>
<span data-ttu-id="f5014-103">지정 된 키 보관소 관리 Azure 저장소 계정에 대 한 키 보관소를 사용 하 여 SAS (공유 액세스 서명) 정의를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="f5014-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5014-104">SYNTAX</span></span>

### <span data-ttu-id="f5014-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f5014-105">Default (Default)</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>] -ValidityPeriod <TimeSpan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f5014-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f5014-106">ByInputObject</span></span>
```
Set-AzKeyVaultManagedStorageSasDefinition [-InputObject] <PSKeyVaultManagedStorageAccountIdentityItem>
 [-Name] <String> [-TemplateUri] <String> [-SasType] <String> [-Disable] [-Tag <Hashtable>]
 -ValidityPeriod <TimeSpan> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f5014-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f5014-107">DESCRIPTION</span></span>
<span data-ttu-id="f5014-108">지정 된 키 보관소 관리 Azure Storage 계정으로 SAS (공유 액세스 서명) 정의를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-108">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="f5014-109">이는 또한이 SAS 정의에 따라 SAS 토큰을 가져오는 데 사용할 수 있는 비밀을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-109">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="f5014-110">SAS 토큰은 이러한 매개 변수와 키 보관소 관리 Azure 저장소 계정의 활성 키를 사용 하 여 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-110">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="f5014-111">예제의</span><span class="sxs-lookup"><span data-stu-id="f5014-111">EXAMPLES</span></span>

### <span data-ttu-id="f5014-112">예제 1: 계정 유형 SAS 정의를 설정 하 고이를 기반으로 현재 SAS 토큰을 구합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-112">Example 1: Set an account-type SAS definition, and obtain a current SAS token based on it</span></span>
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

<span data-ttu-id="f5014-113">자격 증명 모음 ' mykv '의 KeyVault 관리 저장소 계정 ' mysa '에서 계정 SAS 정의 ' accountsas '를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-113">Sets an account SAS definition 'accountsas' on a KeyVault-managed storage account 'mysa' in vault 'mykv'.</span></span> <span data-ttu-id="f5014-114">구체적으로 위의 순서는 다음을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-114">Specifically, the sequence above performs the following:</span></span>
  - <span data-ttu-id="f5014-115">기존 저장소 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-115">gets a (pre-existing) storage account</span></span>
  - <span data-ttu-id="f5014-116">기존 키 보관소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-116">gets a (pre-existing) key vault</span></span>
  - <span data-ttu-id="f5014-117">자격 증명 모음에 KeyVault 관리 저장소 계정을 추가 하 고, Key1을 활성 키로 설정 하 고, 재생성 기간인 180 days를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-117">adds a KeyVault-managed storage account to the vault, setting Key1 as the active key, and with a regeneration period of 180 days</span></span>
  - <span data-ttu-id="f5014-118">Key1을 사용 하 여 지정 된 저장소 계정에 대 한 저장소 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-118">sets a storage context for the specified storage account, with Key1</span></span>
  - <span data-ttu-id="f5014-119">https 및 지정 된 시작 및 종료 날짜를 사용 하 여 모든 권한을 사용 하 여 서비스 Blob, 파일, 테이블 및 큐에 대 한 계정 SAS 토큰 (리소스 형식 서비스, 컨테이너 및 개체)을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-119">creates an account SAS token for services Blob, File, Table and Queue, for resource types Service, Container and Object, with all permissions, over https and with the specified start and end dates</span></span>
  - <span data-ttu-id="f5014-120">' 계정 ' SAS 유형 및 템플릿 uri를 사용 하 여 자격 증명 모음에서 KeyVault 관리 저장소 SAS 정의를 설정 하 고, ' account ' 및 30 일 동안 유효한 SAS 토큰</span><span class="sxs-lookup"><span data-stu-id="f5014-120">sets a KeyVault-managed storage SAS definition in the vault, with the template uri as the SAS token created above, of SAS type 'account' and valid for 30 days</span></span>
  - <span data-ttu-id="f5014-121">SAS 정의에 해당 하는 KeyVault 비밀에서 실제 액세스 토큰을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-121">retrieves the actual access token from the KeyVault secret corresponding to the SAS definition</span></span>

## <span data-ttu-id="f5014-122">변수</span><span class="sxs-lookup"><span data-stu-id="f5014-122">PARAMETERS</span></span>

### <span data-ttu-id="f5014-123">-AccountName</span><span class="sxs-lookup"><span data-stu-id="f5014-123">-AccountName</span></span>
<span data-ttu-id="f5014-124">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-124">Key Vault managed storage account name.</span></span> <span data-ttu-id="f5014-125">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-125">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

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

### <span data-ttu-id="f5014-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5014-126">-DefaultProfile</span></span>
<span data-ttu-id="f5014-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f5014-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5014-128">-Disable</span><span class="sxs-lookup"><span data-stu-id="f5014-128">-Disable</span></span>
<span data-ttu-id="f5014-129">Sas 토큰 생성을 위한 sas 정의 사용을 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-129">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="f5014-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f5014-130">-InputObject</span></span>
<span data-ttu-id="f5014-131">ManagedStorageAccount 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-131">ManagedStorageAccount object.</span></span>

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

### <span data-ttu-id="f5014-132">-이름</span><span class="sxs-lookup"><span data-stu-id="f5014-132">-Name</span></span>
<span data-ttu-id="f5014-133">저장소 sas 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-133">Storage sas definition name.</span></span> <span data-ttu-id="f5014-134">Cmdlet은 자격 증명 모음 이름, 현재 선택 된 환경, 저장소 계정 이름 및 sas 정의 이름에서 저장소 sas 정의의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-134">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

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

### <span data-ttu-id="f5014-135">-SasType</span><span class="sxs-lookup"><span data-stu-id="f5014-135">-SasType</span></span>
<span data-ttu-id="f5014-136">저장소 SAS 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-136">Storage SAS type.</span></span>

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

### <span data-ttu-id="f5014-137">태그</span><span class="sxs-lookup"><span data-stu-id="f5014-137">-Tag</span></span>
<span data-ttu-id="f5014-138">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-138">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f5014-139">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f5014-139">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="f5014-140">-서식 기능 Uri</span><span class="sxs-lookup"><span data-stu-id="f5014-140">-TemplateUri</span></span>
<span data-ttu-id="f5014-141">저장소 SAS 정의 템플릿 uri입니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-141">Storage SAS definition template uri.</span></span>

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

### <span data-ttu-id="f5014-142">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="f5014-142">-ValidityPeriod</span></span>
<span data-ttu-id="f5014-143">Sas 토큰이 생성 된 시간에서 만료 되는 시간을 설정 하는 데 사용 되는 유효 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-143">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

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

### <span data-ttu-id="f5014-144">-VaultName</span><span class="sxs-lookup"><span data-stu-id="f5014-144">-VaultName</span></span>
<span data-ttu-id="f5014-145">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="f5014-145">Vault name.</span></span>
<span data-ttu-id="f5014-146">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-146">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="f5014-147">-확인</span><span class="sxs-lookup"><span data-stu-id="f5014-147">-Confirm</span></span>
<span data-ttu-id="f5014-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5014-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5014-149">-WhatIf</span></span>
<span data-ttu-id="f5014-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5014-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5014-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5014-152">CommonParameters</span></span>
<span data-ttu-id="f5014-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5014-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5014-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5014-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5014-155">입력</span><span class="sxs-lookup"><span data-stu-id="f5014-155">INPUTS</span></span>

### <span data-ttu-id="f5014-156">Microsoft. KeyVault. PSKeyVaultManagedStorageAccountIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f5014-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageAccountIdentityItem</span></span>

## <span data-ttu-id="f5014-157">출력</span><span class="sxs-lookup"><span data-stu-id="f5014-157">OUTPUTS</span></span>

### <span data-ttu-id="f5014-158">Microsoft. KeyVault. PSKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="f5014-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="f5014-159">상속자</span><span class="sxs-lookup"><span data-stu-id="f5014-159">NOTES</span></span>

## <span data-ttu-id="f5014-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5014-160">RELATED LINKS</span></span>

[<span data-ttu-id="f5014-161">Azureâ € ‹ RM. a € ‹ Keyâ € ‹ 볼트</span><span class="sxs-lookup"><span data-stu-id="f5014-161">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/az.keyvault/)
