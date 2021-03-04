---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 2d3db18c49d29cabb8f6459adcd46a9c0242c02f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981968"
---
# <span data-ttu-id="d8acf-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d8acf-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="d8acf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8acf-102">SYNOPSIS</span></span>
<span data-ttu-id="d8acf-103">파일 또는 디렉터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-103">Remove a file or directory.</span></span>

## <span data-ttu-id="d8acf-104">구문</span><span class="sxs-lookup"><span data-stu-id="d8acf-104">SYNTAX</span></span>

### <span data-ttu-id="d8acf-105">ReceiveManual(기본값)</span><span class="sxs-lookup"><span data-stu-id="d8acf-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8acf-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="d8acf-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8acf-107">설명</span><span class="sxs-lookup"><span data-stu-id="d8acf-107">DESCRIPTION</span></span>
<span data-ttu-id="d8acf-108">**Remove-AzDataLakeGen2Item** cmdlet은 Storage 계정에서 파일 또는 디렉터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="d8acf-109">이 cmdlet은 저장소 계정에 대해 계층적 네임스페이스를 사용하도록 설정한 경우만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="d8acf-110">이러한 종류의 계정은 "-EnableHierarchicalNamespace $true"를 사용하여 "New-AzStorageAccount" cmdlet을 실행하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="d8acf-111">예제</span><span class="sxs-lookup"><span data-stu-id="d8acf-111">EXAMPLES</span></span>

### <span data-ttu-id="d8acf-112">예제 1: 디렉터리 제거</span><span class="sxs-lookup"><span data-stu-id="d8acf-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="d8acf-113">이 명령은 Filesystem에서 디렉터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="d8acf-114">예제 2: 프롬프트 없이 파일 제거</span><span class="sxs-lookup"><span data-stu-id="d8acf-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="d8acf-115">이 명령은 프롬프트 없이 Filesystem에서 디렉터리를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="d8acf-116">예제 3: 파이프라인을 사용하여 Filesystem의 모든 항목 제거</span><span class="sxs-lookup"><span data-stu-id="d8acf-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="d8acf-117">이 명령은 파이프라인이 있는 Filesystem의 모든 항목을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="d8acf-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d8acf-118">PARAMETERS</span></span>

### <span data-ttu-id="d8acf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8acf-119">-AsJob</span></span>
<span data-ttu-id="d8acf-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d8acf-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8acf-121">-Context</span><span class="sxs-lookup"><span data-stu-id="d8acf-121">-Context</span></span>
<span data-ttu-id="d8acf-122">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="d8acf-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="d8acf-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8acf-123">-DefaultProfile</span></span>
<span data-ttu-id="d8acf-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8acf-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="d8acf-125">-FileSystem</span></span>
<span data-ttu-id="d8acf-126">FileSystem 이름</span><span class="sxs-lookup"><span data-stu-id="d8acf-126">FileSystem name</span></span>

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

### <span data-ttu-id="d8acf-127">-Force</span><span class="sxs-lookup"><span data-stu-id="d8acf-127">-Force</span></span>
<span data-ttu-id="d8acf-128">파일 및 해당 콘텐츠의 모든 콘텐츠를 제거하려면 강제로</span><span class="sxs-lookup"><span data-stu-id="d8acf-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="d8acf-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8acf-129">-InputObject</span></span>
<span data-ttu-id="d8acf-130">제거할 Azure Datalake Gen2 항목 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="d8acf-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8acf-131">-PassThru</span></span>
<span data-ttu-id="d8acf-132">지정된 Filesystem이 성공적으로 제거된지 여부를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="d8acf-133">-Path</span><span class="sxs-lookup"><span data-stu-id="d8acf-133">-Path</span></span>
<span data-ttu-id="d8acf-134">제거해야 하는 지정된 Filesystem의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="d8acf-135">파일 또는 디렉터리 형식의 'directory/file.txt' 또는 'directory1/directory2/' 형식일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="d8acf-136">-확인</span><span class="sxs-lookup"><span data-stu-id="d8acf-136">-Confirm</span></span>
<span data-ttu-id="d8acf-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8acf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8acf-138">-WhatIf</span></span>
<span data-ttu-id="d8acf-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8acf-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8acf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8acf-141">CommonParameters</span></span>
<span data-ttu-id="d8acf-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d8acf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8acf-143">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d8acf-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8acf-144">입력</span><span class="sxs-lookup"><span data-stu-id="d8acf-144">INPUTS</span></span>

### <span data-ttu-id="d8acf-145">System.String</span><span class="sxs-lookup"><span data-stu-id="d8acf-145">System.String</span></span>

### <span data-ttu-id="d8acf-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="d8acf-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="d8acf-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d8acf-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d8acf-148">출력</span><span class="sxs-lookup"><span data-stu-id="d8acf-148">OUTPUTS</span></span>

### <span data-ttu-id="d8acf-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8acf-149">System.Boolean</span></span>

## <span data-ttu-id="d8acf-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d8acf-150">NOTES</span></span>

## <span data-ttu-id="d8acf-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8acf-151">RELATED LINKS</span></span>
