---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmKey.md
ms.openlocfilehash: 34bc2f074ee37dcf670e3e43ad647781b4d59e56
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215308"
---
# <span data-ttu-id="94b7c-101">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="94b7c-101">Get-AzManagedHsmKey</span></span>

## <span data-ttu-id="94b7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94b7c-102">SYNOPSIS</span></span>
<span data-ttu-id="94b7c-103">관리 되는 Hsm 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-103">Gets Managed Hsm keys.</span></span>

## <span data-ttu-id="94b7c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94b7c-104">SYNTAX</span></span>

### <span data-ttu-id="94b7c-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (기본값)</span><span class="sxs-lookup"><span data-stu-id="94b7c-105">SpecifyHsmByHsmNameGetKeyWithoutConstraint (Default)</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94b7c-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="94b7c-106">SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94b7c-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="94b7c-107">SpecifyHsmByHsmNameGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94b7c-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="94b7c-108">SpecifyHsmByInputObjectGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94b7c-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="94b7c-109">SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94b7c-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="94b7c-110">SpecifyHsmByInputObjectGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94b7c-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span><span class="sxs-lookup"><span data-stu-id="94b7c-111">SpecifyHsmByResourceIdGetKeyWithoutConstraint</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94b7c-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span><span class="sxs-lookup"><span data-stu-id="94b7c-112">SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94b7c-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span><span class="sxs-lookup"><span data-stu-id="94b7c-113">SpecifyHsmByResourceIdGetKeyIncludeAllVersions</span></span>
```
Get-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94b7c-114">설명은</span><span class="sxs-lookup"><span data-stu-id="94b7c-114">DESCRIPTION</span></span>
<span data-ttu-id="94b7c-115">**AzManagedHsmKey** Cmdlet은 Azure 관리 Hsm 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-115">The **Get-AzManagedHsmKey** cmdlet gets Azure Managed Hsm keys.</span></span>
<span data-ttu-id="94b7c-116">이 cmdlet은 특정 **Microsoft Azure. KeyVault** 또는 관리 되는 Hsm의 모든 **keyvault** 개체 목록 또는 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a managed Hsm or by version.</span></span>

## <span data-ttu-id="94b7c-117">예제의</span><span class="sxs-lookup"><span data-stu-id="94b7c-117">EXAMPLES</span></span>

### <span data-ttu-id="94b7c-118">예제 1: 관리 되는 HSM의 모든 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="94b7c-118">Example 1: Get all the keys in a managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm
```

<span data-ttu-id="94b7c-119">자격 증명 모음/i o s 이름: testmhsm 이름: testkey001 Version: Id: https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled: True Expires: Before: Created: 10/14/2020 3:39:16 Am 업데이트: 10/14/2020 3:39:16 Am 복구 수준: 복구 가능한 + Purgeable 태그:</span><span class="sxs-lookup"><span data-stu-id="94b7c-119">Vault/HSM Name : testmhsm Name           : testkey001 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001 Enabled        : True Expires        : Not Before     : Created        : 10/14/2020 3:39:16 AM Updated        : 10/14/2020 3:39:16 AM Recovery Level : Recoverable+Purgeable Tags           :</span></span>

<span data-ttu-id="94b7c-120">자격 증명 모음/i o f 이름: testkey002 Version: Id: https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled: False 만료: 10/14/2022 8:13:29이 (가) 이전 상태가 아님: 10/14/2020 8:13:33 am: 10/14/2020 8:14:01 업데이트 됨: 10/14/2020 8:14:01 Am 복구 수준: 복구 가능한 + Purgeable 태그: 이름 값 심각도 높음 계정 참</span><span class="sxs-lookup"><span data-stu-id="94b7c-120">Vault/HSM Name : testmhsm Name           : testkey002 Version        : Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey002 Enabled        : False Expires        : 10/14/2022 8:13:29 AM Not Before     : 10/14/2020 8:13:33 AM Created        : 10/14/2020 8:14:01 AM Updated        : 10/14/2020 8:14:01 AM Recovery Level : Recoverable+Purgeable Tags           : Name        Value Severity    high Accounting  true</span></span>

<span data-ttu-id="94b7c-121">이 명령은 관리 되는 HSM에 대 한 testmhsm 이라는 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-121">This command gets all the keys in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="94b7c-122">예제 2: 현재 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="94b7c-122">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\>$hsm = Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001
PS C:\>$hsm

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="94b7c-123">이 명령은 testmhsm 이라는 관리 되는 HSM의 testkey001 이라는 키의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-123">This command gets the current version of the key named testkey001 in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="94b7c-124">참고: Hsm 이름은 $hsm 하 여 구할 수 있습니다. VaultName</span><span class="sxs-lookup"><span data-stu-id="94b7c-124">Note: Hsm Name can be obtained by $hsm.VaultName</span></span>

