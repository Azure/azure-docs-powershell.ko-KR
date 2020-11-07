---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: FFB335D4-AE3E-4788-B6FD-9AFC36F52B61
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAcl.md
ms.openlocfilehash: 53cf81c4996a9d77d1452ffd6d5f99c111aecbf1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868494"
---
# <span data-ttu-id="56398-101">Set-AzDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="56398-101">Set-AzDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="56398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56398-102">SYNOPSIS</span></span>
<span data-ttu-id="56398-103">Data Lake Store에서 파일 또는 폴더의 ACL을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56398-103">Modifies the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="56398-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56398-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56398-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56398-105">DESCRIPTION</span></span>
<span data-ttu-id="56398-106">**AzDataLakeStoreItemAcl** Cmdlet은 Data Lake store에서 파일 또는 폴더의 ACL (액세스 제어 목록)을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56398-106">The **Set-AzDataLakeStoreItemAcl** cmdlet modifies the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="56398-107">예제의</span><span class="sxs-lookup"><span data-stu-id="56398-107">EXAMPLES</span></span>

### <span data-ttu-id="56398-108">예제 1: 파일 및 폴더에 대 한 ACL 설정</span><span class="sxs-lookup"><span data-stu-id="56398-108">Example 1: Set the ACL for a file and a folder</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/MyFiles/Test.txt" -Acl $ACL
```

<span data-ttu-id="56398-109">첫 번째 명령은 ContosoADL account의 루트 디렉터리에 대 한 ACL을 가져온 다음이를 $ACL 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="56398-109">The first command gets the ACL for the root directory of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="56398-110">두 번째 명령은 Test.txt 파일의 ACL을 $ACL의 1로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56398-110">The second command sets the ACL for the file Test.txt to the one in $ACL.</span></span>

### <span data-ttu-id="56398-111">예제 2: 폴더에 대 한 ACL을 재귀적으로 설정</span><span class="sxs-lookup"><span data-stu-id="56398-111">Example 2: Set the ACL for folder recursively</span></span>
```
PS C:\>$ACL = Get-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path /Folder1
PS C:\> Set-AzDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/Folder2" -Acl $ACL -Recurse -Concurrency 128
```

<span data-ttu-id="56398-112">첫 번째 명령은 ContosoADL account의 디렉터리 Folder1에 대 한 ACL을 가져온 다음이를 $ACL 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="56398-112">The first command gets the ACL for the directory Folder1 of the ContosoADL account, and then stores it in the $ACL variable.</span></span>
<span data-ttu-id="56398-113">두 번째 명령에서는 ACL을 재귀적으로 Folder2로 설정 하 고 해당 하위 디렉터리와 파일을 $ACL에 있는 항목으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56398-113">The second command sets the ACL recursively to Folder2 and its sub directories and files to the one in $ACL.</span></span>

## <span data-ttu-id="56398-114">변수</span><span class="sxs-lookup"><span data-stu-id="56398-114">PARAMETERS</span></span>

### <span data-ttu-id="56398-115">-계정</span><span class="sxs-lookup"><span data-stu-id="56398-115">-Account</span></span>
<span data-ttu-id="56398-116">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56398-116">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="56398-117">-Acl</span><span class="sxs-lookup"><span data-stu-id="56398-117">-Acl</span></span>
<span data-ttu-id="56398-118">파일 또는 폴더에 대 한 ACL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56398-118">Specifies an ACL for a file or a folder.</span></span>

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

### <span data-ttu-id="56398-119">-동시성</span><span class="sxs-lookup"><span data-stu-id="56398-119">-Concurrency</span></span>
<span data-ttu-id="56398-120">병렬로 처리 된 파일/디렉터리 수입니다.</span><span class="sxs-lookup"><span data-stu-id="56398-120">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="56398-121">선택 사항: 적당 한 기본값이 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56398-121">Optional: a reasonable default will be selected.</span></span>

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

### <span data-ttu-id="56398-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56398-122">-DefaultProfile</span></span>
<span data-ttu-id="56398-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56398-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56398-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56398-124">-PassThru</span></span>
<span data-ttu-id="56398-125">결과 ACL을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56398-125">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="56398-126">-Path</span><span class="sxs-lookup"><span data-stu-id="56398-126">-Path</span></span>
<span data-ttu-id="56398-127">루트 디렉터리 (/)로 시작 하는 파일 또는 폴더의 Data Lake Store 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56398-127">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="56398-128">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="56398-128">-Recurse</span></span>
<span data-ttu-id="56398-129">하위 디렉터리 및 파일에 재귀적으로 설정할 ACL을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56398-129">Indicates the ACL to be set recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="56398-130">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="56398-130">-ShowProgress</span></span>
<span data-ttu-id="56398-131">전달 되 면 진행 상태를 보여 주는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="56398-131">If passed then progress status is showed.</span></span> <span data-ttu-id="56398-132">재귀 Acl 집합이 완료 된 경우에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56398-132">Only applicable when recursive Acl set is done.</span></span>

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

### <span data-ttu-id="56398-133">-확인</span><span class="sxs-lookup"><span data-stu-id="56398-133">-Confirm</span></span>
<span data-ttu-id="56398-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56398-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56398-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56398-135">-WhatIf</span></span>
<span data-ttu-id="56398-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56398-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56398-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56398-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56398-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56398-138">CommonParameters</span></span>
<span data-ttu-id="56398-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56398-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56398-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56398-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56398-141">입력</span><span class="sxs-lookup"><span data-stu-id="56398-141">INPUTS</span></span>

### <span data-ttu-id="56398-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56398-142">System.String</span></span>

### <span data-ttu-id="56398-143">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="56398-143">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="56398-144">DataLakeStore [] DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="56398-144">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="56398-145">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="56398-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="56398-146">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="56398-146">System.Int32</span></span>

## <span data-ttu-id="56398-147">출력</span><span class="sxs-lookup"><span data-stu-id="56398-147">OUTPUTS</span></span>

### <span data-ttu-id="56398-148">DataLakeStore. DataLakeStoreItemAce/.</span><span class="sxs-lookup"><span data-stu-id="56398-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="56398-149">상속자</span><span class="sxs-lookup"><span data-stu-id="56398-149">NOTES</span></span>

## <span data-ttu-id="56398-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56398-150">RELATED LINKS</span></span>
