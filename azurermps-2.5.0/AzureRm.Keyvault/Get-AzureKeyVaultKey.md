---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
ms.openlocfilehash: 5ebb9ca4a59f713ec81e5099cd3bbcc91084ac4d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881898"
---
# <span data-ttu-id="2a0ec-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2a0ec-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="2a0ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a0ec-102">SYNOPSIS</span></span>
<span data-ttu-id="2a0ec-103">키 보관소 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a0ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a0ec-104">SYNTAX</span></span>

### <span data-ttu-id="2a0ec-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2a0ec-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a0ec-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="2a0ec-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a0ec-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="2a0ec-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a0ec-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="2a0ec-108">ByDeletedKey</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a0ec-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2a0ec-109">DESCRIPTION</span></span>
<span data-ttu-id="2a0ec-110">**AzureKeyVaultKey** Cmdlet은 Azure 키 자격 증명 모음 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-110">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="2a0ec-111">이 cmdlet은 특정 **Microsoft Azure.** e. e. e. e. e. e. e. e a **KeyBundle** e.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="2a0ec-112">예제의</span><span class="sxs-lookup"><span data-stu-id="2a0ec-112">EXAMPLES</span></span>

### <span data-ttu-id="2a0ec-113">예제 1: 키 보관소에 모든 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="2a0ec-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="2a0ec-114">이 명령은 Contoso 라는 키 보관소의 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="2a0ec-115">예제 2: 현재 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="2a0ec-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="2a0ec-116">이 명령은 Contoso 라는 키 보관소에 ITPfx 이름의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="2a0ec-117">예제 3: 모든 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="2a0ec-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="2a0ec-118">이 명령은 모든 버전의 key vaultnamed Contoso의 ITPfx에 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="2a0ec-119">예제 4: 특정 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="2a0ec-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="2a0ec-120">이 명령은 Contoso 라는 키 보관소에 ITPfx 라는 특정 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="2a0ec-121">이 명령을 실행 한 후에는 $Key 개체를 탐색 하 여 키의 다양 한 속성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="2a0ec-122">예제 5: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="2a0ec-123">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 했지만 제거 되지 않은 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="2a0ec-124">예제 6: 삭제 되었지만이 키 보관소에는 제거 되지 않은 키 ITPfx를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="2a0ec-125">이 명령은 Contoso 라는 키 자격 증명 모음에서 이전에 삭제 되었지만 제거 되지 않은 키 ITPfx를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="2a0ec-126">이 명령은 삭제 날짜 등의 메타 데이터와이 지운 편지함의 예정 된 제거 날짜 등을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="2a0ec-127">변수</span><span class="sxs-lookup"><span data-stu-id="2a0ec-127">PARAMETERS</span></span>

### <span data-ttu-id="2a0ec-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a0ec-128">-DefaultProfile</span></span>
<span data-ttu-id="2a0ec-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="2a0ec-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2a0ec-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="2a0ec-130">-IncludeVersions</span></span>
<span data-ttu-id="2a0ec-131">이 cmdlet가 모든 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-131">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="2a0ec-132">키의 현재 버전은 목록의 첫 번째 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-132">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="2a0ec-133">이 매개 변수를 지정 하는 경우 *Name* 및 *VaultName* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-133">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="2a0ec-134">*Includeversions* 매개 변수를 지정 하지 않으면이 cmdlet은 지정 된 *이름을* 사용 하 여 현재 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-134">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a0ec-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="2a0ec-135">-InRemovedState</span></span>
<span data-ttu-id="2a0ec-136">출력에 이전에 삭제 된 키를 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-136">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedKey
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a0ec-137">-이름</span><span class="sxs-lookup"><span data-stu-id="2a0ec-137">-Name</span></span>
<span data-ttu-id="2a0ec-138">가져올 키 번들의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-138">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedKey
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0ec-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="2a0ec-139">-VaultName</span></span>
<span data-ttu-id="2a0ec-140">이 cmdlet에서 키를 가져오는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-140">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="2a0ec-141">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 선택한 환경에 따라 키 보관소의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-141">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="2a0ec-142">-버전</span><span class="sxs-lookup"><span data-stu-id="2a0ec-142">-Version</span></span>
<span data-ttu-id="2a0ec-143">키 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-143">Specifies the key version.</span></span>
<span data-ttu-id="2a0ec-144">이 cmdlet은 키 자격 증명 이름, 현재 선택 된 환경, 키 이름 및 키 버전을 기준으로 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-144">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a0ec-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a0ec-145">CommonParameters</span></span>
<span data-ttu-id="2a0ec-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a0ec-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a0ec-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a0ec-148">입력</span><span class="sxs-lookup"><span data-stu-id="2a0ec-148">INPUTS</span></span>

### <span data-ttu-id="2a0ec-149">이름</span><span class="sxs-lookup"><span data-stu-id="2a0ec-149">String</span></span>

## <span data-ttu-id="2a0ec-150">출력</span><span class="sxs-lookup"><span data-stu-id="2a0ec-150">OUTPUTS</span></span>

### <span data-ttu-id="2a0ec-151"><를 나열 합니다. DeletedKeyIdentityItem DeletedKeyBundle, KeyIdentityItem>, 번들. keyvault,<Microsoft azure.->, Microsoft Azure.-KeyVault. 키 모음. i 자격 증명. i 볼트.</span><span class="sxs-lookup"><span data-stu-id="2a0ec-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="2a0ec-152">상속자</span><span class="sxs-lookup"><span data-stu-id="2a0ec-152">NOTES</span></span>

## <span data-ttu-id="2a0ec-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a0ec-153">RELATED LINKS</span></span>

[<span data-ttu-id="2a0ec-154">추가-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2a0ec-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="2a0ec-155">제거-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="2a0ec-155">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="2a0ec-156">실행 취소-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="2a0ec-156">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="2a0ec-157">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="2a0ec-157">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

