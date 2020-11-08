---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzManagedHsmKey.md
ms.openlocfilehash: 89238992b99d86cdd56337a3002167be9c0d78d0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226951"
---
# <span data-ttu-id="90c0e-101">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="90c0e-101">Add-AzManagedHsmKey</span></span>

## <span data-ttu-id="90c0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90c0e-102">SYNOPSIS</span></span>
<span data-ttu-id="90c0e-103">관리 되는 HSM에서 키를 만들거나 관리 되는 HSM으로 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-103">Creates a key in a managed HSM or imports a key into a managed HSM.</span></span>

## <span data-ttu-id="90c0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90c0e-104">SYNTAX</span></span>

### <span data-ttu-id="90c0e-105">InteractiveCreate (기본값)</span><span class="sxs-lookup"><span data-stu-id="90c0e-105">InteractiveCreate (Default)</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c0e-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="90c0e-106">InteractiveImport</span></span>
```
Add-AzManagedHsmKey [-HsmName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90c0e-107">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="90c0e-107">InputObjectCreate</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyType <String> [-CurveName <String>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-Size <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c0e-108">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="90c0e-108">InputObjectImport</span></span>
```
Add-AzManagedHsmKey [-InputObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="90c0e-109">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="90c0e-109">ResourceIdCreate</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyType <String> [-CurveName <String>] [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90c0e-110">Resourcei//포트</span><span class="sxs-lookup"><span data-stu-id="90c0e-110">ResourceIdImport</span></span>
```
Add-AzManagedHsmKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-CurveName <String>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="90c0e-111">설명은</span><span class="sxs-lookup"><span data-stu-id="90c0e-111">DESCRIPTION</span></span>
<span data-ttu-id="90c0e-112">**AzManagedHsmKey** Cmdlet은 Azure 관리 hsm에서 관리 되는 hsm에 키를 만들거나 관리 되는 hsm으로 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-112">The **Add-AzManagedHsmKey** cmdlet creates a key in a managed HSM in Azure Managed Hsm or imports a key into a managed HSM.</span></span>
<span data-ttu-id="90c0e-113">이 cmdlet을 사용 하 여 다음 방법 중 하나를 사용 하 여 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-113">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="90c0e-114">기본 키 특성을 사용 하 여 키 만들기</span><span class="sxs-lookup"><span data-stu-id="90c0e-114">Create a key with default key attributes</span></span>
- <span data-ttu-id="90c0e-115">지정 된 키 특성을 사용 하 여 키 만들기</span><span class="sxs-lookup"><span data-stu-id="90c0e-115">Create a key with given key attributes</span></span>
- <span data-ttu-id="90c0e-116">컴퓨터의 .pfx 파일에서 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-116">Import a key from a .pfx file on your computer.</span></span>
<span data-ttu-id="90c0e-117">이러한 작업의 경우 키 특성을 제공 하거나 기본 설정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-117">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="90c0e-118">관리 되는 HSM의 기존 키와 같은 이름을 가진 키를 만들거나 가져오면 새 키에 대해 지정 하는 값으로 원래 키가 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-118">If you create or import a key that has the same name as an existing key in your managed HSM, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="90c0e-119">해당 버전의 키에 대 한 버전 관련 URI를 사용 하 여 이전 값에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-119">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="90c0e-120">키 버전과 URI 구조에 대 한 자세한 내용은 관리 되는 HSM REST API 설명서의 [키 및 비밀 정보](http://go.microsoft.com/fwlink/?linkid=518560) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="90c0e-120">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Managed HSM REST API documentation.</span></span>

## <span data-ttu-id="90c0e-121">예제의</span><span class="sxs-lookup"><span data-stu-id="90c0e-121">EXAMPLES</span></span>

### <span data-ttu-id="90c0e-122">예제 1: RSA-HSM 키 만들기</span><span class="sxs-lookup"><span data-stu-id="90c0e-122">Example 1: Create a RSA-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType RSA

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 7:55:43 AM
Updated        : 10/14/2020 7:55:43 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="90c0e-123">이 명령은 testmhsm 이라는 관리 되는 HSM testkey에서 testkey 라는 이름의 RSA 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-123">This command creates a RSA-HSM key named testkey in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="90c0e-124">예제 2: EC-HSM 키 만들기</span><span class="sxs-lookup"><span data-stu-id="90c0e-124">Example 2: Create a EC-HSM key</span></span>
```powershell
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType EC -CurveName P-256

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 8:06:26 AM
Updated        : 10/14/2020 8:06:26 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="90c0e-125">이 명령은 testmhsm 이라는 관리 되는 HSM testkey에서 P-256 곡선을 사용 하 여 testkey 라는 EC 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-125">This command creates a EC-HSM key named testkey using P-256 curve in the managed HSM testkey named testmhsm.</span></span>

### <span data-ttu-id="90c0e-126">예제 3: 기본값이 아닌 값을 사용 하 여 oct-HSM 키 만들기</span><span class="sxs-lookup"><span data-stu-id="90c0e-126">Example 3: Create a oct-HSM key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzManagedHsmKey -HsmName testmhsm -Name testkey -KeyType oct -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault/HSM Name : testmhsm
Name           : testkey
Version        : xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
Id             : https://bezmhsm.managedhsm.azure.net:443/keys/testkey/xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
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

<span data-ttu-id="90c0e-127">첫 번째 명령은 $KeyOperations 변수의 암호를 해독 하 고 확인 하는 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-127">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="90c0e-128">두 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 UTC로 정의 된 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-128">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="90c0e-129">이 개체는 앞으로 2 년 동안 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-129">That object specifies a time two years in the future.</span></span> <span data-ttu-id="90c0e-130">이 명령은 $Expires 변수에 해당 날짜를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-130">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="90c0e-131">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="90c0e-131">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="90c0e-132">세 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-132">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="90c0e-133">해당 개체는 현재 UTC 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-133">That object specifies current UTC time.</span></span> <span data-ttu-id="90c0e-134">이 명령은 $NotBefore 변수에 해당 날짜를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-134">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="90c0e-135">마지막 명령은 oct 키 10 인 testkey를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-135">The final command creates a key named testkey that is an oct-HSM key.</span></span> <span data-ttu-id="90c0e-136">명령은 $KeyOperations 저장 된 허용 키 작업에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-136">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="90c0e-137">이 명령은 이전 명령에서 만든 *만료* 및 *NotBefore* 매개 변수에 대 한 시간을 지정 하 고 높은 심각도 및이에 대 한 태그를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-137">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="90c0e-138">새 키를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-138">The new key is disabled.</span></span> <span data-ttu-id="90c0e-139">**AzManagedHsmKey** cmdlet을 사용 하 여이 기능을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-139">You can enable it by using the **Update-AzManagedHsmKey** cmdlet.</span></span>

## <span data-ttu-id="90c0e-140">변수</span><span class="sxs-lookup"><span data-stu-id="90c0e-140">PARAMETERS</span></span>

### <span data-ttu-id="90c0e-141">-CurveName</span><span class="sxs-lookup"><span data-stu-id="90c0e-141">-CurveName</span></span>
<span data-ttu-id="90c0e-142">Elliptic curve 암호화의 곡선 이름을 지정 하며이 값은 KeyType이 EC 일 때 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-142">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

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

### <span data-ttu-id="90c0e-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90c0e-143">-DefaultProfile</span></span>
<span data-ttu-id="90c0e-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90c0e-145">-Disable</span><span class="sxs-lookup"><span data-stu-id="90c0e-145">-Disable</span></span>
<span data-ttu-id="90c0e-146">추가 하는 키가 비활성의 초기 상태로 설정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-146">Indicates that the key you are adding is set to an initial state of disabled.</span></span>
<span data-ttu-id="90c0e-147">키를 사용 하려는 시도는 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-147">Any attempt to use the key will fail.</span></span>
<span data-ttu-id="90c0e-148">나중에 사용 하려는 키를 미리 로드 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-148">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="90c0e-149">-만료</span><span class="sxs-lookup"><span data-stu-id="90c0e-149">-Expires</span></span>
<span data-ttu-id="90c0e-150">UTC에서 키의 만료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-150">Specifies the expiration time of the key in UTC.</span></span>
<span data-ttu-id="90c0e-151">지정 하지 않으면 키가 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-151">If not specified, key will not expire.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c0e-152">-HsmName</span><span class="sxs-lookup"><span data-stu-id="90c0e-152">-HsmName</span></span>
<span data-ttu-id="90c0e-153">HSM 이름.</span><span class="sxs-lookup"><span data-stu-id="90c0e-153">HSM name.</span></span> <span data-ttu-id="90c0e-154">Cmdlet은 이름 및 현재 선택 된 환경에 따라 관리 되는 HSM의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-154">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c0e-155">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90c0e-155">-InputObject</span></span>
<span data-ttu-id="90c0e-156">HSM 개체.</span><span class="sxs-lookup"><span data-stu-id="90c0e-156">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90c0e-157">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="90c0e-157">-KeyFilePassword</span></span>
<span data-ttu-id="90c0e-158">가져올 키 자료가 포함 된 로컬 파일의 암호입니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-158">Password of the local file containing the key material to be imported.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c0e-159">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="90c0e-159">-KeyFilePath</span></span>
<span data-ttu-id="90c0e-160">가져올 키 자료를 포함 하는 로컬 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-160">Path to the local file containing the key material to be imported.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c0e-161">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="90c0e-161">-KeyOps</span></span>
<span data-ttu-id="90c0e-162">키를 사용 하 여 수행할 수 있는 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-162">The operations that can be performed with the key.</span></span>
<span data-ttu-id="90c0e-163">표시 되지 않으면 모든 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-163">If not present, all operations can be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c0e-164">-KeyType</span><span class="sxs-lookup"><span data-stu-id="90c0e-164">-KeyType</span></span>
<span data-ttu-id="90c0e-165">이 키의 키 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-165">Specifies the key type of this key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c0e-166">-이름</span><span class="sxs-lookup"><span data-stu-id="90c0e-166">-Name</span></span>
<span data-ttu-id="90c0e-167">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-167">Key name.</span></span>
<span data-ttu-id="90c0e-168">Cmdlet은 관리 되는 HSM 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-168">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c0e-169">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="90c0e-169">-NotBefore</span></span>
<span data-ttu-id="90c0e-170">키를 사용할 수 없는 UTC 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-170">The UTC time before which the key can't be used.</span></span>
<span data-ttu-id="90c0e-171">지정 하지 않은 경우에는 제한이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-171">If not specified, there is no limitation.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c0e-172">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="90c0e-172">-ResourceId</span></span>
<span data-ttu-id="90c0e-173">HSM 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-173">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90c0e-174">-크기</span><span class="sxs-lookup"><span data-stu-id="90c0e-174">-Size</span></span>
<span data-ttu-id="90c0e-175">RSA 키 크기 (비트 단위)입니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-175">RSA key size, in bits.</span></span>
<span data-ttu-id="90c0e-176">지정 하지 않으면 서비스에서 안전한 기본값을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-176">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90c0e-177">태그</span><span class="sxs-lookup"><span data-stu-id="90c0e-177">-Tag</span></span>
<span data-ttu-id="90c0e-178">키 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-178">A hashtable representing key tags.</span></span>

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

### <span data-ttu-id="90c0e-179">-확인</span><span class="sxs-lookup"><span data-stu-id="90c0e-179">-Confirm</span></span>
<span data-ttu-id="90c0e-180">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90c0e-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90c0e-181">-WhatIf</span></span>
<span data-ttu-id="90c0e-182">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90c0e-183">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90c0e-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90c0e-184">CommonParameters</span></span>
<span data-ttu-id="90c0e-185">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90c0e-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90c0e-186">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="90c0e-186">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90c0e-187">입력</span><span class="sxs-lookup"><span data-stu-id="90c0e-187">INPUTS</span></span>

### <span data-ttu-id="90c0e-188">Microsoft. KeyVault. 모델. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="90c0e-188">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="90c0e-189">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="90c0e-189">System.String</span></span>

## <span data-ttu-id="90c0e-190">출력</span><span class="sxs-lookup"><span data-stu-id="90c0e-190">OUTPUTS</span></span>

### <span data-ttu-id="90c0e-191">Microsoft. KeyVault. 모델. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="90c0e-191">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="90c0e-192">상속자</span><span class="sxs-lookup"><span data-stu-id="90c0e-192">NOTES</span></span>

## <span data-ttu-id="90c0e-193">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90c0e-193">RELATED LINKS</span></span>

[<span data-ttu-id="90c0e-194">백업-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="90c0e-194">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="90c0e-195">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="90c0e-195">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="90c0e-196">제거-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="90c0e-196">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="90c0e-197">실행 취소-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="90c0e-197">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="90c0e-198">업데이트-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="90c0e-198">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="90c0e-199">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="90c0e-199">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)
