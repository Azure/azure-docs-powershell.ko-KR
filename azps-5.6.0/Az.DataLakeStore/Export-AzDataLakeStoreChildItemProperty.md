---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestorechilditemproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreChildItemProperty.md
ms.openlocfilehash: 0f43c372901dbfd571343584f0ca8479d5b7081e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013664"
---
# <span data-ttu-id="79e28-101">Export-AzDataLakeStoreChildItemProperty</span><span class="sxs-lookup"><span data-stu-id="79e28-101">Export-AzDataLakeStoreChildItemProperty</span></span>

## <span data-ttu-id="79e28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79e28-102">SYNOPSIS</span></span>
<span data-ttu-id="79e28-103">지정된 경로에서 출력 경로로 전체 트리에 대한 속성(디스크 사용량 및 Acl)을 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-103">Exports the properties (Disk usage and Acl) for the entire tree from the specified path to a output path</span></span>

## <span data-ttu-id="79e28-104">구문</span><span class="sxs-lookup"><span data-stu-id="79e28-104">SYNTAX</span></span>

### <span data-ttu-id="79e28-105">GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="79e28-105">GetDiskUsage</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79e28-106">GetAllProperties</span><span class="sxs-lookup"><span data-stu-id="79e28-106">GetAllProperties</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>]
 [-GetDiskUsage] [-GetAcl] [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79e28-107">GetAclDump</span><span class="sxs-lookup"><span data-stu-id="79e28-107">GetAclDump</span></span>
```
Export-AzDataLakeStoreChildItemProperty [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-OutputPath] <String> [-SaveToAdl] [-IncludeFile] [-MaximumDepth <Int32>] [-Concurrency <Int32>] [-GetAcl]
 [-HideConsistentAcl] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79e28-108">설명</span><span class="sxs-lookup"><span data-stu-id="79e28-108">DESCRIPTION</span></span>
<span data-ttu-id="79e28-109">**Export-AzDataLakeStoreChildItemProperty는** 주어진 디렉터리에 대한 ADLS 공간 사용량 또는/및 ACL 사용량을 보고하는 데 사용하며 하위 디렉터리 및 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-109">The **Export-AzDataLakeStoreChildItemProperty** is used to report the ADLS space usage or/and ACL usage for the given directory and it's sub directories and files.</span></span>

## <span data-ttu-id="79e28-110">예제</span><span class="sxs-lookup"><span data-stu-id="79e28-110">EXAMPLES</span></span>

### <span data-ttu-id="79e28-111">예제 1: 모든 하위 디렉터리 및 파일에 대한 디스크 사용량 및 ACL 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-111">Example 1: Get the disk usage and ACL usage for all subdirectories and files</span></span>
```
PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -GetDiskUsage -IncludeFile
```

<span data-ttu-id="79e28-112">/a 아래에서 모든 하위 디렉터리 및 파일에 대한 디스크 사용량 및 ACL 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-112">Get the disk usage and ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="79e28-113">IncludeFile을 사용하면 파일에 대한 사용량이 보고됩니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-113">IncludeFile ensures the usage is reported for files also</span></span>

### <span data-ttu-id="79e28-114">예제 2: 일관된 ACL이 숨겨져 있는 모든 하위 및 파일에 대한 ACL 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-114">Example 2: Get the ACL usage for all subdirectories and files with the consistent ACL hidden</span></span>
```
PS C:\> $fullAcl="user:contoso-userid:--x|user::rwx|other::---|group::rwx"
PS C:\> $newFullAcl = $fullAcl.Split("{|}");
PS C:\> Set-AzDataLakeStoreItemAcl -Account ContosoADL -Path /a -Acl $newFullAcl -Recurse -Debug

PS C:\> Export-AzDataLakeStoreChildItemProperty -Account ContosoADL -Path /a -OutputPath "C:\Users\contoso\Desktop\DumpFile.txt" -GetAcl -HideConsistentAcl -IncludeFile
```

<span data-ttu-id="79e28-115">/a 아래에서 모든 하위 및 파일에 대한 ACL 사용량을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-115">Get the ACL usage for all subdirectories and files under /a.</span></span> <span data-ttu-id="79e28-116">IncludeFile은 파일에 대한 사용량도 보고되도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-116">IncludeFile ensures the usage is reported for files also.</span></span> <span data-ttu-id="79e28-117">이 경우 HideconsistentAcl은 모든 자식이 /a와 동일한 acl을 포함하기 때문에 자식이 아닌 /a의 Acl을 보여 주게됩니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-117">HideconsistentAcl in this case will show the Acl of /a, not it's children since all of the children has same acl as /a.</span></span> <span data-ttu-id="79e28-118">이 플래그는 모든 acls가 루트와 같을 경우 하위트리의 acl 출력을 생략합니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-118">This flag skips the acl output of subtree if all it's acls are same as the root.</span></span>

## <span data-ttu-id="79e28-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="79e28-119">PARAMETERS</span></span>

### <span data-ttu-id="79e28-120">-Account</span><span class="sxs-lookup"><span data-stu-id="79e28-120">-Account</span></span>
<span data-ttu-id="79e28-121">Data Lake Store 계정에서 파일계산 작업을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-121">The Data Lake Store account to execute the filesystem operation in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e28-122">-동시성</span><span class="sxs-lookup"><span data-stu-id="79e28-122">-Concurrency</span></span>
<span data-ttu-id="79e28-123">병렬로 처리된 파일/감독의 수를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-123">Indicates the number of files/directories processed in parallel.</span></span>
<span data-ttu-id="79e28-124">기본값은 시스템 사양에 따라 최상의 노력으로 계산됩니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-124">Default will be computed as a best effort based on system specification.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e28-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79e28-125">-DefaultProfile</span></span>
<span data-ttu-id="79e28-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79e28-127">-GetAcl</span><span class="sxs-lookup"><span data-stu-id="79e28-127">-GetAcl</span></span>
<span data-ttu-id="79e28-128">루트 경로에서 시작하여 acl을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-128">Retrieves the acl starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e28-129">-GetDiskUsage</span><span class="sxs-lookup"><span data-stu-id="79e28-129">-GetDiskUsage</span></span>
<span data-ttu-id="79e28-130">루트 경로에서 시작하여 디스크 사용량을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-130">Retrieves the disk usage starting from the root path</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetDiskUsage, GetAllProperties
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e28-131">-HideConsistentAcl</span><span class="sxs-lookup"><span data-stu-id="79e28-131">-HideConsistentAcl</span></span>
<span data-ttu-id="79e28-132">전체 하위트리에서 ACL이 동일한 경우 디렉터리 하위트리를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-132">Do not show directory subtree if the ACLs are the same throughout the entire subtree.</span></span> <span data-ttu-id="79e28-133">이렇게 하면 ACL이 다른 경로만 쉽게 볼 수 있습니다. 예를 들어 /a/b 아래 모든 파일 및 폴더가 동일할 경우 하위treeunder /a/b를 표시하지 않고 일관된 ACL 열에 'True'가 포함된 출력 /a/b만 설정되지 않습니다. IncludeFiles가 설정되지 않은 경우 파일에 대한 acl을 검색하지 않고 일관된 Acl을 찾을 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-133">This makes it easier to see only the paths up to which the ACLs differ.For example if all files and folders under /a/b are the same, do not show the subtreeunder /a/b, and just output /a/b with 'True' in the Consistent ACL columnCannot be set if IncludeFiles is not set, because consistent Acl cannot be determined without retrieving acls for the files.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetAllProperties, GetAclDump
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e28-134">-IncludeFile</span><span class="sxs-lookup"><span data-stu-id="79e28-134">-IncludeFile</span></span>
<span data-ttu-id="79e28-135">파일 수준에서 통계 표시(기본적으로 디렉터리 수준 정보만 표시)</span><span class="sxs-lookup"><span data-stu-id="79e28-135">Show stats at file level (default is to show directory-level info only)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e28-136">-MaximumDepth</span><span class="sxs-lookup"><span data-stu-id="79e28-136">-MaximumDepth</span></span>
<span data-ttu-id="79e28-137">디스크 사용량 또는 acl이 표시될 때까지 루트 디렉터리의 최대 깊이</span><span class="sxs-lookup"><span data-stu-id="79e28-137">Maximum depth from the root directory till which disk usage or acl is displayed</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e28-138">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="79e28-138">-OutputPath</span></span>
<span data-ttu-id="79e28-139">출력 파일에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-139">Path to output file.</span></span> <span data-ttu-id="79e28-140">로컬 경로 또는 Adl 경로일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-140">Can be a Local path or Adl Path.</span></span> <span data-ttu-id="79e28-141">기본적으로 로컬입니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-141">By default it is local.</span></span> <span data-ttu-id="79e28-142">SaveToAdl을 지정한 경우 동일한 계정의 ADL 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-142">If SaveToAdl is specified then it is an ADL path in the same account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e28-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79e28-143">-PassThru</span></span>
<span data-ttu-id="79e28-144">삭제 작업의 결과를 나타내는 부울 응답을 반환해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-144">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e28-145">-Path</span><span class="sxs-lookup"><span data-stu-id="79e28-145">-Path</span></span>
<span data-ttu-id="79e28-146">검색해야 하는 지정된 Data Lake 계정의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-146">The path in the specified Data Lake account that should be retrieve.</span></span>
<span data-ttu-id="79e28-147">파일 또는 폴더 형식 '/folder/file.txt'일 수 있습니다. 여기서 DNS 다음의 첫 번째 '/'는 파일 시스템의 루트를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-147">Can be a file or folder In the format '/folder/file.txt', where the first '/' after the DNS indicates the root of the file system.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e28-148">-SaveToAdl</span><span class="sxs-lookup"><span data-stu-id="79e28-148">-SaveToAdl</span></span>
<span data-ttu-id="79e28-149">통과하면 덤프 파일을 ADL에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-149">If passed then saves the dump file to ADL.</span></span>
<span data-ttu-id="79e28-150">이 경우 DumpFile wil은 ADL 경로가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-150">The DumpFile wil be a ADL path in that case</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79e28-151">-확인</span><span class="sxs-lookup"><span data-stu-id="79e28-151">-Confirm</span></span>
<span data-ttu-id="79e28-152">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79e28-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79e28-153">-WhatIf</span></span>
<span data-ttu-id="79e28-154">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79e28-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79e28-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79e28-156">CommonParameters</span></span>
<span data-ttu-id="79e28-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="79e28-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79e28-158">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="79e28-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79e28-159">입력</span><span class="sxs-lookup"><span data-stu-id="79e28-159">INPUTS</span></span>

### <span data-ttu-id="79e28-160">System.String</span><span class="sxs-lookup"><span data-stu-id="79e28-160">System.String</span></span>

### <span data-ttu-id="79e28-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="79e28-161">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="79e28-162">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="79e28-162">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="79e28-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="79e28-163">System.Int32</span></span>

## <span data-ttu-id="79e28-164">출력</span><span class="sxs-lookup"><span data-stu-id="79e28-164">OUTPUTS</span></span>

### <span data-ttu-id="79e28-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79e28-165">System.Boolean</span></span>

## <span data-ttu-id="79e28-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="79e28-166">NOTES</span></span>

## <span data-ttu-id="79e28-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79e28-167">RELATED LINKS</span></span>
