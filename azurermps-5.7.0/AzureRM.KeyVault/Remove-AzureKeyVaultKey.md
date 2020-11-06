---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultKey.md
ms.openlocfilehash: 5244ed9a8803be07a46c50a15553a4863f7907d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529804"
---
# <span data-ttu-id="010d9-101">Remove-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="010d9-101">Remove-AzureKeyVaultKey</span></span>

## <span data-ttu-id="010d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="010d9-102">SYNOPSIS</span></span>
<span data-ttu-id="010d9-103">키 볼트에서 키를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-103">Deletes a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="010d9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="010d9-104">SYNTAX</span></span>

### <span data-ttu-id="010d9-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="010d9-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="010d9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="010d9-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="010d9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="010d9-107">DESCRIPTION</span></span>
<span data-ttu-id="010d9-108">Remove-AzureKeyVaultKey cmdlet은 키 자격 증명 모음에서 키를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-108">The Remove-AzureKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="010d9-109">키를 실수로 삭제 한 경우 특정 ' 복구 ' 권한이 있는 사용자가 Undo-AzureKeyVaultKeyRemoval를 사용 하 여 키를 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-109">If the key was accidentally deleted the key can be recovered using Undo-AzureKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="010d9-110">이 cmdlet의 값은 ' a/or **영향** ' 속성에 대해 high입니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="010d9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="010d9-111">EXAMPLES</span></span>

### <span data-ttu-id="010d9-112">예제 1: 키 보관소에서 키 제거</span><span class="sxs-lookup"><span data-stu-id="010d9-112">Example 1: Remove a key from a key vault</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware'
```

<span data-ttu-id="010d9-113">이 명령은 Contoso 라는 키 보관소에서 ITSoftware 라는 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="010d9-114">예제 2: 사용자 확인 없이 키 제거</span><span class="sxs-lookup"><span data-stu-id="010d9-114">Example 2: Remove a key without user confirmation</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force -Confirm:$False
```

<span data-ttu-id="010d9-115">이 명령은 Contoso 라는 키 보관소에서 ITSoftware 라는 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="010d9-116">명령에서 *Force* 및 *Confirm* 매개 변수를 지정 하므로 cmdlet이 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="010d9-117">예제 3: 키 보관소에서 삭제 된 키를 영구적으로 제거</span><span class="sxs-lookup"><span data-stu-id="010d9-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="010d9-118">이 명령은 Contoso 라는 키 자격 증명 모음에서 ITSoftware 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="010d9-119">이 cmdlet을 실행 하려면 ' 제거 ' 권한이 필요 하며이 키 보관소에 대해 사용자에 게 명시적으로 부여 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="010d9-120">예제 4: 파이프라인 연산자를 사용 하 여 키 제거</span><span class="sxs-lookup"><span data-stu-id="010d9-120">Example 4: Remove keys by using the pipeline operator</span></span>
```
PS C:\>Get-AzureKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzureKeyVaultKey
```

<span data-ttu-id="010d9-121">이 명령은 Contoso 라는 키 보관소의 모든 키를 가져와 파이프라인 연산자를 사용 하 여 **Where-개체** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="010d9-122">해당 cmdlet은 **Enabled** 특성에 대 한 $False 값을 갖는 키를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="010d9-123">해당 cmdlet은 해당 키를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="010d9-124">변수</span><span class="sxs-lookup"><span data-stu-id="010d9-124">PARAMETERS</span></span>

### <span data-ttu-id="010d9-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="010d9-125">-DefaultProfile</span></span>
<span data-ttu-id="010d9-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="010d9-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="010d9-127">-Force</span><span class="sxs-lookup"><span data-stu-id="010d9-127">-Force</span></span>
<span data-ttu-id="010d9-128">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="010d9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="010d9-129">-InputObject</span></span>
<span data-ttu-id="010d9-130">KeyBundle 개체</span><span class="sxs-lookup"><span data-stu-id="010d9-130">KeyBundle Object</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="010d9-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="010d9-131">-InRemovedState</span></span>
<span data-ttu-id="010d9-132">이전에 삭제 된 키를 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-132">Remove the previously deleted key permanently.</span></span>

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

### <span data-ttu-id="010d9-133">-이름</span><span class="sxs-lookup"><span data-stu-id="010d9-133">-Name</span></span>
<span data-ttu-id="010d9-134">제거할 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="010d9-135">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 키의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="010d9-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="010d9-136">-PassThru</span></span>
<span data-ttu-id="010d9-137">이 cmdlet이 **Microsoft Azure. KeyVault** 개체를 반환 하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** object.</span></span>
<span data-ttu-id="010d9-138">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-138">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="010d9-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="010d9-139">-VaultName</span></span>
<span data-ttu-id="010d9-140">키를 제거할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="010d9-141">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="010d9-142">-확인</span><span class="sxs-lookup"><span data-stu-id="010d9-142">-Confirm</span></span>
<span data-ttu-id="010d9-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="010d9-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="010d9-144">-WhatIf</span></span>
<span data-ttu-id="010d9-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="010d9-146">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="010d9-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-147">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="010d9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="010d9-148">CommonParameters</span></span>
<span data-ttu-id="010d9-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="010d9-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="010d9-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="010d9-151">입력</span><span class="sxs-lookup"><span data-stu-id="010d9-151">INPUTS</span></span>

### <span data-ttu-id="010d9-152">이름</span><span class="sxs-lookup"><span data-stu-id="010d9-152">String</span></span>

## <span data-ttu-id="010d9-153">출력</span><span class="sxs-lookup"><span data-stu-id="010d9-153">OUTPUTS</span></span>

### <span data-ttu-id="010d9-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="010d9-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>
<span data-ttu-id="010d9-155">이 cmdlet은 *PassThru* 매개 변수를 지정 하는 경우에만 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="010d9-155">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="010d9-156">상속자</span><span class="sxs-lookup"><span data-stu-id="010d9-156">NOTES</span></span>

## <span data-ttu-id="010d9-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="010d9-157">RELATED LINKS</span></span>

[<span data-ttu-id="010d9-158">추가-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="010d9-158">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="010d9-159">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="010d9-159">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="010d9-160">Set-AzureKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="010d9-160">Set-AzureKeyVaultKeyAttribute</span></span>](./Set-AzureKeyVaultKeyAttribute.md)

[<span data-ttu-id="010d9-161">실행 취소-AzureKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="010d9-161">Undo-AzureKeyVaultKeyRemoval</span></span>](./Undo-AzureKeyVaultKeyRemoval.md)