### <span data-ttu-id="94b7c-125">예제 3: 모든 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="94b7c-125">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey001 -IncludeVersions

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 9a9de2bcec540c3b160cd54cbae71339
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/9a9de2bcec540c3b160cd54cbae71339
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="94b7c-126">이 명령은 testmhsm 이라는 관리 되는 HSM의 testkey001 이라는 키를 모든 버전으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-126">This command gets all versions the key named testkey001 in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="94b7c-127">예제 4: 특정 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="94b7c-127">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName testkey -Version 80fd43e31e8649873520053c91148418

Vault/HSM Name : testmhsm
Name           : testkey
Version        : 80fd43e31e8649873520053c91148418
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey/80fd43e31e8649873520053c91148418
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="94b7c-128">이 명령은 testmhsm 이라는 관리 되는 HSM에서 testkey 라는 특정 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-128">This command gets a specific version of the key named testkey in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="94b7c-129">이 명령을 실행 한 후에는 $Key 개체를 탐색 하 여 키의 다양 한 속성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-129">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="94b7c-130">예제 5: 삭제 되었지만 관리 되지 않는 HSM에 대해 제거 되지 않은 모든 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="94b7c-130">Example 5: Get all the keys that have been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -InRemovedState

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 : Name        Value
                       Severity    high
                       Accounting  true                :
```

<span data-ttu-id="94b7c-131">이 명령은 testmhsm 이라는 관리 되는 HSM에서 이전에 삭제 되었지만 제거 되지 않은 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-131">This command gets all the keys that have been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>

### <span data-ttu-id="94b7c-132">예제 6:이 관리 되는 HSM에 대해 삭제 되었지만 제거 되지 않은 키 testkey를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-132">Example 6: Gets the key testkey that has been deleted but not purged for this managed HSM</span></span>
```powershell
PS C:\>  Get-AzManagedHsmKey -HsmName testmhsm -Name testkey -InRemovedState 

