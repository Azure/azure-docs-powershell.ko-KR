---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzKeyVault.md
ms.openlocfilehash: 8be76f6eb5cf56e5f4612a175c067a7647576a4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98354938"
---
# <span data-ttu-id="48eb1-101">Restore-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="48eb1-101">Restore-AzKeyVault</span></span>

## <span data-ttu-id="48eb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48eb1-102">SYNOPSIS</span></span>
<span data-ttu-id="48eb1-103">백업에서 관리되는 HSM을 완전히 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="48eb1-104">구문</span><span class="sxs-lookup"><span data-stu-id="48eb1-104">SYNTAX</span></span>

### <span data-ttu-id="48eb1-105">InteractiveStorageName(기본값)</span><span class="sxs-lookup"><span data-stu-id="48eb1-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] [-HsmName] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48eb1-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="48eb1-106">InteractiveStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] [-HsmName] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48eb1-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="48eb1-107">InputObjectStorageUri</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48eb1-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="48eb1-108">InputObjectStorageName</span></span>
```
Restore-AzKeyVault -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48eb1-109">설명</span><span class="sxs-lookup"><span data-stu-id="48eb1-109">DESCRIPTION</span></span>
<span data-ttu-id="48eb1-110">저장소 계정에 저장된 백업에서 관리되는 HSM을 완전히 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="48eb1-111">백업에 `Backup-AzKeyVault` 사용</span><span class="sxs-lookup"><span data-stu-id="48eb1-111">Use `Backup-AzKeyVault` to backup.</span></span>

## <span data-ttu-id="48eb1-112">예제</span><span class="sxs-lookup"><span data-stu-id="48eb1-112">EXAMPLES</span></span>

### <span data-ttu-id="48eb1-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="48eb1-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="48eb1-114">이 예제에서는 저장소 컨테이너 "https://{accountName}.blob.core.windows.net/{containerName}"의 "mhsm-myHsm-2020101308504935"라는 폴더에 저장된 백업을 복원합니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="48eb1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48eb1-115">PARAMETERS</span></span>

### <span data-ttu-id="48eb1-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="48eb1-116">-BackupFolder</span></span>
<span data-ttu-id="48eb1-117">백업의 폴더 이름(예: 'mhsm-*-2020101309020403') 'backups/mhsm-*-2020101309020403'처럼 중첩될 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-117">Folder name of the backup, e.g. 'mhsm-*-2020101309020403'. It can also be nested such as 'backups/mhsm-*-2020101309020403'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eb1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48eb1-118">-DefaultProfile</span></span>
<span data-ttu-id="48eb1-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48eb1-120">-HsmName</span><span class="sxs-lookup"><span data-stu-id="48eb1-120">-HsmName</span></span>
<span data-ttu-id="48eb1-121">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-121">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eb1-122">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="48eb1-122">-HsmObject</span></span>
<span data-ttu-id="48eb1-123">관리되는 HSM 개체</span><span class="sxs-lookup"><span data-stu-id="48eb1-123">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eb1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48eb1-124">-PassThru</span></span>
<span data-ttu-id="48eb1-125">HSM이 복원되면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="48eb1-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="48eb1-126">-SasToken</span></span>
<span data-ttu-id="48eb1-127">저장소 계정을 인증하기 위한 SAS(공유 액세스 서명) 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eb1-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="48eb1-128">-StorageAccountName</span></span>
<span data-ttu-id="48eb1-129">백업을 저장할 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-129">Name of the storage account where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eb1-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="48eb1-130">-StorageContainerName</span></span>
<span data-ttu-id="48eb1-131">백업을 저장할 Blob 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-131">Name of the blob container where the backup is going to be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eb1-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="48eb1-132">-StorageContainerUri</span></span>
<span data-ttu-id="48eb1-133">백업을 저장할 저장소 컨테이너의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-133">URI of the storage container where the backup is going to be stored.</span></span>

```yaml
Type: System.Uri
Parameter Sets: InteractiveStorageUri, InputObjectStorageUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48eb1-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48eb1-134">-Confirm</span></span>
<span data-ttu-id="48eb1-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48eb1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="48eb1-136">-WhatIf</span></span>
<span data-ttu-id="48eb1-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="48eb1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="48eb1-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48eb1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48eb1-139">CommonParameters</span></span>
<span data-ttu-id="48eb1-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="48eb1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48eb1-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="48eb1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48eb1-142">입력</span><span class="sxs-lookup"><span data-stu-id="48eb1-142">INPUTS</span></span>

### <span data-ttu-id="48eb1-143">없음</span><span class="sxs-lookup"><span data-stu-id="48eb1-143">None</span></span>

## <span data-ttu-id="48eb1-144">출력</span><span class="sxs-lookup"><span data-stu-id="48eb1-144">OUTPUTS</span></span>

### <span data-ttu-id="48eb1-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="48eb1-145">System.Boolean</span></span>

## <span data-ttu-id="48eb1-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="48eb1-146">NOTES</span></span>

## <span data-ttu-id="48eb1-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48eb1-147">RELATED LINKS</span></span>
