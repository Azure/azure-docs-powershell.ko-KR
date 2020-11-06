---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A82392AA-B12B-443E-8704-7CF5A9F8ED58
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/backup-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Backup-AzureKeyVaultKey.md
ms.openlocfilehash: 2eecb6d4bb069b1578b3080c04de4c9df1e42f09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528951"
---
# <span data-ttu-id="136ac-101">Backup-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="136ac-101">Backup-AzureKeyVaultKey</span></span>

## <span data-ttu-id="136ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="136ac-102">SYNOPSIS</span></span>
<span data-ttu-id="136ac-103">키 자격 증명 모음에서 키를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-103">Backs up a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="136ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="136ac-104">SYNTAX</span></span>

### <span data-ttu-id="136ac-105">ByKeyName (기본값)</span><span class="sxs-lookup"><span data-stu-id="136ac-105">ByKeyName (Default)</span></span>
```
Backup-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="136ac-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="136ac-106">ByKey</span></span>
```
Backup-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="136ac-107">설명은</span><span class="sxs-lookup"><span data-stu-id="136ac-107">DESCRIPTION</span></span>
<span data-ttu-id="136ac-108">**AzureKeyVaultKey** cmdlet은 지정 된 키를 다운로드 하 여 파일에 저장 하 여 키 보관소에 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-108">The **Backup-AzureKeyVaultKey** cmdlet backs up a specified key in a key vault by downloading it and storing it in a file.</span></span>
<span data-ttu-id="136ac-109">여러 버전의 키가 있는 경우 백업에 모든 버전이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="136ac-110">다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 키 자격 증명 모음 외부에서 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Key Vault.</span></span>
<span data-ttu-id="136ac-111">백업한 키를 백업 된 구독에 있는 모든 키 보관소에 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-111">You can restore a backed-up key to any key vault in the subscription that it was backed up from.</span></span>

<span data-ttu-id="136ac-112">이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-112">Typical reasons to use this cmdlet are:</span></span> 

- <span data-ttu-id="136ac-113">키 자격 증명 모음에서 실수로 키를 삭제 하는 경우 오프 라인 복사본을 사용할 수 있도록 키 복사본을 에스크로 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your key vault.</span></span>
 
- <span data-ttu-id="136ac-114">키 자격 증명 모음을 사용 하 여 키를 만든 다음 해당 키를 다른 Azure 지역에 복제 하 여 분산 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-114">You created a key using Key Vault and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="136ac-115">**AzureKeyVaultKey** cmdlet을 사용 하 여 키를 암호화 된 형식으로 검색 한 다음 Restore-AzureKeyVaultKey cmdlet을 사용 하 고 두 번째 지역에서 키 자격 증명 모음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-115">Use the **Backup-AzureKeyVaultKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzureKeyVaultKey cmdlet and specify a key vault in the second region.</span></span>

## <span data-ttu-id="136ac-116">예제의</span><span class="sxs-lookup"><span data-stu-id="136ac-116">EXAMPLES</span></span>