Vault/HSM Name       : testmhsm
Name                 : testkey
Id                   : https://testmhsm.managedhsm.azure.net:443/keys/testkey/9a9de2bcec540c3b160cd54cbae71339
Deleted Date         : 10/14/2020 9:10:42 AM
Scheduled Purge Date : 1/12/2021 9:10:42 AM
Enabled              : False
Expires              : 10/14/2022 8:13:29 AM
Not Before           : 10/14/2020 8:13:33 AM
Created              : 10/14/2020 8:14:01 AM
Updated              : 10/14/2020 8:14:01 AM
Recovery Level       : Recoverable+Purgeable
Tags                 :
```

<span data-ttu-id="94b7c-133">이 명령은 testmhsm 이라는 관리 되는 HSM에서 이전에 삭제 되었지만 제거 되지 않은 키 testkey를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-133">This command gets the key testkey that has been previously deleted, but not purged, in the managed HSM named testmhsm.</span></span>
<span data-ttu-id="94b7c-134">이 명령은 삭제 날짜 등의 메타 데이터와이 지운 편지함의 예정 된 제거 날짜 등을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-134">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="94b7c-135">예제 7: 필터링을 사용 하 여 관리 되는 HSM의 모든 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="94b7c-135">Example 7: Get all the keys in a managed HSM using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsmKey -HsmName testmhsm -KeyName "test*"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="94b7c-136">이 명령은 "test"로 시작 하는 testmhsm 이라는 관리 되는 HSM의 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-136">This command gets all the keys in the managed HSM named testmhsm that start with "test".</span></span>

### <span data-ttu-id="94b7c-137">예제 8: 공개 키를 pem 파일로 다운로드</span><span class="sxs-lookup"><span data-stu-id="94b7c-137">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> Get-AzManagedHsmKey -HsmName bezmhsm -Name testkey -OutFile  "C:\public.pem"

Vault/HSM Name : testmhsm
Name           : testkey
Version        :
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey
Enabled        : False
Expires        : 10/14/2022 8:13:29 AM
Not Before     : 10/14/2020 8:13:33 AM
Created        : 10/14/2020 8:14:01 AM
Updated        : 10/14/2020 8:14:01 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="94b7c-138">매개 변수를 지정 하 여 RSA 키의 공개 키를 다운로드할 수 있습니다 `-OutFile` .</span><span class="sxs-lookup"><span data-stu-id="94b7c-138">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>

## <span data-ttu-id="94b7c-139">변수</span><span class="sxs-lookup"><span data-stu-id="94b7c-139">PARAMETERS</span></span>

### <span data-ttu-id="94b7c-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94b7c-140">-DefaultProfile</span></span>
<span data-ttu-id="94b7c-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94b7c-142">-HsmName</span><span class="sxs-lookup"><span data-stu-id="94b7c-142">-HsmName</span></span>
<span data-ttu-id="94b7c-143">HSM 이름.</span><span class="sxs-lookup"><span data-stu-id="94b7c-143">HSM name.</span></span> <span data-ttu-id="94b7c-144">Cmdlet은 이름 및 현재 선택 된 환경에 따라 관리 되는 HSM의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-144">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b7c-145">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="94b7c-145">-IncludeVersions</span></span>
<span data-ttu-id="94b7c-146">출력에 키 버전을 포함할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-146">Specifies whether to include the versions of the key in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b7c-147">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94b7c-147">-InputObject</span></span>
<span data-ttu-id="94b7c-148">HSM 개체.</span><span class="sxs-lookup"><span data-stu-id="94b7c-148">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94b7c-149">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="94b7c-149">-InRemovedState</span></span>
<span data-ttu-id="94b7c-150">출력에 이전에 삭제 된 키를 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-150">Specifies whether to show the previously deleted keys in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b7c-151">-이름</span><span class="sxs-lookup"><span data-stu-id="94b7c-151">-Name</span></span>
<span data-ttu-id="94b7c-152">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-152">Key name.</span></span>
<span data-ttu-id="94b7c-153">Cmdlet은 관리 되는 HSM 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-153">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithoutConstraint, SpecifyHsmByInputObjectGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithoutConstraint
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByHsmNameGetKeyIncludeAllVersions, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyIncludeAllVersions, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b7c-154">출력</span><span class="sxs-lookup"><span data-stu-id="94b7c-154">-OutFile</span></span>
<span data-ttu-id="94b7c-155">이 cmdlet이 키를 저장할 출력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-155">Specifies the output file for which this cmdlet saves the key.</span></span>
<span data-ttu-id="94b7c-156">공개 키는 기본적으로 PEM 형식으로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-156">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="94b7c-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94b7c-157">-ResourceId</span></span>
<span data-ttu-id="94b7c-158">HSM 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-158">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByResourceIdGetKeyWithoutConstraint, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyIncludeAllVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94b7c-159">-버전</span><span class="sxs-lookup"><span data-stu-id="94b7c-159">-Version</span></span>
<span data-ttu-id="94b7c-160">키 버전.</span><span class="sxs-lookup"><span data-stu-id="94b7c-160">Key version.</span></span>
<span data-ttu-id="94b7c-161">Cmdlet은 관리 되는 HSM 이름, 현재 선택 된 환경, 키 이름 및 키 버전에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-161">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: SpecifyHsmByHsmNameGetKeyWithSpecifiedVersion, SpecifyHsmByInputObjectGetKeyWithSpecifiedVersion, SpecifyHsmByResourceIdGetKeyWithSpecifiedVersion
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94b7c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94b7c-162">CommonParameters</span></span>
<span data-ttu-id="94b7c-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94b7c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94b7c-164">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="94b7c-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94b7c-165">입력</span><span class="sxs-lookup"><span data-stu-id="94b7c-165">INPUTS</span></span>

### <span data-ttu-id="94b7c-166">Microsoft. KeyVault. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="94b7c-166">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="94b7c-167">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="94b7c-167">System.String</span></span>

## <span data-ttu-id="94b7c-168">출력</span><span class="sxs-lookup"><span data-stu-id="94b7c-168">OUTPUTS</span></span>

### <span data-ttu-id="94b7c-169">Microsoft. KeyVault. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="94b7c-169">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="94b7c-170">Microsoft. KeyVault. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94b7c-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="94b7c-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="94b7c-171">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="94b7c-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="94b7c-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="94b7c-173">상속자</span><span class="sxs-lookup"><span data-stu-id="94b7c-173">NOTES</span></span>

## <span data-ttu-id="94b7c-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94b7c-174">RELATED LINKS</span></span>

[<span data-ttu-id="94b7c-175">추가-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="94b7c-175">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="94b7c-176">백업-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="94b7c-176">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="94b7c-177">제거-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="94b7c-177">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="94b7c-178">실행 취소-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="94b7c-178">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="94b7c-179">업데이트-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="94b7c-179">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="94b7c-180">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="94b7c-180">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)