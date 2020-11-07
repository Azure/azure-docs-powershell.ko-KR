---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
ms.openlocfilehash: 522268cb215a393ef54209b7606c8556d2566fd7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882238"
---
# <span data-ttu-id="d9cb5-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d9cb5-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="d9cb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="d9cb5-103">키 보관소의 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d9cb5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9cb5-104">SYNTAX</span></span>

### <span data-ttu-id="d9cb5-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d9cb5-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9cb5-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="d9cb5-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9cb5-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="d9cb5-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9cb5-108">ByDeletedSecrets</span><span class="sxs-lookup"><span data-stu-id="d9cb5-108">ByDeletedSecrets</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9cb5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d9cb5-109">DESCRIPTION</span></span>
<span data-ttu-id="d9cb5-110">**AzureKeyVaultSecret** cmdlet은 키 보관소의 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-110">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="d9cb5-111">이 cmdlet은 키 자격 증명 모음의 특정 비밀 또는 모든 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-111">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="d9cb5-112">예제의</span><span class="sxs-lookup"><span data-stu-id="d9cb5-112">EXAMPLES</span></span>

### <span data-ttu-id="d9cb5-113">예제 1: 키 보관소에 있는 모든 비밀에 대 한 모든 최신 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9cb5-113">Example 1: Get all current versions of all secrets in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso'
```

<span data-ttu-id="d9cb5-114">이 명령은 Contoso 라는 키 보관소에 있는 모든 비밀의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-114">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="d9cb5-115">예제 2: 특정 비밀의 모든 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9cb5-115">Example 2: Get all versions of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -IncludeVersions
```

<span data-ttu-id="d9cb5-116">이 명령은 Contoso 라는 키 보관소에 ITSecret 라는 모든 버전의 암호를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-116">This command gets all versions of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="d9cb5-117">예제 3: 특정 비밀 정보의 현재 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9cb5-117">Example 3: Get the current version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
```

<span data-ttu-id="d9cb5-118">이 명령은 Contoso 라는 키 보관소에 ITSecret 라는 이름의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-118">This command gets the current version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="d9cb5-119">예제 4: 특정 보안 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9cb5-119">Example 4: Get a specific version of a specific secret</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret' -Version '6A12A286385949DB8B5F82AFEF85CAE9'
```

<span data-ttu-id="d9cb5-120">이 명령은 Contoso 라는 키 보관소에 ITSecret 라는 특정 버전의 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-120">This command gets a specific version of the secret named ITSecret in the key vault named Contoso.</span></span>

### <span data-ttu-id="d9cb5-121">예제 5: 특정 비밀의 현재 버전에 대 한 일반 텍스트 값 가져오기</span><span class="sxs-lookup"><span data-stu-id="d9cb5-121">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```
PS C:\>$secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is: " $secret.SecretValueText
```

<span data-ttu-id="d9cb5-122">이러한 명령은 ITSecret 라는 최신 버전의 비밀을 얻은 다음 해당 비밀의 일반 텍스트 값을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-122">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="d9cb5-123">예제 6: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-123">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="d9cb5-124">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 모든 비밀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-124">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="d9cb5-125">예제 7: 삭제 되었지만이 키 보관소에는 제거 되지 않은 비밀 ITSecret를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-125">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'ITSecret' -InRemovedState
```

<span data-ttu-id="d9cb5-126">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 되었지만 제거 되지 않은 비밀 ITSecret를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-126">This command gets the secret ITSecret that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="d9cb5-127">이 명령은 삭제 날짜와 같은 메타 데이터를 반환 하 고, 해당 비밀의 예정 된 제거 날짜</span><span class="sxs-lookup"><span data-stu-id="d9cb5-127">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="d9cb5-128">변수</span><span class="sxs-lookup"><span data-stu-id="d9cb5-128">PARAMETERS</span></span>

### <span data-ttu-id="d9cb5-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9cb5-129">-DefaultProfile</span></span>
<span data-ttu-id="d9cb5-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d9cb5-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9cb5-131">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="d9cb5-131">-IncludeVersions</span></span>
<span data-ttu-id="d9cb5-132">이 cmdlet이 모든 보안 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-132">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="d9cb5-133">현재 버전의 비밀은 목록의 첫 번째입니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-133">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="d9cb5-134">이 매개 변수를 지정 하는 경우 *Name* 및 *VaultName* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-134">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="d9cb5-135">*Includeversions* 매개 변수를 지정 하지 않으면이 cmdlet은 지정 된 *이름을* 사용 하 여 현재 버전의 암호를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-135">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: BySecretVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9cb5-136">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d9cb5-136">-InRemovedState</span></span>
<span data-ttu-id="d9cb5-137">이전에 삭제 한 비밀을 출력에 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-137">Specifies whether to show the previously deleted secrets in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedSecrets
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9cb5-138">-이름</span><span class="sxs-lookup"><span data-stu-id="d9cb5-138">-Name</span></span>
<span data-ttu-id="d9cb5-139">가져올 비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-139">Specifies the name of the secret to get.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName, BySecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedSecrets
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9cb5-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="d9cb5-140">-VaultName</span></span>
<span data-ttu-id="d9cb5-141">비밀이 속한 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-141">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="d9cb5-142">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 보관소의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-142">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="d9cb5-143">-버전</span><span class="sxs-lookup"><span data-stu-id="d9cb5-143">-Version</span></span>
<span data-ttu-id="d9cb5-144">비밀 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-144">Specifies the secret version.</span></span>
<span data-ttu-id="d9cb5-145">이 cmdlet은 키 보관소 이름, 현재 선택 된 환경, 비밀 이름 및 비밀 버전을 기준으로 비밀의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-145">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9cb5-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9cb5-146">CommonParameters</span></span>
<span data-ttu-id="d9cb5-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9cb5-148">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9cb5-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9cb5-149">입력</span><span class="sxs-lookup"><span data-stu-id="d9cb5-149">INPUTS</span></span>

### <span data-ttu-id="d9cb5-150">이름</span><span class="sxs-lookup"><span data-stu-id="d9cb5-150">String</span></span>

## <span data-ttu-id="d9cb5-151">출력</span><span class="sxs-lookup"><span data-stu-id="d9cb5-151">OUTPUTS</span></span>

### <span data-ttu-id="d9cb5-152"><를 나열 합니다. KeyVault>, SecretIdentityItem,, DeletedSecret,<등의를 나열 합니다.>, Microsoft Azure .를 확인 하세요.-KeyVault .를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9cb5-152">List<Microsoft.Azure.Commands.KeyVault.Models.SecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.Secret, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedSecretIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>

## <span data-ttu-id="d9cb5-153">상속자</span><span class="sxs-lookup"><span data-stu-id="d9cb5-153">NOTES</span></span>

## <span data-ttu-id="d9cb5-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9cb5-154">RELATED LINKS</span></span>

[<span data-ttu-id="d9cb5-155">제거-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d9cb5-155">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="d9cb5-156">실행 취소-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="d9cb5-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="d9cb5-157">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="d9cb5-157">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

