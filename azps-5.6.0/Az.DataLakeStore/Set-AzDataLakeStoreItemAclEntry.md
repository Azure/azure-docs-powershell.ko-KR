---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2577f61476fd5026d75b677e35b994d64f4954e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956176"
---
# <span data-ttu-id="3ed9d-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3ed9d-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="3ed9d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ed9d-102">SYNOPSIS</span></span>
<span data-ttu-id="3ed9d-103">Data Lake Store의 파일 또는 폴더의 ACL에서 항목을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3ed9d-104">구문</span><span class="sxs-lookup"><span data-stu-id="3ed9d-104">SYNTAX</span></span>

### <span data-ttu-id="3ed9d-105">SetByACLObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="3ed9d-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ed9d-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="3ed9d-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3ed9d-107">설명</span><span class="sxs-lookup"><span data-stu-id="3ed9d-107">DESCRIPTION</span></span>
<span data-ttu-id="3ed9d-108">**Set-AzDataLakeStoreItemAclEntry** cmdlet은 Data Lake Store의 파일 또는 폴더의 액세스 제어 목록(ACL)에서 ACE(항목)를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="3ed9d-109">예제</span><span class="sxs-lookup"><span data-stu-id="3ed9d-109">EXAMPLES</span></span>

### <span data-ttu-id="3ed9d-110">예제 1: ACE에 대한 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="3ed9d-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="3ed9d-111">이 명령은 Patti Fuller에 대한 ACE를 모든 권한을 하게 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="3ed9d-112">예제 2: ACE에 대한 사용 권한 수정 재구성</span><span class="sxs-lookup"><span data-stu-id="3ed9d-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="3ed9d-113">예제 3: Acl 개체를 사용하여 ACE에 대한 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="3ed9d-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="3ed9d-114">이 명령은 패티 풀러에 대한 ACE를 재구성하여 루트에 대한 모든 사용 권한과 해당 하위 파일 모두를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="3ed9d-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3ed9d-115">PARAMETERS</span></span>

