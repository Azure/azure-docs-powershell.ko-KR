---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/get-AzKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: a0d79aa0d1699f6e6645f86475732c235447342f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875832"
---
# <span data-ttu-id="738f6-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="738f6-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="738f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="738f6-102">SYNOPSIS</span></span>
<span data-ttu-id="738f6-103">키 보관소 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="738f6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="738f6-104">SYNTAX</span></span>

### <span data-ttu-id="738f6-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="738f6-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="738f6-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="738f6-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="738f6-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="738f6-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="738f6-108">ByDeletedKey</span><span class="sxs-lookup"><span data-stu-id="738f6-108">ByDeletedKey</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="738f6-109">설명은</span><span class="sxs-lookup"><span data-stu-id="738f6-109">DESCRIPTION</span></span>
<span data-ttu-id="738f6-110">**AzKeyVaultKey** Cmdlet은 Azure 키 자격 증명 모음 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-110">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="738f6-111">이 cmdlet은 특정 **Microsoft Azure.** e. e. e. e. e. e. e. e a **KeyBundle** e.</span><span class="sxs-lookup"><span data-stu-id="738f6-111">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="738f6-112">예제의</span><span class="sxs-lookup"><span data-stu-id="738f6-112">EXAMPLES</span></span>

### <span data-ttu-id="738f6-113">예제 1: 키 보관소에 모든 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="738f6-113">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="738f6-114">이 명령은 Contoso 라는 키 보관소의 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-114">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="738f6-115">예제 2: 현재 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="738f6-115">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="738f6-116">이 명령은 Contoso 라는 키 보관소에 ITPfx 이름의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-116">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="738f6-117">예제 3: 모든 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="738f6-117">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="738f6-118">이 명령은 모든 버전의 key vaultnamed Contoso의 ITPfx에 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-118">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="738f6-119">예제 4: 특정 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="738f6-119">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="738f6-120">이 명령은 Contoso 라는 키 보관소에 ITPfx 라는 특정 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-120">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="738f6-121">이 명령을 실행 한 후에는 $Key 개체를 탐색 하 여 키의 다양 한 속성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-121">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="738f6-122">예제 5: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-122">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="738f6-123">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 했지만 제거 되지 않은 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-123">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="738f6-124">예제 6: 삭제 되었지만이 키 보관소에는 제거 되지 않은 키 ITPfx를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-124">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="738f6-125">이 명령은 Contoso 라는 키 자격 증명 모음에서 이전에 삭제 되었지만 제거 되지 않은 키 ITPfx를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-125">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="738f6-126">이 명령은 삭제 날짜 등의 메타 데이터와이 지운 편지함의 예정 된 제거 날짜 등을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-126">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="738f6-127">변수</span><span class="sxs-lookup"><span data-stu-id="738f6-127">PARAMETERS</span></span>

### <span data-ttu-id="738f6-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="738f6-128">-DefaultProfile</span></span>
<span data-ttu-id="738f6-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="738f6-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="738f6-130">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="738f6-130">-IncludeVersions</span></span>
<span data-ttu-id="738f6-131">이 cmdlet가 모든 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-131">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="738f6-132">키의 현재 버전은 목록의 첫 번째 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-132">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="738f6-133">이 매개 변수를 지정 하는 경우 *Name* 및 *VaultName* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-133">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="738f6-134">*Includeversions* 매개 변수를 지정 하지 않으면이 cmdlet은 지정 된 *이름을* 사용 하 여 현재 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-134">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

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

### <span data-ttu-id="738f6-135">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="738f6-135">-InRemovedState</span></span>
<span data-ttu-id="738f6-136">출력에 이전에 삭제 된 키를 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-136">Specifies whether to show the previously deleted keys in the output</span></span>

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

### <span data-ttu-id="738f6-137">-이름</span><span class="sxs-lookup"><span data-stu-id="738f6-137">-Name</span></span>
<span data-ttu-id="738f6-138">가져올 키 번들의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-138">Specifies the name of the key bundle to get.</span></span>

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

### <span data-ttu-id="738f6-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="738f6-139">-VaultName</span></span>
<span data-ttu-id="738f6-140">이 cmdlet에서 키를 가져오는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-140">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="738f6-141">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 선택한 환경에 따라 키 보관소의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-141">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="738f6-142">-버전</span><span class="sxs-lookup"><span data-stu-id="738f6-142">-Version</span></span>
<span data-ttu-id="738f6-143">키 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-143">Specifies the key version.</span></span>
<span data-ttu-id="738f6-144">이 cmdlet은 키 자격 증명 이름, 현재 선택 된 환경, 키 이름 및 키 버전을 기준으로 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-144">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

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

### <span data-ttu-id="738f6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="738f6-145">CommonParameters</span></span>
<span data-ttu-id="738f6-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="738f6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="738f6-147">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="738f6-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="738f6-148">입력</span><span class="sxs-lookup"><span data-stu-id="738f6-148">INPUTS</span></span>

### <span data-ttu-id="738f6-149">이름</span><span class="sxs-lookup"><span data-stu-id="738f6-149">String</span></span>

## <span data-ttu-id="738f6-150">출력</span><span class="sxs-lookup"><span data-stu-id="738f6-150">OUTPUTS</span></span>

### <span data-ttu-id="738f6-151"><를 나열 합니다. DeletedKeyIdentityItem DeletedKeyBundle, KeyIdentityItem>, 번들. keyvault,<Microsoft azure.->, Microsoft Azure.-KeyVault. 키 모음. i 자격 증명. i 볼트.</span><span class="sxs-lookup"><span data-stu-id="738f6-151">List<Microsoft.Azure.Commands.KeyVault.Models.KeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.KeyBundle, List<Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.DeletedKeyBundle</span></span>

## <span data-ttu-id="738f6-152">상속자</span><span class="sxs-lookup"><span data-stu-id="738f6-152">NOTES</span></span>

## <span data-ttu-id="738f6-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="738f6-153">RELATED LINKS</span></span>

[<span data-ttu-id="738f6-154">추가-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="738f6-154">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="738f6-155">제거-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="738f6-155">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="738f6-156">실행 취소-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="738f6-156">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="738f6-157">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="738f6-157">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