### <span data-ttu-id="136ac-117">예제 1: 자동으로 생성 된 파일 이름으로 키 백업</span><span class="sxs-lookup"><span data-stu-id="136ac-117">Example 1: Back up a key with an automatically generated file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
```

<span data-ttu-id="136ac-118">이 명령은 MyKeyVault 이라는 키 자격 증명 모음에서 MyKey 이라는 키를 검색 하 고 해당 키의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고 파일 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-118">This command retrieves the key named MyKey from the key vault named MyKeyVault and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

### <span data-ttu-id="136ac-119">예제 2: 지정 된 파일 이름에 키 백업</span><span class="sxs-lookup"><span data-stu-id="136ac-119">Example 2: Back up a key to a specified file name</span></span>
```
PS C:\>Backup-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey' -OutputFile 'C:\Backup.blob'
```

<span data-ttu-id="136ac-120">이 명령은 키 vaultnamed MyKeyVault에서 MyKey 이라는 키를 검색 하 고 해당 키의 백업을. i a t a b 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-120">This command retrieves the key named MyKey from the key vaultnamed MyKeyVault and saves a backup of that key to a file named Backup.blob.</span></span>

### <span data-ttu-id="136ac-121">예제 3: 이전에 검색 한 키를 지정 된 파일 이름으로 돌아와서 메시지를 표시 하지 않고 대상 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-121">Example 3: Back up a previously retrieved key to a specified file name, overwriting the destination file without prompting.</span></span>
```
PS C:\>$key = Get-AzureKeyVaultKey -VaultName 'MyKeyVault' -Name 'MyKey'
PS C:\>Backup-AzureKeyVaultKey -Key $key -OutputFile 'C:\Backup.blob' -Force
```

<span data-ttu-id="136ac-122">이 명령은 $key 라는 키의 백업을 만듭니다. $Key의 자격 증명 모음에 이름으로 지정 합니다. VaultName 파일에 이미 있는 경우 파일을 자동으로 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-122">This command creates a backup of the key named $key.Name in the vault named $key.VaultName to a file named Backup.blob, silently overwriting the file if it exists already.</span></span>

## <span data-ttu-id="136ac-123">변수</span><span class="sxs-lookup"><span data-stu-id="136ac-123">PARAMETERS</span></span>

### <span data-ttu-id="136ac-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="136ac-124">-DefaultProfile</span></span>
<span data-ttu-id="136ac-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="136ac-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="136ac-126">-Force</span><span class="sxs-lookup"><span data-stu-id="136ac-126">-Force</span></span>
<span data-ttu-id="136ac-127">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-127">Overwrite the given file if it exists</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="136ac-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="136ac-128">-InputObject</span></span>
<span data-ttu-id="136ac-129">검색할 키 번들로, 검색 호출의 출력에서 파이프라인으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-129">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

```yaml
Type: PSKeyVaultKeyIdentityItem
Parameter Sets: ByKey
Aliases: Key

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="136ac-130">-이름</span><span class="sxs-lookup"><span data-stu-id="136ac-130">-Name</span></span>
<span data-ttu-id="136ac-131">백업할 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-131">Specifies the name of the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="136ac-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="136ac-132">-OutputFile</span></span>
<span data-ttu-id="136ac-133">백업 blob이 저장 된 출력 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-133">Specifies the output file in which the backup blob is stored.</span></span>
<span data-ttu-id="136ac-134">이 매개 변수를 지정 하지 않으면이 cmdlet은 파일 이름을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-134">If you do not specify this parameter, this cmdlet generates a file name for you.</span></span>
<span data-ttu-id="136ac-135">기존 출력 파일의 이름을 지정 하는 경우 작업이 완료 되지 않으며 백업 파일이 이미 존재 한다는 오류 메시지가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-135">If you specify the name of an existing output file, the operation will not complete and returns an error message that the backup file already exists.</span></span>

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

### <span data-ttu-id="136ac-136">-VaultName</span><span class="sxs-lookup"><span data-stu-id="136ac-136">-VaultName</span></span>
<span data-ttu-id="136ac-137">백업할 키를 포함 하는 키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-137">Specifies the name of the key vault that contains the key to back up.</span></span>

```yaml
Type: String
Parameter Sets: ByKeyName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="136ac-138">-확인</span><span class="sxs-lookup"><span data-stu-id="136ac-138">-Confirm</span></span>
<span data-ttu-id="136ac-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="136ac-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="136ac-140">-WhatIf</span></span>
<span data-ttu-id="136ac-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="136ac-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="136ac-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="136ac-143">CommonParameters</span></span>
<span data-ttu-id="136ac-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="136ac-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="136ac-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="136ac-146">입력</span><span class="sxs-lookup"><span data-stu-id="136ac-146">INPUTS</span></span>

### <span data-ttu-id="136ac-147">않아야</span><span class="sxs-lookup"><span data-stu-id="136ac-147">None</span></span>
<span data-ttu-id="136ac-148">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="136ac-149">출력</span><span class="sxs-lookup"><span data-stu-id="136ac-149">OUTPUTS</span></span>

### <span data-ttu-id="136ac-150">이름</span><span class="sxs-lookup"><span data-stu-id="136ac-150">String</span></span>
<span data-ttu-id="136ac-151">Cmdlet은 키의 백업이 포함 된 출력 파일의 경로를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="136ac-151">The cmdlet returns the path of the output file containing the backup of the key.</span></span>

## <span data-ttu-id="136ac-152">상속자</span><span class="sxs-lookup"><span data-stu-id="136ac-152">NOTES</span></span>

## <span data-ttu-id="136ac-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="136ac-153">RELATED LINKS</span></span>

[<span data-ttu-id="136ac-154">추가-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="136ac-154">Add-AzureKeyVaultKey</span></span>](./Add-AzureKeyVaultKey.md)

[<span data-ttu-id="136ac-155">Get-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="136ac-155">Get-AzureKeyVaultKey</span></span>](./Get-AzureKeyVaultKey.md)

[<span data-ttu-id="136ac-156">제거-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="136ac-156">Remove-AzureKeyVaultKey</span></span>](./Remove-AzureKeyVaultKey.md)

[<span data-ttu-id="136ac-157">Restore-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="136ac-157">Restore-AzureKeyVaultKey</span></span>](./Restore-AzureKeyVaultKey.md)