### <span data-ttu-id="3ed9d-116">-Account</span><span class="sxs-lookup"><span data-stu-id="3ed9d-116">-Account</span></span>
<span data-ttu-id="3ed9d-117">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3ed9d-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="3ed9d-118">-AceType</span></span>
<span data-ttu-id="3ed9d-119">수정할 ACE 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="3ed9d-120">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ed9d-121">사용자</span><span class="sxs-lookup"><span data-stu-id="3ed9d-121">User</span></span> 
- <span data-ttu-id="3ed9d-122">그룹</span><span class="sxs-lookup"><span data-stu-id="3ed9d-122">Group</span></span> 
- <span data-ttu-id="3ed9d-123">마스크</span><span class="sxs-lookup"><span data-stu-id="3ed9d-123">Mask</span></span> 
- <span data-ttu-id="3ed9d-124">기타</span><span class="sxs-lookup"><span data-stu-id="3ed9d-124">Other</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType
Parameter Sets: SetSpecificACE
Aliases:
Accepted values: User, Group, Mask, Other

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed9d-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="3ed9d-125">-Acl</span></span>
<span data-ttu-id="3ed9d-126">수정할 항목이 포함된 ACL 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-126">Specifies the ACL object that contains the entries to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]
Parameter Sets: SetByACLObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed9d-127">-동시성</span><span class="sxs-lookup"><span data-stu-id="3ed9d-127">-Concurrency</span></span>
<span data-ttu-id="3ed9d-128">병렬로 처리된 파일/감독의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="3ed9d-129">선택 사항: 적절한 기본값이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="3ed9d-130">-Default</span><span class="sxs-lookup"><span data-stu-id="3ed9d-130">-Default</span></span>
<span data-ttu-id="3ed9d-131">이 작업은 지정된 ACL에서 기본 ACE를 수정하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed9d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ed9d-132">-DefaultProfile</span></span>
<span data-ttu-id="3ed9d-133">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ed9d-134">-Id</span><span class="sxs-lookup"><span data-stu-id="3ed9d-134">-Id</span></span>
<span data-ttu-id="3ed9d-135">ACE를 수정할 AzureActive Directory 사용자, 그룹 또는 서비스 주체의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SetSpecificACE
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed9d-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3ed9d-136">-PassThru</span></span>
<span data-ttu-id="3ed9d-137">결과 ACL을 반환해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="3ed9d-138">-Path</span><span class="sxs-lookup"><span data-stu-id="3ed9d-138">-Path</span></span>
<span data-ttu-id="3ed9d-139">루트 디렉터리(/)로 시작하여 ACE를 수정할 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3ed9d-140">-권한</span><span class="sxs-lookup"><span data-stu-id="3ed9d-140">-Permissions</span></span>
<span data-ttu-id="3ed9d-141">ACE에 대한 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="3ed9d-142">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="3ed9d-143">없음</span><span class="sxs-lookup"><span data-stu-id="3ed9d-143">None</span></span>
- <span data-ttu-id="3ed9d-144">실행</span><span class="sxs-lookup"><span data-stu-id="3ed9d-144">Execute</span></span>
- <span data-ttu-id="3ed9d-145">쓰기</span><span class="sxs-lookup"><span data-stu-id="3ed9d-145">Write</span></span>
- <span data-ttu-id="3ed9d-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="3ed9d-146">WriteExecute</span></span>
- <span data-ttu-id="3ed9d-147">읽기</span><span class="sxs-lookup"><span data-stu-id="3ed9d-147">Read</span></span>
- <span data-ttu-id="3ed9d-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="3ed9d-148">ReadExecute</span></span>
- <span data-ttu-id="3ed9d-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="3ed9d-149">ReadWrite</span></span>
- <span data-ttu-id="3ed9d-150">모두</span><span class="sxs-lookup"><span data-stu-id="3ed9d-150">All</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission
Parameter Sets: SetSpecificACE
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ed9d-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="3ed9d-151">-Recurse</span></span>
<span data-ttu-id="3ed9d-152">자식 하위디렉터리 및 파일에 다시 수정될 ACL을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="3ed9d-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="3ed9d-153">-ShowProgress</span></span>
<span data-ttu-id="3ed9d-154">통과하면 진행 상태가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-154">If passed then progress status is showed.</span></span> <span data-ttu-id="3ed9d-155">재구성 Acl 수정이 완료된 경우만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="3ed9d-156">-확인</span><span class="sxs-lookup"><span data-stu-id="3ed9d-156">-Confirm</span></span>
<span data-ttu-id="3ed9d-157">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ed9d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ed9d-158">-WhatIf</span></span>
<span data-ttu-id="3ed9d-159">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ed9d-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ed9d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ed9d-161">CommonParameters</span></span>
<span data-ttu-id="3ed9d-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ed9d-163">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3ed9d-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ed9d-164">입력</span><span class="sxs-lookup"><span data-stu-id="3ed9d-164">INPUTS</span></span>

### <span data-ttu-id="3ed9d-165">System.String</span><span class="sxs-lookup"><span data-stu-id="3ed9d-165">System.String</span></span>

### <span data-ttu-id="3ed9d-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="3ed9d-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="3ed9d-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="3ed9d-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="3ed9d-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="3ed9d-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="3ed9d-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="3ed9d-169">System.Guid</span></span>

### <span data-ttu-id="3ed9d-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span><span class="sxs-lookup"><span data-stu-id="3ed9d-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="3ed9d-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3ed9d-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3ed9d-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3ed9d-172">System.Int32</span></span>

## <span data-ttu-id="3ed9d-173">출력</span><span class="sxs-lookup"><span data-stu-id="3ed9d-173">OUTPUTS</span></span>

### <span data-ttu-id="3ed9d-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="3ed9d-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="3ed9d-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3ed9d-175">NOTES</span></span>

## <span data-ttu-id="3ed9d-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ed9d-176">RELATED LINKS</span></span>

[<span data-ttu-id="3ed9d-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="3ed9d-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


