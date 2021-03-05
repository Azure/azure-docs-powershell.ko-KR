---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/remove-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: e41b1c01976cdc631d146721a4ee63d61d52afef
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962336"
---
# <span data-ttu-id="0cfbb-101">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0cfbb-101">Remove-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="0cfbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cfbb-102">SYNOPSIS</span></span>
<span data-ttu-id="0cfbb-103">Data Lake Store의 파일 또는 폴더의 ACL에서 항목을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0cfbb-104">구문</span><span class="sxs-lookup"><span data-stu-id="0cfbb-104">SYNTAX</span></span>

### <span data-ttu-id="0cfbb-105">RemoveByACLObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="0cfbb-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cfbb-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="0cfbb-106">RemoveSpecificACE</span></span>
```
Remove-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cfbb-107">설명</span><span class="sxs-lookup"><span data-stu-id="0cfbb-107">DESCRIPTION</span></span>
<span data-ttu-id="0cfbb-108">**Remove-AzDataLakeStoreItemAclEntry** cmdlet은 Data Lake Store의 파일 또는 폴더의 액세스 제어 목록(ACL)에서 ACE(항목)를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-108">The **Remove-AzDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0cfbb-109">예제</span><span class="sxs-lookup"><span data-stu-id="0cfbb-109">EXAMPLES</span></span>

### <span data-ttu-id="0cfbb-110">예제 1: 사용자 항목 제거</span><span class="sxs-lookup"><span data-stu-id="0cfbb-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="0cfbb-111">이 명령은 ContosoADL 계정에서 Patti Fuller에 대한 사용자 ACE를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="0cfbb-112">예제 2: 사용자 항목을 재구성적으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="0cfbb-113">예제 3: Acl 개체를 사용하여 ACE에 대한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="0cfbb-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="0cfbb-114">이 명령은 루트에서 Patti Fuller에 대한 사용자 ACE를 제거하고 계정 ContosoADL에 대한 하위 열 및 파일 모두에서 재구성합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="0cfbb-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0cfbb-115">PARAMETERS</span></span>

### <span data-ttu-id="0cfbb-116">-Account</span><span class="sxs-lookup"><span data-stu-id="0cfbb-116">-Account</span></span>
<span data-ttu-id="0cfbb-117">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0cfbb-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="0cfbb-118">-AceType</span></span>
<span data-ttu-id="0cfbb-119">제거할 ACE 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="0cfbb-120">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0cfbb-121">사용자</span><span class="sxs-lookup"><span data-stu-id="0cfbb-121">User</span></span>
- <span data-ttu-id="0cfbb-122">그룹</span><span class="sxs-lookup"><span data-stu-id="0cfbb-122">Group</span></span>
- <span data-ttu-id="0cfbb-123">마스크</span><span class="sxs-lookup"><span data-stu-id="0cfbb-123">Mask</span></span>
- <span data-ttu-id="0cfbb-124">기타</span><span class="sxs-lookup"><span data-stu-id="0cfbb-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: RemoveSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cfbb-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="0cfbb-125">-Acl</span></span>
<span data-ttu-id="0cfbb-126">제거할 항목이 포함된 ACL 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-126">Specifies the ACL object that contains the entries to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: RemoveByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0cfbb-127">-동시성</span><span class="sxs-lookup"><span data-stu-id="0cfbb-127">-Concurrency</span></span>
<span data-ttu-id="0cfbb-128">병렬로 처리된 파일/감독의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="0cfbb-129">선택 사항: 적절한 기본값이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="0cfbb-130">-Default</span><span class="sxs-lookup"><span data-stu-id="0cfbb-130">-Default</span></span>
<span data-ttu-id="0cfbb-131">이 작업은 지정된 ACL에서 기본 ACE를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cfbb-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cfbb-132">-DefaultProfile</span></span>
<span data-ttu-id="0cfbb-133">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cfbb-134">-Id</span><span class="sxs-lookup"><span data-stu-id="0cfbb-134">-Id</span></span>
<span data-ttu-id="0cfbb-135">ACE를 제거할 AzureActive Directory 사용자, 그룹 또는 서비스 주체의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: RemoveSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0cfbb-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cfbb-136">-PassThru</span></span>
<span data-ttu-id="0cfbb-137">삭제 작업의 결과를 나타내는 부울 응답을 반환해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="0cfbb-138">-Path</span><span class="sxs-lookup"><span data-stu-id="0cfbb-138">-Path</span></span>
<span data-ttu-id="0cfbb-139">루트 디렉터리(/)로 시작하여 ACE를 제거할 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0cfbb-140">-Recurse</span><span class="sxs-lookup"><span data-stu-id="0cfbb-140">-Recurse</span></span>
<span data-ttu-id="0cfbb-141">자식 하위디렉터리 및 파일에 다시 제거될 ACL을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="0cfbb-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="0cfbb-142">-ShowProgress</span></span>
<span data-ttu-id="0cfbb-143">통과하면 진행 상태가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-143">If passed then progress status is showed.</span></span> <span data-ttu-id="0cfbb-144">재구성 Acl 제거가 완료된 경우만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="0cfbb-145">-확인</span><span class="sxs-lookup"><span data-stu-id="0cfbb-145">-Confirm</span></span>
<span data-ttu-id="0cfbb-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cfbb-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cfbb-147">-WhatIf</span></span>
<span data-ttu-id="0cfbb-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cfbb-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cfbb-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cfbb-150">CommonParameters</span></span>
<span data-ttu-id="0cfbb-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cfbb-152">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0cfbb-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cfbb-153">입력</span><span class="sxs-lookup"><span data-stu-id="0cfbb-153">INPUTS</span></span>

### <span data-ttu-id="0cfbb-154">System.String</span><span class="sxs-lookup"><span data-stu-id="0cfbb-154">System.String</span></span>

### <span data-ttu-id="0cfbb-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0cfbb-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="0cfbb-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="0cfbb-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="0cfbb-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="0cfbb-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="0cfbb-158">System.Guid</span><span class="sxs-lookup"><span data-stu-id="0cfbb-158">System.Guid</span></span>

### <span data-ttu-id="0cfbb-159">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="0cfbb-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="0cfbb-160">System.Int32</span><span class="sxs-lookup"><span data-stu-id="0cfbb-160">System.Int32</span></span>

## <span data-ttu-id="0cfbb-161">출력</span><span class="sxs-lookup"><span data-stu-id="0cfbb-161">OUTPUTS</span></span>

### <span data-ttu-id="0cfbb-162">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0cfbb-162">System.Boolean</span></span>

## <span data-ttu-id="0cfbb-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0cfbb-163">NOTES</span></span>

## <span data-ttu-id="0cfbb-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0cfbb-164">RELATED LINKS</span></span>

[<span data-ttu-id="0cfbb-165">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="0cfbb-165">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


