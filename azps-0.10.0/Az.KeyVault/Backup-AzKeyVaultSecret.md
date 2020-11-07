---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 80AAA327-77C6-4372-9461-FFED5A15E678
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/backup-AzKeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Backup-AzKeyVaultSecret.md
ms.openlocfilehash: b1f26123579589c15ac4eff6b577706270a7e15a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875848"
---
# <span data-ttu-id="b579e-101">Backup-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b579e-101">Backup-AzKeyVaultSecret</span></span>

## <span data-ttu-id="b579e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b579e-102">SYNOPSIS</span></span>
<span data-ttu-id="b579e-103">키 자격 증명 모음에서 비밀을 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-103">Backs up a secret in a key vault.</span></span>

## <span data-ttu-id="b579e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b579e-104">SYNTAX</span></span>

### <span data-ttu-id="b579e-105">BySecretName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b579e-105">BySecretName (Default)</span></span>
```
Backup-AzKeyVaultSecret [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b579e-106">BySecret</span><span class="sxs-lookup"><span data-stu-id="b579e-106">BySecret</span></span>
```
Backup-AzKeyVaultSecret [-Secret] <Secret> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b579e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b579e-107">DESCRIPTION</span></span>
<span data-ttu-id="b579e-108">**AzKeyVaultSecret** cmdlet은 지정 된 비밀을 다운로드 하 고 파일에 저장 하 여 키 보관소에 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-108">The **Backup-AzKeyVaultSecret** cmdlet backs up a specified secret in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="b579e-109">여러 버전의 비밀이 있으면 백업에 모든 버전이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-109">If there are multiple versions of the secret, all versions are included in the backup.</span></span>
<span data-ttu-id="b579e-110">다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="b579e-111">백업한 비밀을 백업 된 서브스크립션의 모든 키 보관소에 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-111">You can restore a backed-up secret to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="b579e-112">이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-112">Typical reasons to use this cmdlet are:</span></span>

- <span data-ttu-id="b579e-113">비밀 정보 복사본을 사용 하 여 사용자의 키 보관소에서 비밀을 실수로 삭제 한 경우 오프 라인 복사본을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-113">You want to escrow a copy of your secret, so that you have an offline copy in case you accidentally delete your secret in your key vault.</span></span>
- <span data-ttu-id="b579e-114">키 자격 증명 모음에 비밀을 추가 했으며, 이제 배포 된 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 비밀을 다른 Azure 지역에 복제 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-114">You added a secret to a key vault and now want to clone the secret into a different Azure region, so that you can use it from all instances of your distributed application.</span></span> <span data-ttu-id="b579e-115">Backup-AzKeyVaultSecret cmdlet을 사용 하 여 암호화 된 형식으로 비밀을 검색 한 다음 Restore-AzKeyVaultSecret cmdlet을 사용 하 여 두 번째 지역에서 키 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-115">Use the Backup-AzKeyVaultSecret cmdlet to retrieve the secret in encrypted format and then use the Restore-AzKeyVaultSecret cmdlet and specify a key vault in the second region.</span></span> <span data-ttu-id="b579e-116">(지역은 동일한 지리에 속해야 합니다.)</span><span class="sxs-lookup"><span data-stu-id="b579e-116">(Note that the regions must belong to the same geography.)</span></span>

## <span data-ttu-id="b579e-117">예제의</span><span class="sxs-lookup"><span data-stu-id="b579e-117">EXAMPLES</span></span>

### <span data-ttu-id="b579e-118">예제 1: 자동으로 생성 된 파일 이름으로 비밀 백업</span><span class="sxs-lookup"><span data-stu-id="b579e-118">Example 1: Back up a secret with an automatically generated file name</span></span>
```
PS C:\>Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
```

<span data-ttu-id="b579e-119">이 명령은 MyKeyVault 이라는 키 보관소에서 MySecret 라는 비밀을 검색 하 고, 해당 비밀의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고 파일 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-119">This command retrieves the secret named MySecret from the key vault named MyKeyVault and saves a backup of that secret to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="b579e-120">예제 2: 지정 된 파일 이름으로 비밀을 백업 하 고 메시지를 표시 하지 않고 기존 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-120">Example 2: Back up a secret to a specified file name, overwriting the existing file without prompting</span></span>
```
PS C:\>Backup-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret' -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="b579e-121">이 명령은 키 vaultnamed MyKeyVault에서 MySecret 라는 비밀을 검색 하 고 해당 비밀의 백업을 blob 라는 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-121">This command retrieves the secret named MySecret from the key vaultnamed MyKeyVault and saves a backup of that secret to a file named Backup.blob.</span></span>

### <span data-ttu-id="b579e-122">예제 3: 이전에 지정한 파일 이름으로 검색 한 비밀 정보 백업</span><span class="sxs-lookup"><span data-stu-id="b579e-122">Example 3: Back up a secret previously retrieved to a specified file name</span></span>
```
PS C:\>$secret = Get-AzKeyVaultSecret -VaultName 'MyKeyVault' -Name 'MySecret'
PS C:\>Backup-AzKeyVaultSecret -Secret $secret -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="b579e-123">이 명령은 $secret 개체의 자격 증명 모음 이름 및 이름을 사용 하 여 암호를 검색 하 고 백업본 이라는 파일에 해당 백업을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-123">This command uses the $secret object's vault name and name to retrieves the secret and saves its backup to a file named Backup.blob.</span></span>

