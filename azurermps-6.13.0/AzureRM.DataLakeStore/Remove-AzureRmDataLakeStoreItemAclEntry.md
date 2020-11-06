---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 33E7607E-C2BC-4F46-9038-91AC92041F00
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 154c57c6a403fce574a785aaf60d95a7936907b9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524444"
---
# <span data-ttu-id="1242c-101">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1242c-101">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="1242c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1242c-102">SYNOPSIS</span></span>
<span data-ttu-id="1242c-103">Data Lake Store의 파일 또는 폴더의 ACL에서 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-103">Removes an entry from the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1242c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1242c-104">SYNTAX</span></span>

### <span data-ttu-id="1242c-105">Removebyac(기본값)</span><span class="sxs-lookup"><span data-stu-id="1242c-105">RemoveByACLObject (Default)</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Acl] <DataLakeStoreItemAce[]> [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1242c-106">RemoveSpecificACE</span><span class="sxs-lookup"><span data-stu-id="1242c-106">RemoveSpecificACE</span></span>
```
Remove-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-AceType] <AceType> [[-Id] <Guid>] [-Default] [-PassThru] [-Recurse] [-Concurrency <Int32>] [-ShowProgress]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1242c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1242c-107">DESCRIPTION</span></span>
<span data-ttu-id="1242c-108">**AzureRmDataLakeStoreItemAclEntry** Cmdlet은 Data Lake store에 있는 파일 또는 폴더의 ACL (액세스 제어 목록)에서 항목 (ACE)을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-108">The **Remove-AzureRmDataLakeStoreItemAclEntry** cmdlet removes an entry (ACE) from the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="1242c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1242c-109">EXAMPLES</span></span>

### <span data-ttu-id="1242c-110">예제 1: 사용자 항목 제거</span><span class="sxs-lookup"><span data-stu-id="1242c-110">Example 1: Remove a user entry</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId
```

<span data-ttu-id="1242c-111">이 명령은 ContosoADL 계정에서 Patti의 사용자 ACE를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-111">This command removes the user ACE for Patti Fuller from the ContosoADL account.</span></span>

