---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324904"
---
# <span data-ttu-id="3990f-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3990f-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="3990f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3990f-102">SYNOPSIS</span></span>
<span data-ttu-id="3990f-103">파일 또는 디렉터리를 동일한 Storage 계정의 다른 파일 또는 디렉터리로 이동</span><span class="sxs-lookup"><span data-stu-id="3990f-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="3990f-104">구문</span><span class="sxs-lookup"><span data-stu-id="3990f-104">SYNTAX</span></span>

### <span data-ttu-id="3990f-105">ReceiveManual(기본값)</span><span class="sxs-lookup"><span data-stu-id="3990f-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3990f-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="3990f-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3990f-107">설명</span><span class="sxs-lookup"><span data-stu-id="3990f-107">DESCRIPTION</span></span>
<span data-ttu-id="3990f-108">**Move-AzDataLakeGen2Item** cmdlet은 파일 또는 디렉터리를 동일한 Storage 계정의 다른 파일 또는 디렉터리로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="3990f-109">이 cmdlet은 저장소 계정에 대해 계층적 네임스페이스를 사용하도록 설정한 경우만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="3990f-110">"-EnableHierarchicalNamespace $true"를 사용하여 "New-AzStorageAccount" cmdlet을 실행하여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="3990f-111">예제</span><span class="sxs-lookup"><span data-stu-id="3990f-111">EXAMPLES</span></span>

### <span data-ttu-id="3990f-112">예제 1: 동일한 파일에서 접기 이동</span><span class="sxs-lookup"><span data-stu-id="3990f-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="3990f-113">이 명령은 디렉터리 'dir1'을 동일한 파일 파일의 디렉터리 'dir3'로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="3990f-114">예제 2: 파이프라인을 통해 동일한 Storage 계정의 다른 파일 시스템으로 프롬프트 없이 파일 이동</span><span class="sxs-lookup"><span data-stu-id="3990f-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="3990f-115">이 명령은 'filesystem1'의 'dir1/file1' 파일을 프롬프트 없이 동일한 Storage 계정의 'filesystem2'에 있는 'dir2/file2' 파일로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="3990f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3990f-116">PARAMETERS</span></span>

### <span data-ttu-id="3990f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="3990f-117">-Context</span></span>
<span data-ttu-id="3990f-118">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="3990f-118">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3990f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3990f-119">-DefaultProfile</span></span>
<span data-ttu-id="3990f-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3990f-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="3990f-121">-DestFileSystem</span></span>
<span data-ttu-id="3990f-122">Dest FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="3990f-122">Dest FileSystem name</span></span>

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

### <span data-ttu-id="3990f-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="3990f-123">-DestPath</span></span>
<span data-ttu-id="3990f-124">Blob 경로 Dest</span><span class="sxs-lookup"><span data-stu-id="3990f-124">Dest Blob path</span></span>

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

### <span data-ttu-id="3990f-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="3990f-125">-FileSystem</span></span>
<span data-ttu-id="3990f-126">FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="3990f-126">FileSystem name</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3990f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3990f-127">-Force</span></span>
<span data-ttu-id="3990f-128">대상 쓰기를 강제로 하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="3990f-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3990f-129">-InputObject</span></span>
<span data-ttu-id="3990f-130">이동할 Azure Datalake Gen2 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-130">Azure Datalake Gen2 Item Object to move from.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item
Parameter Sets: ItemPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3990f-131">-Path</span><span class="sxs-lookup"><span data-stu-id="3990f-131">-Path</span></span>
<span data-ttu-id="3990f-132">이동해야 하는 지정된 파일 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="3990f-133">'directory/file.txt' 또는 'directory1/directory2/' 형식의 파일 또는 디렉터리일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3990f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3990f-134">-Confirm</span></span>
<span data-ttu-id="3990f-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3990f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3990f-136">-WhatIf</span></span>
<span data-ttu-id="3990f-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3990f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3990f-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3990f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3990f-139">CommonParameters</span></span>
<span data-ttu-id="3990f-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3990f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3990f-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3990f-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3990f-142">입력</span><span class="sxs-lookup"><span data-stu-id="3990f-142">INPUTS</span></span>

### <span data-ttu-id="3990f-143">System.String</span><span class="sxs-lookup"><span data-stu-id="3990f-143">System.String</span></span>

### <span data-ttu-id="3990f-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3990f-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="3990f-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3990f-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3990f-146">출력</span><span class="sxs-lookup"><span data-stu-id="3990f-146">OUTPUTS</span></span>

### <span data-ttu-id="3990f-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3990f-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="3990f-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3990f-148">NOTES</span></span>

## <span data-ttu-id="3990f-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3990f-149">RELATED LINKS</span></span>
