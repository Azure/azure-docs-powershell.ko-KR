---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/restore-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Restore-AzManagedHsm.md
ms.openlocfilehash: 97e5c836d7d6b209d31851264047c6df894d77a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226924"
---
# <span data-ttu-id="390f5-101">Restore-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="390f5-101">Restore-AzManagedHsm</span></span>

## <span data-ttu-id="390f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="390f5-102">SYNOPSIS</span></span>
<span data-ttu-id="390f5-103">백업에서 관리 되는 HSM을 완전히 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-103">Fully restores a managed HSM from backup.</span></span>

## <span data-ttu-id="390f5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="390f5-104">SYNTAX</span></span>

### <span data-ttu-id="390f5-105">InteractiveStorageName (기본값)</span><span class="sxs-lookup"><span data-stu-id="390f5-105">InteractiveStorageName (Default)</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="390f5-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="390f5-106">InteractiveStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] [-Name] <String> -StorageContainerUri <Uri>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="390f5-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="390f5-107">InputObjectStorageUri</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageContainerUri <Uri> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="390f5-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="390f5-108">InputObjectStorageName</span></span>
```
Restore-AzManagedHsm -BackupFolder <String> [-PassThru] -StorageAccountName <String>
 -StorageContainerName <String> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="390f5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="390f5-109">DESCRIPTION</span></span>
<span data-ttu-id="390f5-110">저장소 계정에 저장 된 백업에서 관리 되는 HSM을 완전 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-110">Fully restores a managed HSM from a backup stored in a storage account.</span></span>
<span data-ttu-id="390f5-111">`Backup-AzManagedHsm`백업에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-111">Use `Backup-AzManagedHsm` to backup.</span></span>

## <span data-ttu-id="390f5-112">예제의</span><span class="sxs-lookup"><span data-stu-id="390f5-112">EXAMPLES</span></span>

### <span data-ttu-id="390f5-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="390f5-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"
PS C:\> Restore-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -BackupFolder "mhsm-myHsm-2020101308504935" -SasToken $sasToken
```

<span data-ttu-id="390f5-114">이 예제 2020101308504935에서는 저장소 컨테이너 "https:"///{accountName}. p r o s o t s p//-s p s p s p s p s p s p s p s p s p s p s r r a p s p s p//</span><span class="sxs-lookup"><span data-stu-id="390f5-114">The example restores a backup stored in a folder named "mhsm-myHsm-2020101308504935" of a storage container "https://{accountName}.blob.core.windows.net/{containerName}".</span></span>

## <span data-ttu-id="390f5-115">변수</span><span class="sxs-lookup"><span data-stu-id="390f5-115">PARAMETERS</span></span>

### <span data-ttu-id="390f5-116">-BackupFolder</span><span class="sxs-lookup"><span data-stu-id="390f5-116">-BackupFolder</span></span>
<span data-ttu-id="390f5-117">백업의 폴더 이름 (예: ' mhsm- *-2020101309020403 '). ' 백업본/mhsm--2020101309020403 ' 등으로 중첩 될 수도 있습니다*.</span><span class="sxs-lookup"><span data-stu-id="390f5-117">Folder name of the backup, e.g. 'mhsm- *-2020101309020403'. It can also be nested such as 'backups/mhsm-* -2020101309020403'.</span></span>

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

### <span data-ttu-id="390f5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="390f5-118">-DefaultProfile</span></span>
<span data-ttu-id="390f5-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="390f5-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="390f5-120">-HsmObject</span></span>
<span data-ttu-id="390f5-121">관리 HSM 개체</span><span class="sxs-lookup"><span data-stu-id="390f5-121">Managed HSM object</span></span>

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

### <span data-ttu-id="390f5-122">-이름</span><span class="sxs-lookup"><span data-stu-id="390f5-122">-Name</span></span>
<span data-ttu-id="390f5-123">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-123">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveStorageName, InteractiveStorageUri
Aliases: HsmName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="390f5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="390f5-124">-PassThru</span></span>
<span data-ttu-id="390f5-125">HSM이 복원 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-125">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="390f5-126">-SasToken</span><span class="sxs-lookup"><span data-stu-id="390f5-126">-SasToken</span></span>
<span data-ttu-id="390f5-127">저장소 계정을 인증 하기 위한 SAS (공유 액세스 서명) 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-127">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="390f5-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="390f5-128">-StorageAccountName</span></span>
<span data-ttu-id="390f5-129">백업을 저장 하려는 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-129">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="390f5-130">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="390f5-130">-StorageContainerName</span></span>
<span data-ttu-id="390f5-131">백업이 저장 될 blob 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-131">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="390f5-132">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="390f5-132">-StorageContainerUri</span></span>
<span data-ttu-id="390f5-133">백업을 저장 하려는 저장소 컨테이너의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-133">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="390f5-134">-확인</span><span class="sxs-lookup"><span data-stu-id="390f5-134">-Confirm</span></span>
<span data-ttu-id="390f5-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="390f5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="390f5-136">-WhatIf</span></span>
<span data-ttu-id="390f5-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="390f5-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="390f5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="390f5-139">CommonParameters</span></span>
<span data-ttu-id="390f5-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="390f5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="390f5-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="390f5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="390f5-142">입력</span><span class="sxs-lookup"><span data-stu-id="390f5-142">INPUTS</span></span>

### <span data-ttu-id="390f5-143">않아야</span><span class="sxs-lookup"><span data-stu-id="390f5-143">None</span></span>

## <span data-ttu-id="390f5-144">출력</span><span class="sxs-lookup"><span data-stu-id="390f5-144">OUTPUTS</span></span>

### <span data-ttu-id="390f5-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="390f5-145">System.Boolean</span></span>

## <span data-ttu-id="390f5-146">상속자</span><span class="sxs-lookup"><span data-stu-id="390f5-146">NOTES</span></span>

## <span data-ttu-id="390f5-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="390f5-147">RELATED LINKS</span></span>
