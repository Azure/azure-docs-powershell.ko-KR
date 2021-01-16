---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: a171f967a937873b85adcfca732987037e6db0a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386387"
---
# <span data-ttu-id="9d25a-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9d25a-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="9d25a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d25a-102">SYNOPSIS</span></span>
<span data-ttu-id="9d25a-103">키 자격 증명 모음에 비밀을 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="9d25a-104">구문</span><span class="sxs-lookup"><span data-stu-id="9d25a-104">SYNTAX</span></span>

### <span data-ttu-id="9d25a-105">BySecretName(기본값)</span><span class="sxs-lookup"><span data-stu-id="9d25a-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d25a-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="9d25a-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-InputObject] <PSKeyVaultSecretIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d25a-107">설명</span><span class="sxs-lookup"><span data-stu-id="9d25a-107">DESCRIPTION</span></span>
<span data-ttu-id="9d25a-108">**Backup-AzKeyVaultSecret** cmdlet은 키 자격 증명 모음에 지정된 비밀을 다운로드하고 파일에 저장하여 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="9d25a-109">비밀 버전이 여러 개 있는 경우 모든 버전이 백업에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="9d25a-110">다운로드한 콘텐츠는 암호화되어 있기 때문에 Azure Key Vault 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="9d25a-111">백업된 비밀을 백업된 구독의 키 자격 증명 모음에 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="9d25a-112">이 cmdlet을 사용하는 일반적인 이유는</span><span class="sxs-lookup"><span data-stu-id="9d25a-112">Typical reasons to use this cmdlet are:</span></span>
- <span data-ttu-id="9d25a-113">키 자격 증명 모음에서 비밀을 실수로 삭제하는 경우 오프라인 복사본이 있도록 비밀의 복사본을 에코로 에코합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="9d25a-114">키 자격 증명 모음에 비밀을 추가하고 이제 다른 Azure 지역에 비밀을 복제하여 분산된 애플리케이션의 모든 인스턴스에서 사용할 수 있도록 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="9d25a-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="9d25a-115">Backup-AzKeyVaultSecret cmdlet을 사용하여 암호화된 형식으로 비밀을 검색한 다음 Restore-AzKeyVaultSecret cmdlet을 사용하여 두 번째 지역에 키 자격 증명 모음을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="9d25a-116">(지역은 동일한 지역에 속해야 합니다.)</span><span class="sxs-lookup"><span data-stu-id="9d25a-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="9d25a-117">예제</span><span class="sxs-lookup"><span data-stu-id="9d25a-117">EXAMPLES</span></span>

### <span data-ttu-id="9d25a-118">예제 1: 자동으로 생성된 파일 이름으로 비밀 백업</span><span class="sxs-lookup"><span data-stu-id="9d25a-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'

C:\Users\username\mykeyvault-mysecret-1527029447.01191
```

<span data-ttu-id="9d25a-119">이 명령은 MyKeyVault라는 키 자격 증명 모음에서 MySecret이라는 비밀을 검색하고 해당 비밀의 백업을 자동으로 명명된 파일에 저장하고 파일 이름을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="9d25a-120">예제 2: 메시지를 표시하지 않고 기존 파일을 덮어매는 지정된 파일 이름에 비밀 백업</span><span class="sxs-lookup"><span data-stu-id="9d25a-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```powershell
PS C:\> Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="9d25a-121">이 명령은 Key Vault 이름이 MyKeyVault인 MyKeyVault에서 MySecret이라는 비밀을 검색하고 해당 비밀의 백업을 Backup.blob이라는 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="9d25a-122">예제 3: 이전에 검색된 비밀을 지정된 파일 이름으로 백업</span><span class="sxs-lookup"><span data-stu-id="9d25a-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```powershell
PS C:\> $secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\> Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="9d25a-123">이 명령은 $secret 개체의 자격 증명 모음 이름 및 이름을 사용하여 비밀을 검색하고 Backup.blob이라는 파일에 백업을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="9d25a-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d25a-124">PARAMETERS</span></span>

### <span data-ttu-id="9d25a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d25a-125">-DefaultProfile</span></span>
<span data-ttu-id="9d25a-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9d25a-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d25a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9d25a-127">-Force</span></span>
<span data-ttu-id="9d25a-128">출력 파일을 덮어 사용(있는 경우)하기 전에 확인을 요청합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d25a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d25a-129">-InputObject</span></span>
<span data-ttu-id="9d25a-130">검색 호출의 출력에서 파이프라인으로 백업할 비밀입니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-130">Secret to be backed up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem
Parameter Sets: BySecret
Aliases: Secret

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d25a-131">-Name</span><span class="sxs-lookup"><span data-stu-id="9d25a-131">-Name</span></span>
<span data-ttu-id="9d25a-132">백업할 비밀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-132">Specifies the name of the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d25a-133">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="9d25a-133">-OutputFile</span></span>
<span data-ttu-id="9d25a-134">백업 Blob이 저장되는 출력 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-134">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="9d25a-135">이 매개 변수를 지정하지 않으면 이 cmdlet에서 파일 이름을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-135">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="9d25a-136">기존 출력 파일의 이름을 지정하면 작업이 완료되지 않습니다. 백업 파일이 이미 있는 오류 메시지가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-136">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d25a-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9d25a-137">-VaultName</span></span>
<span data-ttu-id="9d25a-138">백업할 비밀을 포함하는 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d25a-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d25a-139">-Confirm</span></span>
<span data-ttu-id="9d25a-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d25a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d25a-141">-WhatIf</span></span>
<span data-ttu-id="9d25a-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9d25a-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d25a-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d25a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d25a-144">CommonParameters</span></span>
<span data-ttu-id="9d25a-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9d25a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d25a-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9d25a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d25a-147">입력</span><span class="sxs-lookup"><span data-stu-id="9d25a-147">INPUTS</span></span>

### <span data-ttu-id="9d25a-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9d25a-148">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

## <span data-ttu-id="9d25a-149">출력</span><span class="sxs-lookup"><span data-stu-id="9d25a-149">OUTPUTS</span></span>

### <span data-ttu-id="9d25a-150">System.String</span><span class="sxs-lookup"><span data-stu-id="9d25a-150">System.String</span></span>

## <span data-ttu-id="9d25a-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9d25a-151">NOTES</span></span>

## <span data-ttu-id="9d25a-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d25a-152">RELATED LINKS</span></span>

[<span data-ttu-id="9d25a-153">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9d25a-153">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="9d25a-154">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9d25a-154">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="9d25a-155">Remove-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9d25a-155">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="9d25a-156">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="9d25a-156">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

