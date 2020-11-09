---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsmkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsmKey.md
ms.openlocfilehash: 9e75b6de483f0103103434518d31b472660f4a70
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304625"
---
# <span data-ttu-id="d1beb-101">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d1beb-101">Backup-AzManagedHsmKey</span></span>

## <span data-ttu-id="d1beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1beb-102">SYNOPSIS</span></span>
<span data-ttu-id="d1beb-103">관리 되는 HSM의 키를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-103">Backs up a key in a managed HSM.</span></span>

## <span data-ttu-id="d1beb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1beb-104">SYNTAX</span></span>

### <span data-ttu-id="d1beb-105">ByKeyName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d1beb-105">ByKeyName (Default)</span></span>
```
Backup-AzManagedHsmKey [-HsmName] <String> [-Name] <String> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1beb-106">ByKey</span><span class="sxs-lookup"><span data-stu-id="d1beb-106">ByKey</span></span>
```
Backup-AzManagedHsmKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-OutputFile] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1beb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d1beb-107">DESCRIPTION</span></span>
<span data-ttu-id="d1beb-108">**AzManagedHsmKey** cmdlet은 관리 되는 HSM을 다운로드 하 여 파일에 저장 하 여 지정 된 키를 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-108">The **Backup-AzManagedHsmKey** cmdlet backs up a specified key in a managed HSM by downloading it and storing it in a file.</span></span>
<span data-ttu-id="d1beb-109">여러 버전의 키가 있는 경우 백업에 모든 버전이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-109">If there are multiple versions of the key, all versions are included in the backup.</span></span>
<span data-ttu-id="d1beb-110">다운로드 된 콘텐츠는 암호화 되어 있으므로 Azure 관리 HSM 외부에서는 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-110">Because the downloaded content is encrypted, it cannot be used outside of Azure Managed HSM.</span></span>
<span data-ttu-id="d1beb-111">백업 된 구독에서 백업한 키를 관리 되는 HSM에 복원할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-111">You can restore a backed-up key to any managed HSM in the subscription that it was backed up from.</span></span>
<span data-ttu-id="d1beb-112">이 cmdlet을 사용 하는 일반적인 이유는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-112">Typical reasons to use this cmdlet are:</span></span> 
- <span data-ttu-id="d1beb-113">관리 되는 HSM에서 실수로 키를 삭제 하는 경우 오프 라인 복사본을 사용할 수 있도록 키 복사본에 대해 에스크로 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-113">You want to escrow a copy of your key, so that you have an offline copy in case you accidentally delete your key in your managed HSM.</span></span>
 
- <span data-ttu-id="d1beb-114">관리 되는 HSM을 사용 하 여 키를 만들고, 이제 배포 된 응용 프로그램의 모든 인스턴스에서 사용할 수 있도록 해당 키를 다른 Azure 지역에 복제 하려고 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-114">You created a key using Managed HSM and now want to clone the key into a different Azure region, so that you can use it from all instances of your distributed application.</span></span>
<span data-ttu-id="d1beb-115">**AzManagedHsmKey** cmdlet을 사용 하 여 키를 암호화 된 형식으로 검색 한 다음 Restore-AzManagedHsmKey cmdlet을 사용 하 고 두 번째 지역에 관리 되는 HSM을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-115">Use the **Backup-AzManagedHsmKey** cmdlet to retrieve the key in encrypted format and then use the Restore-AzManagedHsmKey cmdlet and specify a managed HSM in the second region.</span></span>

## <span data-ttu-id="d1beb-116">예제의</span><span class="sxs-lookup"><span data-stu-id="d1beb-116">EXAMPLES</span></span>

### <span data-ttu-id="d1beb-117">예제 1: 자동으로 생성 된 파일 이름으로 키 백업</span><span class="sxs-lookup"><span data-stu-id="d1beb-117">Example 1: Back up a key with an automatically generated file name</span></span>
```powershell
PS C:\Users\username\> Backup-AzManagedHsmKey -HsmName testmhsm -Name testkey

C:\Users\username\testmhsm-testkey-1602664728.7106073
```

