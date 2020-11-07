---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0671D833-8B3A-4480-A576-92F1A9E8CE92
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2c82c2c3f47a1dc0f0220faa8654a7281081c73b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868489"
---
# <span data-ttu-id="883a5-101">Set-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="883a5-101">Set-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="883a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="883a5-102">SYNOPSIS</span></span>
<span data-ttu-id="883a5-103">Data Lake Store에서 파일 또는 폴더의 ACL에 있는 항목을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-103">Modifies an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="883a5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="883a5-104">SYNTAX</span></span>

### <span data-ttu-id="883a5-105">Setbyac(기본값)</span><span class="sxs-lookup"><span data-stu-id="883a5-105">SetByACLObject (Default)</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="883a5-106">SetSpecificACE</span><span class="sxs-lookup"><span data-stu-id="883a5-106">SetSpecificACE</span></span>
```
Set-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance> [-AceType] <AceType>
 [[-Id] <Guid>] [-Permissions] <Permission> [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>]
 [-ShowProgress] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="883a5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="883a5-107">DESCRIPTION</span></span>
<span data-ttu-id="883a5-108">**AzDataLakeStoreItemAclEntry** Cmdlet은 Data Lake store에서 파일 또는 폴더의 ACL (액세스 제어 목록)에 있는 항목 (ACE)을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-108">The **Set-AzDataLakeStoreItemAclEntry** cmdlet modifies an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="883a5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="883a5-109">EXAMPLES</span></span>

### <span data-ttu-id="883a5-110">예제 1: ACE에 대 한 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="883a5-110">Example 1: Modify permissions for an ACE</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All
```

<span data-ttu-id="883a5-111">이 명령은 Patti의 ACE를 수정 하 여 모든 권한을 가집니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-111">This command modifies the ACE for Patti Fuller to have all permissions.</span></span>

### <span data-ttu-id="883a5-112">예제 2: ACE에 대 한 사용 권한 재귀적으로 수정</span><span class="sxs-lookup"><span data-stu-id="883a5-112">Example 2: Modify permissions for an ACE recursively</span></span>
```
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzADUser -Mail "PattiFuller@contoso.com").ObjectId -Permissions All -Recurse -Concurrency 128
```

### <span data-ttu-id="883a5-113">예제 3: Acl 개체를 재귀적으로 사용 하 여 ACE에 대 한 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="883a5-113">Example 3: Modify permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1:--x,default:user:userid1:--x"
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Set-AzDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="883a5-114">이 명령은 루트 및 모든 하위 디렉터리와 파일에 대 한 모든 권한을 포함 하도록 Patti의 ACE를 재귀적으로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-114">This command recursively modifies the ACE for Patti Fuller to have all permissions to root and all its subdirectories and files.</span></span>

## <span data-ttu-id="883a5-115">변수</span><span class="sxs-lookup"><span data-stu-id="883a5-115">PARAMETERS</span></span>

### <span data-ttu-id="883a5-116">-계정</span><span class="sxs-lookup"><span data-stu-id="883a5-116">-Account</span></span>
<span data-ttu-id="883a5-117">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="883a5-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="883a5-118">-AceType</span></span>
<span data-ttu-id="883a5-119">수정할 ACE 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-119">Specifies the type of ACE to modify.</span></span>
<span data-ttu-id="883a5-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="883a5-121">클릭할</span><span class="sxs-lookup"><span data-stu-id="883a5-121">User</span></span> 
- <span data-ttu-id="883a5-122">그룹과</span><span class="sxs-lookup"><span data-stu-id="883a5-122">Group</span></span> 
- <span data-ttu-id="883a5-123">마스킹하</span><span class="sxs-lookup"><span data-stu-id="883a5-123">Mask</span></span> 
- <span data-ttu-id="883a5-124">나머지</span><span class="sxs-lookup"><span data-stu-id="883a5-124">Other</span></span>

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

### <span data-ttu-id="883a5-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="883a5-125">-Acl</span></span>
<span data-ttu-id="883a5-126">수정할 항목이 포함 된 ACL 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-126">Specifies the ACL object that contains the entries to modify.</span></span>

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

### <span data-ttu-id="883a5-127">-동시성</span><span class="sxs-lookup"><span data-stu-id="883a5-127">-Concurrency</span></span>
<span data-ttu-id="883a5-128">병렬로 처리 된 파일/디렉터리 수입니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="883a5-129">선택 사항: 적당 한 기본값이 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="883a5-130">-기본</span><span class="sxs-lookup"><span data-stu-id="883a5-130">-Default</span></span>
<span data-ttu-id="883a5-131">이 작업을 수행 하면 지정 된 ACL의 기본 ACE가 수정 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-131">Indicates that this operation modifies the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="883a5-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="883a5-132">-DefaultProfile</span></span>
<span data-ttu-id="883a5-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="883a5-134">-Id</span><span class="sxs-lookup"><span data-stu-id="883a5-134">-Id</span></span>
<span data-ttu-id="883a5-135">ACE를 수정할 AzureActive Directory 사용자, 그룹 또는 서비스 주체의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to modify an ACE.</span></span>

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

