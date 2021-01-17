---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 8b3412acd7513718c8c34e3fc8bb10c5e33f11a8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489072"
---
# <span data-ttu-id="fc709-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="fc709-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="fc709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc709-102">SYNOPSIS</span></span>
<span data-ttu-id="fc709-103">Data Lake Store에서 파일 또는 폴더의 ACL을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fc709-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc709-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc709-105">설명</span><span class="sxs-lookup"><span data-stu-id="fc709-105">DESCRIPTION</span></span>
<span data-ttu-id="fc709-106">**Set-AzDataLakeStoreItemAcl** cmdlet은 Data Lake Store의 파일 또는 폴더의 ACL(액세스 제어 목록)을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fc709-107">예제</span><span class="sxs-lookup"><span data-stu-id="fc709-107">EXAMPLES</span></span>

### <span data-ttu-id="fc709-108">예제 1: 파일 및 폴더에 대한 ACL 설정</span><span class="sxs-lookup"><span data-stu-id="fc709-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="fc709-109">첫 번째 명령은 ContosoADL 계정의 루트 디렉터리에 대한 ACL을 구한 다음 $ACL 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="fc709-110">두 번째 명령은 파일의 ACL을 Test.txt ACL을 $ACL.</span><span class="sxs-lookup"><span data-stu-id="fc709-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="fc709-111">예제 2: 폴더에 대한 ACL 재발 설정</span><span class="sxs-lookup"><span data-stu-id="fc709-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="fc709-112">첫 번째 명령은 ContosoADL 계정의 Folder1 디렉터리에 대한 ACL을 구한 다음, $ACL 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="fc709-113">두 번째 명령은 ACL을 Folder2로 재구성하여 설정하고 하위 $ACL.</span><span class="sxs-lookup"><span data-stu-id="fc709-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="fc709-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc709-114">PARAMETERS</span></span>

### <span data-ttu-id="fc709-115">-Account</span><span class="sxs-lookup"><span data-stu-id="fc709-115">-Account</span></span>
<span data-ttu-id="fc709-116">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="fc709-117">-Acl</span><span class="sxs-lookup"><span data-stu-id="fc709-117">-Acl</span></span>
<span data-ttu-id="fc709-118">파일 또는 폴더에 대한 ACL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-118">Specifies an ACL for a file or a folder.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc709-119">-동시성</span><span class="sxs-lookup"><span data-stu-id="fc709-119">-Concurrency</span></span>
<span data-ttu-id="fc709-120">병렬로 처리된 파일/감독의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="fc709-121">선택 사항: 적절한 기본값이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="fc709-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc709-122">-DefaultProfile</span></span>
<span data-ttu-id="fc709-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc709-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc709-124">-PassThru</span></span>
<span data-ttu-id="fc709-125">결과 ACL이 반환될 것 을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="fc709-126">-Path</span><span class="sxs-lookup"><span data-stu-id="fc709-126">-Path</span></span>
<span data-ttu-id="fc709-127">루트 디렉터리(/)로 시작하는 파일 또는 폴더의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="fc709-128">-Recurse</span><span class="sxs-lookup"><span data-stu-id="fc709-128">-Recurse</span></span>
<span data-ttu-id="fc709-129">자식 하위irectories 및 파일에 재발적으로 설정할 ACL을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="fc709-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="fc709-130">-ShowProgress</span></span>
<span data-ttu-id="fc709-131">전달된 경우 진행 상태가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-131">If passed then progress status is showed.</span></span> <span data-ttu-id="fc709-132">재발 Acl 집합이 완료된 경우만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="fc709-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc709-133">-Confirm</span></span>
<span data-ttu-id="fc709-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc709-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc709-135">-WhatIf</span></span>
<span data-ttu-id="fc709-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fc709-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc709-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc709-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc709-138">CommonParameters</span></span>
<span data-ttu-id="fc709-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc709-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc709-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc709-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc709-141">입력</span><span class="sxs-lookup"><span data-stu-id="fc709-141">INPUTS</span></span>

### <span data-ttu-id="fc709-142">System.String</span><span class="sxs-lookup"><span data-stu-id="fc709-142">System.String</span></span>

### <span data-ttu-id="fc709-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fc709-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="fc709-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="fc709-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="fc709-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fc709-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fc709-146">System.Int32</span><span class="sxs-lookup"><span data-stu-id="fc709-146">System.Int32</span></span>

## <span data-ttu-id="fc709-147">출력</span><span class="sxs-lookup"><span data-stu-id="fc709-147">OUTPUTS</span></span>

### <span data-ttu-id="fc709-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="fc709-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="fc709-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc709-149">NOTES</span></span>

## <span data-ttu-id="fc709-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc709-150">RELATED LINKS</span></span>
