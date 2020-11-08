---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/move-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Move-AzDataLakeGen2Item.md
ms.openlocfilehash: b8d46d85d00f00afdfa326b22a759f60af7b5bbe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048594"
---
# <span data-ttu-id="fd27c-101">Move-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="fd27c-101">Move-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="fd27c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd27c-102">SYNOPSIS</span></span>
<span data-ttu-id="fd27c-103">파일 또는 디렉터리를 같은 저장소 계정으로 다른 파일 또는 디렉터리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-103">Move a file or directory to another a file or directory in same Storage account.</span></span>

## <span data-ttu-id="fd27c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd27c-104">SYNTAX</span></span>

### <span data-ttu-id="fd27c-105">ReceiveManual (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd27c-105">ReceiveManual (Default)</span></span>
```
Move-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd27c-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="fd27c-106">ItemPipeline</span></span>
```
Move-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> -DestFileSystem <String> -DestPath <String>
 [-Force] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd27c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fd27c-107">DESCRIPTION</span></span>
<span data-ttu-id="fd27c-108">**AzDataLakeGen2Item** cmdlet은 파일 또는 디렉터리를 같은 저장소 계정에 있는 다른 파일 또는 디렉터리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-108">The **Move-AzDataLakeGen2Item** cmdlet moves a a file or directory to another a file or directory in same Storage account.</span></span>
<span data-ttu-id="fd27c-109">이 cmdlet은 저장소 계정에 대해 계층적 네임 스페이스를 사용 하는 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="fd27c-110">"-EnableHierarchicalNamespace $true"를 사용 하 여 "New-AzStorageAccount" cmdlet을 실행 하 여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="fd27c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fd27c-111">EXAMPLES</span></span>

### <span data-ttu-id="fd27c-112">예제 1: 같은 파일 시스템에서 접기 이동</span><span class="sxs-lookup"><span data-stu-id="fd27c-112">Example 1: Move a fold in same Filesystem</span></span>
```
PS C:\> Move-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/" -DestFileSystem "filesystem1" -DestPath "dir3/"

   FileSystem Name: filesystem1

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir3                 True                         2020-03-13 13:07:34Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="fd27c-113">이 명령은 ' dir1 ' 디렉터리를 같은 파일 시스템의 ' dir3 ' 디렉터리로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-113">This command move directory 'dir1' to directory 'dir3' in the same Filesystem.</span></span>

### <span data-ttu-id="fd27c-114">예제 2: 파이프라인을 통해 파일을 메시지를 표시 하지 않고 같은 저장소 계정에 있는 다른 Filesystem으로 이동</span><span class="sxs-lookup"><span data-stu-id="fd27c-114">Example 2: Move a file by pipeline, to another Filesystem in the same Storage account without prompt</span></span>
```
PS C:\> Get-AzDataLakeGen2Item -FileSystem "filesystem1" -Path "dir1/file1" | Move-AzDataLakeGen2Item -DestFileSystem "filesystem2" -DestPath "dir2/file2" -Force

   FileSystem Name: filesystem2

Path                 IsDirectory  Length          LastModified         Permissions  Owner                Group               
----                 -----------  ------          ------------         -----------  -----                -----               
dir2/file2           False        1024            2020-03-23 09:57:33Z rwxrw-rw-    $superuser           $superuser
```

<span data-ttu-id="fd27c-115">이 명령은 프롬프트를 표시 하지 않고 같은 저장소 계정으로 ' filesystem1 '의 ' dir1/file1 ' 파일을 ' filesystem2 '의 파일 ' dir2/file2 '로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-115">This command move file 'dir1/file1' in 'filesystem1' to file 'dir2/file2' in 'filesystem2' in the same Storage account without prompt.</span></span>

## <span data-ttu-id="fd27c-116">변수</span><span class="sxs-lookup"><span data-stu-id="fd27c-116">PARAMETERS</span></span>

### <span data-ttu-id="fd27c-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="fd27c-117">-Context</span></span>
<span data-ttu-id="fd27c-118">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="fd27c-118">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="fd27c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd27c-119">-DefaultProfile</span></span>
<span data-ttu-id="fd27c-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fd27c-121">-DestFileSystem</span><span class="sxs-lookup"><span data-stu-id="fd27c-121">-DestFileSystem</span></span>
<span data-ttu-id="fd27c-122">대상 파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="fd27c-122">Dest FileSystem name</span></span>

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

### <span data-ttu-id="fd27c-123">-DestPath</span><span class="sxs-lookup"><span data-stu-id="fd27c-123">-DestPath</span></span>
<span data-ttu-id="fd27c-124">대상 Blob 경로</span><span class="sxs-lookup"><span data-stu-id="fd27c-124">Dest Blob path</span></span>

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

### <span data-ttu-id="fd27c-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="fd27c-125">-FileSystem</span></span>
<span data-ttu-id="fd27c-126">파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="fd27c-126">FileSystem name</span></span>

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

### <span data-ttu-id="fd27c-127">-Force</span><span class="sxs-lookup"><span data-stu-id="fd27c-127">-Force</span></span>
<span data-ttu-id="fd27c-128">대상에 강제를 강제로 씁니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-128">Force to over write the destination.</span></span>

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

### <span data-ttu-id="fd27c-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd27c-129">-InputObject</span></span>
<span data-ttu-id="fd27c-130">Azure Datalake Gen2 Item 개체를 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-130">Azure Datalake Gen2 Item Object to move from.</span></span>

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

### <span data-ttu-id="fd27c-131">-Path</span><span class="sxs-lookup"><span data-stu-id="fd27c-131">-Path</span></span>
<span data-ttu-id="fd27c-132">지정 된 파일 시스템에서 이동 해야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-132">The path in the specified Filesystem that should be move from.</span></span>
<span data-ttu-id="fd27c-133">' Directory/file.txt ' 또는 ' directory1/directory2/' 형식의 파일 또는 디렉터리만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-133">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="fd27c-134">-확인</span><span class="sxs-lookup"><span data-stu-id="fd27c-134">-Confirm</span></span>
<span data-ttu-id="fd27c-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd27c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd27c-136">-WhatIf</span></span>
<span data-ttu-id="fd27c-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd27c-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd27c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd27c-139">CommonParameters</span></span>
<span data-ttu-id="fd27c-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd27c-141">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd27c-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd27c-142">입력</span><span class="sxs-lookup"><span data-stu-id="fd27c-142">INPUTS</span></span>

### <span data-ttu-id="fd27c-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fd27c-143">System.String</span></span>

### <span data-ttu-id="fd27c-144">WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-144">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="fd27c-145">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fd27c-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fd27c-146">출력</span><span class="sxs-lookup"><span data-stu-id="fd27c-146">OUTPUTS</span></span>

### <span data-ttu-id="fd27c-147">WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd27c-147">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

## <span data-ttu-id="fd27c-148">상속자</span><span class="sxs-lookup"><span data-stu-id="fd27c-148">NOTES</span></span>

## <span data-ttu-id="fd27c-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd27c-149">RELATED LINKS</span></span>
