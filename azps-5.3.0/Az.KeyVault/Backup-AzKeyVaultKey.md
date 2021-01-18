---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 88decaffa736f015b8e65aa1217eab4899b07c7c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495332"
---
# <span data-ttu-id="913f8-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="913f8-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="913f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="913f8-102">SYNOPSIS</span></span>
<span data-ttu-id="913f8-103">키 자격 증명 모음에 키를 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="913f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="913f8-104">SYNTAX</span></span>

### <span data-ttu-id="913f8-105">ByKeyName(기본값)</span><span class="sxs-lookup"><span data-stu-id="913f8-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="913f8-106">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="913f8-106">HsmByKeyName</span></span>
```
Backup-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="913f8-107">ByKey</span><span class="sxs-lookup"><span data-stu-id="913f8-107">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="913f8-108">설명</span><span class="sxs-lookup"><span data-stu-id="913f8-108">DESCRIPTION</span></span>
<span data-ttu-id="913f8-109">**Backup-AzKeyVaultKey** cmdlet은 키 자격 증명 모음에 지정된 키를 다운로드하고 파일에 저장하여 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-109">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="913f8-110">키 버전이 여러 개 있는 경우 모든 버전이 백업에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-110">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="913f8-111">다운로드한 콘텐츠는 암호화되어 있기 때문에 Azure Key Vault 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-111">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="913f8-112">백업된 키는 백업된 구독의 키 자격 증명 모음에 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-112">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="913f8-113">이 cmdlet을 사용하는 일반적인 이유는</span><span class="sxs-lookup"><span data-stu-id="913f8-113">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="913f8-114">키 자격 증명 모음에서 키를 실수로 삭제하는 경우 오프라인 복사본이 있도록 키 복사본을 에스코합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-114">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="913f8-115">Key Vault를 사용하여 키를 만들었다가 이제 다른 Azure 지역에 키를 복제하여 분산된 애플리케이션의 모든 인스턴스에서 사용할 수 있도록 하려는 경우</span><span class="sxs-lookup"><span data-stu-id="913f8-115">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="913f8-116">**Backup-AzKeyVaultKey** cmdlet을 사용하여 암호화된 형식으로 키를 검색한 다음 Restore-AzKeyVaultKey cmdlet을 사용하여 두 번째 지역에서 키 자격 증명 모음을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-116">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="913f8-117">예제</span><span class="sxs-lookup"><span data-stu-id="913f8-117">EXAMPLES</span></span>

### <span data-ttu-id="913f8-118">예제 1: 자동으로 생성된 파일 이름으로 키 백업</span><span class="sxs-lookup"><span data-stu-id="913f8-118">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="913f8-119">이 명령은 MyKeyVault라는 키 자격 증명 모음에서 MyKey라는 키를 검색하고 해당 키의 백업을 자동으로 명명된 파일에 저장하고 파일 이름을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-119">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="913f8-120">예제 2: 지정된 파일 이름에 키 백업</span><span class="sxs-lookup"><span data-stu-id="913f8-120">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="913f8-121">이 명령은 Key Vault 이름이 MyKeyVault인 MyKeyVault에서 MyKey라는 키를 검색하고 해당 키의 백업을 Backup.blob이라는 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-121">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="913f8-122">예제 3: 이전에 검색한 키를 지정된 파일 이름에 백업하여 메시지를 표시하지 않고 대상 파일을 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-122">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="913f8-123">이 명령은 이름 있는 키의 백업을 $key. 자격 증명 모음의 이름은 $key. VaultName을 Backup.blob이라는 파일에 저장하고, 파일이 이미 있는 경우 파일을 자동으로 덮어써야 합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-123">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="913f8-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="913f8-124">PARAMETERS</span></span>

### <span data-ttu-id="913f8-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="913f8-125">-DefaultProfile</span></span>
<span data-ttu-id="913f8-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="913f8-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="913f8-127">-Force</span><span class="sxs-lookup"><span data-stu-id="913f8-127">-Force</span></span>
<span data-ttu-id="913f8-128">주어진 파일이 있는 경우 덮어 덮어 사용</span><span class="sxs-lookup"><span data-stu-id="913f8-128">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="913f8-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="913f8-129">-HsmName</span></span>
<span data-ttu-id="913f8-130">HSM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-130">HSM name.</span></span> <span data-ttu-id="913f8-131">Cmdlet은 이름 및 현재 선택한 환경에 따라 관리되는 HSM의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-131">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f8-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="913f8-132">-InputObject</span></span>
<span data-ttu-id="913f8-133">백업할 키 번들로, 검색 호출의 출력에서 파이프라인됩니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-133">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="913f8-134">-Name</span><span class="sxs-lookup"><span data-stu-id="913f8-134">-Name</span></span>
<span data-ttu-id="913f8-135">백업할 키의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-135">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f8-136">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="913f8-136">-OutputFile</span></span>
<span data-ttu-id="913f8-137">백업 Blob이 저장되는 출력 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-137">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="913f8-138">이 매개 변수를 지정하지 않으면 이 cmdlet에서 파일 이름을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-138">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="913f8-139">기존 출력 파일의 이름을 지정하면 작업이 완료되지 않습니다. 백업 파일이 이미 있는 오류 메시지가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-139">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="913f8-140">-VaultName</span><span class="sxs-lookup"><span data-stu-id="913f8-140">-VaultName</span></span>
<span data-ttu-id="913f8-141">백업할 키가 포함된 키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-141">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f8-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="913f8-142">-Confirm</span></span>
<span data-ttu-id="913f8-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f8-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="913f8-144">-WhatIf</span></span>
<span data-ttu-id="913f8-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="913f8-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="913f8-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="913f8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="913f8-147">CommonParameters</span></span>
<span data-ttu-id="913f8-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="913f8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="913f8-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="913f8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="913f8-150">입력</span><span class="sxs-lookup"><span data-stu-id="913f8-150">INPUTS</span></span>

### <span data-ttu-id="913f8-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="913f8-151">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="913f8-152">출력</span><span class="sxs-lookup"><span data-stu-id="913f8-152">OUTPUTS</span></span>

### <span data-ttu-id="913f8-153">System.String</span><span class="sxs-lookup"><span data-stu-id="913f8-153">System.String</span></span>

## <span data-ttu-id="913f8-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="913f8-154">NOTES</span></span>

## <span data-ttu-id="913f8-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="913f8-155">RELATED LINKS</span></span>

[<span data-ttu-id="913f8-156">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="913f8-156">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="913f8-157">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="913f8-157">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="913f8-158">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="913f8-158">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="913f8-159">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="913f8-159">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

