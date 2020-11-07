---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultSecret.md
ms.openlocfilehash: db46a3dd8669d5c8eeeb85aeafc25654faa8c107
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875809"
---
# <span data-ttu-id="58a3d-101">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58a3d-101">Remove-AzKeyVaultSecret</span></span>

## <span data-ttu-id="58a3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58a3d-102">SYNOPSIS</span></span>
<span data-ttu-id="58a3d-103">키 보관소에서 비밀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-103">Deletes a secret in a key vault.</span></span>

## <span data-ttu-id="58a3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58a3d-104">SYNTAX</span></span>

```
Remove-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58a3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="58a3d-105">DESCRIPTION</span></span>
<span data-ttu-id="58a3d-106">Remove-AzKeyVaultSecret cmdlet은 키 자격 증명 모음에서 비밀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-106">The Remove-AzKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="58a3d-107">비밀을 실수로 삭제 한 경우 사용자가 특정 ' 복구 ' 권한을 사용 하 여 Undo-AzKeyVaultSecretRemoval 사용 하 여 비밀을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-107">If the secret was accidentally deleted the secret can be recovered using Undo-AzKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="58a3d-108">이 cmdlet의 값은 ' a/or **영향** ' 속성에 대해 high입니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-108">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="58a3d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="58a3d-109">EXAMPLES</span></span>

### <span data-ttu-id="58a3d-110">예제 1: 키 자격 증명 모음에서 비밀 제거</span><span class="sxs-lookup"><span data-stu-id="58a3d-110">Example 1: Remove a secret from a key vault</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret'
```

<span data-ttu-id="58a3d-111">이 명령은 ' Contoso ' 라는 키 자격 증명 모음에서 FinanceSecret 이라는 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-111">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="58a3d-112">예제 2: 사용자 확인 없이 키 자격 증명 모음에서 비밀 제거</span><span class="sxs-lookup"><span data-stu-id="58a3d-112">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -Force -Confirm:$False
```

<span data-ttu-id="58a3d-113">이 명령은 Contoso 라는 키 자격 증명 모음에서 FinanceSecret 이라는 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-113">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="58a3d-114">명령에서 *Force* 및 *Confirm* 매개 변수를 지정 하므로 cmdlet이 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-114">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="58a3d-115">예제 3: 키 보관소에서 삭제 된 비밀을 영구적으로 제거</span><span class="sxs-lookup"><span data-stu-id="58a3d-115">Example 3: Purge deleted secret from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="58a3d-116">이 명령은 premoves 라는 비밀을 Contoso 라는 키 자격 증명 모음에서 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-116">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="58a3d-117">이 cmdlet을 실행 하려면 ' 제거 ' 권한이 필요 하며이 키 보관소에 대해 사용자에 게 명시적으로 부여 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-117">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="58a3d-118">변수</span><span class="sxs-lookup"><span data-stu-id="58a3d-118">PARAMETERS</span></span>

### <span data-ttu-id="58a3d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58a3d-119">-DefaultProfile</span></span>
<span data-ttu-id="58a3d-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="58a3d-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58a3d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="58a3d-121">-Force</span></span>
<span data-ttu-id="58a3d-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58a3d-123">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="58a3d-123">-InRemovedState</span></span>
<span data-ttu-id="58a3d-124">있는 경우 이전에 삭제 한 비밀을 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-124">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="58a3d-125">-이름</span><span class="sxs-lookup"><span data-stu-id="58a3d-125">-Name</span></span>
<span data-ttu-id="58a3d-126">비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-126">Specifies the name of a secret.</span></span>
<span data-ttu-id="58a3d-127">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 비밀의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-127">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58a3d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58a3d-128">-PassThru</span></span>
<span data-ttu-id="58a3d-129">이 cmdlet이 **Microsoft Azure. KeyVault** . i 볼트. i 자격 증명 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-129">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="58a3d-130">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="58a3d-131">-VaultName</span><span class="sxs-lookup"><span data-stu-id="58a3d-131">-VaultName</span></span>
<span data-ttu-id="58a3d-132">비밀이 속한 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-132">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="58a3d-133">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-133">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="58a3d-134">-확인</span><span class="sxs-lookup"><span data-stu-id="58a3d-134">-Confirm</span></span>
<span data-ttu-id="58a3d-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58a3d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58a3d-136">-WhatIf</span></span>
<span data-ttu-id="58a3d-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58a3d-138">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-138">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58a3d-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58a3d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58a3d-140">CommonParameters</span></span>
<span data-ttu-id="58a3d-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58a3d-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58a3d-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58a3d-143">입력</span><span class="sxs-lookup"><span data-stu-id="58a3d-143">INPUTS</span></span>

### <span data-ttu-id="58a3d-144">이름</span><span class="sxs-lookup"><span data-stu-id="58a3d-144">String</span></span>

## <span data-ttu-id="58a3d-145">출력</span><span class="sxs-lookup"><span data-stu-id="58a3d-145">OUTPUTS</span></span>

### <span data-ttu-id="58a3d-146">Microsoft. KeyVault. DeletedSecret</span><span class="sxs-lookup"><span data-stu-id="58a3d-146">Microsoft.Azure.Commands.KeyVault.Models.DeletedSecret</span></span>
<span data-ttu-id="58a3d-147">이 cmdlet은 *PassThru* 매개 변수를 지정 하는 경우에만 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58a3d-147">This cmdlet returns a value only if you specify the *PassThru* parameter.</span></span>

## <span data-ttu-id="58a3d-148">상속자</span><span class="sxs-lookup"><span data-stu-id="58a3d-148">NOTES</span></span>

## <span data-ttu-id="58a3d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58a3d-149">RELATED LINKS</span></span>

[<span data-ttu-id="58a3d-150">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58a3d-150">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="58a3d-151">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="58a3d-151">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="58a3d-152">실행 취소-AzKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="58a3d-152">Undo-AzKeyVaultSecretRemoval</span></span>](./Undo-AzKeyVaultSecretRemoval.md)

