---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 70DB088D-4AF5-406B-8D66-118A0F766041
online version: https://docs.microsoft.com/powershell/module/az.keyvault/restore-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVaultSecret.md
ms.openlocfilehash: 56f5279b1d3645717a29e392fd45599344515a29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978432"
---
# <span data-ttu-id="aa841-101">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aa841-101">Restore-AzKeyVaultSecret</span></span>

## <span data-ttu-id="aa841-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa841-102">SYNOPSIS</span></span>
<span data-ttu-id="aa841-103">백업된 비밀에서 키 자격 증명 모음에 비밀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-103">Creates a secret in a key vault from a backed-up secret.</span></span>

## <span data-ttu-id="aa841-104">구문</span><span class="sxs-lookup"><span data-stu-id="aa841-104">SYNTAX</span></span>

### <span data-ttu-id="aa841-105">ByVaultName(기본값)</span><span class="sxs-lookup"><span data-stu-id="aa841-105">ByVaultName (Default)</span></span>
```
Restore-AzKeyVaultSecret [-VaultName] <String> [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa841-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="aa841-106">ByInputObject</span></span>
```
Restore-AzKeyVaultSecret [-InputObject] <PSKeyVault> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa841-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="aa841-107">ByResourceId</span></span>
```
Restore-AzKeyVaultSecret [-ResourceId] <String> [-InputFile] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa841-108">설명</span><span class="sxs-lookup"><span data-stu-id="aa841-108">DESCRIPTION</span></span>
<span data-ttu-id="aa841-109">**Restore-AzKeyVaultSecret cmdlet은** 지정된 키 자격 증명 모음에 비밀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-109">The **Restore-AzKeyVaultSecret** cmdlet creates a secret in the specified key vault.</span></span>
<span data-ttu-id="aa841-110">이 비밀은 입력 파일의 백업된 비밀의 복제본으로 원래 비밀과 이름이 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-110">This secret is a replica of the backed-up secret in the input file and has the same name as the original secret.</span></span>
<span data-ttu-id="aa841-111">키 자격 증명 모음에 동일한 이름의 비밀이 이미 있는 경우 이 cmdlet은 원래 비밀을 덮어써야 하는 대신 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-111">If the key vault already has a secret by the same name, this cmdlet fails instead of overwriting the original secret.</span></span>
<span data-ttu-id="aa841-112">백업에 여러 버전의 비밀이 포함된 경우 모든 버전이 복원됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-112">If the backup contains multiple versions of a secret, all versions are restored.</span></span>
<span data-ttu-id="aa841-113">비밀을 복원하는 키 자격 증명 모음은 비밀을 백업한 키 자격 증명 모음과 다를 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-113">The key vault that you restore the secret into can be different from the key vault that you backed up the secret from.</span></span>
<span data-ttu-id="aa841-114">그러나 키 자격 증명 모음은 동일한 구독을 사용하며 동일한 지역(예: 북아메리카)의 Azure 지역에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-114">However, the key vault must use the same subscription and be in an Azure region in the same geography (for example, North America).</span></span>
<span data-ttu-id="aa841-115">Azure 지역을 지역으로 매핑하는 경우 Microsoft Azure Trust https://azure.microsoft.com/support/trust-center/) Center()를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="aa841-115">See the Microsoft Azure Trust Center (https://azure.microsoft.com/support/trust-center/) for the mapping of Azure regions to geographies.</span></span>

## <span data-ttu-id="aa841-116">예제</span><span class="sxs-lookup"><span data-stu-id="aa841-116">EXAMPLES</span></span>

### <span data-ttu-id="aa841-117">예제 1: 백업된 비밀 복원</span><span class="sxs-lookup"><span data-stu-id="aa841-117">Example 1: Restore a backed-up secret</span></span>
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

<span data-ttu-id="aa841-118">이 명령은 Backup.blob이라는 백업 파일에서 contoso라는 키 자격 증명 모음으로 모든 버전을 포함하여 비밀을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-118">This command restores a secret, including all of its versions, from the backup file named Backup.blob into the key vault named contoso.</span></span>

## <span data-ttu-id="aa841-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aa841-119">PARAMETERS</span></span>

### <span data-ttu-id="aa841-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa841-120">-DefaultProfile</span></span>
<span data-ttu-id="aa841-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aa841-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aa841-122">-InputFile</span><span class="sxs-lookup"><span data-stu-id="aa841-122">-InputFile</span></span>
<span data-ttu-id="aa841-123">복원할 비밀의 백업을 포함하는 입력 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-123">Specifies the input file that contains the backup of the secret to restore.</span></span>

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

### <span data-ttu-id="aa841-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa841-124">-InputObject</span></span>
<span data-ttu-id="aa841-125">KeyVault 개체</span><span class="sxs-lookup"><span data-stu-id="aa841-125">KeyVault object</span></span>

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

### <span data-ttu-id="aa841-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa841-126">-ResourceId</span></span>
<span data-ttu-id="aa841-127">KeyVault 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="aa841-127">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="aa841-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="aa841-128">-VaultName</span></span>
<span data-ttu-id="aa841-129">비밀을 복원할 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-129">Specifies the name of the key vault into which to restore the secret.</span></span>

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

### <span data-ttu-id="aa841-130">-확인</span><span class="sxs-lookup"><span data-stu-id="aa841-130">-Confirm</span></span>
<span data-ttu-id="aa841-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa841-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa841-132">-WhatIf</span></span>
<span data-ttu-id="aa841-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa841-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa841-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa841-135">CommonParameters</span></span>
<span data-ttu-id="aa841-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aa841-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa841-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa841-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa841-138">입력</span><span class="sxs-lookup"><span data-stu-id="aa841-138">INPUTS</span></span>

### <span data-ttu-id="aa841-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="aa841-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="aa841-140">System.String</span><span class="sxs-lookup"><span data-stu-id="aa841-140">System.String</span></span>

## <span data-ttu-id="aa841-141">출력</span><span class="sxs-lookup"><span data-stu-id="aa841-141">OUTPUTS</span></span>

### <span data-ttu-id="aa841-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aa841-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

## <span data-ttu-id="aa841-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aa841-143">NOTES</span></span>

## <span data-ttu-id="aa841-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aa841-144">RELATED LINKS</span></span>

[<span data-ttu-id="aa841-145">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aa841-145">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="aa841-146">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aa841-146">Backup-AzKeyVaultSecret</span></span>](./Backup-AzKeyVaultSecret.md)

[<span data-ttu-id="aa841-147">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aa841-147">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="aa841-148">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="aa841-148">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