### <span data-ttu-id="1242c-112">예제 2: 사용자 항목을 재귀적으로 제거</span><span class="sxs-lookup"><span data-stu-id="1242c-112">Example 2: Remove a user entry recursively</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -AceType User -Id (Get-AzureRmADUser -Mail "PattiFuller@contoso.com").ObjectId -Recurse -Concurrency 128
```

### <span data-ttu-id="1242c-113">예제 3: Acl 개체를 재귀적으로 사용 하 여 ACE에 대 한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="1242c-113">Example 3: Remove permissions for an ACE recursively using Acl object</span></span>
```
PS C:\>$fullAcl="user:userid1,default:user:userid1
PS C:\>$newFullAcl = $fullAcl.Split("{,}")
PS C:\>Remove-AzureRmDataLakeStoreItemAclEntry -AccountName "ContosoADL" -Path / -Acl $newFullAcl -Recurse -Concurrency 128
```

<span data-ttu-id="1242c-114">이 명령은 루트에서 Patti의 사용자 ACE를 제거 하 고 계정 ContosoADL의 모든 하위 디렉터리 및 파일에서 재귀적으로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-114">This command removes the user ACE for Patti Fuller from the root and recursively from all it's subdirectories and files for account ContosoADL.</span></span>

## <span data-ttu-id="1242c-115">변수</span><span class="sxs-lookup"><span data-stu-id="1242c-115">PARAMETERS</span></span>

### <span data-ttu-id="1242c-116">-계정</span><span class="sxs-lookup"><span data-stu-id="1242c-116">-Account</span></span>
<span data-ttu-id="1242c-117">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1242c-118">-AceType</span><span class="sxs-lookup"><span data-stu-id="1242c-118">-AceType</span></span>
<span data-ttu-id="1242c-119">제거할 ACE 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-119">Specifies the type of ACE to remove.</span></span>
<span data-ttu-id="1242c-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1242c-121">클릭할</span><span class="sxs-lookup"><span data-stu-id="1242c-121">User</span></span>
- <span data-ttu-id="1242c-122">그룹과</span><span class="sxs-lookup"><span data-stu-id="1242c-122">Group</span></span>
- <span data-ttu-id="1242c-123">마스킹하</span><span class="sxs-lookup"><span data-stu-id="1242c-123">Mask</span></span>
- <span data-ttu-id="1242c-124">나머지</span><span class="sxs-lookup"><span data-stu-id="1242c-124">Other</span></span>

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

### <span data-ttu-id="1242c-125">-Acl</span><span class="sxs-lookup"><span data-stu-id="1242c-125">-Acl</span></span>
<span data-ttu-id="1242c-126">제거할 항목이 포함 된 ACL 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-126">Specifies the ACL object that contains the entries to be removed.</span></span>

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

### <span data-ttu-id="1242c-127">-동시성</span><span class="sxs-lookup"><span data-stu-id="1242c-127">-Concurrency</span></span>
<span data-ttu-id="1242c-128">병렬로 처리 된 파일/디렉터리 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-128">Number of files/directories processed in parallel.</span></span> <span data-ttu-id="1242c-129">선택 사항: 적당 한 기본값이 선택 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-129">Optional: a reasonable default will be selected</span></span>

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

### <span data-ttu-id="1242c-130">-기본</span><span class="sxs-lookup"><span data-stu-id="1242c-130">-Default</span></span>
<span data-ttu-id="1242c-131">이 작업을 수행 하면 지정 된 ACL에서 기본 ACE가 제거 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-131">Indicates that this operation removes the default ACE from the specified ACL.</span></span>

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

### <span data-ttu-id="1242c-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1242c-132">-DefaultProfile</span></span>
<span data-ttu-id="1242c-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1242c-134">-Id</span><span class="sxs-lookup"><span data-stu-id="1242c-134">-Id</span></span>
<span data-ttu-id="1242c-135">ACE를 제거할 AzureActive Directory 사용자, 그룹 또는 서비스 주체의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-135">Specifies the object ID of the AzureActive Directory user, group, or service principal for which to remove an ACE.</span></span>

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

### <span data-ttu-id="1242c-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1242c-136">-PassThru</span></span>
<span data-ttu-id="1242c-137">삭제 작업의 결과를 표시 하는 부울 응답을 반환 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-137">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="1242c-138">-Path</span><span class="sxs-lookup"><span data-stu-id="1242c-138">-Path</span></span>
<span data-ttu-id="1242c-139">ACE를 제거할 항목의 Data Lake Store 경로를 루트 디렉터리 (/)로 시작 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-139">Specifies the Data Lake Store path of the item from which to remove an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1242c-140">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="1242c-140">-Recurse</span></span>
<span data-ttu-id="1242c-141">하위 디렉터리 및 파일에 재귀적으로 제거할 ACL을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-141">Indicates the ACL to be removed recursively to the child subdirectories and files</span></span>

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

### <span data-ttu-id="1242c-142">-ShowProgress</span><span class="sxs-lookup"><span data-stu-id="1242c-142">-ShowProgress</span></span>
<span data-ttu-id="1242c-143">전달 되 면 진행 상태를 보여 주는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-143">If passed then progress status is showed.</span></span> <span data-ttu-id="1242c-144">재귀 Acl 제거를 수행 하는 경우에만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-144">Only applicable when recursive Acl remove is done.</span></span>

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

### <span data-ttu-id="1242c-145">-확인</span><span class="sxs-lookup"><span data-stu-id="1242c-145">-Confirm</span></span>
<span data-ttu-id="1242c-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1242c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1242c-147">-WhatIf</span></span>
<span data-ttu-id="1242c-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1242c-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1242c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1242c-150">CommonParameters</span></span>
<span data-ttu-id="1242c-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1242c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1242c-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1242c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1242c-153">입력</span><span class="sxs-lookup"><span data-stu-id="1242c-153">INPUTS</span></span>

### <span data-ttu-id="1242c-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1242c-154">System.String</span></span>

### <span data-ttu-id="1242c-155">DataLakeStore. DataLakeStorePathInstance/.</span><span class="sxs-lookup"><span data-stu-id="1242c-155">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1242c-156">DataLakeStore [] DataLakeStoreItemAce []</span><span class="sxs-lookup"><span data-stu-id="1242c-156">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce[]</span></span>

### <span data-ttu-id="1242c-157">DataLakeStore. DataLakeStoreEnums + AceType.</span><span class="sxs-lookup"><span data-stu-id="1242c-157">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+AceType</span></span>

### <span data-ttu-id="1242c-158">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="1242c-158">System.Guid</span></span>

### <span data-ttu-id="1242c-159">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1242c-159">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1242c-160">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="1242c-160">System.Int32</span></span>

## <span data-ttu-id="1242c-161">출력</span><span class="sxs-lookup"><span data-stu-id="1242c-161">OUTPUTS</span></span>

### <span data-ttu-id="1242c-162">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="1242c-162">System.Boolean</span></span>

## <span data-ttu-id="1242c-163">상속자</span><span class="sxs-lookup"><span data-stu-id="1242c-163">NOTES</span></span>

## <span data-ttu-id="1242c-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1242c-164">RELATED LINKS</span></span>

[<span data-ttu-id="1242c-165">Set-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="1242c-165">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


