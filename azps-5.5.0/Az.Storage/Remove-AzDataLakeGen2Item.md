---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190817"
---
# <span data-ttu-id="3232d-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3232d-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="3232d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3232d-102">SYNOPSIS</span></span>
<span data-ttu-id="3232d-103">파일 또는 디렉터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-103">Remove a file or directory.</span></span>

## <span data-ttu-id="3232d-104">구문</span><span class="sxs-lookup"><span data-stu-id="3232d-104">SYNTAX</span></span>

### <span data-ttu-id="3232d-105">ReceiveManual(기본값)</span><span class="sxs-lookup"><span data-stu-id="3232d-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3232d-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="3232d-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3232d-107">설명</span><span class="sxs-lookup"><span data-stu-id="3232d-107">DESCRIPTION</span></span>
<span data-ttu-id="3232d-108">**Remove-AzDataLakeGen2Item** cmdlet은 Storage 계정에서 파일 또는 디렉터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="3232d-109">이 cmdlet은 저장소 계정에 대해 계층적 네임스페이스를 사용하도록 설정한 경우만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="3232d-110">"-EnableHierarchicalNamespace $true"를 사용하여 "New-AzStorageAccount" cmdlet을 실행하여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="3232d-111">예제</span><span class="sxs-lookup"><span data-stu-id="3232d-111">EXAMPLES</span></span>

### <span data-ttu-id="3232d-112">예제 1: 디렉터리 제거</span><span class="sxs-lookup"><span data-stu-id="3232d-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="3232d-113">이 명령은 파일 컴퓨터에서 디렉터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="3232d-114">예제 2: 프롬프트 없이 파일 제거</span><span class="sxs-lookup"><span data-stu-id="3232d-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="3232d-115">이 명령은 프롬프트 없이 파일 컴퓨터에서 디렉터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="3232d-116">예제 3: 파이프라인이 있는 파일 파일의 모든 항목 제거</span><span class="sxs-lookup"><span data-stu-id="3232d-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="3232d-117">이 명령은 파이프라인이 있는 파일 파일의 모든 항목을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="3232d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3232d-118">PARAMETERS</span></span>

### <span data-ttu-id="3232d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3232d-119">-AsJob</span></span>
<span data-ttu-id="3232d-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3232d-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3232d-121">-Context</span><span class="sxs-lookup"><span data-stu-id="3232d-121">-Context</span></span>
<span data-ttu-id="3232d-122">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="3232d-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="3232d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3232d-123">-DefaultProfile</span></span>
<span data-ttu-id="3232d-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3232d-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="3232d-125">-FileSystem</span></span>
<span data-ttu-id="3232d-126">FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="3232d-126">FileSystem name</span></span>

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

### <span data-ttu-id="3232d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3232d-127">-Force</span></span>
<span data-ttu-id="3232d-128">파일 파일 및 그 안의 모든 콘텐츠를 제거해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="3232d-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3232d-129">-InputObject</span></span>
<span data-ttu-id="3232d-130">제거할 Azure Datalake Gen2 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="3232d-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3232d-131">-PassThru</span></span>
<span data-ttu-id="3232d-132">지정된 파일 파일이 성공적으로 제거될지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="3232d-133">-Path</span><span class="sxs-lookup"><span data-stu-id="3232d-133">-Path</span></span>
<span data-ttu-id="3232d-134">제거해야 하는 지정된 파일 파일의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="3232d-135">'directory/file.txt' 또는 'directory1/directory2/' 형식의 파일 또는 디렉터리일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="3232d-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3232d-136">-Confirm</span></span>
<span data-ttu-id="3232d-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3232d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3232d-138">-WhatIf</span></span>
<span data-ttu-id="3232d-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3232d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3232d-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3232d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3232d-141">CommonParameters</span></span>
<span data-ttu-id="3232d-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3232d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3232d-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3232d-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3232d-144">입력</span><span class="sxs-lookup"><span data-stu-id="3232d-144">INPUTS</span></span>

### <span data-ttu-id="3232d-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3232d-145">System.String</span></span>

### <span data-ttu-id="3232d-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="3232d-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="3232d-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3232d-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3232d-148">출력</span><span class="sxs-lookup"><span data-stu-id="3232d-148">OUTPUTS</span></span>

### <span data-ttu-id="3232d-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3232d-149">System.Boolean</span></span>

## <span data-ttu-id="3232d-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3232d-150">NOTES</span></span>

## <span data-ttu-id="3232d-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3232d-151">RELATED LINKS</span></span>
