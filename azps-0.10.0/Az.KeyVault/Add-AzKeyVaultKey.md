---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: b01ed80385726660198d3f6fbb20ab1e5ec57dfe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876718"
---
# <span data-ttu-id="571bf-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="571bf-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="571bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="571bf-102">SYNOPSIS</span></span>
<span data-ttu-id="571bf-103">키 자격 증명 모음에 키를 만들거나 키를 키 보관소로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="571bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="571bf-104">SYNTAX</span></span>

### <span data-ttu-id="571bf-105">만들기 (기본값)</span><span class="sxs-lookup"><span data-stu-id="571bf-105">Create (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="571bf-106">Import</span><span class="sxs-lookup"><span data-stu-id="571bf-106">Import</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="571bf-107">설명은</span><span class="sxs-lookup"><span data-stu-id="571bf-107">DESCRIPTION</span></span>
<span data-ttu-id="571bf-108">**AzKeyVaultKey** Cmdlet은 Azure key vault의 키 보관소에 키를 만들거나 키를 키 모음으로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-108">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="571bf-109">이 cmdlet을 사용 하 여 다음 방법 중 하나를 사용 하 여 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-109">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="571bf-110">키 보관소 서비스의 HSM (하드웨어 보안 모듈)에서 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-110">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="571bf-111">키 보관소 서비스의 소프트웨어에서 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-111">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="571bf-112">키 보관소 서비스의 HSM (하드웨어 보안 모듈)에서 Hsm으로 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-112">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="571bf-113">컴퓨터의 .pfx 파일에서 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-113">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="571bf-114">컴퓨터에 있는 .pfx 파일의 키를 키 보관소 서비스의 Hsm (하드웨어 보안 모듈)로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-114">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="571bf-115">이러한 작업의 경우 키 특성을 제공 하거나 기본 설정을 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-115">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="571bf-116">키 자격 증명 모음의 기존 키와 같은 이름을 가진 키를 만들거나 가져오면 새 키에 대해 지정 하는 값으로 원래 키가 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-116">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="571bf-117">해당 버전의 키에 대 한 버전 관련 URI를 사용 하 여 이전 값에 액세스할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-117">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="571bf-118">주요 버전 및 URI 구조에 대 한 자세한 내용은 키 볼트 REST API 설명서의 [키 및 비밀 정보](http://go.microsoft.com/fwlink/?linkid=518560) 를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="571bf-118">To learn about key versions and the URI structure, see [About Keys andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="571bf-119">참고: 고유한 하드웨어 보안 모듈에서 키를 가져오려면 먼저 Azure Key Vault BYOK 도구 집합을 사용 하 여 BYOK 패키지 (이름 확장명을 가진 파일)를 생성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-119">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="571bf-120">자세한 내용은 [Azure 키 보관소에 대 한 HSM-Protected 키를 생성 하 고 전송 하는 방법을](http://go.microsoft.com/fwlink/?LinkId=522252)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="571bf-120">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="571bf-121">가장 좋은 방법은 키를 만들거나 업데이트 한 후 Backup-AzKeyVaultKey cmdlet을 사용 하 여 백업 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-121">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="571bf-122">삭제 취소 기능이 없기 때문에 실수로 키를 삭제 하거나 삭제 한 다음 생각이 바뀌면 다시 복원할 수 있는 백업을가지고 있지 않는 한 키를 복구 가능 하지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-122">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="571bf-123">예제의</span><span class="sxs-lookup"><span data-stu-id="571bf-123">EXAMPLES</span></span>

### <span data-ttu-id="571bf-124">예제 1: 키 만들기</span><span class="sxs-lookup"><span data-stu-id="571bf-124">Example 1: Create a key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="571bf-125">이 명령은 Contoso 라는 키 보관소에 ITSoftware 라는 소프트웨어 보호 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-125">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="571bf-126">예제 2: HSM으로 보호 된 키 만들기</span><span class="sxs-lookup"><span data-stu-id="571bf-126">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="571bf-127">이 명령은 Contoso 라는 키 보관소에 HSM으로 보호 된 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-127">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="571bf-128">예제 3: 기본값이 아닌 값을 사용 하 여 키 만들기</span><span class="sxs-lookup"><span data-stu-id="571bf-128">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="571bf-129">첫 번째 명령은 $KeyOperations 변수의 암호를 해독 하 고 확인 하는 값을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-129">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="571bf-130">두 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 UTC로 정의 된 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-130">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="571bf-131">이 개체는 앞으로 2 년 동안 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-131">That object specifies a time two years in the future.</span></span> <span data-ttu-id="571bf-132">이 명령은 $Expires 변수에 해당 날짜를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-132">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="571bf-133">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="571bf-133">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="571bf-134">세 번째 명령은 **데이터 가져오기** cmdlet을 사용 하 여 **DateTime** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-134">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="571bf-135">해당 개체는 현재 UTC 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-135">That object specifies current UTC time.</span></span> <span data-ttu-id="571bf-136">이 명령은 $NotBefore 변수에 해당 날짜를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-136">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="571bf-137">마지막 명령은 HSM으로 보호 된 키 인 ITHsmNonDefault 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-137">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="571bf-138">명령은 $KeyOperations 저장 된 허용 키 작업에 대 한 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-138">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="571bf-139">이 명령은 이전 명령에서 만든 *만료* 및 *NotBefore* 매개 변수에 대 한 시간을 지정 하 고 높은 심각도 및이에 대 한 태그를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-139">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="571bf-140">새 키를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-140">The new key is disabled.</span></span> <span data-ttu-id="571bf-141">**AzKeyVaultKey** cmdlet을 사용 하 여이 기능을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-141">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="571bf-142">예제 4: HSM으로 보호 된 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="571bf-142">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="571bf-143">이 명령은 *Keyfilepath* 매개 변수에서 지정 하는 위치에서 ITByok 라는 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-143">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="571bf-144">가져온 키는 HSM으로 보호 된 키입니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-144">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="571bf-145">고유한 하드웨어 보안 모듈에서 키를 가져오려면 먼저 Azure Key Vault BYOK 도구 집합을 사용 하 여 BYOK 패키지 (파일 이름 확장명이. a 1)를 생성 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-145">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="571bf-146">자세한 내용은 [Azure 키 보관소에 대 한 HSM-Protected 키를 생성 하 고 전송 하는 방법을](http://go.microsoft.com/fwlink/?LinkId=522252)참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="571bf-146">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="571bf-147">예제 5: 소프트웨어 보호 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="571bf-147">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="571bf-148">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-148">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="571bf-149">자세한 내용은을 입력 `Get-Help
ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="571bf-149">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="571bf-150">두 번째 명령은 Contoso 키 보관소에 소프트웨어 비밀 번호를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-150">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="571bf-151">명령은 $Password에 저장 된 키와 암호의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-151">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="571bf-152">예제 6: 키 가져오기 및 특성 할당</span><span class="sxs-lookup"><span data-stu-id="571bf-152">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="571bf-153">첫 번째 명령은 **ConvertTo-SecureString** cmdlet을 사용 하 여 문자열을 보안 문자열로 변환한 다음 해당 문자열을 $Password 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-153">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="571bf-154">두 번째 명령은 **가져오기-날짜** cmdlet을 사용 하 여 **DateTime** 개체를 만든 다음 해당 개체를 $Expires 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-154">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="571bf-155">세 번째 명령은 $tags 변수를 만들어 높은 심각도 및 그에 대 한 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-155">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="571bf-156">마지막 명령은 지정 된 위치에서 HSM 키로 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-156">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="571bf-157">명령은 $Password에 저장 된 $Expires 및 암호에 저장 된 만료 시간을 지정 하 고 $tags에 저장 된 태그를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-157">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="571bf-158">변수</span><span class="sxs-lookup"><span data-stu-id="571bf-158">PARAMETERS</span></span>

### <span data-ttu-id="571bf-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="571bf-159">-DefaultProfile</span></span>
<span data-ttu-id="571bf-160">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="571bf-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="571bf-161">-대상</span><span class="sxs-lookup"><span data-stu-id="571bf-161">-Destination</span></span>
<span data-ttu-id="571bf-162">키 자격 증명 모음 서비스에서 키를 소프트웨어 보호 키 또는 HSM로 보호 된 키로 추가할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-162">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="571bf-163">유효한 값은 HSM 및 소프트웨어입니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-163">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="571bf-164">참고: 대상으로 HSM을 사용 하려면 Hsm을 지 원하는 키 자격 증명 모음이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-164">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="571bf-165">Azure 키 자격 증명 모음의 서비스 계층 및 기능에 대 한 자세한 내용은 [Azure 키 보관소 가격 웹 사이트](http://go.microsoft.com/fwlink/?linkid=512521)를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="571bf-165">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="571bf-166">이 매개 변수는 새 키를 만들 때 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-166">This parameter is required when you create a new key.</span></span> <span data-ttu-id="571bf-167">*Keyfilepath* 매개 변수를 사용 하 여 키를 가져오는 경우이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-167">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="571bf-168">이 매개 변수를 지정 하지 않고이 cmdlet은 file 이름 확장명이 byok 인 키를 가져오면 해당 키를 HSM 보호 키로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-168">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="571bf-169">Cmdlet에서 해당 키를 소프트웨어 보호 키로 가져올 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-169">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="571bf-170">이 매개 변수를 지정 하지 않고이 cmdlet이 .pfx 파일 이름 확장명을 가진 키를 가져오면 해당 키를 소프트웨어 보호 키로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-170">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="571bf-171">-Disable</span><span class="sxs-lookup"><span data-stu-id="571bf-171">-Disable</span></span>
<span data-ttu-id="571bf-172">추가 하는 키가 비활성의 초기 상태로 설정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-172">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="571bf-173">키를 사용 하려는 시도는 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-173">Any attempt to use the key will fail.</span></span> <span data-ttu-id="571bf-174">나중에 사용 하려는 키를 미리 로드 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-174">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="571bf-175">-만료</span><span class="sxs-lookup"><span data-stu-id="571bf-175">-Expires</span></span>
<span data-ttu-id="571bf-176">이 cmdlet이 추가 하는 키에 대 한 만료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-176">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="571bf-177">이 매개 변수는 UTC (협정 세계시)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-177">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="571bf-178">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-178">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="571bf-179">자세한 내용은을 입력 `Get-Help Get-Date` 하세요.</span><span class="sxs-lookup"><span data-stu-id="571bf-179">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="571bf-180">이 매개 변수를 지정 하지 않으면 키가 만료 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-180">If you do not specify this parameter, the key does not expire.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="571bf-181">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="571bf-181">-KeyFilePassword</span></span>
<span data-ttu-id="571bf-182">가져온 파일의 암호를 **SecureString** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-182">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="571bf-183">**Securestring** 개체를 가져오려면 **ConvertTo-SecureString** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-183">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="571bf-184">자세한 내용은을 입력 `Get-Help ConvertTo-SecureString` 하세요.</span><span class="sxs-lookup"><span data-stu-id="571bf-184">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="571bf-185">파일 이름 확장명이 .pfx 인 파일을 가져오려면이 암호를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-185">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="571bf-186">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="571bf-186">-KeyFilePath</span></span>
<span data-ttu-id="571bf-187">이 cmdlet이 가져오는 키 자료가 포함 된 로컬 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-187">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="571bf-188">올바른 파일 이름 확장명은 byok 및 .pfx입니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-188">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="571bf-189">파일을 byok 파일 인 경우 가져오기 후 키가 Hsm에 의해 자동으로 보호 되며이 기본값을 재정의할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-189">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="571bf-190">파일이 .pfx 파일이 면 가져오기 후 소프트웨어에 의해 키가 자동으로 보호 됩니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-190">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="571bf-191">이 기본값을 재정의 하려면 키가 HSM으로 보호 되도록 *대상* 매개 변수를 hsm으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-191">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="571bf-192">이 매개 변수를 지정 하는 경우 *대상* 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-192">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="571bf-193">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="571bf-193">-KeyOps</span></span>
<span data-ttu-id="571bf-194">이 cmdlet이 추가 하는 키를 사용 하 여 수행할 수 있는 작업 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-194">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="571bf-195">이 매개 변수를 지정 하지 않으면 모든 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-195">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="571bf-196">이 매개 변수에 허용 되는 값은 [JSON Web key (JWK) 사양](http://go.microsoft.com/fwlink/?LinkID=613300)에 정의 된 대로 쉼표로 구분 된 키 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-196">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="571bf-197">해독할</span><span class="sxs-lookup"><span data-stu-id="571bf-197">Encrypt</span></span>
- <span data-ttu-id="571bf-198">해독은</span><span class="sxs-lookup"><span data-stu-id="571bf-198">Decrypt</span></span>
- <span data-ttu-id="571bf-199">줄 바꿈</span><span class="sxs-lookup"><span data-stu-id="571bf-199">Wrap</span></span>
- <span data-ttu-id="571bf-200">래핑을</span><span class="sxs-lookup"><span data-stu-id="571bf-200">Unwrap</span></span>
- <span data-ttu-id="571bf-201">등록할</span><span class="sxs-lookup"><span data-stu-id="571bf-201">Sign</span></span>
- <span data-ttu-id="571bf-202">나타나는지</span><span class="sxs-lookup"><span data-stu-id="571bf-202">Verify</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="571bf-203">-이름</span><span class="sxs-lookup"><span data-stu-id="571bf-203">-Name</span></span>
<span data-ttu-id="571bf-204">키 자격 증명 모음에 추가할 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-204">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="571bf-205">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 키의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-205">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="571bf-206">Name은 0-9, a-z, a-z 및-(대시 기호)만 포함 하는 1 ~ 63 문자 문자열 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-206">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="571bf-207">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="571bf-207">-NotBefore</span></span>
<span data-ttu-id="571bf-208">시간을 **DateTime** 개체로 지정 하 고 그 뒤에 키를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-208">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="571bf-209">이 매개 변수는 UTC를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-209">This parameter uses UTC.</span></span> <span data-ttu-id="571bf-210">**DateTime** 개체를 가져오려면 **날짜 가져오기** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-210">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="571bf-211">이 매개 변수를 지정 하지 않으면 키를 즉시 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-211">If you do not specify this parameter, the key can be used immediately.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="571bf-212">태그</span><span class="sxs-lookup"><span data-stu-id="571bf-212">-Tag</span></span>
<span data-ttu-id="571bf-213">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-213">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="571bf-214">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="571bf-214">For example:</span></span>

<span data-ttu-id="571bf-215">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="571bf-215">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="571bf-216">-VaultName</span><span class="sxs-lookup"><span data-stu-id="571bf-216">-VaultName</span></span>
<span data-ttu-id="571bf-217">이 cmdlet이 키를 추가 하는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-217">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="571bf-218">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-218">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="571bf-219">-확인</span><span class="sxs-lookup"><span data-stu-id="571bf-219">-Confirm</span></span>
<span data-ttu-id="571bf-220">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-220">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="571bf-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="571bf-221">-WhatIf</span></span>
<span data-ttu-id="571bf-222">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="571bf-223">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-223">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="571bf-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="571bf-224">CommonParameters</span></span>
<span data-ttu-id="571bf-225">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="571bf-226">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="571bf-226">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="571bf-227">입력</span><span class="sxs-lookup"><span data-stu-id="571bf-227">INPUTS</span></span>

### <span data-ttu-id="571bf-228">않아야</span><span class="sxs-lookup"><span data-stu-id="571bf-228">None</span></span>
<span data-ttu-id="571bf-229">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="571bf-229">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="571bf-230">출력</span><span class="sxs-lookup"><span data-stu-id="571bf-230">OUTPUTS</span></span>

### <span data-ttu-id="571bf-231">Microsoft. KeyVault. Keyvault</span><span class="sxs-lookup"><span data-stu-id="571bf-231">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="571bf-232">상속자</span><span class="sxs-lookup"><span data-stu-id="571bf-232">NOTES</span></span>

## <span data-ttu-id="571bf-233">관련 링크</span><span class="sxs-lookup"><span data-stu-id="571bf-233">RELATED LINKS</span></span>

[<span data-ttu-id="571bf-234">백업-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="571bf-234">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="571bf-235">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="571bf-235">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="571bf-236">제거-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="571bf-236">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="571bf-237">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="571bf-237">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