## <span data-ttu-id="b579e-124">변수</span><span class="sxs-lookup"><span data-stu-id="b579e-124">PARAMETERS</span></span>

### <span data-ttu-id="b579e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b579e-125">-DefaultProfile</span></span>
<span data-ttu-id="b579e-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b579e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b579e-127">-Force</span><span class="sxs-lookup"><span data-stu-id="b579e-127">-Force</span></span>
<span data-ttu-id="b579e-128">출력 파일 (있는 경우)을 덮어쓰기 전에 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-128">Prompts you for confirmation before overwriting the output file, if that exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b579e-129">-이름</span><span class="sxs-lookup"><span data-stu-id="b579e-129">-Name</span></span>
<span data-ttu-id="b579e-130">백업할 비밀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-130">Specifies the name of the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b579e-131">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="b579e-131">-OutputFile</span></span>
<span data-ttu-id="b579e-132">백업 blob이 저장 된 출력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-132">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="b579e-133">이 매개 변수를 지정 하지 않으면이 cmdlet은 파일 이름을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-133">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="b579e-134">기존 출력 파일의 이름을 지정 하는 경우 작업이 완료 되지 않으며 백업 파일이 이미 존재 한다는 오류 메시지가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-134">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b579e-135">-비밀</span><span class="sxs-lookup"><span data-stu-id="b579e-135">-Secret</span></span>
<span data-ttu-id="b579e-136">이름 및 자격 증명을 백업 작업에 사용 해야 하는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-136">Specifies the object whose name and vault should be used for the backup operation.</span></span>

```yaml
Type: Secret
Parameter Sets: BySecret
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b579e-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b579e-137">-VaultName</span></span>
<span data-ttu-id="b579e-138">백업할 비밀을 포함 하는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-138">Specifies the name of the key vault that contains the secret to back up.</span></span>

```yaml
Type: String
Parameter Sets: BySecretName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b579e-139">-확인</span><span class="sxs-lookup"><span data-stu-id="b579e-139">-Confirm</span></span>
<span data-ttu-id="b579e-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b579e-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b579e-141">-WhatIf</span></span>
<span data-ttu-id="b579e-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b579e-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b579e-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b579e-144">CommonParameters</span></span>
<span data-ttu-id="b579e-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b579e-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b579e-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b579e-147">입력</span><span class="sxs-lookup"><span data-stu-id="b579e-147">INPUTS</span></span>

### <span data-ttu-id="b579e-148">않아야</span><span class="sxs-lookup"><span data-stu-id="b579e-148">None</span></span>
<span data-ttu-id="b579e-149">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b579e-150">출력</span><span class="sxs-lookup"><span data-stu-id="b579e-150">OUTPUTS</span></span>

### <span data-ttu-id="b579e-151">이름</span><span class="sxs-lookup"><span data-stu-id="b579e-151">String</span></span>
<span data-ttu-id="b579e-152">Cmdlet은 키의 백업이 포함 된 출력 파일의 경로를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579e-152">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="b579e-153">상속자</span><span class="sxs-lookup"><span data-stu-id="b579e-153">NOTES</span></span>

## <span data-ttu-id="b579e-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b579e-154">RELATED LINKS</span></span>

[<span data-ttu-id="b579e-155">Set-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b579e-155">Set-AzKeyVaultSecret</span></span>](./Set-AzKeyVaultSecret.md)

[<span data-ttu-id="b579e-156">Get-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b579e-156">Get-AzKeyVaultSecret</span></span>](./Get-AzKeyVaultSecret.md)

[<span data-ttu-id="b579e-157">제거-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b579e-157">Remove-AzKeyVaultSecret</span></span>](./Remove-AzKeyVaultSecret.md)

[<span data-ttu-id="b579e-158">Restore-AzKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="b579e-158">Restore-AzKeyVaultSecret</span></span>](./Restore-AzKeyVaultSecret.md)

