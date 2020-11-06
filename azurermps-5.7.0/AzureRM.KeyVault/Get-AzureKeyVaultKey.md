---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultKey.md
ms.openlocfilehash: eaddfaa6be725d588c8856031a34e1bdefcc3892
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532815"
---
# <span data-ttu-id="0ad73-101">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0ad73-101">Get-AzureKeyVaultKey</span></span>

## <span data-ttu-id="0ad73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ad73-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad73-103">키 보관소 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-103">Gets Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ad73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ad73-104">SYNTAX</span></span>

### <span data-ttu-id="0ad73-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0ad73-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad73-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="0ad73-106">ByKeyName</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad73-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="0ad73-107">ByKeyVersions</span></span>
```
Get-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad73-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="0ad73-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad73-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="0ad73-109">ByInputObjectKeyName</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad73-110">ByKInputObjecteyVersions</span><span class="sxs-lookup"><span data-stu-id="0ad73-110">ByKInputObjecteyVersions</span></span>
```
Get-AzureKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ad73-111">설명은</span><span class="sxs-lookup"><span data-stu-id="0ad73-111">DESCRIPTION</span></span>
<span data-ttu-id="0ad73-112">**AzureKeyVaultKey** Cmdlet은 Azure 키 자격 증명 모음 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-112">The **Get-AzureKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="0ad73-113">이 cmdlet은 특정 **Microsoft Azure.** e. e. e. e. e. e. e. e a **KeyBundle** e.</span><span class="sxs-lookup"><span data-stu-id="0ad73-113">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="0ad73-114">예제의</span><span class="sxs-lookup"><span data-stu-id="0ad73-114">EXAMPLES</span></span>

### <span data-ttu-id="0ad73-115">예제 1: 키 보관소에 모든 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="0ad73-115">Example 1: Get all the keys in a key vault</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso'
```

<span data-ttu-id="0ad73-116">이 명령은 Contoso 라는 키 보관소의 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-116">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="0ad73-117">예제 2: 현재 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="0ad73-117">Example 2: Get the current version of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx'
```

<span data-ttu-id="0ad73-118">이 명령은 Contoso 라는 키 보관소에 ITPfx 이름의 현재 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-118">This command gets the current version of the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="0ad73-119">예제 3: 모든 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="0ad73-119">Example 3: Get all versions of a key</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -IncludeVersions
```

<span data-ttu-id="0ad73-120">이 명령은 모든 버전의 key vaultnamed Contoso의 ITPfx에 이름을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-120">This command gets all versions the key named ITPfx in the key vaultnamed Contoso.</span></span>

### <span data-ttu-id="0ad73-121">예제 4: 특정 버전의 키 가져오기</span><span class="sxs-lookup"><span data-stu-id="0ad73-121">Example 4: Get a specific version of a key</span></span>
```
PS C:\>$Key = Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -Version '5A12A276385949DB8B5F82AFEE85CAED'
```

<span data-ttu-id="0ad73-122">이 명령은 Contoso 라는 키 보관소에 ITPfx 라는 특정 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-122">This command gets a specific version of the key named ITPfx in the key vault named Contoso.</span></span>
<span data-ttu-id="0ad73-123">이 명령을 실행 한 후에는 $Key 개체를 탐색 하 여 키의 다양 한 속성을 검사할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-123">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="0ad73-124">예제 5: 삭제 했지만이 키 보관소에는 제거 되지 않은 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-124">Example 5: Get all the keys that have been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -InRemovedState
```

