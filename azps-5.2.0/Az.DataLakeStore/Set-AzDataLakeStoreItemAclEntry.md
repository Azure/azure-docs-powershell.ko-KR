---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 4f432596e6165989df07187a9383da04f0929a2d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356246"
---
# <span data-ttu-id="822f9-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="822f9-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="822f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="822f9-102">SYNOPSIS</span></span>
<span data-ttu-id="822f9-103">Data Lake Store에서 파일 또는 폴더의 ACL에 있는 항목을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="822f9-104">구문</span><span class="sxs-lookup"><span data-stu-id="822f9-104">SYNTAX</span></span>

### <span data-ttu-id="822f9-105">SetByACLObject(기본값)</span><span class="sxs-lookup"><span data-stu-id="822f9-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="822f9-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="822f9-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="822f9-107">설명</span><span class="sxs-lookup"><span data-stu-id="822f9-107">DESCRIPTION</span></span>
<span data-ttu-id="822f9-108">**Set-AzDataLakeStoreItemAclEntry** cmdlet은 Data Lake Store에 있는 파일 또는 폴더의 ACL(액세스 제어 목록)에서 ACE(항목)를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="822f9-109">예제</span><span class="sxs-lookup"><span data-stu-id="822f9-109">EXAMPLES</span></span>

### <span data-ttu-id="822f9-110">예제 1: ACE에 대한 권한 수정</span><span class="sxs-lookup"><span data-stu-id="822f9-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="822f9-111">이 명령은 모든 사용 권한을 하게 하여 Patti Fuller용 ACE를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="822f9-112">예제 2: 재발적으로 ACE에 대한 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="822f9-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="822f9-113">예제 3: Acl 개체를 사용하여 재발적으로 ACE에 대한 권한 수정</span><span class="sxs-lookup"><span data-stu-id="822f9-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="822f9-114">이 명령은 루트 및 모든 하위irectors 및 파일에 대한 모든 권한을 부여하기 위해 Patti Fuller에 대한 ACE를 재발적으로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="822f9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="822f9-115">PARAMETERS</span></span>

### <span data-ttu-id="822f9-116">-Account</span><span class="sxs-lookup"><span data-stu-id="822f9-116">-Account</span></span>
<span data-ttu-id="822f9-117">Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="822f9-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="822f9-118">-AceType</span></span>
<span data-ttu-id="822f9-119">수정할 ACE의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="822f9-120">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="822f9-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="822f9-121">사용자</span><span class="sxs-lookup"><span data-stu-id="822f9-121">User</span></span> 
- <span data-ttu-id="822f9-122">그룹</span><span class="sxs-lookup"><span data-stu-id="822f9-122">Group</span></span> 
- <span data-ttu-id="822f9-123">마스크</span><span class="sxs-lookup"><span data-stu-id="822f9-123">Mask</span></span> 
- <span data-ttu-id="822f9-124">기타</span><span class="sxs-lookup"><span data-stu-id="822f9-124">Other</span></span>

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

### <span data-ttu-id="822f9-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="822f9-125">-Acl</span></span>
<span data-ttu-id="822f9-126">수정할 항목이 포함된 ACL 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-126">Specifies the ACL object that contains the entries to modify.</span></span>

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

### <span data-ttu-id="822f9-127">-동시성</span><span class="sxs-lookup"><span data-stu-id="822f9-127">-Concurrency</span></span>
<span data-ttu-id="822f9-128">병렬로 처리된 파일/감독의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="822f9-129">선택 사항: 적절한 기본값이 선택됩니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="822f9-130">-Default</span><span class="sxs-lookup"><span data-stu-id="822f9-130">-Default</span></span>
<span data-ttu-id="822f9-131">이 작업이 지정된 ACL에서 기본 ACE를 수정하는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="822f9-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822f9-132">-DefaultProfile</span></span>
<span data-ttu-id="822f9-133">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="822f9-134">-Id</span><span class="sxs-lookup"><span data-stu-id="822f9-134">-Id</span></span>
<span data-ttu-id="822f9-135">ACE를 수정할 AzureActive Directory 사용자, 그룹 또는 서비스 주체의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

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

