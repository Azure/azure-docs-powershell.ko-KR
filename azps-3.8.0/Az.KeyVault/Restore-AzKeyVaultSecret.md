---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 5a00bab81cad7b77873459ab58615a2836970b09
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041889"
---
# <span data-ttu-id="17ee2-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17ee2-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="17ee2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17ee2-102">SYNOPSIS</span></span>
<span data-ttu-id="17ee2-103">백업 비밀의 키 보관소에 비밀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="17ee2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="17ee2-104">SYNTAX</span></span>

### <span data-ttu-id="17ee2-105">ByVaultName (기본값)</span><span class="sxs-lookup"><span data-stu-id="17ee2-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17ee2-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="17ee2-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17ee2-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="17ee2-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17ee2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="17ee2-108">DESCRIPTION</span></span>
<span data-ttu-id="17ee2-109">**Restore-AzKeyVaultSecret** cmdlet은 지정 된 키 보관소에 비밀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="17ee2-110">이 비밀은 입력 파일에 있는 백업 비밀의 복제본 이며, 원래 비밀 이름과 동일한 이름을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="17ee2-111">키 자격 증명 모음에 같은 이름의 비밀이 이미 있는 경우 원래 비밀을 덮어쓰지 않고이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="17ee2-112">백업에 여러 버전의 비밀이 포함 되어 있으면 모든 버전이 복원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="17ee2-113">비밀을 복원 하는 키 보관소는 비밀을 백업한 키 보관소와 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="17ee2-114">그러나 키 자격 증명 모음이 동일한 구독을 사용 해야 하며 같은 지리 (예: 북미)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="17ee2-115"> https://azure.microsoft.com/support/trust-center/)Azure 지역을 지역에 매핑하는 Microsoft Azure 보안 센터를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="17ee2-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="17ee2-116">예제의</span><span class="sxs-lookup"><span data-stu-id="17ee2-116">EXAMPLES</span></span>

### <span data-ttu-id="17ee2-117">예제 1: 백업 된 비밀 복원</span><span class="sxs-lookup"><span data-stu-id="17ee2-117">Example 1: Restore a backed-up secret</span></span>
```powershell
PS C:\> Restore-AzKeyVaultSecret -VaultName 'contoso' -InputFile "C:\Backup.blob"

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="17ee2-118">이 명령은 Backup. a i a i a i a i a i a i a i a i a i.</span><span class="sxs-lookup"><span data-stu-id="17ee2-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="17ee2-119">변수</span><span class="sxs-lookup"><span data-stu-id="17ee2-119">PARAMETERS</span></span>

### <span data-ttu-id="17ee2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17ee2-120">-DefaultProfile</span></span>
<span data-ttu-id="17ee2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="17ee2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17ee2-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="17ee2-122">-InputFile</span></span>
<span data-ttu-id="17ee2-123">복원할 비밀의 백업을 포함 하는 입력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17ee2-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17ee2-124">-InputObject</span></span>
<span data-ttu-id="17ee2-125">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="17ee2-125">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17ee2-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17ee2-126">-ResourceId</span></span>
<span data-ttu-id="17ee2-127">KeyVault 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="17ee2-127">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17ee2-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="17ee2-128">-VaultName</span></span>
<span data-ttu-id="17ee2-129">비밀을 복원할 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="17ee2-130">-확인</span><span class="sxs-lookup"><span data-stu-id="17ee2-130">-Confirm</span></span>
<span data-ttu-id="17ee2-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17ee2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17ee2-132">-WhatIf</span></span>
<span data-ttu-id="17ee2-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17ee2-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17ee2-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17ee2-135">CommonParameters</span></span>
<span data-ttu-id="17ee2-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="17ee2-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17ee2-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="17ee2-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17ee2-138">입력</span><span class="sxs-lookup"><span data-stu-id="17ee2-138">INPUTS</span></span>

### <span data-ttu-id="17ee2-139">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="17ee2-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="17ee2-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="17ee2-140">System.String</span></span>

## <span data-ttu-id="17ee2-141">출력</span><span class="sxs-lookup"><span data-stu-id="17ee2-141">OUTPUTS</span></span>

### <span data-ttu-id="17ee2-142">Microsoft. KeyVault. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17ee2-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="17ee2-143">상속자</span><span class="sxs-lookup"><span data-stu-id="17ee2-143">NOTES</span></span>

## <span data-ttu-id="17ee2-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17ee2-144">RELATED LINKS</span></span>

[<span data-ttu-id="17ee2-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17ee2-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="17ee2-146">백업-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17ee2-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="17ee2-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17ee2-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="17ee2-148">제거-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="17ee2-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

