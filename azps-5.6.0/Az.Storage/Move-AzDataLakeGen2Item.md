---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: 203e7a246c16345631da290645b356392c165bad
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979184"
---
# <span data-ttu-id="84c76-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="84c76-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="84c76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84c76-102">SYNOPSIS</span></span>
<span data-ttu-id="84c76-103">파일 또는 디렉터리를 동일한 Storage 계정의 다른 파일 또는 디렉터리로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="84c76-104">구문</span><span class="sxs-lookup"><span data-stu-id="84c76-104">SYNTAX</span></span>

### <span data-ttu-id="84c76-105">ReceiveManual(기본값)</span><span class="sxs-lookup"><span data-stu-id="84c76-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="84c76-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="84c76-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84c76-107">설명</span><span class="sxs-lookup"><span data-stu-id="84c76-107">DESCRIPTION</span></span>
<span data-ttu-id="84c76-108">**Move-AzDataLakeGen2Item** cmdlet은 파일 또는 디렉터리를 동일한 Storage 계정의 다른 파일 또는 디렉터리로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="84c76-109">이 cmdlet은 저장소 계정에 대해 계층적 네임스페이스를 사용하도록 설정한 경우만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="84c76-110">이러한 종류의 계정은 "-EnableHierarchicalNamespace $true"를 사용하여 "New-AzStorageAccount" cmdlet을 실행하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="84c76-111">예제</span><span class="sxs-lookup"><span data-stu-id="84c76-111">EXAMPLES</span></span>

### <span data-ttu-id="84c76-112">예제 1: 동일한 파일로 접기 이동</span><span class="sxs-lookup"><span data-stu-id="84c76-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="84c76-113">이 명령은 디렉터리 'dir1'을 동일한 Filesystem의 디렉터리 'dir3'로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="84c76-114">예제 2: 프롬프트 없이 동일한 Storage 계정의 다른 파일 시스템으로 파이프라인으로 파일 이동</span><span class="sxs-lookup"><span data-stu-id="84c76-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="84c76-115">이 명령은 'filesystem1'에서 'dir1/file1'을 이동하여 프롬프트 없이 동일한 Storage 계정의 'filesystem2'에 'dir2/file2'를 파일로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="84c76-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="84c76-116">PARAMETERS</span></span>

### <span data-ttu-id="84c76-117">-Context</span><span class="sxs-lookup"><span data-stu-id="84c76-117">-Context</span></span>
<span data-ttu-id="84c76-118">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="84c76-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="84c76-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84c76-119">-DefaultProfile</span></span>
<span data-ttu-id="84c76-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84c76-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="84c76-121">-DestFileSystem</span></span>
<span data-ttu-id="84c76-122">Dest FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="84c76-122">Dest FileSystem name</span></span>

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

### <span data-ttu-id="84c76-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="84c76-123">-DestPath</span></span>
<span data-ttu-id="84c76-124">Dest Blob 경로</span><span class="sxs-lookup"><span data-stu-id="84c76-124">Dest Blob path</span></span>

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

### <span data-ttu-id="84c76-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="84c76-125">-FileSystem</span></span>
<span data-ttu-id="84c76-126">FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="84c76-126">FileSystem name</span></span>

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

### <span data-ttu-id="84c76-127">-Force</span><span class="sxs-lookup"><span data-stu-id="84c76-127">-Force</span></span>
<span data-ttu-id="84c76-128">대상을 강제로 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="84c76-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84c76-129">-InputObject</span></span>
<span data-ttu-id="84c76-130">이동할 Azure Datalake Gen2 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="84c76-131">-Path</span><span class="sxs-lookup"><span data-stu-id="84c76-131">-Path</span></span>
<span data-ttu-id="84c76-132">이동해야 하는 지정된 Filesystem의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="84c76-133">파일 또는 디렉터리 형식의 'directory/file.txt' 또는 'directory1/directory2/' 형식일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="84c76-134">-확인</span><span class="sxs-lookup"><span data-stu-id="84c76-134">-Confirm</span></span>
<span data-ttu-id="84c76-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84c76-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84c76-136">-WhatIf</span></span>
<span data-ttu-id="84c76-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84c76-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84c76-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84c76-139">CommonParameters</span></span>
<span data-ttu-id="84c76-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="84c76-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84c76-141">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="84c76-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84c76-142">입력</span><span class="sxs-lookup"><span data-stu-id="84c76-142">INPUTS</span></span>

### <span data-ttu-id="84c76-143">System.String</span><span class="sxs-lookup"><span data-stu-id="84c76-143">System.String</span></span>

### <span data-ttu-id="84c76-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="84c76-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="84c76-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="84c76-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="84c76-146">출력</span><span class="sxs-lookup"><span data-stu-id="84c76-146">OUTPUTS</span></span>

### <span data-ttu-id="84c76-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="84c76-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="84c76-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="84c76-148">NOTES</span></span>

## <span data-ttu-id="84c76-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84c76-149">RELATED LINKS</span></span>