### <span data-ttu-id="883a5-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="883a5-136">-PassThru</span></span>
<span data-ttu-id="883a5-137">결과 ACL을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-137">Indicates the resulting ACL should be returned.</span></span>

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

### <span data-ttu-id="883a5-138">-Path</span><span class="sxs-lookup"><span data-stu-id="883a5-138">-Path</span></span>
<span data-ttu-id="883a5-139">ACE를 수정할 항목의 Data Lake Store 경로를 루트 디렉터리 (/)로 시작 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-139">Specifies the Data Lake Store path of the item for which to modify an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="883a5-140">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="883a5-140">-Permissions</span></span>
<span data-ttu-id="883a5-141">ACE에 대 한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-141">Specifies the permissions for the ACE.</span></span>
<span data-ttu-id="883a5-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="883a5-143">않아야</span><span class="sxs-lookup"><span data-stu-id="883a5-143">None</span></span>
- <span data-ttu-id="883a5-144">세기</span><span class="sxs-lookup"><span data-stu-id="883a5-144">Execute</span></span>
- <span data-ttu-id="883a5-145">작성</span><span class="sxs-lookup"><span data-stu-id="883a5-145">Write</span></span>
- <span data-ttu-id="883a5-146">WriteExecute</span><span class="sxs-lookup"><span data-stu-id="883a5-146">WriteExecute</span></span>
- <span data-ttu-id="883a5-147">자세한</span><span class="sxs-lookup"><span data-stu-id="883a5-147">Read</span></span>
- <span data-ttu-id="883a5-148">ReadExecute</span><span class="sxs-lookup"><span data-stu-id="883a5-148">ReadExecute</span></span>
- <span data-ttu-id="883a5-149">쓰기</span><span class="sxs-lookup"><span data-stu-id="883a5-149">ReadWrite</span></span>
- <span data-ttu-id="883a5-150">모든</span><span class="sxs-lookup"><span data-stu-id="883a5-150">All</span></span>

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

### <span data-ttu-id="883a5-151">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="883a5-151">-Recurse</span></span>
<span data-ttu-id="883a5-152">하위 디렉터리 및 파일에 재귀적으로 수정할 ACL을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-152">Indicates the ACL to be modified recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="883a5-153">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="883a5-153">-ShowProgress</span></span>
<span data-ttu-id="883a5-154">전달 되 면 진행 상태를 보여 주는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-154">If passed then progress status is showed.</span></span> <span data-ttu-id="883a5-155">재귀 Acl 수정을 완료 한 경우에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-155">Only applicable when recursive Acl modify is done.</span></span>

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

### <span data-ttu-id="883a5-156">-확인</span><span class="sxs-lookup"><span data-stu-id="883a5-156">-Confirm</span></span>
<span data-ttu-id="883a5-157">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="883a5-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="883a5-158">-WhatIf</span></span>
<span data-ttu-id="883a5-159">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="883a5-160">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="883a5-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="883a5-161">CommonParameters</span></span>
<span data-ttu-id="883a5-162">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="883a5-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="883a5-163">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="883a5-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="883a5-164">입력</span><span class="sxs-lookup"><span data-stu-id="883a5-164">INPUTS</span></span>

### <span data-ttu-id="883a5-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="883a5-165">System.String</span></span>

### <span data-ttu-id="883a5-166">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="883a5-166">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="883a5-167">DataLakeStore [] DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="883a5-167">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="883a5-168">DataLakeStore. DataLakeStoreEnums + AceType.</span><span class="sxs-lookup"><span data-stu-id="883a5-168">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="883a5-169">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="883a5-169">System.Guid</span></span>

### <span data-ttu-id="883a5-170">DataLakeStore. DataLakeStoreEnums + 사용 권한</span><span class="sxs-lookup"><span data-stu-id="883a5-170">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Permission</span></span>

### <span data-ttu-id="883a5-171">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="883a5-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="883a5-172">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="883a5-172">System.Int32</span></span>

## <span data-ttu-id="883a5-173">출력</span><span class="sxs-lookup"><span data-stu-id="883a5-173">OUTPUTS</span></span>

### <span data-ttu-id="883a5-174">DataLakeStore. DataLakeStoreItemAce/.</span><span class="sxs-lookup"><span data-stu-id="883a5-174">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="883a5-175">상속자</span><span class="sxs-lookup"><span data-stu-id="883a5-175">NOTES</span></span>

## <span data-ttu-id="883a5-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="883a5-176">RELATED LINKS</span></span>

[<span data-ttu-id="883a5-177">제거-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="883a5-177">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)


