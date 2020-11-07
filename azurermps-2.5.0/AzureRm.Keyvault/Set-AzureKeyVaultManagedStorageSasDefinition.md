---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultmanagedstoragesasdefinition
schema: 2.0.0
ms.openlocfilehash: 0b1cc516f4ca3e434c0cc5e6dfe47b199ad509a3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880418"
---
# <span data-ttu-id="56af4-101">Set-AzureKeyVaultManagedStorageSasDefinition</span><span class="sxs-lookup"><span data-stu-id="56af4-101">Set-AzureKeyVaultManagedStorageSasDefinition</span></span>

## <span data-ttu-id="56af4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56af4-102">SYNOPSIS</span></span>
<span data-ttu-id="56af4-103">지정 된 키 보관소 관리 Azure 저장소 계정에 대 한 키 보관소를 사용 하 여 SAS (공유 액세스 서명) 정의를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-103">Sets a Shared Access Signature (SAS) definition with Key Vault for a given Key Vault managed Azure Storage Account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56af4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56af4-104">SYNTAX</span></span>

### <span data-ttu-id="56af4-105">RawSas (기본값)</span><span class="sxs-lookup"><span data-stu-id="56af4-105">RawSas (Default)</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Parameter] <Hashtable> [-Disable] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af4-106">AdhocAccountSas</span><span class="sxs-lookup"><span data-stu-id="56af4-106">AdhocAccountSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition -Service <String[]> -ResourceType <String[]>
 [-ApiVersion <String>] [-VaultName] <String> [-AccountName] <String> [-Name] <String> [-Disable]
 [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>] [-IPAddressOrRange <String>]
 -ValidityPeriod <TimeSpan> -Permission <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af4-107">AdhocServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="56af4-107">AdhocServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Blob <String>
 -Container <String> [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af4-108">AdhocServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="56af4-108">AdhocServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Container <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56af4-109">AdhocServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="56af4-109">AdhocServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> -Path <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af4-110">AdhocServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="56af4-110">AdhocServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]>
 [-SharedAccessHeader <String[]>] -Share <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af4-111">AdhocServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="56af4-111">AdhocServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Queue <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af4-112">AdhocServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="56af4-112">AdhocServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -ValidityPeriod <TimeSpan> -Permission <String[]> -Table <String>
 [-StartPartitionKey <String>] [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af4-113">StoredPolicyServiceBlobSas</span><span class="sxs-lookup"><span data-stu-id="56af4-113">StoredPolicyServiceBlobSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Blob <String> -Container <String> -Policy <String>
 [-SharedAccessHeader <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="56af4-114">StoredPolicyServiceContainerSas</span><span class="sxs-lookup"><span data-stu-id="56af4-114">StoredPolicyServiceContainerSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Container <String> -Policy <String> [-SharedAccessHeader <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af4-115">StoredPolicyServiceFileSas</span><span class="sxs-lookup"><span data-stu-id="56af4-115">StoredPolicyServiceFileSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String> -Path <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af4-116">StoredPolicyServiceShareSas</span><span class="sxs-lookup"><span data-stu-id="56af4-116">StoredPolicyServiceShareSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> [-SharedAccessHeader <String[]>] -Share <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af4-117">StoredPolicyServiceQueueSas</span><span class="sxs-lookup"><span data-stu-id="56af4-117">StoredPolicyServiceQueueSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Queue <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56af4-118">StoredPolicyServiceTableSas</span><span class="sxs-lookup"><span data-stu-id="56af4-118">StoredPolicyServiceTableSas</span></span>
```
Set-AzureKeyVaultManagedStorageSasDefinition [-VaultName] <String> [-AccountName] <String> [-Name] <String>
 [-Disable] [-Tag <Hashtable>] [-TargetStorageVersion <String>] [-Protocol <String>]
 [-IPAddressOrRange <String>] -Policy <String> -Table <String> [-StartPartitionKey <String>]
 [-StartRowKey <String>] [-EndPartitionKey <String>] [-EndRowKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56af4-119">설명은</span><span class="sxs-lookup"><span data-stu-id="56af4-119">DESCRIPTION</span></span>
<span data-ttu-id="56af4-120">지정 된 키 보관소 관리 Azure Storage 계정으로 SAS (공유 액세스 서명) 정의를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-120">Sets a Shared Access Signature (SAS) definition with a given Key Vault managed Azure Storage Account.</span></span> <span data-ttu-id="56af4-121">이는 또한이 SAS 정의에 따라 SAS 토큰을 가져오는 데 사용할 수 있는 비밀을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-121">This also sets a secret which can be used to get the SAS token per this SAS definition.</span></span>
<span data-ttu-id="56af4-122">SAS 토큰은 이러한 매개 변수와 키 보관소 관리 Azure 저장소 계정의 활성 키를 사용 하 여 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-122">SAS token is generated using these parameters and the active key of the Key Vault managed Azure Storage Account.</span></span>

## <span data-ttu-id="56af4-123">예제의</span><span class="sxs-lookup"><span data-stu-id="56af4-123">EXAMPLES</span></span>

### <span data-ttu-id="56af4-124">예제 1: ad hoc 서비스 Blob sas 정의 설정</span><span class="sxs-lookup"><span data-stu-id="56af4-124">Example 1 : Set an ad hoc service Blob sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Blob 'blob1' -Container 'container1' -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add -SharedAccessHeader CacheControl,ContentDisposition -Protocol HttpsOnly -IPAddressOrRange '168.1.5.60-168.1.5.70'
```

<span data-ttu-id="56af4-125">' Vault1 ' 자격 증명 모음의 ' 계정 1 ' 키 보관소 관리 저장소 계정으로 ad hoc 서비스 blob sas 정의 ' sas1 '를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-125">Sets an ad hoc service blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="56af4-126">예제 2: ad hoc 계정 sas 정의 설정</span><span class="sxs-lookup"><span data-stu-id="56af4-126">Example 2 : Set an ad hoc account sas definition</span></span>
```
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -Service Blob,File -ResourceType Container,Service -VaultName 'vault1' -AccountName 'account1' -Name 'sas1' -Protocol HttpsOrHttp -IPAddressOrRange '168.1.5.60' -ValidityPeriod ([System.Timespan]::FromDays(30)) -Permission Read,Add
```

<span data-ttu-id="56af4-127">' Vault1 ' 자격 증명 모음의 ' 계정 1 ' 키 보관소 관리 저장소 계정으로 ad hoc blob sas 정의 ' sas1 '을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-127">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1'.</span></span>

### <span data-ttu-id="56af4-128">예제 3: hashtable를 사용 하 여 sas 정의 설정</span><span class="sxs-lookup"><span data-stu-id="56af4-128">Example 3 : Set a sas definition using a hashtable</span></span>
```
PS C:\> $parameters = @{"sasType"="blob";"signedVersion"="2016-05-31";"signedProtocols"="https";"signedIp"="168.1.5.60-168.1.5.70";"validityPeriod"="P30D";"signedPermissions"="ra";"blobName"="blob1";"containerName"="container1";"rscd"="";"rscc"=""}
PS C:\> Set-AzureKeyVaultManagedStorageSasDefinition -VaultName vault1 -AccountName account1 -Name sas1 -Parameter $parameters
```

<span data-ttu-id="56af4-129">해시 테이블을 사용 하는 자격 증명 모음 ' vault1 '의 키 보관소 관리 저장소 계정 ' 계정 1 '을 사용 하 여 ad hoc blob sas 정의 ' sas1 '을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-129">Sets an ad hoc blob sas definition 'sas1' with key vault managed storage account 'account1' in vault 'vault1' using a hashtable.</span></span>

## <span data-ttu-id="56af4-130">변수</span><span class="sxs-lookup"><span data-stu-id="56af4-130">PARAMETERS</span></span>

### <span data-ttu-id="56af4-131">-AccountName</span><span class="sxs-lookup"><span data-stu-id="56af4-131">-AccountName</span></span>
<span data-ttu-id="56af4-132">키 자격 증명 모음 관리 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-132">Key Vault managed storage account name.</span></span> <span data-ttu-id="56af4-133">Cmdlet은 자격 증명 모음 이름, 현재 선택한 환경 및 manged 저장소 계정 이름에서 관리 되는 저장소 계정 이름의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-133">Cmdlet constructs the FQDN of a managed storage account name from vault name, currently selected environment and manged storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-134">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="56af4-134">-ApiVersion</span></span>
<span data-ttu-id="56af4-135">계정 SAS URI를 사용 하 여 수행 된 요청을 실행 하는 데 사용할 저장소 서비스 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-135">Specifies the storage service version to use to execute the request made using the account SAS URI.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-136">-Blob</span><span class="sxs-lookup"><span data-stu-id="56af4-136">-Blob</span></span>
<span data-ttu-id="56af4-137">Blob 이름</span><span class="sxs-lookup"><span data-stu-id="56af4-137">Blob Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, StoredPolicyServiceBlobSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-138">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="56af4-138">-Container</span></span>
<span data-ttu-id="56af4-139">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="56af4-139">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56af4-140">-DefaultProfile</span></span>
<span data-ttu-id="56af4-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="56af4-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56af4-142">-Disable</span><span class="sxs-lookup"><span data-stu-id="56af4-142">-Disable</span></span>
<span data-ttu-id="56af4-143">Sas 토큰 생성을 위한 sas 정의 사용을 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-143">Disables the use of sas definition for generation of sas token.</span></span>

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

### <span data-ttu-id="56af4-144">-EndPartitionKey</span><span class="sxs-lookup"><span data-stu-id="56af4-144">-EndPartitionKey</span></span>
<span data-ttu-id="56af4-145">파티션 키 종료</span><span class="sxs-lookup"><span data-stu-id="56af4-145">End Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-146">-EndRowKey</span><span class="sxs-lookup"><span data-stu-id="56af4-146">-EndRowKey</span></span>
<span data-ttu-id="56af4-147">마지막 행 키</span><span class="sxs-lookup"><span data-stu-id="56af4-147">End Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: endrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-148">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="56af4-148">-IPAddressOrRange</span></span>
<span data-ttu-id="56af4-149">Azure Storage에서 허용 되는 요청의 ip 범위 ACL (액세스 제어 목록)입니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-149">IP, or IP range ACL (access control list) of the request that would be accepted by Azure Storage.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-150">-이름</span><span class="sxs-lookup"><span data-stu-id="56af4-150">-Name</span></span>
<span data-ttu-id="56af4-151">저장소 sas 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-151">Storage sas definition name.</span></span> <span data-ttu-id="56af4-152">Cmdlet은 자격 증명 모음 이름, 현재 선택 된 환경, 저장소 계정 이름 및 sas 정의 이름에서 저장소 sas 정의의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-152">Cmdlet constructs the FQDN of a storage sas definition from vault name, currently selected environment, storage account name and sas definition name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SasDefinitionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-153">-Parameter</span><span class="sxs-lookup"><span data-stu-id="56af4-153">-Parameter</span></span>
<span data-ttu-id="56af4-154">Sas 토큰을 만드는 데 사용 되는 sas 정의 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="56af4-154">Sas definition parameters that will be used to create the sas token.</span></span>

```yaml
Type: Hashtable
Parameter Sets: RawSas
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-155">-Path</span><span class="sxs-lookup"><span data-stu-id="56af4-155">-Path</span></span>
<span data-ttu-id="56af4-156">Sas 토큰을 생성할 클라우드 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-156">Path to the cloud file to generate sas token against.</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, StoredPolicyServiceFileSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-157">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="56af4-157">-Permission</span></span>
<span data-ttu-id="56af4-158">있는.</span><span class="sxs-lookup"><span data-stu-id="56af4-158">Permission.</span></span> <span data-ttu-id="56af4-159">값에는 ' 쿼리 ', ' 추가 ', ' 업데이트 ', ' 공정 '이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-159">Values include 'Query','Add','Update','Process'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 
Accepted values: Add, Create, Delete, List, Process, Read, Query, Update, Write

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-160">-정책</span><span class="sxs-lookup"><span data-stu-id="56af4-160">-Policy</span></span>
<span data-ttu-id="56af4-161">정책 식별자</span><span class="sxs-lookup"><span data-stu-id="56af4-161">Policy Identifier</span></span>

```yaml
Type: String
Parameter Sets: StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-162">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="56af4-162">-Protocol</span></span>
<span data-ttu-id="56af4-163">프로토콜은 SAS 토큰을 사용 하 여 요청에 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-163">Protocol can be used in the request with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-164">-큐</span><span class="sxs-lookup"><span data-stu-id="56af4-164">-Queue</span></span>
<span data-ttu-id="56af4-165">큐 이름</span><span class="sxs-lookup"><span data-stu-id="56af4-165">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceQueueSas, StoredPolicyServiceQueueSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-166">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="56af4-166">-ResourceType</span></span>
<span data-ttu-id="56af4-167">이 SAS 토큰이 적용 되는 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-167">Resource types that this SAS token applies to.</span></span> <span data-ttu-id="56af4-168">값에는 ' 서비스 ', ' 컨테이너 ', ' 개체 '가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-168">Values include 'Service','Container','Object'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-169">-서비스</span><span class="sxs-lookup"><span data-stu-id="56af4-169">-Service</span></span>
<span data-ttu-id="56af4-170">이 SAS 토큰이 적용 되는 서비스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-170">Service types that this SAS token applies to.</span></span> <span data-ttu-id="56af4-171">값에는 ' Blob ', ' File ', ' Queue ', ' Table '이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-171">Values include 'Blob','File','Queue','Table'</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocAccountSas
Aliases: 
Accepted values: Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-172">-공유</span><span class="sxs-lookup"><span data-stu-id="56af4-172">-Share</span></span>
<span data-ttu-id="56af4-173">공유 이름</span><span class="sxs-lookup"><span data-stu-id="56af4-173">Share Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-174">-SharedAccessHeader</span><span class="sxs-lookup"><span data-stu-id="56af4-174">-SharedAccessHeader</span></span>
<span data-ttu-id="56af4-175">응답 헤더를 재정의 하는 쿼리 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-175">Specifies the query parameters to override response headers.</span></span>

```yaml
Type: String[]
Parameter Sets: AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas
Aliases: 
Accepted values: CacheControl, ContentDisposition, ContentEncoding, ContentLanguage, ContentType

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-176">-StartPartitionKey</span><span class="sxs-lookup"><span data-stu-id="56af4-176">-StartPartitionKey</span></span>
<span data-ttu-id="56af4-177">파티션 키 시작</span><span class="sxs-lookup"><span data-stu-id="56af4-177">Start Partition Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startpk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-178">-StartRowKey</span><span class="sxs-lookup"><span data-stu-id="56af4-178">-StartRowKey</span></span>
<span data-ttu-id="56af4-179">시작 행 키</span><span class="sxs-lookup"><span data-stu-id="56af4-179">Start Row Key</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: startrk

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-180">-테이블</span><span class="sxs-lookup"><span data-stu-id="56af4-180">-Table</span></span>
<span data-ttu-id="56af4-181">테이블 이름</span><span class="sxs-lookup"><span data-stu-id="56af4-181">Table Name</span></span>

```yaml
Type: String
Parameter Sets: AdhocServiceTableSas, StoredPolicyServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-182">태그</span><span class="sxs-lookup"><span data-stu-id="56af4-182">-Tag</span></span>
<span data-ttu-id="56af4-183">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-183">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="56af4-184">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="56af4-184">For example:</span></span>

<span data-ttu-id="56af4-185">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="56af4-185">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-186">-TargetStorageVersion</span><span class="sxs-lookup"><span data-stu-id="56af4-186">-TargetStorageVersion</span></span>
<span data-ttu-id="56af4-187">SAS 토큰으로 생성 된 요청을 인증 하는 데 사용할 서명 된 저장소 서비스 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-187">Specifies the signed storage service version to use to authenticate requests made with the SAS token.</span></span>

```yaml
Type: String
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas, StoredPolicyServiceBlobSas, StoredPolicyServiceContainerSas, StoredPolicyServiceFileSas, StoredPolicyServiceShareSas, StoredPolicyServiceQueueSas, StoredPolicyServiceTableSas
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-188">-ValidityPeriod</span><span class="sxs-lookup"><span data-stu-id="56af4-188">-ValidityPeriod</span></span>
<span data-ttu-id="56af4-189">Sas 토큰이 생성 된 시간에서 만료 되는 시간을 설정 하는 데 사용 되는 유효 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-189">Validity period that will get used to set the expiry time of sas token from the time it gets generated</span></span>

```yaml
Type: TimeSpan
Parameter Sets: AdhocAccountSas, AdhocServiceBlobSas, AdhocServiceContainerSas, AdhocServiceFileSas, AdhocServiceShareSas, AdhocServiceQueueSas, AdhocServiceTableSas
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-190">-VaultName</span><span class="sxs-lookup"><span data-stu-id="56af4-190">-VaultName</span></span>
<span data-ttu-id="56af4-191">자격 증명 모음 이름</span><span class="sxs-lookup"><span data-stu-id="56af4-191">Vault name.</span></span>
<span data-ttu-id="56af4-192">Cmdlet은 이름 및 현재 선택 된 환경을 기준으로 자격 증명 모음의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-192">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56af4-193">-확인</span><span class="sxs-lookup"><span data-stu-id="56af4-193">-Confirm</span></span>
<span data-ttu-id="56af4-194">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-194">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56af4-195">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56af4-195">-WhatIf</span></span>
<span data-ttu-id="56af4-196">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-196">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56af4-197">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-197">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56af4-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56af4-198">CommonParameters</span></span>
<span data-ttu-id="56af4-199">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56af4-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56af4-200">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56af4-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56af4-201">입력</span><span class="sxs-lookup"><span data-stu-id="56af4-201">INPUTS</span></span>

## <span data-ttu-id="56af4-202">출력</span><span class="sxs-lookup"><span data-stu-id="56af4-202">OUTPUTS</span></span>

### <span data-ttu-id="56af4-203">Microsoft. KeyVault. ' Managed' 모델. i 볼트로 Esasdefinition</span><span class="sxs-lookup"><span data-stu-id="56af4-203">Microsoft.Azure.Commands.KeyVault.Models.ManagedStorageSasDefinition</span></span>

## <span data-ttu-id="56af4-204">상속자</span><span class="sxs-lookup"><span data-stu-id="56af4-204">NOTES</span></span>

## <span data-ttu-id="56af4-205">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56af4-205">RELATED LINKS</span></span>

[<span data-ttu-id="56af4-206">Azureâ € ‹ RM. a € ‹ Keyâ € ‹ 볼트</span><span class="sxs-lookup"><span data-stu-id="56af4-206">Azureâ€‹RM.â€‹Keyâ€‹Vault</span></span>](/powershell/module/azurerm.keyvault/)
