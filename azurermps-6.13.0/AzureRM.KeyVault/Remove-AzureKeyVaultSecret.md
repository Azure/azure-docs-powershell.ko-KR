---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultSecret.md
ms.openlocfilehash: bff9c08a0c36fb7a4d89fb86d9c219491f3642b7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530269"
---
# <span data-ttu-id="4b3e0-101">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4b3e0-101">Remove-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="4b3e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b3e0-102">SYNOPSIS</span></span>
<span data-ttu-id="4b3e0-103">키 보관소에서 비밀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-103">Deletes a secret in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b3e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b3e0-104">SYNTAX</span></span>

### <span data-ttu-id="4b3e0-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="4b3e0-105">ByVaultName (Default)</span></span>
```
Remove-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b3e0-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4b3e0-106">ByInputObject</span></span>
```
Remove-AzureKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b3e0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4b3e0-107">DESCRIPTION</span></span>
<span data-ttu-id="4b3e0-108">Remove-AzureKeyVaultSecret cmdlet은 키 자격 증명 모음에서 비밀을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-108">The Remove-AzureKeyVaultSecret cmdlet deletes a secret in a key vault.</span></span>
<span data-ttu-id="4b3e0-109">비밀을 실수로 삭제 한 경우 사용자가 특정 ' 복구 ' 권한을 사용 하 여 Undo-AzureKeyVaultSecretRemoval 사용 하 여 비밀을 복구할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-109">If the secret was accidentally deleted the secret can be recovered using Undo-AzureKeyVaultSecretRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="4b3e0-110">이 cmdlet의 값은 ' a/or **영향** ' 속성에 대해 high입니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="4b3e0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="4b3e0-111">EXAMPLES</span></span>

### <span data-ttu-id="4b3e0-112">예제 1: 키 자격 증명 모음에서 비밀 제거</span><span class="sxs-lookup"><span data-stu-id="4b3e0-112">Example 1: Remove a secret from a key vault</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="4b3e0-113">이 명령은 ' Contoso ' 라는 키 자격 증명 모음에서 FinanceSecret 이라는 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-113">This command removes the secret named FinanceSecret from the key vault named Contoso.'</span></span>

### <span data-ttu-id="4b3e0-114">예제 2: 사용자 확인 없이 키 자격 증명 모음에서 비밀 제거</span><span class="sxs-lookup"><span data-stu-id="4b3e0-114">Example 2: Remove a secret from a key vault without user confirmation</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -PassThru -Force

