---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azdatalakegen2item
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzDataLakeGen2Item.md
ms.openlocfilehash: 06bb30dd98c491267675893192f61d4eb61529bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212073"
---
# <span data-ttu-id="57ba1-101">Remove-AzDataLakeGen2Item</span><span class="sxs-lookup"><span data-stu-id="57ba1-101">Remove-AzDataLakeGen2Item</span></span>

## <span data-ttu-id="57ba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="57ba1-103">파일 또는 디렉터리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-103">Remove a file or directory.</span></span>

## <span data-ttu-id="57ba1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57ba1-104">SYNTAX</span></span>

### <span data-ttu-id="57ba1-105">ReceiveManual (기본값)</span><span class="sxs-lookup"><span data-stu-id="57ba1-105">ReceiveManual (Default)</span></span>
```
Remove-AzDataLakeGen2Item [-FileSystem] <String> [-Path] <String> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="57ba1-106">ItemPipeline</span><span class="sxs-lookup"><span data-stu-id="57ba1-106">ItemPipeline</span></span>
```
Remove-AzDataLakeGen2Item -InputObject <AzureDataLakeGen2Item> [-Force] [-AsJob] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="57ba1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="57ba1-107">DESCRIPTION</span></span>
<span data-ttu-id="57ba1-108">**AzDataLakeGen2Item** Cmdlet은 저장소 계정에서 파일 또는 디렉터리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-108">The **Remove-AzDataLakeGen2Item** cmdlet removes a file or directory from a Storage account.</span></span>
<span data-ttu-id="57ba1-109">이 cmdlet은 저장소 계정에 대해 계층적 네임 스페이스를 사용 하는 경우에만 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-109">This cmdlet only works if Hierarchical Namespace is enabled for the Storage account.</span></span> <span data-ttu-id="57ba1-110">"-EnableHierarchicalNamespace $true"를 사용 하 여 "New-AzStorageAccount" cmdlet을 실행 하 여 이러한 종류의 계정을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-110">This kind of account can be created by run "New-AzStorageAccount" cmdlet with "-EnableHierarchicalNamespace $true".</span></span>

## <span data-ttu-id="57ba1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="57ba1-111">EXAMPLES</span></span>

### <span data-ttu-id="57ba1-112">예제 1: 디렉터리 제거</span><span class="sxs-lookup"><span data-stu-id="57ba1-112">Example 1: Removes a directory</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/"
```

<span data-ttu-id="57ba1-113">이 명령은 파일 시스템에서 디렉터리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-113">This command removes a directory from a Filesystem.</span></span>

### <span data-ttu-id="57ba1-114">예제 2: 메시지가 표시 되지 않고 파일 제거</span><span class="sxs-lookup"><span data-stu-id="57ba1-114">Example 2: Removes a file without prompt</span></span>
```
PS C:\>Remove-AzDataLakeGen2tem -FileSystem "filesystem1" -Path "dir1/file1" -Force
```

<span data-ttu-id="57ba1-115">이 명령은 프롬프트 없이 파일 시스템에서 디렉터리를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-115">This command removes a directory from a Filesystem, without prompt.</span></span>

### <span data-ttu-id="57ba1-116">예제 3: 파이프라인을 사용 하 여 Filesystem의 모든 항목 제거</span><span class="sxs-lookup"><span data-stu-id="57ba1-116">Example 3: Remove all items in a Filesystem with pipeline</span></span>
```
PS C:\>Get-AzDataLakeGen2ChildItem -FileSystem "filesystem1" | Remove-AzDataLakeGen2Item -Force
```

<span data-ttu-id="57ba1-117">이 명령은 파이프라인을 사용 하 여 Filesystem의 모든 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-117">This command removes all items in a Filesystem with pipeline.</span></span>

## <span data-ttu-id="57ba1-118">변수</span><span class="sxs-lookup"><span data-stu-id="57ba1-118">PARAMETERS</span></span>

### <span data-ttu-id="57ba1-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="57ba1-119">-AsJob</span></span>
<span data-ttu-id="57ba1-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="57ba1-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="57ba1-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="57ba1-121">-Context</span></span>
<span data-ttu-id="57ba1-122">Azure 저장소 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="57ba1-122">Azure Storage Context Object</span></span>

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

### <span data-ttu-id="57ba1-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57ba1-123">-DefaultProfile</span></span>
<span data-ttu-id="57ba1-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57ba1-125">-FileSystem</span><span class="sxs-lookup"><span data-stu-id="57ba1-125">-FileSystem</span></span>
<span data-ttu-id="57ba1-126">파일 시스템 이름</span><span class="sxs-lookup"><span data-stu-id="57ba1-126">FileSystem name</span></span>

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

### <span data-ttu-id="57ba1-127">-Force</span><span class="sxs-lookup"><span data-stu-id="57ba1-127">-Force</span></span>
<span data-ttu-id="57ba1-128">파일 시스템 및 모든 콘텐츠를 강제로 제거</span><span class="sxs-lookup"><span data-stu-id="57ba1-128">Force to remove the Filesystem and all content in it</span></span>

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

### <span data-ttu-id="57ba1-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57ba1-129">-InputObject</span></span>
<span data-ttu-id="57ba1-130">제거할 Azure Datalake Gen2 Item 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-130">Azure Datalake Gen2 Item Object to remove.</span></span>

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

### <span data-ttu-id="57ba1-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57ba1-131">-PassThru</span></span>
<span data-ttu-id="57ba1-132">지정 된 파일 시스템이 성공적으로 제거 되었는지 여부 반환</span><span class="sxs-lookup"><span data-stu-id="57ba1-132">Return whether the specified Filesystem is successfully removed</span></span>

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

### <span data-ttu-id="57ba1-133">-Path</span><span class="sxs-lookup"><span data-stu-id="57ba1-133">-Path</span></span>
<span data-ttu-id="57ba1-134">지정 된 파일 시스템에서 제거 해야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-134">The path in the specified Filesystem that should be removed.</span></span>
<span data-ttu-id="57ba1-135">' Directory/file.txt ' 또는 ' directory1/directory2/' 형식의 파일 또는 디렉터리만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-135">Can be a file or directory In the format 'directory/file.txt' or 'directory1/directory2/'</span></span>

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

### <span data-ttu-id="57ba1-136">-확인</span><span class="sxs-lookup"><span data-stu-id="57ba1-136">-Confirm</span></span>
<span data-ttu-id="57ba1-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57ba1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57ba1-138">-WhatIf</span></span>
<span data-ttu-id="57ba1-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57ba1-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57ba1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57ba1-141">CommonParameters</span></span>
<span data-ttu-id="57ba1-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57ba1-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57ba1-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57ba1-144">입력</span><span class="sxs-lookup"><span data-stu-id="57ba1-144">INPUTS</span></span>

### <span data-ttu-id="57ba1-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="57ba1-145">System.String</span></span>

### <span data-ttu-id="57ba1-146">WindowsAzure. ResourceModel를 AzureDataLakeGen2Item로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="57ba1-146">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureDataLakeGen2Item</span></span>

### <span data-ttu-id="57ba1-147">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="57ba1-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="57ba1-148">출력</span><span class="sxs-lookup"><span data-stu-id="57ba1-148">OUTPUTS</span></span>

### <span data-ttu-id="57ba1-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="57ba1-149">System.Boolean</span></span>

## <span data-ttu-id="57ba1-150">상속자</span><span class="sxs-lookup"><span data-stu-id="57ba1-150">NOTES</span></span>

## <span data-ttu-id="57ba1-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57ba1-151">RELATED LINKS</span></span>
