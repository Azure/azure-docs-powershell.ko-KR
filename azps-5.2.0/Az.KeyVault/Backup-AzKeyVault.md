---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzKeyVault.md
ms.openlocfilehash: 7e5aa5091376b8c80d71bdeb2bbad7bd8d22c3a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357218"
---
# <span data-ttu-id="38138-101">Backup-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="38138-101">Backup-AzKeyVault</span></span>

## <span data-ttu-id="38138-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38138-102">SYNOPSIS</span></span>
<span data-ttu-id="38138-103">관리되는 HSM을 완전히 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="38138-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="38138-104">구문</span><span class="sxs-lookup"><span data-stu-id="38138-104">SYNTAX</span></span>

### <span data-ttu-id="38138-105">InteractiveStorageName(기본값)</span><span class="sxs-lookup"><span data-stu-id="38138-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38138-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="38138-106">InteractiveStorageUri</span></span>
```
Backup-AzKeyVault [-HsmName] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38138-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="38138-107">InputObjectStorageUri</span></span>
```
Backup-AzKeyVault -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38138-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="38138-108">InputObjectStorageName</span></span>
```
Backup-AzKeyVault -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38138-109">설명</span><span class="sxs-lookup"><span data-stu-id="38138-109">DESCRIPTION</span></span>
<span data-ttu-id="38138-110">저장소 계정에 관리되는 HSM을 완전히 백업합니다.</span><span class="sxs-lookup"><span data-stu-id="38138-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="38138-111">백업을 `Restore-AzKeyVault` 복원하는 데 사용</span><span class="sxs-lookup"><span data-stu-id="38138-111">Use `Restore-AzKeyVault` to restore the backup.</span></span>

## <span data-ttu-id="38138-112">예제</span><span class="sxs-lookup"><span data-stu-id="38138-112">EXAMPLES</span></span>

### <span data-ttu-id="38138-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="38138-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzKeyVault -HsmName myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="38138-114">cmdlet은 저장소 컨테이너에 폴더(일반적으로 이름이 지정)를 만들고, 해당 폴더에 백업을 `mhsm-{name}-{timestamp}` 저장하고, 폴더 URI를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="38138-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="38138-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38138-115">PARAMETERS</span></span>

### <span data-ttu-id="38138-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38138-116">-DefaultProfile</span></span>
<span data-ttu-id="38138-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38138-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38138-118">-HsmName</span><span class="sxs-lookup"><span data-stu-id="38138-118">-HsmName</span></span>
<span data-ttu-id="38138-119">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38138-119">Name of the HSM.</span></span>

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

### <span data-ttu-id="38138-120">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="38138-120">-HsmObject</span></span>
<span data-ttu-id="38138-121">관리되는 HSM 개체</span><span class="sxs-lookup"><span data-stu-id="38138-121">Managed HSM object</span></span>

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

### <span data-ttu-id="38138-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="38138-122">-SasToken</span></span>
<span data-ttu-id="38138-123">저장소 계정을 인증하기 위한 SAS(공유 액세스 서명) 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="38138-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="38138-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="38138-124">-StorageAccountName</span></span>
<span data-ttu-id="38138-125">백업을 저장할 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38138-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="38138-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="38138-126">-StorageContainerName</span></span>
<span data-ttu-id="38138-127">백업을 저장할 Blob 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38138-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="38138-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="38138-128">-StorageContainerUri</span></span>
<span data-ttu-id="38138-129">백업을 저장할 저장소 컨테이너의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="38138-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="38138-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38138-130">-Confirm</span></span>
<span data-ttu-id="38138-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="38138-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38138-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38138-132">-WhatIf</span></span>
<span data-ttu-id="38138-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="38138-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38138-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38138-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38138-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38138-135">CommonParameters</span></span>
<span data-ttu-id="38138-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38138-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38138-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="38138-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38138-138">입력</span><span class="sxs-lookup"><span data-stu-id="38138-138">INPUTS</span></span>

### <span data-ttu-id="38138-139">없음</span><span class="sxs-lookup"><span data-stu-id="38138-139">None</span></span>

## <span data-ttu-id="38138-140">출력</span><span class="sxs-lookup"><span data-stu-id="38138-140">OUTPUTS</span></span>

### <span data-ttu-id="38138-141">System.String</span><span class="sxs-lookup"><span data-stu-id="38138-141">System.String</span></span>

## <span data-ttu-id="38138-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38138-142">NOTES</span></span>

## <span data-ttu-id="38138-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38138-143">RELATED LINKS</span></span>
