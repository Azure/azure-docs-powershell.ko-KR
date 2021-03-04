---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/backup-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
ms.openlocfilehash: 9f1d18586d0d903f705b3b2be21dd8f864efcf9c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986020"
---
# <span data-ttu-id="0b2ef-101">Backup-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="0b2ef-101">Backup-AzKeyVault</span></span>

## <span data-ttu-id="0b2ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b2ef-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2ef-103">관리되는 HSM을 완전히 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="0b2ef-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b2ef-104">SYNTAX</span></span>

### <span data-ttu-id="0b2ef-105">InteractiveStorageName(기본값)</span><span class="sxs-lookup"><span data-stu-id="0b2ef-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2ef-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="0b2ef-106">InteractiveStorageUri</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2ef-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="0b2ef-107">InputObjectStorageUri</span></span>
```
Backup-AzKeyVault -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2ef-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="0b2ef-108">InputObjectStorageName</span></span>
```
Backup-AzKeyVault -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b2ef-109">설명</span><span class="sxs-lookup"><span data-stu-id="0b2ef-109">DESCRIPTION</span></span>
<span data-ttu-id="0b2ef-110">관리되는 HSM을 저장소 계정에 완전히 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="0b2ef-111">백업을 `Restore-AzKeyVault` 복원하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-111">Use `Restore-AzKeyVault` to restore the backup.</span></span>

## <span data-ttu-id="0b2ef-112">예제</span><span class="sxs-lookup"><span data-stu-id="0b2ef-112">EXAMPLES</span></span>

### <span data-ttu-id="0b2ef-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="0b2ef-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="0b2ef-114">cmdlet은 저장소 컨테이너에 폴더(일반적으로 이름)를 만들고 해당 폴더에 백업을 저장하고 `mhsm-{name}-{timestamp}` 폴더 URI를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="0b2ef-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0b2ef-115">PARAMETERS</span></span>

### <span data-ttu-id="0b2ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2ef-116">-DefaultProfile</span></span>
<span data-ttu-id="0b2ef-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b2ef-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="0b2ef-118">-HsmName</span></span>
<span data-ttu-id="0b2ef-119">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-119">Name of the HSM.</span></span>

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

### <span data-ttu-id="0b2ef-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="0b2ef-120">-HsmObject</span></span>
<span data-ttu-id="0b2ef-121">관리되는 HSM 개체</span><span class="sxs-lookup"><span data-stu-id="0b2ef-121">Managed HSM object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: InputObjectStorageUri, InputObjectStorageName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2ef-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="0b2ef-122">-SasToken</span></span>
<span data-ttu-id="0b2ef-123">저장소 계정을 인증하는 SAS(공유 액세스 서명) 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="0b2ef-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0b2ef-124">-StorageAccountName</span></span>
<span data-ttu-id="0b2ef-125">백업을 저장할 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="0b2ef-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="0b2ef-126">-StorageContainerName</span></span>
<span data-ttu-id="0b2ef-127">백업을 저장할 Blob 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="0b2ef-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="0b2ef-128">-StorageContainerUri</span></span>
<span data-ttu-id="0b2ef-129">백업을 저장할 저장소 컨테이너의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="0b2ef-130">-확인</span><span class="sxs-lookup"><span data-stu-id="0b2ef-130">-Confirm</span></span>
<span data-ttu-id="0b2ef-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b2ef-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2ef-132">-WhatIf</span></span>
<span data-ttu-id="0b2ef-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b2ef-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b2ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2ef-135">CommonParameters</span></span>
<span data-ttu-id="0b2ef-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b2ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2ef-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b2ef-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2ef-138">입력</span><span class="sxs-lookup"><span data-stu-id="0b2ef-138">INPUTS</span></span>

### <span data-ttu-id="0b2ef-139">없음</span><span class="sxs-lookup"><span data-stu-id="0b2ef-139">None</span></span>

## <span data-ttu-id="0b2ef-140">출력</span><span class="sxs-lookup"><span data-stu-id="0b2ef-140">OUTPUTS</span></span>

### <span data-ttu-id="0b2ef-141">System.String</span><span class="sxs-lookup"><span data-stu-id="0b2ef-141">System.String</span></span>

## <span data-ttu-id="0b2ef-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0b2ef-142">NOTES</span></span>

## <span data-ttu-id="0b2ef-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b2ef-143">RELATED LINKS</span></span>