<span data-ttu-id="d1beb-118">이 명령은 testmhsm 이라는 관리 되는 HSM에서 testkey 라는 키를 검색 하 고 해당 키의 백업을 자동으로 이름이 지정 된 파일에 저장 하 고 파일 이름을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-118">This command retrieves the key named testkey from the managed HSM named testmhsm and saves a backup of that key to a file that is automatically named for you, and displays the file name.</span></span>

## <span data-ttu-id="d1beb-119">변수</span><span class="sxs-lookup"><span data-stu-id="d1beb-119">PARAMETERS</span></span>

### <span data-ttu-id="d1beb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1beb-120">-DefaultProfile</span></span>
<span data-ttu-id="d1beb-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1beb-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d1beb-122">-Force</span></span>
<span data-ttu-id="d1beb-123">지정 된 파일 (있는 경우)을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-123">Overwrite the given file if it exists</span></span>

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

### <span data-ttu-id="d1beb-124">-HsmName</span><span class="sxs-lookup"><span data-stu-id="d1beb-124">-HsmName</span></span>
<span data-ttu-id="d1beb-125">HSM 이름.</span><span class="sxs-lookup"><span data-stu-id="d1beb-125">HSM name.</span></span> <span data-ttu-id="d1beb-126">Cmdlet은 이름 및 현재 선택 된 환경에 따라 관리 되는 HSM의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-126">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="d1beb-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1beb-127">-InputObject</span></span>
<span data-ttu-id="d1beb-128">검색할 키 번들로, 검색 호출의 출력에서 파이프라인으로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-128">Key bundle to back up, pipelined in from the output of a retrieval call.</span></span>

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

### <span data-ttu-id="d1beb-129">-이름</span><span class="sxs-lookup"><span data-stu-id="d1beb-129">-Name</span></span>
<span data-ttu-id="d1beb-130">키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-130">Key name.</span></span>
<span data-ttu-id="d1beb-131">Cmdlet은 관리 되는 HSM 이름, 현재 선택 된 환경 및 키 이름에서 키의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-131">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="d1beb-132">-OutputFile</span><span class="sxs-lookup"><span data-stu-id="d1beb-132">-OutputFile</span></span>
<span data-ttu-id="d1beb-133">출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-133">Output file.</span></span>
<span data-ttu-id="d1beb-134">백업 된 키 blob을 저장할 출력 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-134">The output file to store the backed up key blob in.</span></span>
<span data-ttu-id="d1beb-135">표시 되지 않으면 기본 파일 이름이 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-135">If not present, a default filename is chosen.</span></span>

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

### <span data-ttu-id="d1beb-136">-확인</span><span class="sxs-lookup"><span data-stu-id="d1beb-136">-Confirm</span></span>
<span data-ttu-id="d1beb-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1beb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1beb-138">-WhatIf</span></span>
<span data-ttu-id="d1beb-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1beb-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1beb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1beb-141">CommonParameters</span></span>
<span data-ttu-id="d1beb-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1beb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1beb-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d1beb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1beb-144">입력</span><span class="sxs-lookup"><span data-stu-id="d1beb-144">INPUTS</span></span>

### <span data-ttu-id="d1beb-145">Microsoft. KeyVault. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d1beb-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="d1beb-146">출력</span><span class="sxs-lookup"><span data-stu-id="d1beb-146">OUTPUTS</span></span>

### <span data-ttu-id="d1beb-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1beb-147">System.String</span></span>

## <span data-ttu-id="d1beb-148">상속자</span><span class="sxs-lookup"><span data-stu-id="d1beb-148">NOTES</span></span>

## <span data-ttu-id="d1beb-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1beb-149">RELATED LINKS</span></span>

[<span data-ttu-id="d1beb-150">추가-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d1beb-150">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="d1beb-151">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d1beb-151">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="d1beb-152">제거-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d1beb-152">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="d1beb-153">실행 취소-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="d1beb-153">Undo-AzManagedHsmKeyRemoval</span></span>](./Undo-AzManagedHsmKeyRemoval.md)

[<span data-ttu-id="d1beb-154">업데이트-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d1beb-154">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)

[<span data-ttu-id="d1beb-155">Restore-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="d1beb-155">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)