Vault Name           : Contoso
Name                 : FinanceSecret
Version              : f622abc7b1394092812f1eb0f85dc91c
Id                   : https://contoso.vault.azure.net:443/secrets/financesecret/f622abc7b1394092812f1eb0f85dc91c
Deleted Date         : 5/25/2018 4:45:34 PM
Scheduled Purge Date : 8/23/2018 4:45:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/19/2018 5:56:02 PM
Updated              : 4/26/2018 7:48:40 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="4b3e0-115">이 명령은 Contoso 라는 키 자격 증명 모음에서 FinanceSecret 이라는 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-115">This command removes the secret named FinanceSecret from the key vault named Contoso.</span></span>
<span data-ttu-id="4b3e0-116">명령에서 *Force* 및 *Confirm* 매개 변수를 지정 하므로 cmdlet이 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-116">The command specifies the *Force* and *Confirm* parameters, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="4b3e0-117">예제 3: 키 보관소에서 삭제 된 비밀을 영구적으로 제거</span><span class="sxs-lookup"><span data-stu-id="4b3e0-117">Example 3: Purge deleted secret from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'FinanceSecret' -InRemovedState
```

<span data-ttu-id="4b3e0-118">이 명령은 premoves 라는 비밀을 Contoso 라는 키 자격 증명 모음에서 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-118">This command premoves the secret named FinanceSecret from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="4b3e0-119">이 cmdlet을 실행 하려면 ' 제거 ' 권한이 필요 하며이 키 보관소에 대해 사용자에 게 명시적으로 부여 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

## <span data-ttu-id="4b3e0-120">변수</span><span class="sxs-lookup"><span data-stu-id="4b3e0-120">PARAMETERS</span></span>

### <span data-ttu-id="4b3e0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b3e0-121">-DefaultProfile</span></span>
<span data-ttu-id="4b3e0-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4b3e0-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-123">-Force</span><span class="sxs-lookup"><span data-stu-id="4b3e0-123">-Force</span></span>
<span data-ttu-id="4b3e0-124">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-124">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4b3e0-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b3e0-125">-InputObject</span></span>
<span data-ttu-id="4b3e0-126">키 자격 증명 모음 비밀 개체</span><span class="sxs-lookup"><span data-stu-id="4b3e0-126">Key Vault Secret Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="4b3e0-127">-InRemovedState</span></span>
<span data-ttu-id="4b3e0-128">있는 경우 이전에 삭제 한 비밀을 영구적으로 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-128">If present, removes the previously deleted secret permanently.</span></span>

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

### <span data-ttu-id="4b3e0-129">-이름</span><span class="sxs-lookup"><span data-stu-id="4b3e0-129">-Name</span></span>
<span data-ttu-id="4b3e0-130">비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-130">Specifies the name of a secret.</span></span>
<span data-ttu-id="4b3e0-131">이 cmdlet은이 매개 변수에서 지정 하는 이름, 키 보관소의 이름 및 현재 환경에 따라 비밀의 FQDN (정규화 된 도메인 이름)을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-131">This cmdlet constructs the fully qualified domain name (FQDN) of a secret based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b3e0-132">-PassThru</span></span>
<span data-ttu-id="4b3e0-133">이 cmdlet이 **Microsoft Azure. KeyVault** . i 볼트. i 자격 증명 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-133">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.Secret** object.</span></span>
<span data-ttu-id="4b3e0-134">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="4b3e0-135">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4b3e0-135">-VaultName</span></span>
<span data-ttu-id="4b3e0-136">비밀이 속한 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-136">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="4b3e0-137">이 cmdlet은이 매개 변수에서 지정 하는 이름 및 현재 환경에 따라 키 자격 증명의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-137">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-138">-확인</span><span class="sxs-lookup"><span data-stu-id="4b3e0-138">-Confirm</span></span>
<span data-ttu-id="4b3e0-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b3e0-140">-WhatIf</span></span>
<span data-ttu-id="4b3e0-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b3e0-142">Cmdlet이 실행 되지 않습니다. Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-142">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b3e0-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b3e0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b3e0-144">CommonParameters</span></span>
<span data-ttu-id="4b3e0-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b3e0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b3e0-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b3e0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b3e0-147">입력</span><span class="sxs-lookup"><span data-stu-id="4b3e0-147">INPUTS</span></span>

### <span data-ttu-id="4b3e0-148">Microsoft. KeyVault. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4b3e0-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>
<span data-ttu-id="4b3e0-149">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4b3e0-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4b3e0-150">출력</span><span class="sxs-lookup"><span data-stu-id="4b3e0-150">OUTPUTS</span></span>

### <span data-ttu-id="4b3e0-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4b3e0-151">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="4b3e0-152">상속자</span><span class="sxs-lookup"><span data-stu-id="4b3e0-152">NOTES</span></span>

## <span data-ttu-id="4b3e0-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b3e0-153">RELATED LINKS</span></span>

[<span data-ttu-id="4b3e0-154">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4b3e0-154">Get-AzureKeyVaultSecret</span></span>](./Get-AzureKeyVaultSecret.md)

[<span data-ttu-id="4b3e0-155">Set-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="4b3e0-155">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

[<span data-ttu-id="4b3e0-156">실행 취소-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="4b3e0-156">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