<span data-ttu-id="0ad73-125">이 명령은 Contoso 라는 키 보관소에서 이전에 삭제 했지만 제거 되지 않은 모든 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-125">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="0ad73-126">예제 6: 삭제 되었지만이 키 보관소에는 제거 되지 않은 키 ITPfx를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-126">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' -KeyName 'ITPfx' -InRemovedState
```

<span data-ttu-id="0ad73-127">이 명령은 Contoso 라는 키 자격 증명 모음에서 이전에 삭제 되었지만 제거 되지 않은 키 ITPfx를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-127">This command gets the key ITPfx that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="0ad73-128">이 명령은 삭제 날짜 등의 메타 데이터와이 지운 편지함의 예정 된 제거 날짜 등을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-128">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

## <span data-ttu-id="0ad73-129">변수</span><span class="sxs-lookup"><span data-stu-id="0ad73-129">PARAMETERS</span></span>

### <span data-ttu-id="0ad73-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad73-130">-DefaultProfile</span></span>
<span data-ttu-id="0ad73-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0ad73-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ad73-132">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="0ad73-132">-IncludeVersions</span></span>
<span data-ttu-id="0ad73-133">이 cmdlet가 모든 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-133">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="0ad73-134">키의 현재 버전은 목록의 첫 번째 항목입니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-134">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="0ad73-135">이 매개 변수를 지정 하는 경우 *Name* 및 *VaultName* 매개 변수도 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-135">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>

<span data-ttu-id="0ad73-136">*Includeversions* 매개 변수를 지정 하지 않으면이 cmdlet은 지정 된 *이름을* 사용 하 여 현재 버전의 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-136">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByKeyVersions, ByKInputObjecteyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad73-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ad73-137">-InputObject</span></span>
<span data-ttu-id="0ad73-138">KeyVault 개체.</span><span class="sxs-lookup"><span data-stu-id="0ad73-138">KeyVault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad73-139">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="0ad73-139">-InRemovedState</span></span>
<span data-ttu-id="0ad73-140">출력에 이전에 삭제 된 키를 표시할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-140">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad73-141">-이름</span><span class="sxs-lookup"><span data-stu-id="0ad73-141">-Name</span></span>
<span data-ttu-id="0ad73-142">가져올 키 번들의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-142">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByInputObjectVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByKInputObjecteyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad73-143">-VaultName</span><span class="sxs-lookup"><span data-stu-id="0ad73-143">-VaultName</span></span>
<span data-ttu-id="0ad73-144">이 cmdlet에서 키를 가져오는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-144">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="0ad73-145">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 선택한 환경에 따라 키 보관소의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-145">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad73-146">-버전</span><span class="sxs-lookup"><span data-stu-id="0ad73-146">-Version</span></span>
<span data-ttu-id="0ad73-147">키 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-147">Specifies the key version.</span></span>
<span data-ttu-id="0ad73-148">이 cmdlet은 키 자격 증명 이름, 현재 선택 된 환경, 키 이름 및 키 버전을 기준으로 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-148">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName, ByInputObjectKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad73-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad73-149">CommonParameters</span></span>
<span data-ttu-id="0ad73-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ad73-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad73-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad73-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad73-152">입력</span><span class="sxs-lookup"><span data-stu-id="0ad73-152">INPUTS</span></span>

### <span data-ttu-id="0ad73-153">이름</span><span class="sxs-lookup"><span data-stu-id="0ad73-153">String</span></span>

## <span data-ttu-id="0ad73-154">출력</span><span class="sxs-lookup"><span data-stu-id="0ad73-154">OUTPUTS</span></span>

### <span data-ttu-id="0ad73-155"><를 나열 합니다. Keyvault>, PSKeyVaultKey, eletedKeyVaultKeyIdentityItem, eletedKeyVaultKey., List<, Microsoft.Azure.Commands.KeyVault.Models.PSD> Microsoft.Azure.Commands.KeyVault.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="0ad73-155">List<Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey, List<Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem>, Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="0ad73-156">상속자</span><span class="sxs-lookup"><span data-stu-id="0ad73-156">NOTES</span></span>

## <span data-ttu-id="0ad73-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ad73-157">RELATED LINKS</span></span>

[<span data-ttu-id="0ad73-158">추가-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0ad73-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="0ad73-159">제거-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0ad73-159">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="0ad73-160">실행 취소-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="0ad73-160">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

[<span data-ttu-id="0ad73-161">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="0ad73-161">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