### <span data-ttu-id="822f9-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="822f9-136">-PassThru</span></span>
<span data-ttu-id="822f9-137">결과 ACL이 반환될 것 을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="822f9-138">-Path</span><span class="sxs-lookup"><span data-stu-id="822f9-138">-Path</span></span>
<span data-ttu-id="822f9-139">루트 디렉터리(/)로 시작하는 ACE를 수정할 항목의 Data Lake Store 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="822f9-140">-Permissions</span><span class="sxs-lookup"><span data-stu-id="822f9-140">-Permissions</span></span>
<span data-ttu-id="822f9-141">ACE에 대한 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="822f9-142">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="822f9-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="822f9-143">없음</span><span class="sxs-lookup"><span data-stu-id="822f9-143">None</span></span>
- <span data-ttu-id="822f9-144">실행</span><span class="sxs-lookup"><span data-stu-id="822f9-144">Execute</span></span>
- <span data-ttu-id="822f9-145">쓰기</span><span class="sxs-lookup"><span data-stu-id="822f9-145">Write</span></span>
- <span data-ttu-id="822f9-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="822f9-146">WriteExecute</span></span>
- <span data-ttu-id="822f9-147">읽기</span><span class="sxs-lookup"><span data-stu-id="822f9-147">Read</span></span>
- <span data-ttu-id="822f9-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="822f9-148">ReadExecute</span></span>
- <span data-ttu-id="822f9-149">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="822f9-149">ReadWrite</span></span>
- <span data-ttu-id="822f9-150">모두</span><span class="sxs-lookup"><span data-stu-id="822f9-150">All</span></span>

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

### <span data-ttu-id="822f9-151">-Recurse</span><span class="sxs-lookup"><span data-stu-id="822f9-151">-Recurse</span></span>
<span data-ttu-id="822f9-152">자식 하위 간접 및 파일에 재발적으로 수정할 ACL을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="822f9-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="822f9-153">-ShowProgress</span></span>
<span data-ttu-id="822f9-154">전달된 경우 진행 상태가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-154">If passed then progress status is showed.</span></span> <span data-ttu-id="822f9-155">재발 Acl 수정이 수행될 때만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="822f9-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="822f9-156">-Confirm</span></span>
<span data-ttu-id="822f9-157">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="822f9-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="822f9-158">-WhatIf</span></span>
<span data-ttu-id="822f9-159">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="822f9-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="822f9-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="822f9-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822f9-161">CommonParameters</span></span>
<span data-ttu-id="822f9-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="822f9-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822f9-163">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="822f9-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822f9-164">입력</span><span class="sxs-lookup"><span data-stu-id="822f9-164">INPUTS</span></span>

### <span data-ttu-id="822f9-165">System.String</span><span class="sxs-lookup"><span data-stu-id="822f9-165">System.String</span></span>

### <span data-ttu-id="822f9-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="822f9-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="822f9-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span><span class="sxs-lookup"><span data-stu-id="822f9-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="822f9-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span><span class="sxs-lookup"><span data-stu-id="822f9-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="822f9-169">System.Guid</span><span class="sxs-lookup"><span data-stu-id="822f9-169">System.Guid</span></span>

### <span data-ttu-id="822f9-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span><span class="sxs-lookup"><span data-stu-id="822f9-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="822f9-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="822f9-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="822f9-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="822f9-172">System.Int32</span></span>

## <span data-ttu-id="822f9-173">출력</span><span class="sxs-lookup"><span data-stu-id="822f9-173">OUTPUTS</span></span>

### <span data-ttu-id="822f9-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="822f9-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="822f9-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="822f9-175">NOTES</span></span>

## <span data-ttu-id="822f9-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="822f9-176">RELATED LINKS</span></span>

[<span data-ttu-id="822f9-177">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="822f9-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


