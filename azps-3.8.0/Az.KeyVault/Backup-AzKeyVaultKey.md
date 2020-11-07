---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVaultKey.md
ms.openlocfilehash: 28f4550ac850b7bcc5bab4c90ec510128a8e2ab0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879261"
---
# <span data-ttu-id="1e68b-101">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e68b-101">Backup-AzKeyVaultKey</span></span>

## <span data-ttu-id="1e68b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e68b-102">SYNOPSIS</span></span>
<span data-ttu-id="1e68b-103">키 자격 증명 모음에서 키를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-103">Backs up a key in a key vault.</span></span>

## <span data-ttu-id="1e68b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e68b-104">SYNTAX</span></span>

### <span data-ttu-id="1e68b-105">ByKeyName (기본값)</span><span class="sxs-lookup"><span data-stu-id="1e68b-105">ByKeyName (Default)</span></span>
```
Backup-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e68b-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="1e68b-106">ByKey</span></span>
```
Backup-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e68b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1e68b-107">DESCRIPTION</span></span>
<span data-ttu-id="1e68b-108">**AzKeyVaultKey** cmdlet은 지정 된 키를 다운로드 하 여 파일에 저장 하 여 키 보관소에 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-108">The **Backup-AzKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="1e68b-109">여러 버전의 키가 있는 경우 백업에 모든 버전이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="1e68b-110">다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="1e68b-111">백업한 키를 백업 된 구독에 있는 모든 키 보관소에 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>
<span data-ttu-id="1e68b-112">이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="1e68b-113">키 자격 증명 모음에서 실수로 키를 삭제 하는 경우 오프 라인 복사본을 사용할 수 있도록 키 복사본을 에스크로 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="1e68b-114">키 자격 증명 모음을 사용 하 여 키를 만든 다음 해당 키를 다른 Azure 지역에 복제 하 여 분산 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="1e68b-115">**AzKeyVaultKey** cmdlet을 사용 하 여 키를 암호화 된 형식으로 검색 한 다음 Restore-AzKeyVaultKey cmdlet을 사용 하 고 두 번째 지역에서 키 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-115">Use the **Backup-AzKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="1e68b-116">예제의</span><span class="sxs-lookup"><span data-stu-id="1e68b-116">EXAMPLES</span></span>

### <span data-ttu-id="1e68b-117">예제 1: 자동으로 생성 된 파일 이름으로 키 백업</span><span class="sxs-lookup"><span data-stu-id="1e68b-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'

C:\Users\username\mykeyvault-mykey-1527029447.01191
```

<span data-ttu-id="1e68b-118">이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyKey 이라는 키를 검색 하 고 해당 키의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고 파일 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="1e68b-119">예제 2: 지정 된 파일 이름에 키 백업</span><span class="sxs-lookup"><span data-stu-id="1e68b-119">Example 2: Back up a key to a specified file name</span></span>
```powershell
PS C:\> Backup-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'

C:\Backup.blob
```

<span data-ttu-id="1e68b-120">이 명령은 키 vaultnamed MyKeyVault에서 MyKey 이라는 키를 검색 하 고 해당 키의 백업을. i a t a b 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="1e68b-121">예제 3: 이전에 검색 한 키를 지정 된 파일 이름으로 돌아와서 메시지를 표시 하지 않고 대상 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```powershell
PS C:\> $key = Get-AzKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\> Backup-AzKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force

C:\Backup.blob
```

<span data-ttu-id="1e68b-122">이 명령은 $key 라는 키의 백업을 만듭니다. $Key의 자격 증명 모음에 이름으로 지정 합니다. VaultName 파일에 이미 있는 경우 파일을 자동으로 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="1e68b-123">변수</span><span class="sxs-lookup"><span data-stu-id="1e68b-123">PARAMETERS</span></span>

### <span data-ttu-id="1e68b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e68b-124">-DefaultProfile</span></span>
<span data-ttu-id="1e68b-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1e68b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e68b-126">-Force</span><span class="sxs-lookup"><span data-stu-id="1e68b-126">-Force</span></span>
<span data-ttu-id="1e68b-127">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-127">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="1e68b-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1e68b-128">-InputObject</span></span>
<span data-ttu-id="1e68b-129">검색할 키 번들로, 검색 호출의 출력에서 파이프라인으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="1e68b-130">-이름</span><span class="sxs-lookup"><span data-stu-id="1e68b-130">-Name</span></span>
<span data-ttu-id="1e68b-131">백업할 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e68b-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="1e68b-132">-OutputFile</span></span>
<span data-ttu-id="1e68b-133">백업 blob이 저장 된 출력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="1e68b-134">이 매개 변수를 지정 하지 않으면이 cmdlet은 파일 이름을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="1e68b-135">기존 출력 파일의 이름을 지정 하는 경우 작업이 완료 되지 않으며 백업 파일이 이미 존재 한다는 오류 메시지가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="1e68b-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="1e68b-136">-VaultName</span></span>
<span data-ttu-id="1e68b-137">백업할 키를 포함 하는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-137">Specifies the name of the key vault that contains the key to back up.</span></span>

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

### <span data-ttu-id="1e68b-138">-확인</span><span class="sxs-lookup"><span data-stu-id="1e68b-138">-Confirm</span></span>
<span data-ttu-id="1e68b-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e68b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e68b-140">-WhatIf</span></span>
<span data-ttu-id="1e68b-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e68b-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e68b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e68b-143">CommonParameters</span></span>
<span data-ttu-id="1e68b-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e68b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e68b-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e68b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e68b-146">입력</span><span class="sxs-lookup"><span data-stu-id="1e68b-146">INPUTS</span></span>

### <span data-ttu-id="1e68b-147">Microsoft. KeyVault. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="1e68b-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="1e68b-148">출력</span><span class="sxs-lookup"><span data-stu-id="1e68b-148">OUTPUTS</span></span>

### <span data-ttu-id="1e68b-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1e68b-149">System.String</span></span>

## <span data-ttu-id="1e68b-150">상속자</span><span class="sxs-lookup"><span data-stu-id="1e68b-150">NOTES</span></span>

## <span data-ttu-id="1e68b-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e68b-151">RELATED LINKS</span></span>

[<span data-ttu-id="1e68b-152">추가-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e68b-152">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="1e68b-153">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e68b-153">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="1e68b-154">제거-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e68b-154">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="1e68b-155">Restore-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="1e68b-155">Restore-AzKeyVaultKey</span></span>](./Restore-AzKeyVaultKey.md)

