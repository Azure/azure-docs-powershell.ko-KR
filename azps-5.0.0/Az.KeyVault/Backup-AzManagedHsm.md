---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/backup-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Backup-AzManagedHsm.md
ms.openlocfilehash: 5353adade342b7f73cf60ff6b0befa88f4a3da73
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215320"
---
# <span data-ttu-id="dfa1d-101">Backup-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="dfa1d-101">Backup-AzManagedHsm</span></span>

## <span data-ttu-id="dfa1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfa1d-102">SYNOPSIS</span></span>
<span data-ttu-id="dfa1d-103">관리 되는 HSM을 완벽 하 게 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-103">Fully backup a managed HSM.</span></span>

## <span data-ttu-id="dfa1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dfa1d-104">SYNTAX</span></span>

### <span data-ttu-id="dfa1d-105">InteractiveStorageName (기본값)</span><span class="sxs-lookup"><span data-stu-id="dfa1d-105">InteractiveStorageName (Default)</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageAccountName <String> -StorageContainerName <String>
 -SasToken <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfa1d-106">InteractiveStorageUri</span><span class="sxs-lookup"><span data-stu-id="dfa1d-106">InteractiveStorageUri</span></span>
```
Backup-AzManagedHsm [-Name] <String> -StorageContainerUri <Uri> -SasToken <SecureString>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfa1d-107">InputObjectStorageUri</span><span class="sxs-lookup"><span data-stu-id="dfa1d-107">InputObjectStorageUri</span></span>
```
Backup-AzManagedHsm -StorageContainerUri <Uri> -SasToken <SecureString> -HsmObject <PSManagedHsm>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfa1d-108">InputObjectStorageName</span><span class="sxs-lookup"><span data-stu-id="dfa1d-108">InputObjectStorageName</span></span>
```
Backup-AzManagedHsm -StorageAccountName <String> -StorageContainerName <String> -SasToken <SecureString>
 -HsmObject <PSManagedHsm> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfa1d-109">설명은</span><span class="sxs-lookup"><span data-stu-id="dfa1d-109">DESCRIPTION</span></span>
<span data-ttu-id="dfa1d-110">관리 되는 HSM을 저장소 계정에 완전히 백업 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-110">Fully backup a managed HSM to a storage account.</span></span>
<span data-ttu-id="dfa1d-111">`Restore-AzManagedHsm`백업을 복원 하는 데 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-111">Use `Restore-AzManagedHsm` to restore the backup.</span></span>

## <span data-ttu-id="dfa1d-112">예제의</span><span class="sxs-lookup"><span data-stu-id="dfa1d-112">EXAMPLES</span></span>

### <span data-ttu-id="dfa1d-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="dfa1d-113">Example 1</span></span>
```powershell
PS C:\> $sasToken = ConvertTo-SecureString -AsPlainText -Force "?sv=2019-12-12&ss=bfqt&srt=sco&sp=rwdlacupx&se=2020-10-12T14:42:19Z&st=2020-10-12T06:42:19Z&spr=https&sig=******"

PS C:\> Backup-AzManagedHsm -Name myHsm -StorageContainerUri "https://{accountName}.blob.core.windows.net/{containerName}" -SasToken $sasToken

https://{accountName}.blob.core.windows.net/{containerName}/{backupFolder}
```

<span data-ttu-id="dfa1d-114">Cmdlet은 저장소 컨테이너에 폴더 (일반적으로 이름이 지정 됨)를 만들고 `mhsm-{name}-{timestamp}` 해당 폴더에 백업을 저장 한 다음 폴더 URI를 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-114">The cmdlet will create a folder (typically named `mhsm-{name}-{timestamp}`) in the storage container, store the backup in that folder and output the folder URI.</span></span>

## <span data-ttu-id="dfa1d-115">변수</span><span class="sxs-lookup"><span data-stu-id="dfa1d-115">PARAMETERS</span></span>

### <span data-ttu-id="dfa1d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfa1d-116">-DefaultProfile</span></span>
<span data-ttu-id="dfa1d-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfa1d-118">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="dfa1d-118">-HsmObject</span></span>
<span data-ttu-id="dfa1d-119">관리 HSM 개체</span><span class="sxs-lookup"><span data-stu-id="dfa1d-119">Managed HSM object</span></span>

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

### <span data-ttu-id="dfa1d-120">-이름</span><span class="sxs-lookup"><span data-stu-id="dfa1d-120">-Name</span></span>
<span data-ttu-id="dfa1d-121">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-121">Name of the HSM.</span></span>

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

### <span data-ttu-id="dfa1d-122">-SasToken</span><span class="sxs-lookup"><span data-stu-id="dfa1d-122">-SasToken</span></span>
<span data-ttu-id="dfa1d-123">저장소 계정을 인증 하기 위한 SAS (공유 액세스 서명) 토큰입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-123">The shared access signature (SAS) token to authenticate the storage account.</span></span>

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

### <span data-ttu-id="dfa1d-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="dfa1d-124">-StorageAccountName</span></span>
<span data-ttu-id="dfa1d-125">백업을 저장 하려는 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-125">Name of the storage account where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="dfa1d-126">-StorageContainerName</span><span class="sxs-lookup"><span data-stu-id="dfa1d-126">-StorageContainerName</span></span>
<span data-ttu-id="dfa1d-127">백업이 저장 될 blob 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-127">Name of the blob container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="dfa1d-128">-StorageContainerUri</span><span class="sxs-lookup"><span data-stu-id="dfa1d-128">-StorageContainerUri</span></span>
<span data-ttu-id="dfa1d-129">백업을 저장 하려는 저장소 컨테이너의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-129">URI of the storage container where the backup is going to be stored.</span></span>

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

### <span data-ttu-id="dfa1d-130">-확인</span><span class="sxs-lookup"><span data-stu-id="dfa1d-130">-Confirm</span></span>
<span data-ttu-id="dfa1d-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfa1d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfa1d-132">-WhatIf</span></span>
<span data-ttu-id="dfa1d-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfa1d-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfa1d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfa1d-135">CommonParameters</span></span>
<span data-ttu-id="dfa1d-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfa1d-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dfa1d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfa1d-138">입력</span><span class="sxs-lookup"><span data-stu-id="dfa1d-138">INPUTS</span></span>

### <span data-ttu-id="dfa1d-139">않아야</span><span class="sxs-lookup"><span data-stu-id="dfa1d-139">None</span></span>

## <span data-ttu-id="dfa1d-140">출력</span><span class="sxs-lookup"><span data-stu-id="dfa1d-140">OUTPUTS</span></span>

### <span data-ttu-id="dfa1d-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dfa1d-141">System.String</span></span>

## <span data-ttu-id="dfa1d-142">상속자</span><span class="sxs-lookup"><span data-stu-id="dfa1d-142">NOTES</span></span>

## <span data-ttu-id="dfa1d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dfa1d-143">RELATED LINKS</span></span>
